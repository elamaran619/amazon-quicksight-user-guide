# Working with Vertical Stacked Bar Charts<a name="vertical-stacked-bar-chart"></a>

Use a vertical stacked bar chart to show values for hierarchical data, for example sales total by car model, stacked by car maker\. A vertical stacked bar chart uses a scale based on the maximum value for the selected measure\. To create a chart that uses a scale based on 100 percent instead, use the [Working with Vertical Stacked 100 Percent Bar Charts](vertical-stacked-100-percent-bar-chart.md)\.

Vertical stacked bar charts show up to 50 data points on the Y axis and up to 50 data points for group/color\. For more information about how we handle data that falls outside display limits, see [Display Limits in Visuals](working-with-visual-types.md#display-limits)\.

The icon for a vertical stacked bar chart is as follows:

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/vertical-stacked-bar-chart.png)

## Vertical Stacked Bar Chart Features<a name="vertical-stacked-bar-chart-features"></a>

Use the following table to understand the features supported by vertical stacked bar charts\.


****  

| Feature | Supported? | Comments | For More Information | 
| --- | --- | --- | --- | 
| Changing the legend display | Yes |  | [Customizing the Visual Legend](formatting-a-visual.md#customizing-visual-legend) | 
| Changing the title display | Yes |  | [Customizing a Visual Title](formatting-a-visual.md#displaying-visual-title) | 
| Changing the axis range | Yes | You can set the range for the Y axis\. | [Changing the Visual Scale with the Axis Range](formatting-a-visual.md#changing-visual-scale-axis-range) | 
| Changing the visual colors | Yes |  | [Changing Visual Colors in Amazon QuickSight](changing-visual-colors.md) | 
| Focusing on or excluding elements | Yes, with exceptions | You can focus on or exclude any bar or color block within a bar, except when you are using a date field as one of the dimensions\. In that case, you can only focus on the bar or color block that uses the date dimension, not exclude it\. |  [Focusing on Visual Elements](focusing-on-visual-elements.md) [Excluding Visual Elements](excluding-visual-elements.md) | 
| Sorting | Yes | You can sort on the fields you choose for the X axis and the values\. | [Sorting Visual Data in Amazon QuickSight](sorting-visual-data.md) | 
| Field aggregation | Yes | You must apply aggregation to the fields you choose for the value and group/color, and can't apply aggregation to the field you choose for the X axis\. | [Changing Field Aggregation](changing-field-aggregation.md) | 
| Adding drill\-downs | Yes | You can add drill\-down levels to the X axis and Group/Color field wells\. | [Adding Drill\-Downs to Visual Data in Amazon QuickSight](adding-drill-downs.md) | 

## Creating a Vertical Stacked Bar Chart<a name="create-vertical-stacked-bar-chart"></a>

Use the following procedure to create a vertical stacked bar chart\.

1. On the analysis page, choose **Visualize** on the tool bar\.

1. Choose **Add** on the application bar, and then choose **Add visual**\.

1. On the **Visual types** pane, choose the vertical stacked bar chart icon\.

1. From the **Fields list** pane, drag the fields that you want to use to the appropriate field wells\. Typically, you want to use dimension or measure fields as indicated by the target field well\. If you choose to use a dimension field as a measure, the **Count** aggregate function is automatically applied to it to create a numeric value\.

   To create a vertical stacked bar chart, drag a dimension to the **X axis** field well, one measure to the **Value** field well, and one dimension to the **Group/Color** field well\.

1. \(Optional\) Add drill\-down layers by dragging one or more additional fields to the **X axis** or **Group/Color** field wells\. For more information about adding drill\-downs, see [Adding Drill\-Downs to Visual Data in Amazon QuickSight](adding-drill-downs.md)\. 