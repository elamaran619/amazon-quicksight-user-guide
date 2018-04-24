# Formatting a Visual in Amazon QuickSight<a name="formatting-a-visual"></a>

Use visual formatting to determine if a visual displays a title or a legend\. For some visual types, you can also set the range for the X or Y axis to determine the values it starts and ends at\.

Use the following table to determine what types of formatting each visual type supports\.


****  

| Visual Type | Hide/Display Visual Title | Hide/Display Visual Legend | Specify Axis Range | 
| --- | --- | --- | --- | 
| Horizontal bar charts \(all\) | Yes | Yes, except for simple bar charts \(those that don't have clustering or multiple measures\), which don't display a legend | Yes, on the X axis | 
| Vertical bar charts \(all\) | Yes | Yes, except for simple bar charts \(those that don't have clustering or multiple measures\), which don't display a legend | Yes, on the Y axis | 
| Combo charts \(all\) | Yes | Yes, except for simple bar charts \(those that don't have clustering, stacking, or multiple measures\), which don't display a legend | Yes, on the Bars and Lines | 
| Line charts \(all\) | Yes | Yes | Yes, on the Y axis | 
| Pivot table | No | No | No | 
| Scatter plot | Yes | Yes | Yes, on both the X and Y axes | 
| Tree map | Yes | Yes | No | 
| Pie graph | Yes | Yes | No | 
| Heat map | Yes  | Yes | No | 

## Displaying a Visual's Title<a name="displaying-visual-title"></a>

Use the following procedure to hide or display the title for a visual\. The visual title displays by default\.

1. On the analysis page, select the visual you want to format\.

1. Choose the on\-visual menu at the upper\-right corner of the visual, and then choose **Format visual**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/format-visual.png)

1. On the **Format Visual** pane, select or deselect **Show title**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/show-title.png)

1. Close the **Format Visual** pane, either by choosing either the X icon in the upper\-right corner of the pane, or by choosing the on\-visual menu at the upper\-right corner of the visual, and then choosing **Format visual** again\.

## Displaying the Visual Legend<a name="displaying-the-visual-legend"></a>

The visual legend helps you identify what a given visual element represents by mapping the element value to a color\. For example, on a line chart, line color might represent store location\.

You can use the visual menu to toggle between hiding and displaying the legend\. You can use the **Format Visual** pane to do so as well, and also to choose where on the visual the legend displays\. The visual legend displays to the right of the visual by default\.

When you move your cursor over the legend, a handle appears that you can use to adjust the width of the legend pane by dragging it wider or narrower\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/legend-resize.png)

### Changing the Legend Format by Using the Format Visual Pane<a name="displaying-visual-legend-format"></a>

Use the following procedure to hide or display the visual title\. The visual title displays by default\.

1. On the analysis page, select the visual you want to format\.

1. Choose the on\-visual menu at the upper\-right corner of the visual, and then choose **Format visual**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/format-visual.png)

1. On the **Format Visual** pane, expand the **Legend** section\.

1. Select or deselect **Show legend**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/show-legend2.png)

1. For **POSITION**, choose **Right**, **Bottom**, or **Top** to determine where on the visual the legend displays\.

1. Close the **Format Visual** pane by either choosing the X icon in the upper\-right corner of the pane, or by choosing the on\-visual menu at the upper\-right corner of the visual, and then choosing **Format visual** again\.

### Changing the Legend Format by Using the Visual Menu<a name="displaying-visual-legend-menu"></a>

Use the following procedure to toggle between showing or hiding the legend by using the visual menu\.

1. On the analysis page, select the visual you want to show or hide the legend for\.

1. Choose the on\-visual menu at the upper\-right corner of the visual, and then choose **Show legend** or **Hide legend** as appropriate\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/show-legend.png)

## Changing the Axis Range<a name="changing-axis-range"></a>

You can use the **Format Visual** pane to set the range for one or both axes of the visual, depending on what is supported by the visual type\. By default, the axis range starts at 0 and ends around the highest value for the measure being displayed\.

Use the following procedure to set the axis range for a visual\.

1. On the analysis page, select the visual you want to format\.

1. Choose the on\-visual menu at the upper\-right corner of the visual, and then choose **Format visual**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/format-visual.png)

1. On the **Format Visual** pane, expand the **<X\-or\-Y>\-Axis** section\. This is the **X\-Axis** section for horizontal bar charts, the **Y\-Axis** section for vertical bar charts and line charts, and both axes are available for scatter plots\.

1. Set the range for the axis by choosing one of the following options:
   + Choose **Auto \(starting at 0\)** to have the range start at 0 and end around the highest value for the measure being displayed\.
   + Choose **Auto \(based on data range\)** to have the range start at the lowest value for the measure being displayed and end around the highest value for the measure being displayed\.
   + Choose **Custom range** to have the range start and end at values that you specify\.

     If you choose **Custom range**, type the start and end values in the fields in that section\. Typically, you use integers for the range values\. For stacked 100 percent bar charts, use a decimal value to indicate the percentage you want\. For example, if you want the range to be 0–30 percent instead of 0–100 percent, type 0 for the start value and \.3 for the end value\.

1. Close the **Format Visual** pane, either by choosing the X icon in the upper\-right corner of the pane, or by choosing the on\-visual menu at the upper\-right corner of the visual, and then choosing **Format visual** again\.