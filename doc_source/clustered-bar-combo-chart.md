# Working with Clustered Bar Combo Charts<a name="clustered-bar-combo-chart"></a>

The combo chart is like using two different types of visualization at the same time\. You should make sure the data in the bars \(or columns\) directly relates to the data in the line or lines\. This relationship is not technically enforced by the tool, so it's essential that you determine this relationship yourself\. Without some relation between the lines and bars, the visual loses meaning\.

You can use the combo chart visual type to create a single\-measure or single\-line chart\. A single\-measure combo chart shows one measure for one dimension\. 

To create a multi\-measure chart, you can choose to add multiple lines, or multiple bars\. A multi\-measure bar chart shows two or more measures for one dimension\. You can group the bars in clusters, or stack them\. 

A clustered bar chart shows values for a dimension grouped by a parent dimension\. 

To create a vertical bar chart, use a dimension for the X axis and a measure for the value\. The dimension is typically a text field that is related to the measure in some way and can be used to segment it in order to see more detailed information\. You can also use a date field in this way, but we recommend using a line chart because it's better suited to showing changes in a measure over time\. Each vertical bar in the chart represents a measure value for an item in the dimension you chose\. 

Vertical bar charts show up to 2500 data points on the Y axis for visuals that don't use group/color\. Visuals that do use group/color show up to 50 data points on the Y axis and up to 50 data points for group/color\. For more information about how Amazon QuickSight handles data that falls outside display limits, see [Display Limits in Visuals](working-with-visual-types.md#display-limits)\.

The icon for a clustered bar combo chart is as follows\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/clustered-bar-combo-chart.png)

## Clustered Bar Combo Chart Features<a name="clustered-bar-combo-chart-features"></a>

Use the following table to understand the features supported by clustered bar combo charts\.


****  

| Feature | Supported? | Comments | For More Information | 
| --- | --- | --- | --- | 
| Changing the legend display | Yes, with exceptions | Multi\-measure combo charts display a legend, and single\-measure combo charts don't\. | [Displaying the Visual Legend](formatting-a-visual.md#displaying-the-visual-legend) | 
| Changing the title display | Yes |  | [Displaying a Visual's Title](formatting-a-visual.md#displaying-visual-title) | 
| Changing the axis range | Yes | You can set the range for the Y axis\. | [Changing the Axis Range](formatting-a-visual.md#changing-axis-range) | 
| Changing the visual colors | Yes |  | [Changing Visual Colors in Amazon QuickSight](changing-visual-colors.md) | 
| Focusing on or excluding elements | Yes, with exceptions | You can focus on or exclude any bar on the chart, except when you are using a date field as the dimension for the X axis\. In that case, you can only focus on a bar, not exclude it\. |  [Focusing on Visual Elements](focusing-on-visual-elements.md) [Excluding Visual Elements](excluding-visual-elements.md) | 
| Sorting | Yes | You can sort on the fields you choose for the X axis and the values\. | [Sorting Visual Data in Amazon QuickSight](sorting-visual-data.md) | 
| Field aggregation | Yes | You must apply aggregation to the field or fields you choose for the value\. You can't apply aggregation to the fields you choose for the X axis or group/color\. | [Changing Field Aggregation](changing-field-aggregation.md) | 
| Adding drill\-downs | Yes | You can add drill\-down levels to the X axis and Group/Color field wells\. | [Adding Drill\-Downs to Visual Data in Amazon QuickSight](adding-drill-downs.md) | 

## Creating a Clustered Bar Combo Chart<a name="create-clustered-bar-combo-chart"></a>

Use the following procedure to create a clustered bar combo chart\.

1. On the analysis page, choose **Visualize** on the tool bar\.

1. Choose **Add** on the application bar, and then choose **Add visual**\.

1. On the **Visual types** pane, choose the clustered bar combo chart icon\.

1. From the **Fields list** pane, drag the fields you want to use to the appropriate field wells\. Typically, you want to use dimension or measure fields as indicated by the target field well\. If you choose to use a dimension field as a measure, the **Count** aggregate function is automatically applied to it to create a numeric value\. You can create combo charts as follows:
   + To create a single\-measure clustered bar combo chart, drag a dimension to the **X axis** field well\. Then drag one measure to either the **Bars** or **Lines** field well\.
   + To create a multi\-measure clustered bar combo chart, drag a dimension or dimensions to the **X axis** field well\. Then drag two or more measures to the **Bars** or **Lines** field well\. 

     Optionally, add a dimension to the **Group/Color** field well\. If you have a field in **Group/Color**, you can't have more than one field under **Bars**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/combo-chart-example2-clustered.png)

1. \(Optional\) Add drill\-down layers by dragging one or more additional fields to the **X axis** or **Group/Color** field wells\. For more information about adding drill\-downs, see [Adding Drill\-Downs to Visual Data in Amazon QuickSight](adding-drill-downs.md)\. 