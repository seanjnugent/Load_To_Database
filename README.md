# Data Import Utility
# Purpose
Automate importing CSV, XLS, and XLSX files into SQL Server or PostgreSQL databases with robust error handling and naming sanitization.

# Features

- Multiple file format support (CSV, XLSX, XLS)
- Automatic table and column name sanitization
- Multi-sheet Excel file processing
- Secure database connection via environment variables
- Error-tolerant file handling

# Prerequisites

Python 3.8+

Required libraries:
- pandas
- pyodbc/psycopg2
- python-dotenv
- SQL Server or PostgreSQL database

# Setup

Install dependencies:

````
pip install pandas pyodbc python-dotenv
````
Create .env file:
```
ss_server=your_server
ss_database=your_database
ss_username=your_username
ss_password=your_password
```

# Usage

- Place input files in specified folder
- Configure database connection
- Run script

# Key Functions

sanitize_name(): Cleans table/column names
create_table_from_df(): Generates database tables
load_df_to_sql(): Imports dataframe data

# Limitations

Data imported as NVARCHAR(MAX)
128-character limit on identifiers
UTF-8/ISO-8859-1 encoding assumed

# Customization
Modify sanitize_name() to adjust naming rules as needed.
