# Working with Amazon VPC<a name="working-with-aws-vpc"></a>

Amazon QuickSight is fully integrated with Amazon VPC \(VPC\)\. Use this section to find how to configure Amazon QuickSight to access data in your VPC\.

In Amazon QuickSight Enterprise edition, you can create connections to your VPCs from your AWS account's Amazon QuickSight subscription\. Each connection defines a set of rules for connecting to a private subnet without an internet gateway\. When creating a data set, the Amazon QuickSight user can then use a VPC connection to connect to an instance that is not on the public network\.

**What is VPC?**

Amazon Virtual Private Cloud \(Amazon VPC\) enables you to define a virtual network in your own logically isolated area within the AWS cloud, known as a *virtual private cloud \(VPC\)*\. You can launch your AWS resources, such as instances, into your VPC\. Your VPC closely resembles a traditional network that you might operate in your own data center, with the benefits of using AWS's scalable infrastructure\. You can configure your VPC; you can select its IP address range, create subnets, and configure route tables, network gateways, and security settings\. You can connect instances in your VPC to the internet\. You can connect your VPC to your own corporate data center, making the AWS cloud an extension of your data center\. To protect the resources in each subnet, you can use multiple layers of security, including security groups and network access control lists\. For more information, see the [Amazon VPC User Guide](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/)\.

## Create a Private Connection to Amazon VPC using Amazon QuickSight<a name="private-connection-to-vpc-using-quicksight"></a>

Use the following procedure to create a connection to a VPC\.

1. Go to the **Account Settings** page\. 

   To do this, choose your profile icon at the top right of the screen, then choose **Manage QuickSight**\. From the menu on the left, choose **Manage VPC connections**\.

   Any existing private connections to VPCs display here\. To add a new one, choose **Add VPC connection**\. To delete one, remove it by using the delete icon\. 

   If you need to change a VPC connection, you can create a new VPC connection and remove the old one\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/vpc-connections-managing.png)

1. After you choose **Add VPC connection**, enter a unique descriptive name for the **VPC connection name**\. This doesn't need to be an actual VPC ID or VPC name\. Then enter the subnet ID for **Subnet ID**, and enter the group ID for **Security group ID**\. Make sure that the subnet and the security group are in the same VPC\. 

   To help locate the information you need, you can use the links to the consoles at the top of the following screen\. The location of the information is described in the following steps\.

   If you already know the subnet and security group you want to use, you can enter the information and skip to the last step in this procedure\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/vpc-connections-adding.png)

1. \(Optional\) From the AWS VPC console, find the **VPC ID** that you want to use\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/vpc-console.png)

1. \(Optional\) From the AWS VPC subnet console, you can see which subnets are in a VPC by locating the VPC ID on the screen\. Locate the VPC ID you are using, and copy one of its **Subnet ID**s\. Paste it into the **Subnet ID** field on the **Adding VPC connection** screen\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/vpc-subnet-console.png)

1. \(Optional\) From the AWS VPC Security Group console, you can see which security groups are in a VPC by finding the VPC ID on the screen\. Locate the VPC ID you are using, and copy one of its **Group ID**s\. Paste it into the **Security group ID** field on the **Adding VPC connection** screen\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/vpc-security-group-console.png)

1. Settings for a VPC connection can't be altered\. If your choices are correct, then choose **Create**\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/vpc-connections-creating.png)

For best practices when using VPC, see:
+ [AWS Single VPC Design](https://aws.amazon.com/answers/networking/aws-single-vpc-design/)
+ [Recommended Network ACL Rules for Your VPC](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Appendix_NACLs.html)
+ [ VPC Scenarios and Examples ](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Scenarios.html)

**Note**  
When you create a data set, you can only access private connections which are using a private subnet\. You can't create or use a private connection to access a public endpoint\. 