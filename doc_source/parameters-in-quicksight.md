# Parameters in Amazon QuickSight<a name="parameters-in-quicksight"></a>

*Parameters* are named variables that can provide values to an action or an object\. They provide a way to create a connection between the dashboard user and the technical features that make the dashboard interactive\. 

For example, the dashboard user can use a list control to choose a value for a parameter\. That parameter then sets the filter, calculation, or URL action to the chosen value\. Then the visuals in the dashboard react to the user's choices\.

In Amazon QuickSight analyses, you can use parameters in any of the following:
+ Calculated fields
+ Controls \(a control can only exist as part of a parameter\)
+ Filters
+ URL actions

Some ways that you can use parameters are the following:
+ Using a calculation, you can transform data that is shown in an analysis\. 
+ If you add a control with a filter to an analysis you are publishing, the dashboard users can filter the data without creating their own filters\.
+ Using controls and URL actions, you can let dashboard users set values for the URL actions\. 

## Setting Up Parameters in Amazon QuickSight<a name="parameters-set-up"></a>

### Creating or Editing Parameters in Amazon QuickSight<a name="parameters-basic-create-or-edit"></a>

Use the following procedure to create or edit a basic parameter\.

1. Choose an analysis to work with, and decide which field you want to parameterize\. 

1. Choose the **Parameters** pane from the left side of the screen\. 

1. Add a new parameter by choosing the add icon \(**\+**\) near the top of the pane\. Edit an existing parameter by choosing the `v`\-shaped icon near the parameter name and then choosing **Edit parameter**\. 

1. Give the parameter an alphanumeric name and choose its data type\. 

1. Choose **Create** or **Update** to complete creating or updating the parameter\.

After you create a parameter, you can use it in a variety of ways\. You can create a control \(such as a button\) so that you can choose a value for your parameter\. You can also create defaults for each user for your parameter by using the **Set a dynamic default** option\. For more information, see the following sections\.

### Using a Control with a Parameter in Amazon QuickSight<a name="parameters-controls"></a>

In dashboards, parameter controls appear at the top of the data sheet, which contains a set of visuals\. Providing a control allows users to choose a value to use in a predefined filter or URL action\. Dashboard users can use controls to apply filtering across all visuals data sets on a dashboard, without having to create the filters themselves\. 

Use the following procedure to create or edit a control for an existing parameter\. You need to have an existing parameter to create or edit a control\.

1. Choose an existing parameter's context menu, the `v` icon near the parameter name, and choose **Add control**\.

1. Type a name to give the new control a label\. This label displays at the top of the workspace, and later at the top of the sheet that a dashboard displays on\. 

1. Choose a style for the control from the following:
   + **Text box**

     A text box lets a user type in their own value\. A text box works with numbers and text \(strings\)\.
   + **Drop\-down \(single select\)**

     A drop\-down list lets a user select from multiple options, for example, a list of regions or products\. A drop\-down list works with numbers and text \(strings\)\.
   + **Slider**

     A slider lets a user select a numeric value by sliding the control from one end of the bar to another\. A slider works with numbers\.
   + **Date\-picker**

     A date\-picker lets a user select a date from a calendar control\. 

1. \(Optional\) If you choose a drop\-down control, the screen expands so you can choose the values to display\. You can either specify a list of values, or use a field in a data set\. Choose one of the following:
   + **Specific values**

     To create a list of specific values, type in one per line, with no separating spaces or commas, as shown in the following screenshot\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/parameters-controls-specific-values.png)

     In the control, the values display in the order you typed them, not alphabetically\.
   + **Link to a data set field**

     To link to a field, choose the data set that contains your field, then choose the field from the list\. The values display alphabetically in the control\.

     If you change the default values in the parameter, choose **Reset** on the control to show the new values\.

1. When you finish choosing options for your control, choose **Add**\.

The finished control appears at the top of the workspace\. The context menu, shaped like a `v`, offers four options:
+ **Reset** restores the user's selection to its default state\.
+ **Refresh list** applies only to drop\-downs that are linked to a field in a data set\. Choosing **Refresh list** queries the data to check for changes\. Data used in the control is cached\.
+ **Edit** reopens the control creation screen so that you can change your settings\.
+ **Delete** removes the control\. You can recreate it by choosing the parameter context menu\.

In the workspace, you can also resize and rearrange your controls\. The dashboard users see them as you do, except without being able to edit or delete them\.

### Creating Parameter Defaults in Amazon QuickSight<a name="parameters-default-values"></a>

Use this section to learn more about the types of parameter defaults that are available, and how to set up each of them\. If you set up a dynamic default, the parameter's control automatically uses that user's preselected default\. In the absence of a dynamic default, the parameter's control uses the static default\.

Use the following procedure to create or edit a static \(unchanging\) default value for a parameter\. 

1. Choose the context menu \(`v`\) by the parameter you want to edit, or create a new parameter by following the steps in [Creating or Editing Parameters in Amazon QuickSight](#parameters-basic-create-or-edit)\. 

1. To set a static default, type one in the **Default value** field\. Otherwise, leave this blank\. The value you set for a static default can't be changed by the dashboard user\. 

To create or edit an optional dynamic default value for a parameter, use the following procedure\. The data set for dynamic defaults can use a database query or an uploaded file\. 

1. Create a database table or SQL query similar to the following\. For the sake of maintainability, the names of other fields \(columns\) should closely match those in the data set you are analyzing\. It doesn't matter what order the fields are in\. It also doesn't matter if there are fields in this data set that aren't in the current analysis\. 

   `UserID` must be unique in the data set\.     
[\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/quicksight/latest/user/parameters-in-quicksight.html)

   After you finish this procedure, you can use these fields to choose the default settings for each user, based on a filter you create\. To learn more about using filters with parameters, see [Using Filters with Parameters in Amazon QuickSight](#parameters-filtering-by)\.

1. Create a data set based on this data, and add it to your analysis\.

1. Open the **Parameters** pane, choose a parameter's context \(`v`\) menu, and choose **Edit parameter**\. 

1. Choose **Set a dynamic default**\. 

1. Choose the data set you put your user ID and dynamic default values in\. Then choose the `UserID` column for the **User name column**\. Next, choose the relevant value field for the **Default value column**, for example `Region` or `Segment`\.

1. Choose **Apply** to save your changes\. After you finish this step, each user's dynamic default value is used in the parameter controls\. This doesn't stop them from choosing a different value\. 

   If a dynamic default can't be resolved to a single value, Amazon QuickSight uses the static default value\. If a user has no dynamic default value, or the user ID doesn't exist in the data set, then the static default value is used\. If there is no static default either, then the user can still choose values from the controls\.

**Note**  
If you are trying to use a parameter with dynamic values by linking to a data set \(rather than trying to create dynamic defaults\), don't use the **Set a dynamic default** option\. Instead, use a control to offer dynamic values in a list, as explained in [Using a Control with a Parameter in Amazon QuickSight](#parameters-controls)\.

## Connecting to Parameters in Amazon QuickSight<a name="parameters-connections"></a>

Use this section after you have a parameter set up, to connect it and make it work\. 

After you create a parameter, the following screen appears\. You can choose your next step from this screen\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/parameters-connect.png)

### Using Filters with Parameters in Amazon QuickSight<a name="parameters-filtering-by"></a>

Use this section to filter the data in an analysis or dashboard by a parameter value\. Before using a filter with a parameter, you should already know how to work with filters\. 

1. Verify that your analysis has a parameter already created\. Choose **Edit** from either the parameter or the control's menu to find out what settings are in use\.

1. Choose the **Filter** pane from the left side of the screen\. If there is already a filter for the field that you want to use, choose it to open its settings\. Otherwise, create a filter for the field that you want to filter by parameter\.

1. Select** Use Parameters**\.

1. Choose your parameters from the list or lists below **Use parameters**\. For text \(string\) fields, first choose **Custom Filter**, and then enable **Use Parameters**\.

   For date fields, choose the **Start date** and **End date** parameters, as shown in the following screenshot\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/parameters-add-a-filter-datetime.png)

   For fields with other data types, choose **Select a parameter** and then choose your parameter from the list\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/parameters-add-to-filter-text.png)

1. Choose **Apply** to save your changes\.

Test your new filter by choosing the control in the workspace\. In this example, we use a basic parameter that has no defaults, and a dynamic control that is linked to the **Region** field in the sample data set named **Sales Pipeline**\. The control queries the data, returning all values\. 

Two context menus appear in the following screenshot\. The menu that is highlighted in the screenshot manages the parameter\. The menu that is not highlighted manages the control settings\. Using the control's menu, you can reset the control by choosing **Reset**, or refresh your data by choosing **Refresh list**\. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/parameters-using-in-a-control.png)

If you delete or rename a parameter that you are using in a filter, you can update the filter with the new parameter\. Open the filter, choose the new parameter that you want to use, and then choose **Apply**\.

### Using Calculated Fields with Parameters in Amazon QuickSight<a name="parameters-calculated-fields"></a>

You can pass the value of a parameter to a calculated field in an analysis\. When you create a calculation, you can choose existing parameters from the list of parameters under **Parameter list**\. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/add-calc-field3.png)

### Using Custom URL Actions with Parameters in Amazon QuickSight<a name="parameters-custom-URL-actions"></a>

You can pass or send parameters to custom URL actions\. For example, you could add a parameter to a custom URL action so you can send it to another URL\. The parameters on both the sending and the receiving end should match in name and data type\.

To use a parameter in a custom URL action, select it from the list\. Parameters are enclosed in curly braces, for example: `{Region}`, or `{StartDate}`\.