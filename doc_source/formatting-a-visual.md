# Formatting a Visual in Amazon QuickSight<a name="formatting-a-visual"></a>

Use visual formatting to choose display options for your data visualization\. The following list indicates which visuals support what type of formatting\.
+ Bar charts \(both horizontal and vertical\):
  + Customize, display, or hide title and labels
  + Customize, display, or hide legend \(exception: simple charts without clustering or multiple measures don't show a legend\)
  + Specify axis range and steps on x\-axis for horizontal bar charts, and on y\-axis for vertical bar charts
  + Show or hide the “other” category
+ Combo charts:
  + Customize, display, or hide title and labels
  + Customize, display, or hide legend \(exception: simple charts without clustering, stacking, or multiple measures don't show a legend\)
  + Specify axis range on bars and lines
  + Show or hide the “other” category
+ Geospatial charts \(maps\):
  + Customize, display, or hide title and legend
+ Heat maps:
  + Customize, display, or hide title, legend, and labels
+ Key performance indicators \(KPIs\):
  + Customize, display, or hide title
  + Display or hide trend arrows and progress bar
  + Customize comparison method as auto, difference, percent \(%\), or difference as percent \(%\)
  + Customize primary value displayed to be comparison or actual
+ Line charts:
  + Customize, display, or hide title and labels
  + Customize, display, or hide legend \(exception: simple charts don't show a legend\)
  + Specify axis range and steps \(on y\-axis\)
  + Show or hide the “other” category, except when the x\-axis is a date
+ Pie charts:
  + Customize, display, or hide title and legend
  + Customize, display, or hide the labels for group/color and value fields
  + Show or hide the “other” category
+ Pivot tables:
  + Customize, display, or hide title
  + Customize, display, or hide the column names for row and value fields
  + Show or hide the “other” category
+ Scatter plots:
  + Customize, display, or hide title, legend, and labels
  + Specify axis range \(on x\-axis and y\-axis\)
+ Tabular reports:
  + Customize, display, or hide title and legend
  + Customize, display, or hide the column names for group\-by and value fields
  + Display or hide totals at the top or bottom of the table
+ Tree maps:
  + Customize, display, or hide title and legend
  + Customize, display, or hide the labels for group\-by, size, and color fields
  + Show or hide the “other” category

## Customizing a Visual Title<a name="displaying-visual-title"></a>

Use the following procedure to hide or display the title for a visual\. The visual title displays by default\.

1. On the analysis page, select the visual that you want to format\. You can change the title by putting your cursor in the title and editing it directly\. To revert to the default name, delete your entry\.

1. Choose the on\-visual menu at the upper\-right corner of the visual, and then choose **Format visual**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/format-visual.png)

1. On the **Format Visual** pane, enable or disable **Show title**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/show-title.png)

1. Close the **Format Visual** pane by choosing the X icon in the upper\-right corner of the pane\.

## Customizing Visual Labels<a name="customizing-visual-labels"></a>

Use the following procedure to customize, display, or hide the labels for a visual\. 

1. On the analysis page, select the visual that you want to format\. You can change the labels by choosing the label directly on the visual, and choosing **Rename**\. To revert to the default name, delete your entry\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/customize-visual-labels-direct-edit.png)

1. To see more options, choose the on\-visual menu at the upper\-right corner of the visual, and then choose **Format visual**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/format-visual.png)

1. On the **Format Visual** pane, enable or disable **Show label**\. This option takes its name from the name of the axis, for example **Show X\-Axis label**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/customize-visual-labels.png)

1. Close the **Format Visual** pane by choosing the X icon in the upper\-right corner of the pane\.

## Customizing the Visual Legend<a name="customizing-visual-legend"></a>

The visual legend helps you identify what a visual element represents by mapping its value to a color\. For example, on a line chart, line color might represent store location\.

To hide or display the legend, you can use the visual menu\. You can also use the **Format Visual** pane, which provides more options\. The visual legend displays to the right of the visual by default\.

When you move your cursor over the legend, a handle appears that you can use to adjust the width of the legend pane by dragging it wider or narrower\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/legend-resize.png)

Use the following procedure to hide or display the visual title\. The visual title displays by default\.

1. On the analysis page, select the visual that you want to format\.

1. Choose the on\-visual menu at the upper\-right corner of the visual, and choose **Display legend** or **Hide legend**\. 

1. Choose **Format visual** to see formatting options\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/format-visual.png)

1. On the **Format Visual** pane, expand the **Legend** section\.

1. Enable or disable **Show legend** and **Show legend title**\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/show-legend2.png)

1. To customize the title of the legend, type a new title in the **Legend** text box\. To revert to the default name, delete your entry\.

1. For **POSITION**, choose **Right**, **Bottom**, or **Top** to determine where on the visual the legend displays\.

1. Close the **Format Visual** pane by choosing the X icon in the upper\-right corner of the pane\.

## Changing the Visual Scale with the Axis Range<a name="changing-visual-scale-axis-range"></a>

To change the scale of the values shown on the visual, you can use the **Format Visual** pane to set the range for one or both axes of the visual\. This option is available for the value axis on bar charts, combo charts, line charts, and scatter plots\. 

By default, the axis range starts at 0 and ends with the highest value for the measure being displayed\. For the group\-by axis, you can use the data zoom tool on the visual to dynamically adjust the scale\.

Use the following procedure to set the axis range for a visual\. 

1. On the analysis page, select the visual that you want to format\.

1. Choose the on\-visual menu at the upper\-right corner of the visual, and then choose **Format visual**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/format-visual.png)

1. On the **Format Visual** pane, choose **X\-Axis** or **Y\-axis**, depending on what type of visual you are customizing\. This is the **X\-Axis** section for horizontal bar charts, the **Y\-Axis** section for vertical bar charts and line charts, and both axes are available for scatter plots\. On combo charts, use **Bars** and **Lines** instead\. 

1. Type a new name in the box to rename the axis\. To revert to the default name, delete your entry\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/customize-visual-scale.png)

1. Set the range for the axis by choosing one of the following options:
   + Choose **Auto \(starting at 0\)** to have the range start at 0 and end around the highest value for the measure being displayed\.
   + Choose **Auto \(based on data range\)** to have the range start at the lowest value for the measure being displayed and end around the highest value for the measure being displayed\.
   + Choose **Custom range** to have the range start and end at values that you specify\.

     If you choose **Custom range**, type the start and end values in the fields in that section\. Typically, you use integers for the range values\. For stacked 100 percent bar charts, use a decimal value to indicate the percentage that you want\. For example, if you want the range to be 0–30 percent instead of 0–100 percent, type 0 for the start value and \.3 for the end value\.

1. To customize the number of values to show on the axis, type in an integer between 1 and 50\.

1. Close the **Format Visual** pane by choosing the X icon in the upper\-right corner of the pane\.