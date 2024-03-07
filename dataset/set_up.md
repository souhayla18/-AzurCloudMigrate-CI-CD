# AdventureWorks Database Setup Instructions

Follow these steps to set up the AdventureWorks database in your PostgreSQL instance:

## Step 1: Download Adventure Works 2014 OLTP Script

Download the Adventure Works 2014 OLTP Script from the following link:

[Adventure Works 2014 OLTP Script](https://github.com/AdventureWorks/AdventureWorks-for-SQL-Server/releases/download/oltp2014/AdventureWorks-oltp-install-script.zip)

Extract the contents of the .zip file.

## Step 2: Prepare CSV Files

Copy all CSV files from the extracted folder to the same directory where this setup script is located. Ensure that the directory also contains the `update_csvs.rb` file and `install.sql`(Please search for these files within the dataset repository ) .
## Step 3: Create Database and Import Data
Run the following commands to create the database, tables, import data, and set up views and keys:
```bash 
psql -c "CREATE DATABASE \"Adventureworks\";"
psql -d Adventureworks < install.sql
```
## Step 4: Verify Setup
Open psql, connect to the Adventureworks database, and display a list of tables:
```bash 
psql
\c "Adventureworks"
\dt (humanresources|person|production|purchasing|sales).*
```


