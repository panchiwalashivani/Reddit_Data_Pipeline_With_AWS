# Reddit_Data_Pipeline_With_AWS

Data Pipeline with Reddit, Airflow, Celery, Postgres, S3, AWS Glue, Athena, and Redshift

This project provides a comprehensive data pipeline solution to extract, transform, and load (ETL) Reddit data into a Redshift data warehouse. The pipeline leverages a combination of tools and services including Apache Airflow, Celery, PostgreSQL, Amazon S3, AWS Glue, Amazon Athena, and Amazon Redshift.

Ref: https://www.youtube.com/watch?v=LSlt6iVI_9Y&t=176s&ab_channel=CodeWithYu

## Overview
The pipeline is designed to:

Extract data from Reddit using its API.
Store the raw data into an S3 bucket from Airflow.
Transform the data using AWS Glue and Amazon Athena.
Load the transformed data into Amazon Redshift for analytics and querying.

## Architecture

![image](https://github.com/panchiwalashivani/Reddit_Data_Pipeline_With_AWS/assets/72301600/99681b6d-fb7d-44a9-9955-19a27648be76)

Reddit API: Source of the data.

Apache Airflow: Orchestrates the ETL process and manages task distribution.

PostgreSQL: Temporary storage and metadata management.

Amazon S3: Raw data storage.

AWS Glue: Data cataloging and ETL jobs.

Amazon Athena: SQL-based data transformation.

Amazon Redshift: Data warehousing and analytics.

## System Setup
Create a virtual environment.

 python3 -m venv venv
 
Activate the virtual environment.

 source venv/bin/activate
 
Install the dependencies.

 pip install -r requirements.txt
 
Rename the configuration file and the credentials to the file.

 mv config/config.conf.example config/config.conf
 
Starting the containers

 docker-compose up -d
 
Launch the Airflow web UI.

 open http://localhost:8080
