# Postgresql-documentation

1. SELECT current_user;

2. SELECT current_database();

3.SELECT current_schema(); //public


CREATE TABLE maindatabase (
    connection_id SERIAL PRIMARY KEY,
    host VARCHAR(255) NOT NULL,
    database_name VARCHAR(255) NOT NULL,
    schema_name VARCHAR(255) NOT NULL
);

INSERT INTO maindatabase (host, database_name, schema_name)
VALUES
    ('host1.example.com', 'database1', 'schema1'),
    ('host2.example.com', 'database2', 'schema2'),
    
    ('host3.example.com', 'database3', 'schema3');
	
	Select * from maindatabase;



-------------------
Certainly! Here is the formatted README with the provided code embedded:

markdown
Copy code
# PostgreSQL Documentation

This repository contains simple SQL commands and a table creation script for managing PostgreSQL database connection information.

## Table of Contents

1. [Retrieve Current User](#1-retrieve-current-user)
2. [Retrieve Current Database](#2-retrieve-current-database)
3. [Retrieve Current Schema](#3-retrieve-current-schema)
4. [Create Connection Info Table](#4-create-connection-info-table)
5. [Populate Connection Info Table](#5-populate-connection-info-table)
6. [Query Data from Connection Info Table](#6-query-data-from-connection-info-table)

## 1. Retrieve Current User

```sql
SELECT current_user;
This SQL command retrieves the current PostgreSQL user.

2. Retrieve Current Database
sql
Copy code
SELECT current_database();
This SQL command retrieves the name of the current PostgreSQL database.

3. Retrieve Current Schema
sql
Copy code
SELECT current_schema(); --public
This SQL command retrieves the name of the current PostgreSQL schema. The default is set to "public."

4. Create Connection Info Table
sql
Copy code
CREATE TABLE maindatabase (
    connection_id SERIAL PRIMARY KEY,
    host VARCHAR(255) NOT NULL,
    database_name VARCHAR(255) NOT NULL,
    schema_name VARCHAR(255) NOT NULL
);
This SQL script creates a table named maindatabase to store connection information, including host, database_name, and schema_name.

5. Populate Connection Info Table
sql
Copy code
INSERT INTO maindatabase (host, database_name, schema_name)
VALUES
    ('host1.example.com', 'database1', 'schema1'),
    ('host2.example.com', 'database2', 'schema2'),
    ('host3.example.com', 'database3', 'schema3');
This SQL script populates the maindatabase table with sample connection information.

6. Query Data from Connection Info Table
sql
Copy code
SELECT * FROM maindatabase;
This SQL command retrieves all records from the maindatabase table, displaying connection information.
