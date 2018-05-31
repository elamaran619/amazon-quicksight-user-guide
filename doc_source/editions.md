# Different Editions of Amazon QuickSight<a name="editions"></a>

Amazon QuickSight offers Standard and Enterprise editions\. To learn more about the differences in availability, user management, permissions, and security between the two versions, see the following topic\. 

Both editions offer a full set of features for creating and sharing data visualizations\. Enterprise edition additionally offers encryption at rest and Microsoft Active Directory \(Microsoft Active Directory\) integration\. In Enterprise edition, you select a Microsoft Active Directory directory in AWS Directory Service\. You use that active directory to identify and manage your Amazon QuickSight users and administrators\. 

For more information about the features offered by the Amazon QuickSight editions and about pricing, see the [Amazon QuickSight website](https://aws.amazon.com/quicksight/)\. 

## Comparing Editions<a name="compare-editions"></a>

To help you decide which edition is for you, take a look at the following table to compare features between editions\.


| Features | Standard Edition | Enterprise Edition | 
| --- | --- | --- | 
| Upload \.csv files, flat files, and Excel files | ✓ | ✓ | 
| Connect to supported AWS data sources | ✓ | ✓ | 
| Connect to third\-party data sources | ✓ | ✓ | 
| Connect to on\-premises or hosted databases | ✓ | ✓ | 
| Data preparation tools | ✓ | ✓ | 
| Build visualizations and share dashboards | ✓ | ✓ | 
| Access all chart types | ✓ | ✓ | 
| Filter data | ✓ | ✓ | 
| Scale to thousands of users | ✓ | ✓ | 
| In\-memory calculation with SPICE | ✓ | ✓ | 
| Enable audit logs with AWS CloudTrail | ✓ | ✓ | 
| Federated Single Sign\-On with SAML | ✓ | ✓ | 
| Active Directory integration |   | ✓ | 
| Encryption at rest |   | ✓ | 
| Row\-level security |   | ✓ | 
| Private VPC access |   | ✓ | 

## Availability of Editions<a name="edition-availability"></a>

If you want to use Amazon QuickSight Enterprise edition, currently you must choose the US East \(N\. Virginia\) Region as your Amazon QuickSight capacity region\. The Microsoft Active Directory directory that you select to integrate with Amazon QuickSight must also reside in US East \(N\. Virginia\) Region\. This AWS Region is also where default [SPICE](welcome.md#spice) capacity for your account is allocated\. However, you can purchase additional SPICE capacity in any AWS Region supported by Amazon QuickSight\. You can access other AWS resources in any AWS Region\.

## User Management Between Edititons<a name="edition-user-management"></a>

User management is different between the Amazon QuickSight Standard and Enterprise editions\. However, both editions support identity federation, or Federated Single Sign\-On \(SSO\), through Security Assertion Markup Language 2\.0 \(SAML 2\.0\)\.

### User Management for Standard Edition<a name="edition-user-management-standard"></a>

In Standard edition, you can invite an AWS Identity and Access Management \(IAM\) user and allow that user to use their credentials to access Amazon QuickSight\. Alternatively, you can invite any person with an email address to create an Amazon QuickSight–only user account\. When you create a user account, Amazon QuickSight sends email to that user inviting them to activate their account\. 

When you create a user account, you also choose to assign it either an administrative or a user role\. This role assignment determines the user's permissions in Amazon QuickSight\. You perform all management of users by adding, changing, and deleting user accounts in Amazon QuickSight\. 

For more information about managing Standard edition user accounts, see [Managing User Access inside Amazon QuickSight](managing-quicksight-users.md)\.

### User Management for Enterprise Edition<a name="edition-user-management-enterprise"></a>

In Enterprise edition, you can select one or more Microsoft Active Directory active directory groups in AWS Directory Service for administrative access\. All users in these groups are authorized to sign in to Amazon QuickSight as administrators\. You can also select one or more Microsoft Active Directory active directory groups in AWS Directory Service for user access\. All users in these groups are authorized to sign in to Amazon QuickSight as users\. 

**Important**  
Amazon QuickSight administrators and users added in this way aren't automatically notified of their access to Amazon QuickSight\. You must email users with the sign\-in URL, the account name, and their credentials\.

You can only add or remove Enterprise edition user accounts by adding or removing a person from a Microsoft Active Directory group that you associated with Amazon QuickSight\. When you add a user account, the permissions it gets rely on whether the Microsoft Active Directory group is an administrative group or a user group in Amazon QuickSight\. 

You can also bulk add or remove user accounts by integrating Microsoft Active Directory groups with, or removing Microsoft Active Directory groups from, Amazon QuickSight\. 

Deactivating a user by removing the user from a Microsoft Active Directory group, or by removing their Microsoft Active Directory group from integration with Amazon QuickSight, doesn't delete the associated Amazon QuickSight user account for that person\. 

For more information about managing Enterprise edition user accounts, see [Access and Authentication in Amazon QuickSight](access-and-authentication.md)\.

## Permissions for the Different Editions<a name="edition-permissions"></a>

In Standard edition, all Amazon QuickSight administrators can manage subscriptions and SPICE capacity\. They can also add, modify, and delete user accounts\. 

Additional AWS permissions are required to manage Amazon QuickSight permissions to AWS resources and to unsubscribe from Amazon QuickSight\. These tasks can only be performed by an IAM user who also has administrative permissions in Amazon QuickSight, or by the IAM user or AWS account that created the Amazon QuickSight account\.

To manage access to AWS resources from Amazon QuickSight, you must be logged in as one of the following:
+ Any IAM user who is a Amazon QuickSight adminstrator
+ The IAM user or AWS root account that created the Amazon QuickSight account

In Enterprise edition, you must add AD users or groups to an IAM role that has QuickSight permissions, rather than adding IAM users individually\. All Microsoft Active Directory users that are Amazon QuickSight administrators can to manage subscriptions and SPICE capacity\. 

Additional AWS permissions are required to manage Microsoft Active Directory groups, manage access to AWS resources, or unsubscribe from Amazon QuickSight\. Administrators are prompted for AWS or IAM credentials to perform these tasks\.

For more information about the permissions needed for specific tasks, see [Setting Your IAM Policy](set-iam-policy.md)\.

## Secure Transmission and Storage Between Editions<a name="security"></a>

In both editions of Amazon QuickSight, all transfers of data \(for example, from the data source to SPICE, or from SPICE to the user interface\) are encrypted\. Database connections are secured using Secure Sockets Layer \(SSL\), and all other transfers are secured using Transport Layer Security \(TLS\)\.

In Enterprise edition, data at rest in SPICE is also encrypted using block\-level encryption with AWS\-managed keys\.