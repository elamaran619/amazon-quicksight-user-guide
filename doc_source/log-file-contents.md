# Understanding Amazon QuickSight Log File Contents<a name="log-file-contents"></a>

Every log entry contains information about who generated the request\. The user identity information in the log entry helps you determine the following: 
+ Whether the request was made with root or AWS Identity and Access Management \(IAM\) user credentials
+ Whether the request was made with temporary security credentials for an IAM role or federated user
+ Whether the request was made by another AWS service

For more information on user identity, see the [CloudTrail userIdentity Element](http://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-event-reference-user-identity.html)\.

By default, each Amazon QuickSight log entry contains the following information:
+ userIdentity
+ eventTime
+ eventId
+ readOnly
+ awsRegion
+ eventSource \(quicksight\)
+ eventType \(AwsServiceEvent\)
+ recipientAccountId \(customer AWS account\)

**Note**  
 CloudTrail displays users as `unknown` if they were provisioned by Amazon QuickSight\. This display is because these users aren't a known IAM identity type\. 