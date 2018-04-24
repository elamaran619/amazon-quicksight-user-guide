# Adding Drill\-Downs to Visual Data in Amazon QuickSight<a name="adding-drill-downs"></a>

All visual types except pivot tables offer the ability to create a hierarchy of fields for a visual element, and then to drill down to see data at different levels of the hierarchy\. For example, you could associate the country, state, and city fields with the X axis on a bar chart, then drill down or up to see data at each of those levels\. As you drill down each level, the data displayed is refined by the value of the element you drill down on\. For example, if you drill down to city on the bar that represents California at the state level, you get data on all of the cities in California\.

The field wells you can use to create drill\-downs varies by visual type, so refer to the topic for a given visual type to learn more about its drill\-down support\. 

Drill\-down functionality is added automatically when you associate a date field with the drill\-down field well of a visual\. In this case, you can always drill up and down through the levels of date granularity \(year, month, week, day, and hour\)\. 

Use the following table to identify the field wells/on\-visual editors that support drill\-down for each visual type\.


****  

| Visual type | Field well or on\-visual editor | 
| --- | --- | 
| Bar charts \(all Horizontal\) | Y axis and Group/Color | 
| Bar charts \(all Vertical\) | X axis and Group/Color | 
| Combo charts \(all\) | X axis and Group/Color | 
| Geospatial charts | Geospatial and Color | 
| Heat map | Rows and Columns | 
| KPIs | Trend Group | 
| Line charts \(all\) | X axis and Color | 
| Pie chart | Group/Color | 
| Pivot table | Drill\-down not supported | 
| Scatter plot | Group/Color | 
| Tabular Reports | Drill\-down not supported | 
| Tree map | Group by | 

## Adding a Drill\-Down<a name="add-drill-downs"></a>

Use the following procedure to add drill\-down levels to a visual\.

1. On the analysis page, choose the visual you want to add drill\-downs to\.
**Note**  
You can't add drill\-downs to pivot tables\.

1. Expand the **Field wells** pane\.

1. Drag a field that you want to use in the drill\-down hierarchy to an appropriate field well, depending on the visual type\. Make sure that the label for the dragged field says **Add drill\-down layer**\. Position it above or below the existing field based on where you want it to be based on the hierarchy you are creating\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/drill-down1.png)  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/drill-down2.png)  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/drill-down3.png)

1. Continue until you have added all of the levels of hierarchy you want\. To remove a field from the hierarchy, choose the field, and then choose **Remove**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/drill-down4.png)

1. To drill down or up in order to see data at a different level of the hierarchy, choose an element on the visual \(like a line or bar\), and then choose **Drill down to <lower level>** or **Drill up to <higher level>**\. In this example, from the region level you can drill down to state or up to country to see data at those levels\. If you drill down to state from the **Northeast** region, you see only states in that region\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/drill-down5.png)

   After you drill down to see data at the state level, you can then drill down further to see city\-level data, or go back up to region\. If you drill down to city from the color block representing **NJ**, you see only cities in New Jersey\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/drill-down6.png)