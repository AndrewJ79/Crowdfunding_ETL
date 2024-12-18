# Crowdfunding Database Project

Overview

This project focuses on extracting, transforming, and loading (ETL) crowdfunding data from Excel files into a PostgreSQL database. The project includes data preparation, creation of structured tables, and establishing relationships between them.

## Steps Completed


1. Category and Subcategory DataFrames
   
* Extracted and transformed data from crowdfunding.xlsx.

* Created two DataFrames:
   
    * Category DataFrame:
        
        * category_id: Sequential IDs (cat1, cat2, ...).
        
        * category: Unique category titles.
   
    * Subcategory DataFrame:
       
        * subcategory_id: Sequential IDs (subcat1, subcat2, ...).
        
        * subcategory: Unique subcategory titles.

* Exported these DataFrames as category.csv and subcategory.csv.


2. Campaign DataFrame

* Extracted and transformed relevant data from crowdfunding.xlsx into the following columns:

  * cf_id, contact_id, company_name, description

  * goal (float), pledged (float), outcome, backers_count, country, currency

  * launch_date and end_date (UTC to datetime format).

  * category_id and subcategory_id (linked to Category and Subcategory DataFrames).

* Exported the Campaign DataFrame as campaign.csv.


3. Contacts DataFrame
   
* Option 1: Python Dictionary Methods

  * Extracted contact_id, name, and email from contacts.xlsx.

    * Split "name" column into first_name and last_name.

    * Created and cleaned a new Contacts DataFrame.


4. Database Creation
   
* Designed an Entity Relationship Diagram (ERD) to define relationships between tables.

* Created a PostgreSQL database schema:
    
    * Tables: category, subcategory, campaign, and contacts.
   
    * Defined primary keys, foreign keys, and constraints.

* Imported CSV data into corresponding SQL tables.

* Verified table creation and data integrity with SELECT statements.

--
Tools & Technologies

* Data Processing: Python, Pandas, NumPy

* Database: PostgreSQL

* ERD Design: QuickDBD

* File Formats: Excel (crowdfunding.xlsx, contacts.xlsx), CSV

--
Deliverables

* category.csv

* subcategory.csv

* campaign.csv

* contacts.csv

* crowdfunding_db_schema.sql


### Instructions

1. Run the Python script to generate and clean the required DataFrames.

2. Use the crowdfunding_db_schema.sql to set up the PostgreSQL database.

3. Import the CSV files into the database and verify data integrity.
