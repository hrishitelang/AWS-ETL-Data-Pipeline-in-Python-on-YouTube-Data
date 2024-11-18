# AWS ETL Data Pipeline in Python on YouTube Data
![alt text](https://github.com/hrishitelang/AWS-ETL-Data-Pipeline-in-Python-on-YouTube-Data/image.jpg?raw=true)

## Problem Statement
The customer required insights to launch a data-driven advertising campaign on YouTube. They sought answers on categorizing videos based on comments and statistics and identifying factors influencing video popularity, such as views, likes, shares, and comments. The dataset included YouTube's top trending videos, sourced from Kaggle, in structured (CSV) and semi-structured (JSON) formats.

## Methodology and Steps
1. Data Lake Setup:

Built a data lake using Amazon S3 to store and manage structured and semi-structured data.
Uploaded raw datasets (JSON and CSV) into a designated landing bucket.

2. Data Processing:
Created a Data Catalog using AWS Glue for metadata management.
Developed a light ETL pipeline using AWS Lambda to:
Convert JSON files to Parquet format for efficient querying.
Address nested JSON structures for easier integration.

3. Data Transformation:
Performed SQL joins on cleaned Parquet files using AWS Athena to integrate data from JSON and CSV sources.
Created another S3 bucket for the reporting layer, holding the aggregated and transformed data.

4. Visualization:
Built a BI dashboard using AWS QuickSight to analyze and visualize insights, including:
Bar graphs summarizing likes and dislikes by genre.
Donut charts showing views by genre and channel titles.
Tools and Technologies
Amazon S3: Data lake and storage.
AWS Glue: Data catalog and ETL management.
AWS Lambda: Serverless ETL for JSON to Parquet conversion.
AWS Athena: SQL querying for data transformation and integration.
AWS QuickSight: Visualization and reporting.
IAM: Configured roles and policies for secure access across services.

5. Challenges Faced
Directly querying nested JSON files was not feasible, requiring an additional ETL step for conversion.
Data cleansing and identifying join keys were essential but complex steps in the process.

6. Outcome
The pipeline provided insights into factors driving video engagement on YouTube, enabling the customer to tailor their advertising campaign. This included visualizations on views, likes, and dislikes categorized by genre and channel titles. The customer successfully launched a campaign using these insights, maximizing user engagement.

## What I Learned
This project enhanced my skills in data engineering, particularly building ETL pipelines and managing data lakes. I gained hands-on experience with AWS services, handling structured and semi-structured data, and creating efficient reporting layers integrated with BI tools. While the dashboards were a byproduct, the focus was on developing robust data pipeline solutions for real-world applications.
