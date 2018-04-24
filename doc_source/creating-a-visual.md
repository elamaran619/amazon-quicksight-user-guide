# Creating an Amazon QuickSight Visual<a name="creating-a-visual"></a>

You can create a visual in several ways\. You can select the fields you want and use AutoGraph to let Amazon QuickSight determine the most appropriate visual type, or you can choose a specific visual type and choose fields to populate it\. Alternatively, if you aren't sure what questions your data can answer for you, you can choose **Suggested** on the tool bar and choose a visual that Amazon QuickSight suggests for you\. Suggested visuals are ones that we think are of interest, based on a preliminary examination of your data\. For more information about AutoGraph, see [Using AutoGraph](autograph.md)\.

To create a useful visual, it helps to know what question you are trying to answer as specifically as possible, and to use the smallest data set that can answer that question\. Doing so helps you create simpler visuals that are easier to analyze\. 

## Fields as Dimensions and Measures<a name="dimensions-and-measures"></a>

In the **Fields list** pane, dimension fields have blue icons and measure fields have green icons\. Dimensions are text or date fields that can be items, like products, or attributes that are related to measures and can be used to partition them, like sales date for sales figures\. Measures are numeric values that you use for measurement, comparison, and aggregation\. You typically use a combination of dimension and measure fields to produce a visual, for example sales totals \(a measure\) by sales date \(a dimension\)\. For more information about the types of fields expected by the different visual types, see the specific visual type topics in the [Working with Visual Types in Amazon QuickSight](working-with-visual-types.md) section\. For more information about changing a field's measure or dimension setting, see [Setting a Field as a Dimension or Measure](setting-dimension-or-measure.md)\.

## Field Limitations<a name="visual-field-limitations"></a>

You can only use one date field per visual\. This limitation applies to all visual types\.

You can't use the same field for more than one dimension field well or drop target on a visual\. For more information about how expected field type is indicated by field wells and drop targets, see [Using Visual Field Controls](using-visual-field-controls.md)\.

## Searching for Fields<a name="searching-for-a-field"></a>

If you have a long field list in the **Fields list** pane, you can search to locate a specific field by choosing the search icon at the top of the **Fields list** pane and then typing a search term into the search box\. Any field whose name contains the search term is shown\. Search is case\-insensitive and wildcards are not supported\. Choose the cancel icon \(**X**\) to the right of the search box to return to viewing all fields\.

## Creating a Visual<a name="create-a-visual"></a>

Use the following procedure to create a new visual\.

1. On the Amazon QuickSight start page, choose the analysis that you want to add a visual to\.

1. On the analysis page, choose the data set you want to use from the data set list at the top of the **Fields list** pane\. For more information, see [Adding a Data Set to an Analysis](adding-a-data-set-to-an-analysis.md)\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/data-set-dropdown.png)

1. Choose **Add** on the application bar, and then choose **Add visual**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/add-visual.png)

   A new, blank visual is created and receives focus\.

1. Choose one of the following options:
   + Create a visual by choosing fields and letting Amazon QuickSight determine the most appropriate visual type\.

     1. In the **Visual types** pane, choose the AutoGraph icon\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/autograph-icon.png)

     1. In the **Fields list** pane, choose the fields you want to use\.

        Amazon QuickSight creates the visual, using the visual type it determines is most compatible with the data you selected\.
   + Create a visual by choosing a visual type and then choosing fields to populate it\.

     1. In the **Visual types** pane, choose the icon of the visual type you want to use\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/visual-types.png)

        The field wells for that visual type open at the top of the visual pane\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/field-wells.png)

     1. From the **Fields list** pane, drag the fields you want to use to the appropriate field wells\. Typically, you want to use dimension or measure fields as indicated by the color of the target field well\. If you choose to use a dimension field to populate a **Value** field well, the **Count** aggregate function is automatically applied to it to create a numeric value\.

        Amazon QuickSight creates the visual using the visual type you selected\.
   + Create a visual using a suggestion\.

     On the tool bar, choose **Suggested**, then choose a suggested visual\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/visuals-pane.png)