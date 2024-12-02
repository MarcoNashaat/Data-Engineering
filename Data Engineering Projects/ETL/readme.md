# ETL Project: Customer Transactions Data

## Overview

This project demonstrates the end-to-end process of extracting, transforming, and loading (ETL) data from multiple sources into a MySQL database. The data simulates a business environment where transactions are linked to customers and products.

### Purpose
The main goal of this project is to practice ETL processes, including:
- Extracting data from external sources (Mockaroo API).
- Transforming data by cleaning and applying basic transformations and user-defined rules.
- Loading data into a MySQL database for further analysis.

## Tools & Libraries
- **Python**: Main programming language for data processing and API integration.
- **MySQL**: Database used for storing the final transformed data.
- **pandas**: Library for data manipulation and cleaning.
- **requests**: Used for making HTTP requests to the Mockaroo API to fetch the data.
- **curl**: Used as an alternative for data extraction via the command line.

## Methods
- **Data Extraction**: Data is fetched from the Mockaroo API using `requests` (or `curl` in the command line).
- **Data Transformation**: 
  - Lowercasing column names for consistency.
  - Filtering and selecting relevant columns.
  - Applying basic transformations and user-defined rules to the data.
- **Data Loading**: Transformed data is loaded into MySQL for further use.

## Project Steps
1. **Data Extraction**:
   - Use Mockaroo API to generate customer transaction data in JSON format.
   - Store the data as `transaction_data.json`.

2. **Data Transformation**:
   - Clean data: 
     - Lowercase column names.
     - Filter relevant columns: `url`, `name`, `offers/0/price`, `sku`.
   - Apply user-defined rules (e.g., filter out transactions with null values).
   
3. **Data Loading**:
   - Load the cleaned data into a MySQL database using `pandas` and `SQLAlchemy`.
