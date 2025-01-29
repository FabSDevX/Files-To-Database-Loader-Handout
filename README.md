# File To Database Loader Handout
The objective of this project is to develop solutions based on the design provided. In this case, the source data was obtained in the form of files from a MySQL DB.

We require the data to be loaded into PostgreSQL, which is a common scenario in companies who want to change underlying database technologies, in which case the data from one DB needs to be migrated into another DB. The Project scope is to migrate file-based data to PostgreSQL tables

### Data Model Details
![image](https://github.com/user-attachments/assets/5c96e890-5940-45cd-a827-d377aa6f7bd3)

### Design
![image](https://github.com/user-attachments/assets/a1aaa86d-ac49-40bc-bd98-1f5fdf591cb7)

### Setup Instructions
The previous project can be used as a reference for the following steps. Watch the relevant videos to take care of the setup.

1. Setup the Project Using VSCode
2. Make sure you have set up a virtual environment (creating venv, requirements.txt, etc.,) and installed dependencies for the project.
3. It is essential that you deploy the application with the core logic.
4. Be sure to drop the tables and recreate them using the scripts OR simply truncate the tables with the truncate command before running the scripts
5. Run the project after setting all the environment variables.

### Validation Steps

* You should check whether the data in the tables have been populated by running queries.
* In postgres tables, we need to confirm that the schema structure (column name, data type, etc.) was accurately reflected from the CSV file. (Hint: Refer to schemas.json).
* Take the count of records in the CSV files and compare it to the number of records in the PostgreSQL tables. The count should match the numbers below.
``` SQL
select count(*) from orders; --68883
select count(*) from order_items; --172198
select count(*) from categories; --58
select count(*) from customers; --12435
select count(*) from departments; --6
select count(*) from products; --1345
```

### Technologies Used
* Programming Language – Python
* Pandas – For Converting CSV to Dataframe and then load the Dataframe into Postgres Database

