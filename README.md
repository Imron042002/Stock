# Overview
This project is a comprehensive stock data analysis tool that leverages Python and various libraries to fetch, store, and visualize stock market data. The primary goal is to provide insights into stock performance through fundamental metrics and visual representations. The project is designed to be user-friendly and efficient, allowing users to analyze multiple stocks simultaneously.
# Features
Data Retrieval: Fetch stock data from Yahoo Finance using the yfinance library.
Database Storage: Store stock information in a PostgreSQL database for persistent storage and easy retrieval.
Fundamental Analysis: Retrieve and display key fundamental metrics such as:
Price-to-Earnings (P/E) Ratio
Earnings Per Share (EPS)
Market Capitalization
Dividend Yield
Data Visualization: Visualize stock metrics using bar charts to facilitate comparison and analysis.
Batch Processing: Load and process multiple stock symbols from a CSV file.
Error Handling: Robust error handling to manage issues during data retrieval and database operations.
# Requirements
To run this project, you will need:
Python 3.x: Ensure you have Python installed on your machine.
Libraries: The following Python libraries are required:
yfinance: For fetching stock data.
pandas: For data manipulation and analysis.
matplotlib: For data visualization.
psycopg2: For PostgreSQL database interaction.
sqlalchemy: For database management.
# Installation of Required Libraries
You can install the required libraries using pip:
![Screenshot 2025-03-12 140007](https://github.com/user-attachments/assets/b86ee42b-1541-4474-8d66-24dcf73f1128)
# Installation Steps
1.Clone the Repository:

2.Set Up PostgreSQL Database:

Install PostgreSQL on your machine if you haven't already.
Create a new database (e.g., stockdata).
Create the necessary tables in your PostgreSQL database. Below are the SQL commands to create the required tables:
 # SQL Commands to Create Tables
 CREATE TABLE company_info (
    symbol VARCHAR(10) PRIMARY KEY,
    company_name VARCHAR(255),
    sector VARCHAR(100),
    industry VARCHAR(100),
    address1 VARCHAR(255),
    address2 VARCHAR(255),
    city VARCHAR(100),
    zip VARCHAR(10),
    country VARCHAR(100),
    phone VARCHAR(50),
    fax VARCHAR(50),
    website VARCHAR(255),
    long_business_summary TEXT,
    market_cap BIGINT,
    total_revenue BIGINT,
    net_income BIGINT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE stock_fundamentals (
    id SERIAL PRIMARY KEY,
    symbol VARCHAR(10),
    metric VARCHAR(50),
    value VARCHAR(50),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (symbol) REFERENCES company_info(symbol)
);

CREATE TABLE company_officers (
    id SERIAL PRIMARY KEY,
    symbol VARCHAR(10),
    name VARCHAR(100),
    age INT,
    title VARCHAR(100),
    fiscal_year INT,
    total_pay BIGINT,
    exercised_value BIGINT,
    unexercised_value BIGINT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (symbol) REFERENCES company_info(symbol)
);
