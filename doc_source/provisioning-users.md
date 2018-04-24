# Provisioning users for Amazon QuickSight<a name="provisioning-users"></a>

## Self\-Provisioning an Amazon QuickSight administrator<a name="assigning-the-admin"></a>

Amazon QuickSight administrators are users who can also manage Amazon QuickSight features such as account settings and user accounts\. They can also purchase additional Amazon QuickSight user subscriptions, purchase [SPICE](welcome.md#spice) capacity, and cancel the subscription to Amazon QuickSight for your AWS account\.

You can use an AWS user or group policy to give users the ability to add themselves as administrators of Amazon QuickSight\. Their accounts become active and billable the first time they open Amazon QuickSight\. To set up self\-provisioning, you need to give them permission to use the `quicksight:CreateAdmin` action\. For more information using using IAM, see [Working with AWS Identity and Access Management \(IAM\) Users, Roles, and Policies](working-with-iam.md)\. 

Alternately, you can use the following procedure to use the console set or create the administrator for Amazon QuickSight\. 

**To make a user the Amazon QuickSight administrator**

1. Create the AWS user
   + Use IAM to create the user you want to be the administrator of Amazon QuickSight\. Or, identify an existing user in IAM for the administrator role\. If you prefer, you can put the user inside a new group, for manageability\. 
   + Grant the user \(or group\) sufficient permissions, as described in [Setting Your IAM Policy](set-iam-policy.md)\. 
   + For more information on working with IAM, see [Working with AWS Identity and Access Management \(IAM\) Users, Roles, and Policies](working-with-iam.md)\. 

1. Log in to your AWS console with the target user's credentials\.

1. Go to [http://quicksight.aws.amazon.com/sn/console/get-user-email](http://quicksight.aws.amazon.com/sn/console/get-user-email)\.

1. Type in the target user's email, and choose **Continue**

1. On success, the target IAM user is now an administrator in Amazon QuickSight\.

## Self\-Provisioning an Amazon QuickSight user<a name="self-service-access"></a>

Amazon QuickSight users can create data sources, data sets, analyses, and dashboards\. They can share analyses and dashboards with other Amazon QuickSight users in your Amazon QuickSight account\. However, they don't have access to the Manage QuickSight menu\. They can't change account settings, manage user accounts, purchase additional Amazon QuickSight user subscriptions or [SPICE](welcome.md#spice) capacity, or cancel the subscription to Amazon QuickSight for your AWS account\.

You can use an AWS user or group policy to give users the ability to create a Amazon QuickSight user account for themselves\. Their accounts become active and billable the first time they open Amazon QuickSight\. To set up self\-provisioning, you need to give them permission to use the `quicksight:CreateUser` action\. For more information using using IAM, see [Working with AWS Identity and Access Management \(IAM\) Users, Roles, and Policies](working-with-iam.md)\. 