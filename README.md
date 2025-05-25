## Notebooks

This project includes two versions of the pipeline:

- retail_pipeline_basic.ipynb: Loads and cleans data from AWS S3 using Python.

- retail_pipeline_to_postgresql.ipynb: Extends the pipeline by securely uploading the cleaned data into a PostgreSQL database on AWS RDS.

# retail_pipeline_basic.ipynb

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

# retail_pipeline_to_postgresql.ipynb

This version builds on the basic pipeline by securely uploading the cleaned data into a cloud-hosted PostgreSQL database using AWS RDS. It simulates a real-world backend data flow, where data isn’t just analyzed but stored in a scalable production environment.

## Tools Used
- **AWS S3**: For pulling the raw CSV data
- **Google Colab + Python**: For processing the data
- **Pandas**: For manipulation and validation
- **SQLAlchemy + psycopg2**: For securely connecting to the PostgreSQL database
- **AWS RDS (PostgreSQL)**: For storing the cleaned data in the cloud

## What This Project Adds
1. Prompts the user to securely enter AWS RDS host and password
2. Verifies that total revenue = quantity × price per unit
3. Uploads the cleaned data to a PostgreSQL table (`retail_sales`)
4. Runs a test SQL query from Colab to confirm success

## How to Run This Yourself
1. Open the notebook in Google Colab
2. When prompted, enter your own AWS RDS host and password (kept private)
3. Execute each cell in order
4. Check your PostgreSQL database for the uploaded data

## Example Output
**Test Query:**
```sql
SELECT * FROM retail_sales LIMIT 5;
