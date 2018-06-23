# Working with Vertical Bar Charts<a name="vertical-bar-chart"></a>

You can use the vertical bar chart visual type to create a single\-measure, multi\-measure, or clustered vertical bar chart\. A single\-measure bar chart shows one measure for one dimension, for example average delay time by flight number\. A multi\-measure bar chart shows two or more measures for one dimension, for example sales total and profit total by automobile mode\. A clustered bar chart shows values for a dimension grouped by a related dimension, for example sales totals by automobile model, grouped by car maker\.

To create a vertical bar chart, use a dimension for the X axis and a measure for the value\. The dimension is typically a text field that is related to the measure in some way\. You can use the dimension to segment the measure to see more detailed information\. You can also use a date field in this way, but we recommend using a line chart for that because they are better suited to showing changes in a measure over time\. Each vertical bar in the chart represents a measure value for an item in the dimension you chose\. 

Vertical bar charts show up to 2500 data points on the Y axis for visuals that don't use group/color\. For visuals that do use group/color, they show up to 50 data points on the Y axis and up to 50 data points for group/color\. For more information about how we handle data that falls outside display limits, see [Display Limits in Visuals](working-with-visual-types.md#display-limits)\.

The icon for a vertical bar chart is as follows:

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/vertical-bar-chart.png)

## Vertical Bar Chart Features<a name="vertical-bar-chart-features"></a>

Use the following table to understand the features supported by vertical bar charts\.


****  

| Feature | Supported? | Comments | For More Information | 
| --- | --- | --- | --- | 
| Changing the legend display | Yes, with exceptions | Multi\-measure vertical bar charts and clustered vertical bar charts display a legend, while single\-measure vertical bar charts do not\. | [Customizing the Visual Legend](formatting-a-visual.md#customizing-visual-legend) | 
| Changing the title display | Yes |  | [Customizing a Visual Title](formatting-a-visual.md#displaying-visual-title) | 
| Changing the axis range | Yes | You can set the range for the Y axis\. | [Changing the Visual Scale with the Axis Range](formatting-a-visual.md#changing-visual-scale-axis-range) | 
| Changing the visual colors | Yes |  | [Changing Visual Colors in Amazon QuickSight](changing-visual-colors.md) | 
| Focusing on or excluding elements | Yes, with exceptions | You can focus on or exclude any bar on the chart, except when you are using a date field as the dimension for the X axis\. In that case, you can only focus on a bar, not exclude it\. |  [Focusing on Visual Elements](focusing-on-visual-elements.md) [Excluding Visual Elements](excluding-visual-elements.md) | 
| Sorting | Yes | You can sort on the fields you choose for the X axis and the values\. | [Sorting Visual Data in Amazon QuickSight](sorting-visual-data.md) | 
| Field aggregation | Yes | You must apply aggregation to the field or fields you choose for the value, and can't apply aggregation to the fields you choose for the X axis or group/color\. | [Changing Field Aggregation](changing-field-aggregation.md) | 
| Adding drill\-downs | Yes | You can add drill\-down levels to the X axis and Group/Color field wells\. | [Adding Drill\-Downs to Visual Data in Amazon QuickSight](adding-drill-downs.md) | 

## Creating a Vertical Bar Chart<a name="create-vertical-bar-chart"></a>

Use the following procedure to create a vertical bar chart\.

1. On the analysis page, choose **Visualize** on the tool bar\.

1. Choose **Add** on the application bar, and then choose **Add visual**\.

1. On the **Visual types** pane, choose the vertical bar chart icon\.

1. From the **Fields list** pane, drag the fields that you want to use to the appropriate field wells\. Typically, you want to use dimension or measure fields as indicated by the target field well\. If you choose to use a dimension field as a measure, the **Count** aggregate function is automatically applied to it to create a numeric value\.
   + To create a single\-measure vertical bar chart, drag a dimension to the **X axis** field well and one measure to the **Value** field well\.
   + To create a multi\-measure vertical bar chart, drag a dimension to the **X axis** field well and two or more measures to the **Value** field well\. Leave the **Group/Color** field well empty\.
   + To create a clustered vertical bar chart, drag a dimension to the **X axis** field well, one measure to the **Value** field well, and one dimension to the **Group/Color** field well\.

1. \(Optional\) Add drill\-down layers by dragging one or more additional fields to the **X axis** or **Group/Color** field wells\. For more information about adding drill\-downs, see [Adding Drill\-Downs to Visual Data in Amazon QuickSight](adding-drill-downs.md)\. 