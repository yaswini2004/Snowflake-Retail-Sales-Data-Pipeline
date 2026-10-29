
# Snowflake Retail Sales Data Pipeline

An end-to-end retail sales data engineering project using Snowflake SQL to automate data ingestion, validation, transformation, and incremental processing for sales analytics and business reporting.

## Features

- Automated CSV data ingestion using Snowflake internal stages and file formats
- Data preview and validation before loading into target tables
- Loaded and validated 9,995 retail sales records using `COPY INTO`
- Implemented SQL User-Defined Functions (UDFs) for data cleaning and transformation
- Standardized customer, order, and product identifiers
- Calculated order year, shipping duration, and sales revenue
- Implemented Snowflake Streams to capture incremental data changes
- Configured Snowflake Tasks for scheduled processing
- Used `MERGE` operations to synchronize transformed data
- Monitored ingestion status and errors using Snowflake load history

## Technologies Used

- **Cloud Data Warehouse:** Snowflake
- **Query Language:** SQL
- **Data Ingestion:** Internal Stages, CSV File Formats, `COPY INTO`
- **Data Transformation:** User-Defined Functions (UDFs)
- **Incremental Processing:** Snowflake Streams and Tasks
- **Data Operations:** INSERT, MERGE, Data Validation, Load History

## Project Architecture

```text
Retail Sales CSV Files
          |
          v
Snowflake Internal Stage
          |
          v
CSV File Format & Validation
          |
          v
COPY INTO Raw Sales Table
          |
          v
SQL Transformations (UDFs)
          |
          v
Transformed Retail Sales Table
          |
          v
Streams + Scheduled Tasks
          |
          v
Incremental MERGE Processing
          |
          v
Sales Analytics & Reporting
```

## Project Workflow

1. **Database Setup:** Created a Snowflake database and schema for retail sales processing.
2. **File Format and Staging:** Configured the CSV file format and internal stage for raw data ingestion.
3. **Data Loading:** Uploaded the CSV dataset and loaded 9,995 records into the raw sales table.
4. **Data Transformation:** Created UDFs to standardize identifiers and calculate analytical attributes.
5. **Incremental Processing:** Configured Streams and Tasks to capture and process data changes.
6. **Monitoring and Validation:** Verified loaded records, transformation results, and ingestion status using SQL queries and load history.

## Setup and Execution

### Prerequisites

- Snowflake account with appropriate database and warehouse privileges
- Retail sales dataset in CSV format
- Access to a Snowflake SQL worksheet

### Steps

1. Create the project database and schema.
2. Create the CSV file format and internal stage.
3. Upload the retail sales CSV file to the stage.
4. Create the raw sales table with appropriate column data types.
5. Load the data using `COPY INTO`.
6. Create the transformation UDFs and target retail sales table.
7. Configure Streams and Tasks for incremental processing.
8. Validate the results using SQL queries.

## Key Outcomes

- Successfully loaded and validated 9,995 sales records.
- Standardized identifiers to improve data consistency.
- Derived sales revenue and shipping duration for business analysis.
- Designed an incremental processing workflow using Snowflake Streams and Tasks.
- Established ingestion monitoring and data validation procedures.

## Future Enhancements

- Integrate automated CSV file delivery.
- Add data quality checks for invalid or duplicate records.
- Build interactive dashboards for sales and customer analytics.
- Add automated pipeline failure alerts.

## License

Specify the license applicable to this repository.
