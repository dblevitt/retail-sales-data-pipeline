# Retail Sales Data Engineering Pipeline

This project demonstrates a complete end-to-end data engineering pipeline using AWS and Python. The goal is to simulate a real-world workflow where raw sales data is collected, processed, stored in a production-ready database, and made ready for analysis.

## Tools Used
- **AWS S3**: For storing raw CSV data
- **Google Colab + Python**: For data cleaning, transformation, and PostgreSQL connection
- **Pandas**: For data manipulation
- **SQLAlchemy + psycopg2**: For writing data into PostgreSQL
- **AWS RDS (PostgreSQL)**: As the final cloud-hosted relational database

## What This Project Does
1. Loads a raw retail sales CSV file into Google Colab
2. Cleans and processes the data using Python
3. Uploads the cleaned data into a PostgreSQL database hosted on AWS RDS
4. Executes test SQL queries to verify successful storage and access

## How to Run This Yourself
1. Clone the repo or open the notebook in Google Colab
2. Replace the placeholders with your actual AWS RDS credentials 
3. Run each cell step-by-step
4. The data will be uploaded to your PostgreSQL instance under the table "retail_sales"

## Example Output
Sample SQL query:
**SELECT * FROM retail_sales LIMIT 5;**
Returns a snapshot of the transformed data, confirming successful ingestion.
