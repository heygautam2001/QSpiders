
## SQL : Structured Query Language

- userOne  ----->  EstablishCommunication(Language)  ------>  userTwo

- SQL is language which is used to communication with the software known as Relational 
  Database Management System.(RDBMS)

- SQL   --->   Communication(PL)   ---->  RDBMS (Software)

## Relational Database Management System

1. Database : Database is aplace in  which we can sture the information in systematic manner.


    ===============
    ||           ||
    ||  info     ||   ------> Database
    ||           ||
    ||___________||

2. Basic operations in database
  - Create
  - Read/Retrieve
  - Update/Modify
  - Delete/Drop

3. DBMS is software which is used to manage  and maintain the database
 - Data is stored in two ways
 - 1. Table : structured
 - 2. file : Non-structured   

4. DBMS is a software which is used to maintain and manage the database
   1. The DBMS stores data int the either table format or file format 
   2. Table -> Structured
   3. File -> Non-Structured
- since the DBMS is a software to interact with this we have to pass the comment -> communication : that should ber in the form 
- of either sql or n0-sql
- Basically there are 5 types of DBMS
  1. NDBMS - Network Database Management System.
  2. OODBMS - Object oriented Database Management System.
  3. HDBMS - Hierarchy Database Management System.
  4. NRDBMS - Non-relational Database Management System.
  5. RDBMS - Relational Database Management System.
-  To interact with RDBMS we have to use command line tool like sql

## History of sql
  - 1979 Invented --> sequel
  - Invented by IBM
  - In 1981 oracle corporation's one person renames it as SQl(EF CODD ) 
  - The father of sequel F. Boycee , D . chamberlin


    _________________________
    |     |         |       |
    |     |         |       |
    |     |         |       |  -----> Table
    |     |         |       |
    |     |         |       |
    |_____|_________|_______|


## $ Data Types and constraints
   - it is used to determine which type of data is going to store into the particular memory location.
   - In sql there are 5 types of data types
     1. CHAR
     2. VARCHAR
     3. VARCHAR2
     4. DATE
     5. NUMBER
     6. LARGE OBJECT 
        1. CLOB - character large object
        2. BLOB - Binary large object
   - CHAR : 
       1. It will allow
          1. uppercase : A - Z
          2. lowercase : a-z
          3. Alpha-numeric
          4. special characters
          5. No character
          6. Numeric value 0 - 9 
          7. CHAR(size) ---> CHAR(25) ----> maxCapacity = 2000 character
          8. char ----> fixed size memory allocation.
          9. varchar ----> variable / Dynamic length memory allocation.
   - VARCHAR:
          1. Same data type as char
          2. It will follow the variable length of memory allocation
   - VARCHAR2
          1. VARCHAR2(SIZE)
          2. capacity (4000) character
