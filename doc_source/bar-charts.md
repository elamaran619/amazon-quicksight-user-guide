# Using Bar Charts<a name="bar-charts"></a>

Amazon QuickSight supports the following types of bar charts, with either horizontal or vertical orientation:
+ Single\-measure
+ Multi\-measure
+ Clustered
+ Stacked
+ Stacked 100 percent

You use these as follows:
+ Use the horizontal or vertical bar chart visual types to create single\-measure, multi\-measure, or clustered bar charts\.
+ Use a single\-measure bar chart to show values for a single measure for a dimension\.
+ Use a multi\-measure bar chart to show values for a two or more measures for a dimension\.
+ Use a clustered bar chart to show values for a single measure for a dimension that is then grouped by another dimension, for example sales total by state, grouped by region\.
+ Use any of the stacked bar chart visual types to create stacked bar charts\. A *stacked bar chart *is similar to a clustered bar chart in that it displays a measure for two dimensions\. However, instead of clustering bars for each child dimension by the parent dimension, it displays one bar per parent dimension\. It uses color blocks within the bars to show the relative values of each item in the child dimension\.

Amazon QuickSight offers both regular stacked bar charts and stacked 100 percent bar charts\. A regular stacked bar chart differs from a stacked 100 percent bar chart in that the color blocks reflect the value of each item in the child dimension relative to the total for the measure\. In contrast, a stacked 100 percent bar chart shows them by their percentage\. 

For example, the following stacked bar chart shows that total sales in the southern region were $2735\.51, with $1474\.96 from Texas and $1260\.55 from Florida\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/stacked-bar1.png)

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/stacked-bar2.png)

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/stacked-bar3.png)

The following stacked 100 percent bar chart shows this same data by percentage, which is 100 percent for the southern region\. The color block for Florida represents the approximately 46 percent of revenue from that state\. The color block for Texas represents the remaining 54 percent\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/stacked-bar4.png)

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/stacked-bar5.png)

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/stacked-bar6.png)

**Topics**
+ [Working with Horizontal Bar Charts](horizontal-bar-chart.md)
+ [Working with Horizontal Stacked Bar Charts](horizontal-stacked-bar-chart.md)
+ [Working with a Horizontal Stacked 100 Percent Bar Chart](horizontal-stacked-100-percent-bar-chart.md)
+ [Working with Vertical Bar Charts](vertical-bar-chart.md)
+ [Working with Vertical Stacked Bar Charts](vertical-stacked-bar-chart.md)
+ [Working with Vertical Stacked 100 Percent Bar Charts](vertical-stacked-100-percent-bar-chart.md)