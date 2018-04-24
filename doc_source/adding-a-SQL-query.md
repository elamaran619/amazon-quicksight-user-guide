# Using a SQL Query<a name="adding-a-SQL-query"></a>

When creating a new database data set, you can choose an existing SQL query or create a new SQL query to refine the data retrieved from a database, or to combine data from multiple tables\. Using a SQL query, you can specify SQL statements in addition to any join criteria in order to refine the data set\. If all you want to do is join multiple tables by specifying the join type and the fields to use to join the tables, you can use the join interface instead\. For more information about using the join interface, see [Joining Tables](joining-tables.md)\.

You can only specify a SQL query for data sets based on SQL database data sources\.

**Important**  
If you chose a table and made any changes to the fields \(for example, changing a field name or adding a calculated field\), these changes are discarded when you switch from the table selector to the Custom SQL tool\.

## Creating a Custom SQL Query<a name="add-a-SQL-query"></a>

Use the following procedure to create a custom SQL query to define a data set\.

1. Create a new database data set and open it for data preparation\. For more information about creating a data set from a database, see [Creating Data Sets from New Database Data Sources](creating-database-data-sets.md)\.

1. On the data preparation page, expand the **Tables** pane and then choose **Switch to Custom SQL tool**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/choose-sql.png)
**Tip**  
In some cases, Amazon QuickSight can't change a table data source into a query\. In this case, the screen doesn't display the option to switch to a custom SQL query\. To use a query instead, create a new data set that is based on the query you want to use\. 

1. Do one of the following:
   + Choose an existing query in the **Custom SQL** pane\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/existing-query.png)
   + Enter information for a new SQL query:
     + In the **Custom SQL** pane, choose **New Custom SQL**\.
     + For **Custom SQL name**, type a query name\.
     + For **Custom SQL**, type or paste in a SQL query\. The query must conform to the SQL syntax of the target database engine in terms of capitalization, command termination, and other requirements\.
**Note**  
The **Custom SQL** box has no query editing functionality\. It's significantly easier to create the query you want in your SQL editor of choice and then paste it in\.
     + Choose **Finish**\. The query is processed and the query results display in the data preview pane\. The saved query appears in the **Custom SQL** pane\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/enter-sql.png)

### Switching Back to Using a Table<a name="switch-to-table"></a>

To stop using a SQL query and use regular table data instead, choose **Switch to table selector** in the **Custom SQL** pane, and then choose a table\. You can only do this with new data sets\. Once you have saved the data set to use a SQL query, you can edit the query, but you can't switch to using a table\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/table-selector.png)

### Modifying Existing Queries<a name="modifying-existing-queries"></a>

To update an existing data set based on a SQL query, choose **Edit SQL** on the **Fields** pane to open the SQL pane and edit the query\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/edit-sql.png)