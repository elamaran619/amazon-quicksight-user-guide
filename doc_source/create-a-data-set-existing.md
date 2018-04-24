# Creating a Data Set Using an Existing Data Source<a name="create-a-data-set-existing"></a>

After you make an initial connection to a Salesforce, AWS data store, or other database data source, Amazon QuickSight saves the connection information and adds the data source to the **FROM EXISTING DATA SOURCES** section of the **Create a Data Set** page\. You can use these existing data sources to create new data sets without re\-specifying connection information\.

## Creating a Data Set Using an Existing Amazon S3 Data Source<a name="create-a-data-set-existing-s3"></a>

Use the following procedure to create a data set using an existing Amazon S3 data source\.

1. On the Amazon QuickSight start page, choose **Manage data**\.

1. On the **Your Data Sets** page, choose **New data set**\.

1. In the **FROM EXISTING DATA SOURCES** section of the **Create a Data Set** page, choose the Amazon S3 data source to use\.

1. To prepare the data before creating the data set, choose **Edit/Preview data**, to create an analysis using the data as\-is, choose **Visualize**\.

## Creating a Data Set Using an Existing Amazon Athena Data Source<a name="create-a-data-set-existing-athena"></a>

If you want to create a data set using an existing Amazon Athena data source, use the following procedure\.

**To create a data set using an existing Amazon Athena data source**

1. On the Amazon QuickSight start page, choose **Manage data**\.

1. On the **Your Data Sets** page, choose **New data set**\.

1. In the **FROM EXISTING DATA SOURCES** section of the **Create a Data Set** page, choose the Athena data source to use\.

1. Choose **Create data set**\.

1. For **Database: contain sets of tables\.**, choose **Select**, and then choose your Athena database\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/athena-select-dbschema.png)
**Note**  
If you want to create a custom SQL query, click **Edit/Preview data** to edit a query\. If you do this without selecting a table, you see an error in the data preview area\. You can safely ignore this\. The error is saying that there is no data to display until your query is created\. 

1. Choose one of the following options:
   + To prepare the data before creating an analysis, choose **Edit/Preview data** to begin data preparation\. Choose to prepare data at this point if you are planning on writing a SQL query, rather than selecting data from a single table\. For more information about data preparation, see [Preparing Data Sets](preparing-data-sets.md)\.
   + Otherwise, choose a table, and then choose **Select** to confirm\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/athena-select-table.png)

1. If you didn't choose to prepare the data in the previous step, the following screen appears\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/athena-finish-data-set.png)

   To load your data into [SPICE](welcome.md#spice), choose **Import to SPICE**\. The green indicator shows whether or not you have space available\. 

   Alternately, you can choose to query your data without using SPICE\. To do this, choose **Directly query your data**\.

1. After choosing how to query your data, choose one of the following options:
   + To prepare the data before creating an analysis, choose **Edit/Preview data** to begin data preparation for the selected table\. For more information about data preparation, see [Preparing Data Sets](preparing-data-sets.md)\.
   + To create a data set and analyze the data using the table as\-is, choose **Visualize**\.

## Create a Data Set Using an Existing Salesforce Data Source<a name="create-a-data-set-existing-salesforce"></a>

Use the following procedure to create a data set using an existing Salesforce data source\.

1. On the Amazon QuickSight start page, choose **Manage data**\.

1. On the **Your Data Sets** page, choose **New data set**\.

1. In the **FROM EXISTING DATA SOURCES** section of the **Create a Data Set** page, choose the Salesforce data source to use\.

1. Choose **Create Data Set**\.

1. For **Data elements: contain your data**, choose **Select** and then choose either **REPORT** or **OBJECT**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/salesforce2.png)

1. Choose one of the following options:
   + To prepare the data before creating an analysis, choose **Edit/Preview data** to open data preparation\. For more information about data preparation, see [Preparing Data Sets](preparing-data-sets.md)\.
   + Otherwise, choose a report or object and then choose **Select**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/salesforce3.png)

1. Choose one of the following options:
   + To create a data set and an analysis using the data as\-is, choose **Visualize**\.
**Note**  
If you don't have enough [SPICE](welcome.md#spice) capacity, choose **Edit/Preview data**\. In data preparation, you can remove fields from the data set to decrease its size or apply a filter that reduces the number of rows returned\. For more information about data preparation, see [Preparing Data Sets](preparing-data-sets.md)\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/salesforce4.png)
   + To prepare the data before creating an analysis, choose **Edit/Preview data** to open data preparation for the selected report or object\. For more information about data preparation, see [Preparing Data Sets](preparing-data-sets.md)\.

## Creating a Data Set Using an Existing Database Data Source<a name="create-a-data-set-existing-database"></a>

Use the following procedure to create a data set using an existing database data source\.

1. On the Amazon QuickSight start page, choose **Manage data**\.

1. On the **Your Data Sets** page, choose **New data set**\.

1. In the **FROM EXISTING DATA SOURCES** section of the **Create a Data Set** page, choose the database data source to use, and then choose **Create Data Set**\.

1. For **Schema: contain sets of tables**, choose **Select** and then choose a schema\. 

   In some cases where there is only a single schema in the database, that schema is automatically chosen and the schema selection option isn't displayed\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/select-schema.png)

1. Choose one of the following options:
   + To prepare the data before creating an analysis, choose **Edit/Preview data** to open data preparation\. Typically, you would choose to prepare data at this point if you are planning on writing a SQL query rather than selecting data from a single table\. For more information about data preparation, see [Preparing Data Sets](preparing-data-sets.md)\.
   + Otherwise, choose a table and then choose **Select**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/select-table.png)

1. Choose one of the following options:
   + To prepare the data before creating an analysis, choose **Edit/Preview data** to open data preparation for the selected table\. For more information about data preparation, see [Preparing Data Sets](preparing-data-sets.md)\.
   + To create a data set and an analysis using the table data as\-is, and to import the data set data into [SPICE](welcome.md#spice) for improved performance \(recommended\), check the SPICE indicator to see if you have enough space\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/spice-meter.png)

     If you have enough SPICE capacity, choose the **Import to SPICE for quicker analytics** radio button and then create an analysis by choosing **Visualize**\.
**Note**  
If you want to use SPICE and you don't have enough space, choose **Edit/Preview data**\. In data preparation, you can remove fields from the data set to decrease its size, apply a filter, or write a SQL query that reduces the number of rows or columns returned\. For more information about data preparation, see [Preparing Data Sets](preparing-data-sets.md)\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/spice-or-query2.png)
   + To create a data set and an analysis using the table data as\-is, and to have the data queried directly from the database, choose the **Directly query your data** radio button and then create an analysis by choosing **Visualize**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/quicksight/latest/user/images/spice-or-query3.png)