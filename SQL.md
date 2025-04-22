
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
   - DATE 
      1. DD - MM - YYYY ---> 12-Apr-2025
      2. DD - MM - YY   ----> 18-Apr-25
      3. DATE are used to store dates in the above formats
   - Large Object : it is used to store the huge amount of info.
   - syntax LOB(Size) ----> capacity --> 4GB ---> 1GB ---> 64000 character
      1. CLOB - Character Large Object : it is similar to varchar data type syntax ---> CLOB(Size)
      2. BLOB - Binary Large Object : it is used to store the meta-data upto 4GB syntax -- BLOB(Size); 
   - NUMBER
      - it is used to store any type of numeric value.
      - syntax : NUMBER(Precision , [Scale]-->Optional)
        - precision -> it is used to determine the number of digits which are required
          to store any Integer value.The range for the precision is 1 to 38.There is no default
          value for precision. It is used to determine the number of digits which are required to store any decimal value within the decimal.
        - The range of the scale is (-84 to 127)
        - The default value of scale is 0.
   - constraints 
        - constraints are the rule that area used to rules and restriction of each column
        - 1. UNIQUE
          2. NULL AND NOT NULL
          3. CHECK
          4. PRIMARY KEY FOREIGN KEY
      -  UNIQUE: It is used to avoid the repeated or duplicated value from the columns.
      - syntax: UNIQUE
      - NOT NUll : it is used to make the column is mandatory.
      - CHECK CONSTRAINTS: It is used to assign the extra validation to the column by using the conditions.
      - syntax : CHECK(Conditions)
      - PRIMARY KEY : primary key is used to identify the unique records from the table.
        1. properties of primary key .....
        2. It is the combination of unique and the not null.
        3. The primary key will not allow any repeated values and a duplicated values.
        4. In a same table we need to have only one primary key.
     - FOREiGN KEY : IT IS USE TO ESTABLISH A CONN BETWEEN THE MULTIPLE TABLE
        5. It is not a combination of unique and not null
        6. It will allow the empty cells and the repeated value
        7. In a same table we can have up-to 255 foreign key
        8. To become the foreign key it should be the primary key of another table.
        9. The foreign key will be present in child table , but it actually belongs to parent table.
        10. Foreign key also known as referential integrity constraints.
   

## statement in sql
- writing a query is known as statement
- mainly there are five statement in sql
- DDL , DML , DCL , TCL , DQL ----> crud operation.
- DQL 
- it is used to fetch the data from table or database.
- there are the four subcommands in a dql
- 1. projection process of fetching the data from the table the selecting only the columns
  3. Selection - The process of fetching the data from the table by selecting both rows and columns
  4. joins - The process of fetching the data from multiple table simultaneously is known as joins.
  5. select - select is a keyword which is used to display the data which has selected by projection selection and joins.
  6. 
           