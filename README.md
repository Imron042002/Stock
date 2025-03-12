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
![Screenshot 2025-03-12 140351](https://github.com/user-attachments/assets/b6dd9f4f-df80-4167-b3af-51b5ca3e8d18)
# company_info
![Screenshot 2025-03-12 140511](https://github.com/user-attachments/assets/468ea2b3-134c-4170-87a0-f543058dfbd0)
# stock_fundamentals 
![Screenshot 2025-03-12 140537](https://github.com/user-attachments/assets/31718aca-9a97-4c34-a2d0-5cb65ae3dfef)
# company_officers
![Screenshot 2025-03-12 140549](https://github.com/user-attachments/assets/132b8311-7694-45de-9e83-e39363d9d71f)

### Usage
# Fetch Stock Data:
The script reads stock symbols from a CSV file named thai_stocks_updated.csv. Ensure this file is present in the project directory.
Each symbol is processed to fetch its corresponding stock data from Yahoo Finance.

# Store Data:
The fetched data is stored in the PostgreSQL database, including company information, fundamental metrics, and executive details.

# Visualize Data:
The project includes functionality to visualize stock metrics using bar charts. This helps in comparing different stocks based on their fundamental metrics.

### Example Code Snippet for Fetching and Storing Data
![Screenshot 2025-03-12 141251](https://github.com/user-attachments/assets/e9d4f25a-68c2-4a93-aa87-d6bd3be45db2)
![Screenshot 2025-03-12 141305](https://github.com/user-attachments/assets/46af57b2-3fa8-4d8c-87bb-d7b59d85c76a)
![Screenshot 2025-03-12 141325](https://github.com/user-attachments/assets/19c72d44-849e-4a13-8c8e-2a4573639949)
![Screenshot 2025-03-12 141339](https://github.com/user-attachments/assets/127c54f9-f41f-4c3d-954e-9a908657771c)
![Screenshot 2025-03-12 141355](https://github.com/user-attachments/assets/64b75fac-3234-4595-a3ef-999759de91c6)
# Visualization
The project includes visualizations for comparing key metrics of different stocks. An example of a bar chart comparing PE Ratio, EPS, and Market Cap is provided in the code.

### Example Visualization Code
![Screenshot 2025-03-12 141545](https://github.com/user-attachments/assets/484bc0e3-a9ce-486b-b1ef-34e9cdc4a23f)
![Screenshot 2025-03-12 141800](https://github.com/user-attachments/assets/8aeb8a38-d9a1-42f6-8d0b-a1de0824ebb2)

# Future Enhancements
Implement additional visualizations such as line charts for historical stock prices.
Add functionality to analyze stock trends over time.
Integrate machine learning models for stock price prediction.
Create a user interface for easier interaction with the tool.

