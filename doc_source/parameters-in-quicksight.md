# Parameters in Amazon QuickSight<a name="parameters-in-quicksight"></a>

*Parameters* are named variables that can provide values to an action or an object\. They provide a way to create a connection between the dashboard user and the technical features that make the dashboard interactive\. They can also connect one dashboard to another, so the user can drill down into data in a different analysis\.

For example, the dashboard user can use a list control to choose a value for a parameter\. That parameter then sets the filter, calculation, or URL action to the chosen value\. Then the visuals in the dashboard react to the user's choices\. 

For parameters to work, you reference them in one of the following:
+ Calculated fields
+ Filters
+ URL actions

To make the parameters accessible to the dashboard viewer, you add a parameter control\. If you don't create a control, you can still pass a value to your parameter in the dashboard URL\.

Some ways that you can use parameters are the following:
+ Using a calculation, you can transform data that is shown in an analysis\. 
+ If you add a control with a filter to an analysis you are publishing, the dashboard users can filter the data without creating their own filters\.
+ Using controls and URL actions, you can let dashboard users set values for the URL actions\. 

**Topics**
+ [Setting Up Parameters in Amazon QuickSight](parameters-set-up.md)
+ [Connecting to Parameters in Amazon QuickSight](parameters-connections.md)