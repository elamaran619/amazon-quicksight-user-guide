# Logging Operations with AWS CloudTrail<a name="logging-using-cloudtrail"></a>

Amazon QuickSight is integrated with AWS CloudTrail\. This service captures specific API calls and delivers log files to your Amazon S3 bucket\. Amazon QuickSight doesn't currently have public API operations\. However, you can use CloudTrail to capture non\-API events made from the Amazon QuickSight console\. CloudTrail logs show user request information: who made the request, the IP address the request was made from, when it happened, and more\. 

To learn about CloudTrail, including how to configure and enable it, see the [AWS CloudTrail User Guide](http://docs.aws.amazon.com/awscloudtrail/latest/userguide/)\.

When CloudTrail logging is enabled in your AWS account, Amazon QuickSight operations are tracked in CloudTrail log files\. Amazon QuickSight actions are written with other AWS service records\. CloudTrail determines when to create and write to a new file based on a time period and file size\.

**Note**  
AWS CloudTrail logging for Amazon QuickSight is available for both Standard and Enterprise Editions, across all supported Amazon QuickSight regions\. For more information, read [AWS Regions and IP Address Ranges](regions.md)\.

**Topics**
+ [Working with Amazon QuickSight Log Files](log-files.md)
+ [Understanding Amazon QuickSight Log File Contents](log-file-contents.md)
+ [Tracking Non\-API Events by Using CloudTrail Logs](logging-non-api.md)
+ [Understanding Amazon QuickSight Log File Entries](understanding-qs-entries.md)