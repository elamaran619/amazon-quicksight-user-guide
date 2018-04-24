# I can't connect to Athena<a name="troubleshoot-connect-athena"></a>

You get an insufficient permissions error when your run a query and the permissions aren't configured\. To verify that you can connect Amazon QuickSight to Athena, check these settings: 
+ AWS resource permissions inside of Amazon QuickSight
+ IAM policies
+ S3 location
+ Query results location
+ KMS key policy \(for encrypted data sets only\)

Use the following procedure to make sure you authorized Amazon QuickSight to use Athena\. Permissions to AWS resources apply to all Amazon QuickSight users\.

**Authorizing Amazon QuickSight to access Athena**

1. You must temporarily switch to the US East \(N\. Virginia\) region \(top right\), while you edit your account permissions\. 

1. Open Amazon QuickSight, then choose your profile name \(top right\)\. Choose **Manage QuickSight**\. 

1. Then choose **Account Settings**, on the left\. 

1. From the **Account Settings** page, choose **Edit AWS permissions**\. 

1. If **Athena** is not enabled \(checked\), check\-mark it now\. 

1. Use the following steps to verify that you enabled access to the Amazon S3 buckets for your &ATE; query\.

   1. On the same page, named **Edit QuickSight read\-only access to AWS resources**, find Amazon S3\. 

      If Amazon S3 is not enabled \(checked\), check\-mark it now\. 

   1. To select individual buckets, choose **Choose S3 buckets**\.

   1. Select the buckets you want to access from your Athena query\. Then choose **Select buckets** to confirm\.

1. On the **Edit QuickSight read\-only access to AWS resources** page, choose **Apply**\. 

1. If you changed your region during the first step of this process, change it back to the region you want to use\.

Your IAM policies must grant permissions to specific actions\. Your IAM user or role must be able to read and write both the input and the output of the S3 buckets that Athena uses for your query\.

**Verifying that your IAM policies have permission to use to the S3 buckets\.**

1. Open the IAM console at [https://console\.aws\.amazon\.com/iam/](https://console.aws.amazon.com/iam/)\.

1. Locate the user or role you are using\. Choose the user or role name to see the associated policies\.

1. Verify that the policy has the correct permissions\. Choose a policy you want to verify, then choose **Edit policy**\. Use the visual editor, which opens by default\. If you have the JSON editor open instead, choose the **Visual editor** tab\. 

1. Choose the S3 entry in the list to see its contents\. The policy needs to grant permissions to list, read, and write\. If S3 is not in the list, or it doesn't have the correct permissions, you can add them here\.

The IAM user needs access to read and write to the results location in S3\. By default, Athena stores query results in `aws-athena-query-results-<ACCOUNTID>-<REGION>`, however you may be using a different S3 bucket\. Also, if the data set is encrypted, the IAM user needs to be a key user in the specified KMS key's policy\.

**Important**  
Do not put the endpoint in the S3 URL\.   
This is correct: `s3://bucket/path`  
This generates an "Access Denied" error: **s3://us\-east\-1\.amazonaws\.com/bucket/path**

**Setting permissions to your Athena query results location**

1. Open the AWS Artifact console at [https://console\.aws\.amazon\.com/artifact/](https://console.aws.amazon.com/artifact/)\. 

1. Choose **Settings** and get the value in **Query result location**\. If **Encrypt query results** is enabled \(checked\), check whether it uses SSE\-KMS or CSE\-KMS, and note the key\. 

1. Next, make sure your IAM user has access to the correct bucket\. You can do this in the [https://console\.aws\.amazon\.com/s3/](https://console.aws.amazon.com/s3/)\. However, if you are managing access with an Access Control List \(ACL\), check the ACLs\. 

1. Encrypted data sets require one more step\. If **Encrypt query results** is enabled, make sure the IAM user or role is added as a key user in that KMS key's policy\. You can access KMS settings in IAM\.

**Granting access to the S3 bucket**

1. Open the Amazon S3 console at [https://console\.aws\.amazon\.com/s3/](https://console.aws.amazon.com/s3/)\.

1. Choose the S3 bucket used by Athena in the **Query result location**\. 

1. On the **Permissions** tab, verify the permissions\.