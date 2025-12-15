This project implements an event-driven data analytics pipeline on AWS to ingest, process, and analyze Spotify data. 
Raw data files (CSV/JSON) are uploaded to Amazon S3, which orchestrate AWS Glue ETL jobs to transform and store curated datasets in the processed data folder.
The processed data is cataloged using AWS Glue Crawlers and queried using Amazon Athena for analytics.
ETL PIPELINE 
Storage layer 
o Amazon S3 bucket 
   Raw data 
   Processed data
Processing layer  
o AWS Glue ETL Jobs: Creates dimension tables from raw data and creates fact 
tables referencing dimension tables 
Data Crawling 
o Processed-data crawler: Scans the processed data files to create catalog 
o Raw-data crawler: Scans the raw data files to create catalog tables 
Serving layer 
o AWS Athena is used as a SQL query interface for the analytics. It enables 
direct querying of the processed data 
