# Data Engineer Pipeline Project using AWS S3 - GLUE - ATHENA - QUICKSIGHT
The ETL pipeline is using S3 as data Lake and  AWS GLUE ETL as access datalake. Using ATHENA to query a view.<br/><br/>

## Porject Background
Data engineering immersion day Project. The project will be completing the following tasks. Data Validation and ETL with Glue to be tables that can be queried using Amazon Athena and Visualize with Amazon Quciksight

Data architecture that needs to be created:<br/><br/>
<img src="https://github.com/Jira-saki/ETL-AWS-GLUE/blob/master/image/architect-diagram.png"><br/><br/>

1. Retrieve data from RDS Postgres and then save it into datalake in the form of csv file.
2. Add Glue Clawler to create Data Catalog.
3. Perform ETL using Glue Studio
4. Create View with Athena
5. Create a visualization using Quicksight to display a sport events graph.

## Prerequisites
- AWS Account
- IAM , Resource permission setting


## Getting Started

 - **Import the data set from RDS Postgres to Datalake**<br/>
Using AWS CLI to import data.
<img src="https://github.com/Jira-saki/ETL-AWS-GLUE/blob/master/image/rds-s3.png"><br/>
 
 - **Datalake (S3)**<br/>
The files is storing in S3 "tickets" directory.<br/>
<img src="https://github.com/Jira-saki/ETL-AWS-GLUE/blob/master/image/dataset-in-s3.png"><br/><br/>

- **Add Clawler Process**<br/>
Create data catalog (database and tables) in Glue. Edit schema in each table.<br/><br/>

- **Run job in Glue Studio**<br/>
Check incorrect schema and creat job to processed data in parquet format.<br/>
<img src="https://github.com/Jira-saki/ETL-AWS-GLUE/blob/master/image/job-succeeded.png"><br/><br/>



- **Create Glue Crawler for Parquet Files**<br/>
Add Crawler . Once crawler has finished running, Tables were added. Then and Run Crawler.<br/>
<img src="https://github.com/Jira-saki/ETL-AWS-GLUE/blob/master/image/parquet-crawler.png"><br/><br/>
<img src="https://github.com/Jira-saki/ETL-AWS-GLUE/blob/master/image/parquet-table.png"><br/><br/>

- **Create View (Athena)**<br/>
Query data and create a view with Amazon Athena
Athena Workgroups to Control Query Access and Costs.<br/>
<br/>
<img src="https://github.com/Jira-saki/ETL-AWS-GLUE/blob/master/image/query-view-Athena.png"><br/><br/>

### Visualization (Quicksight)
Data visualization is created from dataset in QuickSight
<img src="https://github.com/Jira-saki/ETL-AWS-GLUE/blob/master/image/dashboard.png"><br/><br/>
