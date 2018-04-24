# Adding a Numeric Filter<a name="add-a-numeric-filter"></a>

Fields with decimal or int data types are considered numeric fields\. You create filters on numeric fields by specifying a comparison type, for example **Greater than** or **Between**, and a comparison value or values as appropriate to the comparison type\. Comparison values must be positive integers and should not contain commas\.

You can use the following comparison types in numeric filters:
+ Equals
+ Does not equal
+ Greater than
+ Less than
+ Greater than or equal to
+ Less than or equal to
+ Between

For data sets based on database queries, you can also optionally apply an aggregate function to the comparison value or values, for example **Sum** or **Average**\. 

You can use the following aggregate functions in numeric filters:
+ Average
+ Count
+ Max
+ Min
+ Sum

## Creating a Numeric Filter<a name="create-a-numeric-filter"></a>

Use the following procedure to create a numeric field filter\.

1. Choose **Filter** on the tool bar\.

1. On the **Applied filters** pane, choose the new filter icon, and then choose a numeric field to filter on\.

   This creates a new filter with no criteria\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/new-numeric-filter.png)

1. Choose the new filter to expand it\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/choose-numeric-filter.png)

1. Choose a comparison type\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/filter-numeric-comparison.png)

1. \(Optional\) If you are using a query\-based data set, choose an aggregate function if you want to use one\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/numeric-filter-aggregate.png)

1. If you have chosen a comparison type other than **Between**, type a comparison value\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/enter-numeric-value.png)

   If you have chosen a comparison type of **Between**, type the beginning of the value range in **Minimum value** and the end of the value range in **Maximum value**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/enter-numeric-value2.png)

1. Choose **Apply**\.