# I can't add a visual to my analysis<a name="troubleshoot-adding-visuals"></a>

If you are editing an analysis for a selected data source, and the connection to the data source terminates unexpectedly, this error state can prevent further changes to the analysis\. In this case, you will not be able to add more visuals to the analysis\.

To fix:
+ Verify that you still have access to the data source\.
+ Add exceptions to your ad blocker for `*.aws.amazon.com`, `amazonaws.com`, and `https://mobileanalytics.*.amazonaws.com`\.
+ If you are using a proxy server, verify that `*.quicksight.aws.amazon.com` is added to the list of whitelisted \(safe\) domains\.