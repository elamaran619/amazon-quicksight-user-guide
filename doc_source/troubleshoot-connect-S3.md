# I can't connect to S3<a name="troubleshoot-connect-S3"></a>

To successfully connect to Amazon S3, you must configure authentication, create a valid manifest file inside the bucket you are trying to access, and make sure the file described by the manifest is available\.

To verify authentication, make sure you authorized Amazon QuickSight to access the S3 account\. It’s not enough that you, the user, are authorized\. Amazon QuickSight must be authorized separately\. 

**Authorizing Amazon QuickSight to access your Amazon S3 bucket**

1. You must temporarily switch to the US East \(N\. Virginia\) region \(top right\), while you edit your account permissions\. 

1. Inside of Amazon QuickSight, choose your profile name \(top right\)\. Choose **Manage QuickSight**\. 

1. Then choose **Account Settings**, on the left\. 

1. From the **Account Settings** page, choose **Edit AWS permissions**\. 

1. If **Amazon S3** is check\-marked, you can see how many buckets are authorized\. 

1. To select individual buckets, choose **Choose S3 buckets**\.

1. Select the buckets you want to access from Amazon QuickSight\. Then choose **Select buckets**\.

1. Choose **Apply**\.

1. If you changed your region during the first step of this process, change it back to the region you want to use\.

It is crucial to make sure your manifest file is valid\. If Amazon QuickSight can't parse your file, it will give you an error similar to "We can't parse the manifest file as a valid JSON" or "We can't connect to the S3 bucket"\.

**Verifying your manifest file**

1. Open your manifest file\. You can do this directly from the Amazon S3 console at [https://console\.aws\.amazon\.com/s3/](https://console.aws.amazon.com/s3/)\. Navigate to your manifest file and choose **Open**\.

1. Make sure the URI\(s\) provided inside the manifest file are in fact the file\(s\) you want connect to\.

1. If you are using a link to the manifest file, rather than uploading it, make sure the link does not have any additional phrases after the word `.json`\. You can get the proper link to an S3 file by viewing its details on Amazon S3\. Look for **Link**\.

1. To make sure the content of the manifest file is valid, you can use a JSON validator, like the one at [https://jsonlint.com](https://jsonlint.com)\. 

1. Verify permissions on your bucket or file\. In the [https://console\.aws\.amazon\.com/s3/](https://console.aws.amazon.com/s3/), navigate to your Amazon S3 bucket, select the **Permissions** tab, and add the appropriate permissions\. Be sure the permissions are at the right level: either on the bucket or on the file\(s\)\. 

1. If you are using the `s3://` protocol, rather than `https://`, check to make sure you reference your bucket directly\. For example, use *s3://mybucket/myfile\.csv* instead of *s3://s3\-us\-west\-2\.amazonaws\.com/mybucket/myfile\.csv*\. Doubly specifying Amazon S3, by using `s3://` and also `s3-us-west-2.amazonaws.com`, will cause an error\.

   For more information on manifest files and connecting to Amazon S3 see: [Supported Formats for Amazon S3 Manifest Files](supported-manifest-file-format.md)

Finally, verify that your Amazon S3 dataset was created according to these steps: [Creating a Data Set Using Amazon S3 Files](create-a-data-set-s3.md)

If you use Athena to connect to Amazon S3 , see [I can't connect to Athena](troubleshoot-connect-athena.md)