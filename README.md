The ETL process consists of *extracting* data from datasets, *transforming* the data, and then *loading* the transformed data into a database. This project builds an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform the data. After the data is transformed, four CSV files are generated and used to create an ERD and a table schema. The CSV file data is then uploaded into a Postgres database.

This project is divided into the following subsections:

**1. Create the Category and Subcategory DataFrames**
- Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame 
- Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame
- Export DataFrames to csv files 

**2. Create the Campaign DataFrame**
- Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame
- Export DataFrame to csv file

**3. Create the Contacts DataFrame**

Both of the following two options were used for extracting and transforming the data:

- Option 1: Python dictionary methods
  - Iterated through the DataFrame, converting each row to a dictionary
  - Iterated through each dictionary
      - Extracted the dictionary values from the keys using a Python list comprehension
      - Added values for each row to a new list
  - Created a new DataFrame with extracted data

- Option 2: Regular expressions
  - Extracted columns using regular expressions
  - Created new DataFrame with extracted data
   
**4. Create the Crowdfunding Database**
- The four CSV files were inspected and an ERD of the tables was created
- The information from the ERD was used to create a table schema for each CSV file
- A Postgres database was created
- The tables were created in the database using the schema
- Each CSV file was imported into its corresponding SQL table






