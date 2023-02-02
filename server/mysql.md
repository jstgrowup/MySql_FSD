## 1
- My sql is a Database management system 
- It is basically a software which is used to manage the database
- No one can directly put data into database it has to be processed through a software called DBMS(Database Management system)
- the data will first go to DBMS and than the DBMS will process it and than it will store the data into the database
- DBMS is just like a middleware it will be there in both post and get methods 
- DBMS examples
   - Oracle
   - MySQL
   - PostgreSQL
   - MongoDB
- `two types of Databases`
   1. Relational Databases: 
    - The data are stored in the form of tables this is the reason it is also known as RDBMS
    - These DBMS uses SQL(structured Query Language) to communicate with the databases
    - If the database is Relational datbase than we will need RDBMS
    - When we are using RDBMS we have to know SQL
    - Examples
       - Oracle
       - MySQL
       - PostgreSQL
   2. NoSQL:
    - NoSQL is not a Table-based Database
    - NoSQL databases are document based
    - Examples
       - MongoDB
       - Redis
       - Cassandra
- Advantages if MySQL
  - It is a cross platform which means can be used in any OS
  - It can be used with multiple languages (PHP,NodeJS,Python,C#)
  - MySQL is a open source software
  - MySQL is a RDBMS
  - The MySQL Database Server is fast ,reliable,scalable and easy to use.
  - MySQL Server works in client/server or embedded systems
## 2
`creating a database`
```
create database <databaseName>
```
## 3
`data types in sql`
- String
- Numeric
- Date and Time
# String datatypes
![image](https://user-images.githubusercontent.com/40628582/216316113-56e3db63-c94a-45f4-8bfd-3f2e206667d3.png)
# Numeric datatypes
![Image](https://user-images.githubusercontent.com/40628582/216316852-fb33705a-a4c8-4e90-a9a6-7b04cff5d21e.png)
# Date and Time
![image](https://user-images.githubusercontent.com/40628582/216317026-bf1745f3-b0f2-4560-8706-888367672d66.png)

# Commands
```
CREATE TABLE personal(
id INT,
name VARCHAR(40),
birth_date DATE,
phone VARCHAR(12),
gender VARCHAR(1)
)
```
```
CREATE TABLE product (
pid INT,
pname VARCHAR(50),
pcompany VARCHAR(50),
price INT
);
```
- INSERTING DATA
```
INSERT INTO personal(id,name,birth_date,phone,gender)
VALUES (1,"subham","1999-10-06","9435355529","M")
```
- INSERTING MULTIPLE DATAS
```
INSERT INTO personal(id,name,birth_date,phone,gender)
VALUES 
(3,"subham","1999-10-06","9435355529","M"),
(4,"dey","1999-04-09","7086580239","F"),
(5,"deyfsd","1234-04-09","7023423423","F");
```
# Constraints in MySQL
1. NOT Null - Means the field cant be null
2. Unique - In phone number we can use this by this we are telling that it will be unique it can never by duplicate
3. Default - A default value will be set if there is no value 
4. Check - Lets say we want to check the age lets say we dont the data who is below age 18
5. Foreign Key 
6. Primary Key
These are basically restrictions 
```
CREATE table personal(
id INT NOT NULL UNIQUE,
name VARCHAR(50) NOT NULL,
age INT NOT NULL CHECK(age>=18),
gender VARCHAR(1) NOT NULL,
phone VARCHAR(10) NOT NULL UNIQUE ,
city VARCHAR(15) NOT NULL DEFAULT "Guwahati"
);
```
example 
```
INSERT INTO personal(id,name,age,gender,phone,city)
VALUES (
1,"subham",23,"M","9435355529","nagaon"
)
```
