sqlite3 getting_started.db  #create basic database named getting_started and give me a command prompt to start working within that database
.tables
.indices
.schema

CREATE TABLE cities (name text, state text); # Create a table named cities with name and state as the columns

INSERT INTO cities (name, state) VALUES  #add rows into table named cities with name and state columns...values begins the list
    ('New York City', 'NY'),
    ('Boston', 'MA'),

INSERT INTO weather (city, year, warm_month, cold_month, average_high) VALUES
    ('Boston','2013','July','January','62');


  city            year    warm month  cold month  average high
  New York City   2013    July        January     62
  Boston          2013    July        January     59
  Chicago         2013    July        January     59
  Miami           2013    August      January     84
  Dallas          2013    July        January     77
  Seattle         2013    July        January     61
  Portland        2013    July        December    63
  San Francisco   2013    September   December    64
  Los Angeles     2013    September   December    75
  
  SELECT * FROM cities;
  SELECT name, state FROM cities;
  SELECT name, state FROM cities WHERE state='CA';
  SELECT name FROM cities WHERE name LIKE '%le%';
  SELECT name FROM cities LIMIT 2 OFFSET 3;
  SELECT COUNT(*) FROM cities WHERE name LIKE 'San%' AND state='CA';
  in addition to count there is also
    SUM() finds the sum of the results
    AVG() finds the average of the results
    MIN() finds the lowest result
    MAX() finds the highest result
  UPDATE cities SET state='Californ-I-A' WHERE state='CA';
  DELETE FROM cities where state='CA';  

Export data to CSV  
> .mode csv
> .headers on
> .output cities.csv
> select * from cities;
> .output stdout

Import from CSV  
> create table cities_copy (name text, state text);
> .separator ","
> .import cities.csv cities_copy
  