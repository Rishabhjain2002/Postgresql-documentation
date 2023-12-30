# Postgresql-documentation

1. SELECT current_user;

2. 
SELECT current_database();

3.
SELECT current_schema(); //public


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
