# Troubleshooting Amazon QuickSight<a name="troubleshooting"></a>

 Use this information to help you diagnose and fix common issues that you can encounter when using Amazon QuickSight\. 

****  
 Need more help? You can visit the Amazon QuickSight [User Community](https://answers.quicksight.aws.amazon.com/sn/index.html) or the [AWS forums](https://forums.aws.amazon.com)\. See also the [Amazon QuickSight Resource Library](https://aws.amazon.com/quicksight/resource-library/)\. 

**Topics**
+ [I can't connect to my data source\.](troubleshoot-connect-to-datasources.md)
+ [My rows were skipped during data preparation](troubleshooting-skipped-rows.md)
+ [My SPICE data won't sort alphabetically](troubleshoot-sorting-SPICE.md)
+ [I can't add a visual to my analysis](troubleshoot-adding-visuals.md)
+ [I get a feedback bar across my printed docs](troubleshoot-printing-docs.md)
+ [How do I delete my Amazon QuickSight account?](#troubleshoot-delete-quicksight-account)
+ [Why won't my map charts show locations?](#troubleshoot-geocoding)
+ [Why isn't this working in my browser?](#troubleshoot-browser)
+ [Troubleshooting Issues When Using Athena with Amazon QuickSight](troubleshoot-athena.md)

## How do I delete my Amazon QuickSight account?<a name="troubleshoot-delete-quicksight-account"></a>

If you need to delete your Amazon QuickSight account, even when you can't access Amazon QuickSight to unsubscribe, log in to AWS and use the following link to open [the unsubscribe screen](https://us-east-1.quicksight.aws.amazon.com/sn/console/unsubscribe): `https://us-east-1.quicksight.aws.amazon.com/sn/console/unsubscribe`\. This works no matter what AWS Regions you use\. It will delete all data, analyses, Amazon QuickSight users, and Amazon QuickSight administrators\. If you have further difficulty, contact support\. 

## Why won't my map charts show locations?<a name="troubleshoot-geocoding"></a>

For automatic mapping, called geocoding, to work on map charts, your data must be prepared following specific rules\. For help with geospatial issues, see [Geospatial Troubleshooting](geospatial-troubleshooting.md)\. For help with preparing data for geospatial charts, see [Adding Geospatial Data](geospatial-data-prep.md)\.

## Why isn't this working in my browser?<a name="troubleshoot-browser"></a>

If you can't view Amazon QuickSight correctly in your Chrome browser, follow these steps to fix the problem\.

1. Open Chrome and navigate to `chrome://flags/#touch-events` 

1. If the option is set to **Automatic**, change it to **Disabled** 

1. Close and re\-open Chrome\.