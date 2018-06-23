# Adding a Text Filter<a name="add-a-text-filter"></a>

You can filter text fields by either choosing field values from a list or by specifying field values\.

Use the **Filter list** filter type to filter by choosing field values\. Using this filter type, Amazon QuickSight retrieves a list of the field values for the selected field\. You choose the values that you want to filter on, and whether you want to include or exclude records with those values\.

**Important**  
You are only offered this option in cases where Amazon QuickSight can quickly retrieve the full set of field values\. In cases where the data set is very large or there's a very high number of unique values, this is not possible, and you must filter by specifying field values instead\.

You can filter by specifying field values by using either the **Custom filter list** filter type or the **Custom filter** filter type\. 

With the **Custom filter list** filter type, you specify one or more field values to filter on, and whether you want to include or exclude records that contain those values\. The specified value and actual field value must match exactly in order for the filter to be applied to a given record\.

With the **Custom filter** filter type, you specify a single value that the field value must equal or not equal\. If you choose an equal comparison, the specified value and actual field value must match exactly in order for the filter to be applied to a given record\.

For any type of text filter, you can refresh the list of field values by choosing the refresh icon\. This is helpful when you have created a filter before Amazon QuickSight has retrieved the entire data set and so does not initially have a complete list to display\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/refresh-filter.png)

Details on how to create each type of text field filter are provided in the following sections\.

## Adding a Text Filter by Choosing Field Values<a name="add-a-text-filter-choose-values"></a>

Use the following procedure to create a text field filter for by selecting field values\.

**Important**  
You can only filter by choosing field values in cases where Amazon QuickSight can quickly retrieve the full set of values\. In cases where you are working with very large record sets and this is not possible, you must filter by specifying field values instead\. For more information about filtering with specified field values, see [Adding a Text Filter by Specifying Multiple Field Values](#add-text-custom-filter-list) and [Adding a Text Filter by Specifying a Single Field Value](#add-text-filter-custom-list)\.

1. Choose **Filter** on the tool bar\.

1. On the **Applied filters** pane, choose the new filter icon, and then choose a text field to filter on\. 

   This creates a new filter with no criteria\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/choose-text-filter-field.png)

1. Choose the new filter to expand it\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/choose-text-filter.png)

1. Choose **Filter list** for the filter type\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/filter-list.png)

1. Choose whether to include or exclude records that contain the field values you will select in the next step\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/pick-fields-include.png)

1. Select the field values that you want to filter on\.

   Scroll through the checklist and select or clear values, or toggle the **ALL** check box to select or deselect all of the values at once\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/filter-text-select.png)

   Toggle the sort icon to change the sort order of the field values from ascending \(the default\) to descending and back\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/sort-filter-field.png)

   To narrow down the values displayed, type a search term into the box above the checklist and choose **Search**\. Search terms are case\-insensitive and wildcards are not supported\. Any field value that contains the search term is returned\. For example, searching on **L** returns **al**, **AL**, **la**, and **LA**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/text-filter-search.png)

   To return to viewing the full set of field values rather than just those that match the search term, choose **Search** again\.
**Note**  
The filter list can display up to 10,000 values\. If you have more than 10,000 values in your list, use a custom filter\. For information about custom filters, see [Adding a Text Filter by Specifying Multiple Field Values](#add-text-custom-filter-list)\. 

## Adding a Text Filter by Specifying Multiple Field Values<a name="add-text-custom-filter-list"></a>

You can use the **Custom filter list** filter type to specify one or more field values to filter on, and choose whether you want to include or exclude records that contain those values\. The specified value and actual field value must match exactly in order for the filter to be applied to a given record\. 

Use the following procedure to create a text field filter by specifying exact field values\.

1. Choose **Filter** on the tool bar\.

1. On the **Applied filters** pane, choose the new filter icon, and then choose a text field to filter on\. 

   This creates a new filter with no criteria\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/choose-text-filter-field.png)

1. Choose the new filter to expand it\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/choose-text-filter.png)

1. Choose **Custom filter list** for the filter type\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/custom-filter-list.png)

1. Type a field value in **Enter a value to add**, and then choose the add icon\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/add-field-value.png)  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/add-icon.png)

   To remove a field value from the criteria, choose its delete icon\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/delete-icon.png)

1. \(Optional\) Repeat Step 5 until you have added all of the field values that you want to filter on\.

1. Choose whether to include or exclude records that contain the field values you selected\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/custom-filter-list-include.png)

1. Choose **Apply**\.

## Adding a Text Filter by Specifying a Single Field Value<a name="add-text-filter-custom-list"></a>

With the **Custom filter** filter type, you specify a single value that the field value must equal or not equal\. If you choose an equal comparison, the specified value and actual field value must match exactly in order for the filter to be applied to a given record\.

Use the following procedure to create a text field filter by specifying one field value\.

1. Choose **Filter** on the tool bar\.

1. On the **Applied filters** pane, choose the new filter icon, and then choose a text field to filter on\. 

   This creates a new filter with no criteria\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/choose-text-filter-field.png)

1. Choose the new filter to expand it\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/choose-text-filter.png)

1. Choose **Custom filter** for the filter type\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/custom-filter.png)

1. Choose a comparison type\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/filter-equals.png)

1. Type a field value in the **value** field\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/custom-value.png)

1. Choose **Apply**\.