# Setting Up Parameters in Amazon QuickSight<a name="parameters-set-up"></a>

**Topics**
+ [Creating or Editing Parameters](#parameters-basic-create-or-edit)
+ [Parameter Controls](#parameters-controls)
+ [Parameter Defaults](#parameters-default-values)

## Creating or Editing Parameters in Amazon QuickSight<a name="parameters-basic-create-or-edit"></a>

Use the following procedure to create or edit a basic parameter\.

1. Choose an analysis to work with, and decide which field you want to parameterize\. 

1. Choose the **Parameters** pane from the left side of the screen\. 

1. Add a new parameter by choosing the add icon \(**\+**\) near the top of the pane\. 

   Edit an existing parameter by first choosing the `v`\-shaped icon near the parameter name and then choosing **Edit parameter**\. 

1. The following screen appears\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/parameter-create-or-edit.png)

   A parameter consists of the following parts, which you enter on this screen:  
Name  
Type in an alphanumeric value for the parameter **Name**\. This name is used as a reference in the consumers of the parameters \(for example, calculated field, filter, custom URL action, and so on\)\. For ease of use, you can choose a name that reflects the data type and purpose of the parameter\.  
Data type  
Choose a value for **Data type**\. This data type can't be altered after you create the parameter\. If you want to use the parameter for a text box or drop\-down list, choose `String`\.  
Default value  
Type in a value for **Default value** for the parameter\. This static value is used during the first page load, if a dynamic default value or URL parameter isn't provided\.  
Dynamic default value  
Choose **Set a dynamic default** to create a default that is user\-specific\. A *dynamic default *is a per\-user default value for the first page load of the dashboard\. It lets you create a personalized view for each user\.   
Calculated fields can't be used as dynamic defaults\.   
Dynamic defaults don't prevent a user from selecting a different value\. If you want to also secure the data, you can add row\-level locking\. For more information, see [Restricting Access to a Data Set by Using Row\-Level Security](restrict-access-to-a-data-set-using-row-level-security.md)\.

1. Choose **Create** or **Update** to complete creating or updating the parameter\.

After you create a parameter, you can use it in a variety of ways\. You can create a control \(such as a button\) so that you can choose a value for your parameter\. For more information, see the following sections\.

## Using a Control with a Parameter in Amazon QuickSight<a name="parameters-controls"></a>

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

     To link to a field, choose the data set that contains your field, then choose the field from the list\. It can't be a calculated field\. The values display alphabetically in the control\. Using more than 10,000 distinct values for linked data isn't supported\. If you need more than 10,000 values, you can enter them in **Specific values**\.

     If you change the default values in the parameter, choose **Reset** on the control to show the new values\.

1. When you finish choosing options for your control, choose **Add**\.

The finished control appears at the top of the workspace\. The context menu, shaped like a `v`, offers four options:
+ **Reset** restores the user's selection to its default state\.
+ **Refresh list** applies only to drop\-downs that are linked to a field in a data set\. Choosing **Refresh list** queries the data to check for changes\. Data used in the control is cached\.
+ **Edit** reopens the control creation screen so that you can change your settings\.
+ **Delete** removes the control\. You can recreate it by choosing the parameter context menu\.

In the workspace, you can also resize and rearrange your controls\. The dashboard users see them as you do, except without being able to edit or delete them\.

## Creating Parameter Defaults in Amazon QuickSight<a name="parameters-default-values"></a>

Use this section to learn more about the types of parameter defaults that are available, and how to set up each of them\. If you set up a dynamic default, the parameter's control automatically uses that user's preselected default\. In the absence of a dynamic default, the parameter's control uses the static default\.

Use the following procedure to create or edit a static \(unchanging\) default value for a parameter\. 

1. Choose the context menu \(`v`\) by the parameter you want to edit, or create a new parameter by following the steps in [Creating or Editing Parameters in Amazon QuickSight](#parameters-basic-create-or-edit)\. 

1. To set a static default, type a value in the **Default value** field\. Otherwise, leave this blank\. The value you set for a static default can't be changed by the dashboard user\. 

To create or edit an optional dynamic default value for a parameter, use the following procedure\. The data set for dynamic defaults can use a database query or an uploaded file\. 

1. Create a database table or SQL query similar to the following\. For the sake of maintainability, the names of other fields \(columns\) should closely match those in the data set you are analyzing\. It doesn't matter what order the fields are in\. It also doesn't matter if there are fields in this data set that aren't in the current analysis\. 

   `UserID` must be unique in the data set\.     
[\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/quicksight/latest/user/parameters-set-up.html)

   After you finish this procedure, you can use these fields to choose the default settings for each user, based on a filter you create\. To learn more about using filters with parameters, see [Using Filters with Parameters in Amazon QuickSight](parameters-filtering-by.md)\.

1. Create a data set based on this data, and add it to your analysis\.

1. Open the **Parameters** pane, choose a parameter's context \(`v`\) menu, and choose **Edit parameter**\. 

1. Choose **Set a dynamic default**\. 

1. Choose the data set you put your user ID and dynamic default values in\. Then choose the `UserID` column for the **User name column**\. Next, choose the relevant value field for the **Default value column**, for example `Region` or `Segment`\.

1. Choose **Apply** to save your changes\. After you finish this step, each user's dynamic default value is used in the parameter controls\. This doesn't stop them from choosing a different value\. 

   If a dynamic default can't be resolved to a single value, Amazon QuickSight uses the static default value\. If a user has no dynamic default value, or the user ID doesn't exist in the data set, then the static default value is used\. If there is no static default either, then the user can still choose values from the controls\.