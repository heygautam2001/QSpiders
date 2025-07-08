
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
   1. The DBMS stores data in the form of either table format or file format 
   2. Table -> Structured
   3. File -> Non-Structured
- since the DBMS is a software to interact with this we have to pass the comment -> communication : that should be in the form 
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
  - In 1981 oracle corporation's one person renames it as SQL(EF CODD ) 
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
      1. DD - MYN - YYYY ---> 12-Apr-2025
      2. DD - MYN - YY   ----> 18-Apr-25
      3. DATE are used to store dates in the above formats
   - Large Object : it is used to store the huge amount of info.
   - syntax LOB(Size) ----> Max-capacity --> 4GB ---> 1GB ---> 64000 character
      1. CLOB - Character Large Object : it is similar to varchar data type syntax ---> CLOB(Size)
      2. BLOB - Binary Large Object : it is used to store the meta-data upto 4GB syntax -- BLOB(Size); 
   - NUMBER
      - it is used to store any type of numeric value.
      - syntax : NUMBER(Precision , [Scale]-->Optional)
        - precision -> it is used to determine the number of digits which are required
          to store any Integer value.The range for the precision is 1 to 38.There is no default
          value for precision. 
        - Scale : It is used to determine the number of digits which are required to store any decimal value within the decimal.
        - The range of the scale is (-84 to 127)
        - The default value of scale is 0.
        - Number(5,-2)---> 99999.00
        - Number(4,-3) ----> 9999.000
   - constraints 
        - constraints are the rule that area used to rules and restriction of each column
        - 1. UNIQUE
          2. NULL AND NOT NULL
          3. CHECK
          4. PRIMARY KEY
          5. FOREIGN KEY
          6. AutoIncrement and default .
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
     - FOREIGN KEY : IT IS USE TO ESTABLISH A CONN BETWEEN THE MULTIPLE TABLE.
        5. It is not a combination of unique and not null
        6. It will allow the empty cells and the repeated value
        7. In a same table we can have up-to 255 foreign key
        8. To become the foreign key it should be the primary key of another table.
        9. The foreign key will be present in child table , but it actually belongs to parent table.
        10. Foreign key also known as referential integrity constraints.
   
# # How to use sql+ software
1. print/show/list Database : select * from all_users
2. CURRENT DATABASE : SHOW USER
3. SHOW TABLES IN DATABASE :SELECT * FROM TAB;
4.  SHOW SPECIFIC TABLE DATA :SELECT * FROM  EMP;
5. SET LINES 1000 PAGES 1000;
6. CLEAR THE SCREEN : CL SCR
7. EDIT QUERY : ED 
8. -- : SINGLE LINE COMMENT
9. /*   */: MULTI LINE COMMENT
10. DISC : DISCONNECT FROM THE USERS
11. CONNECT : CONNECT TO ANOTHER USER
12. EXIT : TO CLOSE THE SOFTWARE
13. DESC : PRINT THE STRUCTURE OF THE TABLE

DELETE --> DATA / RECORDS
DROP ----> RELATED TO TABLE

UPDATE --> RELATED TO RECORDS/DATA
MODIFY ---> RELATED TO TABLE...


## # statement in sql
- THE STATEMENT WHICH ARE USED TO PERFORM THE COMPLETE CRUD OPERATION 
- writing a query is  known as statement
- mainly there are five statement in sql
- DDL , DML , DCL , TCL , DQL ----> crud operation.
- DQL 
- it is used to fetch the data from table or database.
- there are the four subcommands in a dql
- 1. projection process of fetching the data from the table the selecting only the columns
  3. Selection - The process of fetching the data from the table by selecting both rows and columns
  4. joins - The process of fetching the data from multiple table simultaneously is known as joins.
  5. select - select is a keyword which is used to display the data which has selected by projection selection and joins.

# projection 
- The process of fetching data from table by selecting only with columns.
- syntax : 

         keywords                      input
         
         select             * /[Distinct] column-name /
         from                    Expression{Alias}
         keyword is known as      Table name:
         clauses

- Write a query to display that are present in table Employee.
- Write a query to display that are present in table Employee who are working on dept = 20;
- WAQTD the salaries of all the employees from employee table.
- WAQTD Employee name and the job 0f all employee.
- WAQTD emp_name salary , dept no , and the job of all employee table.
- WAQTD all the details from emp.
- WAQTD The jobs from the employee table , but there should not be any repeated record.
- WAQTD the job and dept-no and the salary of all the employee but there should not be any repeated one.
- The statement which consists of operand and operator


  # Expression : 
   - Any statement which gives the result is known as expression.
   - statement is a collection/combination of operand or operator.
   - Examples : 2 + 5 = 7;  M * A = F ; H2 + SO4 = H2SO4; 
   - Sql Expression
   - Salary + commission =  Result.
   - Note : In order the sql expression instead of using the values as a operand , we need to use
     column as a operand.
   - Example : salary * 12 


 # SELECTION : IT IS USED TO FETCH THE DATA FROM THE TABLE BY SELECTING BOTH COLUMNS AND ROWS (ROWS AND ATTRIBUTE)
 - SYNTAX : SELECT * / [DISTINCT] COL_NAME/ EXPRESSION [ALIAS] FROM TABLE_NAME 
   WHERE FILTER_CONDITIONS;
 - WHERE : IT IS USED TO FILTER THE RECORDS BASED ON THE CONDITIONS.
 - THE WHERE CLAUSE WILL EXECUTE ROW BY ROW
 - THE WHERE CLAUSE WILL CHECK THE CONDITIONS IF THE CONDITION IS TRUE IT WILL SELECT THE RECORD AND IF THE CONDITION IS FALSE
    IT WILL REJECT THE RECORD.
 - THE OUTPUT OF THE WHERE CLAUSE IS IN THE FORM OF BOOLEAN VALUES
 - IN WHERE CLAUSE WE CAN ALSO USE THE MULTIPLE CONDITIONS WITH THE HELP OF LOGICAL OPERATORS
 - THE FORMAT OF CONDITION IS : COL_NAME / EXPRESSION OPERATOR VALUES.
 - WRITE A QUERY TO DISPLAY ALL THE EMPLOYEES NAME , THE EMPLOYEES WHO ARE WORKING IN DEPT_NO 20.-----> SELECTION
 - WRITE A QUERY TO DISPLAY ALL THE EMPLOYEE NAME.----> PROJECTION
 - WRITE A QUERY TO DISPLAY ALL THE DETAILS OF THE EMPLOYEES WHOSE SALARIES ARE MORE THAN 2000;
 - SELECT * FROM EMP WHERE SAL > 2000;
 - WRITE A QUERY TO DISPLAY ALL THE DETAILS OF THE EMPLOYEES WHERE JOB IS MANAGER.
 - SELECT * FROM EMP WHERE JOB = 'MANAGER';
 - NOTE : IN WHERE CLAUSE IF WE ARE USING ANY NUMERIC VALUE WE CAN USE DIRECTLY.
 - NOTE : IN CASE WE ARE USING ANY STRING DATA OR DATA DATA THEN WE HAVE MENTION THE DATA AND STRING WITHIN
 - SINGLE QUOTES AND THESE TO DATA ARE CASE SENSATIVE.
 - IF WE ARE USING DATE DATA WE NEED TO FOLLOW THE DATE FORMAT OF ORACLE 'DD-MON-YY' OR 'DD-MON-YYYY'
 - MYSQL WORKBENCH : 'YYYY-MM-DD' OR 'YY-MM-DD'
 - WAQTD OF THE EMPLOYEES , THE EMPLOYEE WHOSE NAME IS SMITH;
 - SELECT * FROM EMP WHERE ENAME = 'SMITH';
 - WAQTD ALL THE DETAILS OF EMPLOYEES THE EMPLOYEES WHO HIRED ON 23-MAY-87
 - SELECT * FROM EMP WHERE HIREDATE = '23-MAY-87';
 - WAQTD ALL THE DETAILS OF EMPLOYEES THE EMPLOYEES WHO HIRED AFTER 1985.
 - SELECT * FROM EMP WHERE HIREDATE >= '01-JAN-1986';
 - SELECT * FROM EMP WHERE HIREDATE > '31-DEC-1985';
 - WAQTD ALL THE DETAILS OF THE EMPLOYEE WHO ARE WORKING IN DEPTNO 10 AND 20;
 - SELECT * FROM EMP WHERE DEPTNO = 10 OR DEPTNO = 20;
 - WAQTD ALL THE DETAILS OF THE EMPLOYEES , THE EMPLOYEES WHOSE SALARY ARE 3000 AND 5000;
 - SELECT * FROM EMP WHERE SAL = 3000 OR SAL = 5000;
 - WAQTD ALL THE DETAILS OF THE EMPLOYEES , THE EMPLOYEES WHOSE SALARY MORE THAN 3000 AND LESS THAN 5000;
 - SELECT * FROM EMP WHERE SAL > 3000 AND SAL < 5000;
 - WAQTD ALL THE DETAILS OF THE EMPLOYEES , THE EMPLOYEES WHO ARE WORKING DEPTNO 10 AND 20 AS A MANAGER;
 - WAQTD ALL THE DETAILS OF THE EMPLOYEES , THE EMPLOYEES WHOSE SALARY ARE 3000 , 5000 , 1600 , 1500 IN DEPTNO 20 
 - WORKING AS MANAGER AND CLERK;
 - SELECT * FROM EMP 
   WHERE DEPTNO = 20 AND (SAL = 3000 0R SAL = 1500 AND SAL = 1600) AND (JOB = 'MANAGER' OR JOB='CLERK');
 - DISAPLY ALL THE DETAILS OF EMPLOYEE INCLUDING THE ANNUAL SAL OF THE EMPLOYEE IF THEIR ANNUAL SAL IN MORE THAN 30000;
 - SELECT EMP.*  , SAL*12  "ASALARY" FROM EMP WHERE SAL*12 > 30000;
 - NOTE : THE ALIAS NAME WHICH WE ARE USING IN A SELECT CLAUSE IT IS NOT POSSIBLE TO ACCESS IN A WHERE CLAUSE.
 - WAQTD ALL THE DETAILS OF THE EMPLOYEE INCLUDING ANNUAL SAL , HALF TERM SAL AND QUATERV SAL AND 10 PERCENT INC IN ACTAL SAL 
 - 12 % DEC IN ANNUAL SAL 6% INC HALF TERM SAL  FOR ALL THE EMPLOYEES AXCEPT SALESMAN WHO ARE WORKING IN DEPT NO 1
 - 10 AND 20 HIRED AFTER 1980 USE THE ALIAS NAME FOR ALL THE EXPRESSION.


# LOGICAL OPERATOR
- THERE ARE THREE LOGICAL OPERATOR IN SQL;
- Logical AND , Logical OR , Logical NOT


## special operator in sql
   - These Operators are used to perform the special type of task in sql.
   - There are 4 set of special operators
   - IN and NOT IN
   - BETWEEN , NOT BETWEEN
   - IS , IS NOT
   - LIKE ,  NOT LIKE
   - Extra part : Regular expression
   - Note : These all the operators are not mandatory we can also solve the queries by using n no. of different
     ways.

   - IN VS NOT IN
     - These are special  which  operator which are help us to pass the multiple value at the RHS side to make the comparisons.
     - NOT || != || <> 
     - write a query to display all the details of the employees the employee were working in department no. 10 and 20.
     - select* from emp where deptNo = 10 0R dept = 20;
     - select * from emp where deptNo IN (10 , 20);
     - q . write a query to display all the details of employees , the employess whose salary are 1500 , 1600 , 3000 , and 5000;
     - select * from emp where sal IN(1600 , 1500 , 3000 , 5000);
     - ques : write a query to display all the details of the employee whose names are smith and kang.
     - select * from emp where ename = "SMITH" OR ename = "KANG";
     - select * from emp where ename IN ('SMITH' , 'KANE');
     - ques: all the details of the employees except all the employees working in deptno 10 and 30.
     - select * from emp where deptno NOT IN (10 , 30);
     - THESE OPERATOR WILL WORK WITH ONE COLUMN DATA 
     - EX : DEPTNO IN(10 , 20 , 30); VALID
     - EX : DEPTNO IN(10, 'SALES',40) ; INVALID
     - WRITE A QUERY TO DISPLAY ALL THE DETAILS OF EMPLOYEES , THE EMPLOYEES WHO WHO ARE WORKING SALESMAN , MANAGER , CLERK.
     - SELECT * FROM EMP WHERE JOB = 'SALESMAN' OR JOB = 'CLERK' OR JOB = 'MANAGER';
     - SELECT * FROM EMP WHERE JOB IN('SALESMAN' , 'CLERK' , 'MANAGER');
     - DISPLAY ALL THE DETAILS OF EMPLOYEES WHOSE SALARY ARE 3000, 5000 , 5000;
     - SELECT * FROM EMP WHERE SALARY IN(1500 , 1600 , 3000 , 5000);
     - DISPLAY ALL THE DETAILS OF EMPLOYEES , EXPECT ALL THE EMPLOYEES WHOSE SALARY ARE 1500 1600 3000 5000;
     - SELECT * FROM EMP WHERE SAL NOT IN(1500 , 1600 , 3000 , 5000);
     - DISPLAY ALL THE DETAILS OF EMPLOYEES , THE EMPLOYEES WHO  ARE W0RKING IN DEPARTMENT NO 10 AND 20 EXCEPT MANAGER AND CLERK 
        WHOSE SALARIES ARE LESS THAN 6000 ;
     - SELECT * FROM EMP WHERE SAL < 6000 AND (DEPTNO != 10 OR DEPTNO != 20) AND (JOB != 'MANAGER' OR JOB = 'CLERK');
     - SELECT * FROM EMP WHERE SAL < 6000 AND DEPTNO NOT IN (10 , 20) AND JOB NOT IN ('MANAGER' , ''CLERK');
   
   - BETWEEN VS NOT BETWEEN
     - These are the special operators which are help us to solve the range value queries.
     - syntax : 
     - WHERE COL_NAME /EXP BETWEEN / NOT BETWEEN LOWER_VALUE AND HIGHER_VALUE;
     - QUES : write a query to display all the details of the employees , the employee whose salary are between 1600 to 3000.
     - select * from emp where salary > 1600 AND salary < 3000; XXX WRONG ASKING BETWEEN NOT RANGE
     - select * from emp where salary between 1601 and 2999 ; ✅✅CORRECT
     - Ques : Display all the details of employees whose salary are in the range of 1600 and 3000;
     - select * from emp where salary between 1600 and 3000;
     - ques : Display all the details from , the employee who hired BETWEEN 1980 to 1987.
     - SELECT * FROM EMP WHERE HIREDATE BETWEEN '01-JAN-1981' AND '31-DEC-1986';
     - ques: Display all the details of the employees who hired in the range of 1980 and 1987.
     - SELECT * FROM EMP WHERE HIREDATE BETWEEN '01-JAN-1980' AND '31-DEC-1987';
     - Display all the details of employee , the employee who hired during the year of 1981 INTO DEPTNO 10 AND 20 EXCEPT MANAGER.
     - SELECT * FROM EMP WHERE HIREDATE BETWEEN  '01-JAN-1981' AND '31-DEC-1981' AND DEPT IN(10 , 20) AND DOB NOT IN('MANAGER'); 
     - Display all the details of employees , except  the employees whose salaries are in  between 1600 to 3000.
     - SELECT * FROM EMP WHERE SAL NOT BETWEEN 1601 AND 2999;
     - Display all the details Of the employees except all the employees , the  employees whose salary are in the range of 
       1600 to 3000;
     - SELECT * FROM EMP WHERE SAL BETWEEN 1600 AND 3000;
     
   - IS Vs IS NOT
     - These are the special operator which are used to compare null values. 
     - Ques : write a query to display all the details of employees the employees who are earning the commission
     - Ques : Display all the details of the employees , the employees who are not earning the commission.
     - the employees who are working in 10 and 20 and earning the salaries..
     - Write a query to  display all the details of employee the employees who are working in department no 30 and not earning any salaries.
     - The employee who are not having any reporting managers.
     - SELECT * FROM EMP WHERE MGR IS NULL;
     - 
     # regular expression /REGEXP
   - It is the advance version  of like operator which is used to perform the pattern matching Operation.
   - 1. ^ ---- STARTS
     2. $ ----- FROM ENDS
     3. [ ] --- FOR CHARACTERS ALSO WE CAN USE MULTIPLE  CHARACTERS.
     4. . ------FOR SINGLE CHARACTER.
     5. .* ---- IF WE WANT TO CONSIDER MULTIPLE CHARACTERS.
     6. -  ----- RANGE CHARACTER. 
     

      DISPLAY ALL THE DFETAILS OF THE EMPLOYEES WHOSE NAME STARTS WITH S CHARACTER..
      SELECT * FROM EMP WHERE ENAME LIKE S%;
      SELECT * FROM EMP WHERE REGEXP_LIKE(ENAME,'^S');
    
      DISPLAY STARTS WITH C AND ENDING WITH K;
      SELECT * FROM EMP HWERE ENAME LIKE C%K;
      SELECT * FROM EMP REGEXP_LIKE( ENAME , ^C .* K$);
     
      ALL DETAILS , THE EMLOYEES WHOISE NAME HAVING 3 CHARACTER AS A L ENDS WITH THE R.  
      SELECT * FROM EMP WHERE  REGEXP_LIKE(ENAME , ^..L.*R$)

     DISPLAY ALL THE DETAILS OF EMOPLOYEES THE EMPLOYEES WHOSE NAME DOES NOT STARTS WITH VOWELS.
     SELECT * FROM EMP WHERE NOT REGEXP_LIKE(ENAME ,  '^[A,E,I,O,U]');
     DIAPLAY ALL THE DETAILS OF THE EMPLOYEES WHOSE  STARTS WITH PERCENTILE.
     SELECT * FROM EMP WHRE REGEXP_LIKE(ENAME , '^%');
     
   - LIKE VS NOT LIKE 
     - It is used to perform the pattern matching operations.
     - THESE ARE USED TO SOLVE THE PATTERN RELATED QUERY.
     - Syntax:
     - WHERE COL_NAME/EXP LIKE/NOT LIKE 'PATTERN'
     - To create a pattern the two special characters we have to use '%' , "_";
     - % : the percentage will allow any type of characters , n number of characters.
     - _ : the underscore will allow any type of characters but only one digit of characters.
     - Ques : Display all tye details of the employees , the employees whose names end with r characters.
     - select * from emp where ename like '%R';
     - Ques : Display all the details of the employees , the employee whose name having 'a' character
     - select * from emp where ename like '%A%';
     - Ques : Display all the details of employee , the employees who hired in the dec.
     - SELECT * FROM EMP WHERE HIREDATE LIKE '%DEC%';
     - SELECT * FROM EMP WHERE HIREDATE LIKE '__-DEC-__';
     - Display all the details of employee , the employees whose name having last second character in the E.
     - SELECT * FROM EMP WHERE ENAME LIKE '%E_';
     - Display all the details of employees . the employees whose name starts with A character and starts with S character.
     - SELECT * FROM EMP WHERE ENAME LIKE 'A%' OR ENAME LIKE 'S%';
     - Display all the details of employees , except all the employees whose name not starts with A and B;
     - SELECT * FROM EMP WHERE ENAME NOT LIKE 'A%' AND ENAME NOT LIKE 'B%';
     - Display all the details of employees whose name starts with vowels;
     - SELECT * FROM EMPLOYEES WHERE ENAME LIKE 'A%' OR ENAME  LIKE '%E' OR ENAME LIKE 'I%' OR ENAME LIKE 'O%' ENAME LIKE '%U';
     - SELECT * FROM EMPLOYEES WHERE ENAME NOT  LIKE 'A%' AND ENAME NOT LIKE '%E' AND ENAME  NOT LIKE 'I%' AND ENAME NOT LIKE 'O%' AND ENAME LIKE '%U';
     - Display all the details of employees whose name not starts with vowels.
     - Display all the details of employees , 

     select emp.* sal*12 "Annual Salary" , sal*6 "Halfturn salary" from emp where dept IN(10 , 20);

  ##  Functions
      - The set of instructions which are help is to perform the specific task is known as
        functions.
      - 1. input
      - 2. working procedure for execution
      - 3. Output
      - In general there are two types of functions--> 1.user-defined 2.InBuilt


      - user-defined : A functions that are defined by users according to their requirements are known as 
        user defined functions. 
      - we can do modifications in user defined function.
      - only the person who create the functions can used it. 
        static
      - security will be more.
      



      - InBuilt : the functions which are peredefined in the software are known as builtIn functions ,      
        Inbuilt functions and pre-defined functions.
      - we cannot do modifications in user defined function.
      - Everyone can use builtIn functions . 
      - Dynamic 
      - security will be less.
      - Inbuilt Functions ---> 1.Single row function , 2.Multi row function.
      - These funtions are classified based on the output of the function


     single row functions
      The functons in which the number of inputs are equal to no of outputs are known as single row functions.
      The single row functions executes line  by line or row by row.
       1) length()
       2) upper()
       3.) substrings() ......ETC
       4.) Lower
       5.) INSTR
        No aggregation
     Multi row functions.
       The functions which gives only one output , on multiple input..
       It executes group by group.
       After the aggregation the execution takes place , hence these function also known as aggregate functions. 
       AVG()
       MAX()
       MIN()
       SUM()
       COUNT()
       aggregation will happen.
   ## Rules of multi row functions.
      1)syntax:
             MRF_NAME(COL_NAME/EXPRESSION/FUNCTION)
             MAX(SAL/SAL*12) , MIN(SAL/SAL*12) , .....
      2. ALL THE MRF WILL ALLOWS ONLY COLUMN/EXP/FUNCTION AS ARGUMENT
         --- WAQTD THE MAXIMUM SALARY FROM THE EMPLOYEE
          SELECT ,MAX(SAL) FROM EMP;
          --- WAQTD THE MAXIMUM SALARY AND MAXIMUM COMM FROM THE EMPLOYEE ?
          SELECT MAX(SAL , COMM) FROM EMP; ---> INVALID
          SELECT MAX(SAL) , MAX(COMM) FROM EMP ;

      3. IN SELECT CLAUSE WE CAN USE N NUMBERS OF MRF
         SELECT MAX(SAL) , MIN(SAL) , ANG(SAL) , SUM(SAL) , COUNT(SAL) , MAX(HIREDATE) , MIN(COMM)
         FROM EMP;

      4. IN WHERE CLAUSE : IT IS NOT POSSIBLE TO USE ANY MULTIROW FUNCTION.
         SELECT * FROM EMP WHERE SAL = MAX(SAL);
         NOTE : WHERE CLAUSE WILL EXECUTE ROW BY ROW WHEREAS MRF WILL EXECUTE GROUP BY GROUP.
         THE EXECUTION FUNCTION OF BOTH ARE DIFFERENT.




     5. IN SELECT CLAUSE ALONG WITH MULTIROW FUNCTION IT IS DIFFICULT TO USE ANY OTHER COLUMN.
        WE CAN USE IF WE ARE USING THE GROUP BY CLAUSE
        RESULT OF ANY COLUMNS WITH MRF IN SELECT CLAUSE IS NOT IN THE FORM OF TABLE.

     6. MULTIROW FUNCTION WILL IGNORES  NULL VALUE.

     7. AMONG ALL THE MULTIROW FUNCTIONS ONLY THE COUNT FUNCTION WILL ALLOW THE '*' AS A ARGUMENT.
        COUNT(*) GO WITH THE PRIMARY KEY COLUMN.

     8. YOU CAN ALSO USE ALIAS NAME ALONG WITH MRF .

      QUES: WRITE A QUERY TO DISPLAY THE TOTAL SALARY AND THE NUMBER OF EMPLOYEES WHO ARE 
      WORKING AS A MANAGER.
     
      QUES: WRITE A QUERY TO DISPLAY THE NUMBER OF EMPLOYEES WORKING IN DEPTNO 10 AND 30.
       
      QUES : DISPLAY THE NUMBER OF EMPLOYEE WHO ARE WORKING IN EACH DEPARTMENT FOR THE DEPARTMENTNO 10 AND 30
      WRITE A QUERY TO DISPLAY ALL THE DETAILS TOTAL SALARY NEEDED TO PAY FOR ALL THE EMPLOYEES WHO ARE WORKING IN DEPTNO 20
       
      QUES: DISPLAY THE NUMBER OF EMPLOYEES WORKING AS A MANAGER.
      SELECT COUNT(*) FROM EMP WHERE JOB = "MANAGER";

      QUES: DISPLAY THE MAXIMUM SALARIES , AVG SALARY AND THE TOTAL SALARIES , INCLUDING MAXIMUM ANNUAL AVG SALARIES WHO
      ARE WORKING AS SALESMAN.
       SELECT MAX(SAL) , AVG(SAL) , SUM(SAL) , AVG(SAL*12) , MAX(SAL*12) FROM EMP WHERE JOB = SALESMAN;
      
       WRITE A QUERY TO DISPLAY THE NUMBER OF SALARIES PRESENT IN EMPLOYEE TABLE.
       
       WRITE A QUERY TO DISPLAY NUMBER OF DISTINCT SALARY FROM EMP TABLE.
       SELECT COUNT(DISTINCT SAL)  FROM EMP;

       WRITE A QUERY TO DISPLAY THE NUMBER OF EMPLOYEES ARE WORKING IN DEPARTMENT NUMBER 13 AND 20;
       SELECT COUNT(*) "NO OF EMP" FROM EMP WHERE DEPTNO IN(20,30);
     
## group by clause.
    - IT IS USED TO CONVERT THE RECORD INTO GROUPS BASED ON THE COLUMNS
    - SYNTAX
      SELECT MRF / GROUP EXPRESSIONS FROM TABLE_NAME 
      [WHERE FILTER CONDITIONS] ---- OPTIONAL
      GROUP BY COL_NAME;
       Note: IF WE USE THE GROUP BY CLAUSE THEN IN SELECT ONLY WE HAVE USE MRF OR GROUPEXP (* AND ALL NOT POSSIBLE)
       FOR THAT WE HAVE TO USE THE SUB QUERY.
      1.THE FROM CLAUSE WILL EXECUTE FIRST..
      2.AFTER THE FORM CLAUSE IF WE ARE USING THE WHERE CLAUSE IT WILL EXECUTE SECOND ELSE THE GROUP BY CLAUSE EXECUTE SECOND
      3.THE GROUP BY CLAUSE WILL EXECUTE ROW BY ROW
      4.AFTER THE EXECUTION OF A GROPUP BY CLAUSE , ALL THE RECIORDS WILL BE CONVERTED AS A NO . OF GROUPS
      5.FINALLY THE SELECT CLAUSE IS EXECUTE IT WILL DISPLAYU THE FINAL RESULT.
      6.THE COL WHICH WE ARE USING IN THE GROUP BY CLAUSE THE SAME COL WE CAN ALSO USE IN THE SELECT CLAUSE THAT COL IS 
       KNOWN AS GROUP EXPERESSION.

      EXAMPLE: WRITE A QUERY TO DISPLAY THE NO OF EMPLOYEE WORKING IN EACH DEPARTMENT.
      SELECT COUNT(*) , DNO , FROM EMP 
      GROUP BY DNO; 
     
       SELECT COUNT(*) , DNO , FROM EMP 
       GROUP BY ROLLUP (DNO);

      QUES : WRITE A QUERY TO DISPLAY THE NUMBER OF EMPLOYEES WORKING IN EACH JOB.
             SELECT COUNT(*) , JOB FROM EMP
             GROUP BY JOB;

      QUES : WRITE A QUERY TO DISPLAY THE NUMBER OF EMPLOYEE WORKING AS A MANAGER IN EACH DEPARTMENT.
             SELECT COUNT(*) , DEPTNO FROM EMP
             WHERE JOB = 'MANAGER'
             GROUP BY DEPTNO;

      QUES : DISPLAY THE REPEATED SALARIES FROM EMPLOYEE SALARY;
             DISPLAY THE AVERAGE SALARIES NEEDED TO PAY FOR EACH DEPARTMENT THE EMPLOYEES WHO HIRED AFTER 1980;
             SELECT AVF(SAL) , DEPTNO 
              WHERE HAIREDATE > '31-DEC-1980';
              GROUP BY DEPTNO;
      QUSES : WRITE A QUERY TO DISPLAY THE NUMBER OF EMPLOYEES WHO ARE WORKING IN SAME DEPARTMENT;
                SELECT COUNT(*) ,DEPTNO FROM EMP
                GROUP BY DEPTNO;
      QUES:WRITE A QUERY TO DISPLAY THE NUMBER OF EMPLOYEE WHO ARE WORKONG IN SAME DEPARTMENT AND HAVE SAME JOB;
                  SELECT COUNT(*) ,DEPTNO , JOB FROM EMP
                  GROUP BY DEPTNO , JOB;
      QUES:WRITE A QUERY TO DISPLAY THE NUMBER OF EMPLOYEE WHO ARE WORKONG IN SAME DEPARTMENT, HAVE SAME JOB , HIREDATE IS SAME;
                   SELECT COUNT(*) , HIREDATE , DEPTNO , JOB
                   FROM EMP
                   GROUP BY DEPTNO , HIREDATE , JOB;

      QUES:WRITE A QUERY TO DISPLAY THE TOTAL  SALARY WHICH IS NEEDED TO PAY FOR EACH DEPARTMENT.
           SELECT SUM(SAL) FROM EMP 
           GROUP BY DEPTNO;
           
           SELECT SUM(SAL) , DEPTNO FROM EMP 
           GROUP BY DEPTNO;
      
      QUES: WRITE A QUERY TO DISPLAY THE NO OF EMPLOYEES WHOSE NA,E HAVING 'A' CHARACTER IIN THEIR NAME.
            SELECT COUNT(*) FROM EMP
            WHERE ENAME LIKE '%A%';
      QUES : WRITE A QUERY TO DISPLAY THE NO OF EMPLOYEES WHOSE NA,E HAVING 'A' CHARACTER IIN THEIR NAME IN EACH DEPARTMENT.
               SELECT COUNT(*) , DEPTNO FROM EMP
               WHERE ENAME LIKE '%A%'
               GROUP BY DEPTNO;
      QUES : 
               SELECT COUNT(*) , JOB FROM EMP
               WHERE ENAME LIKE '%A%'
               GROUP BY JOB;
      QUES: WRITE A QUERY TO DISPLAY NUMBER OF SALARY ARE PRESENT IN EMPLOYEE TABLE ?
            SELECT COUNT(*)
      QUES: WRITE A QUERY TO DISPLAY NUMBER OF TIMES EACH SALARIES ARE PRESENT IN EMPLOYEE TABLE ?
            SELECT COUNT(*) , SAL FROM EMP GROUP BY SAL;

   ## HAVING CLAUSE
      - IT IS USED TO FILTER THE GROUPS WHICH ARE CREATED BY GROUP BY  CLAUSE.
      - SYNTAX:
         SELECT MRF/GROUP EXP
         FROM TABLE_NAME
         [WHERE FILTER_CONDITION] 
         GROUP BY COL_NAME
         HAVING GROUP FILTER CONDITION..(THE CONDITIONS WHICH COMES WITH ANY MRF FUNCTION)
      - 1.FROM CLAUSE  WILL EXECUTE FIRST.
      - 2.IF WE ARE USING WHERE CLAUSE WHERE WILL EXECIUTE SECOND ELSE GROUP BY WILL EXECUTE
      - 3.GROUP BY WILL EXECUTE ROW BY ROW
      - 4.AFTER EXECITIOON OF A GROUP BY CLAUSE THE RECORDS ARE GIONG TO CONVERT AS A GROUP
      - 5.AFTER THE GROUP BY CLAUSE THE HAVING CKLAUSE WILL EXEXUTE AN IT WILL APPLY THE FILTERATION METHOD ON THE GROUPS.
      - 6.FINALLY THE SELECT CLAUSE WILL EXECUTRE AND IT WILL PRINT THE FINAL RESULT.

      - QUES: WRITE A QUERY TO DISPLAY THE DEPARTMENT NUMBER IN WHICH MORE THAN TWO EMPLOYEES ARE WORKING.
         SELECT DEPTNO 
         FROM EMP 
         GROUP BY DEPTNO
         HAVING COUNT(*) > 2;
     - QUES : WRITE A QUERY TO DISPLAY THE JOB OF THE EMPLOYEE ATLEAST 3 EMPLOYEES ARE WORKING.
               SELECT COUNT(*) , JOB 
               FROM EMP
               GROUP BY JOB
               HAVING COUNT(*) >= 3;
     -QUES : WRITE A QUERY TO DISPLAY  IN WHICH ATLEAST TWO CLEARKS ARE WORKING..
      

    -QUES : DISPLAY THE SALARY WHICH ARE REPEATED IN EMP TABLE . 
            SELECT SAL FROM EMP GROUP GROUP BY SAL HAVING COUNT(*) > 1;
    -QUES: DISPLAY THE SALARY WHICH ARE NOT REPEATED IN EMP TABLE.   
            SELECT SAL FROM EMP GROUP GROUP BY SAL HAVING COUNT(*) > 1;
    -QUES: DISPLAY THE JOB IN WHICH THE TOTAL SALARY WHICH IS NEEDED TO PAY MORE THAN 7000;
           SELECT SUM(SALARY) , JOB FROM EMP GROUP BY JOB HAVING SUM(SAL) > 7000
    -QUES: DISPLAY THE DEPARTMENT NUMBER IN WHICH MORE THAN 4 AND LESS THAN 6 EMPLOYEES ARE WORKING.
            SELECT COUNT(*) , DEPTNO FROM EMP GROUP BY DEPTNO HAVING COUNT(*) > 4 AND COUNT(*) < 6;
    -Ques : departmnt more than 2 and less than 7 employees working , having A character..
            SELECT COUNT(*) , DEPTNO 
            GROUP BY DEPTNO 
            HAVING 
    -QUES : DISPLAY THE SALARIES REPEATED IN SAME DEPARTMENT AND SAME JOB;
    - NOTE : WE CAN CREATE A GROUP FOR ANY TYPE OF COILUMN BUT MOST OF THE CASES IF WE CREATES THE GROUP THE COLUMN WHICH CONSISTS OF REPEATED
            DATA THOSE GROUP WILL BE USEFUL

    - Diffrence between where clause and the having clause---> HomeWork...

# SUB QUERY : 
    - THE QUERY WRITTEN INSIDE AN ANOTHER QUERY IS KNOWN AS SUBQUERY
    1. THE INNER QUERY WILL EXECUTE FIRST
    2. ONCE THE INNER QUERY WILL EXECUTE IT WILL GIVES YOU AN OUTPUT , BUT IT IS NOT FINAL RESULT.
    3. THE OUTPUT OF THE INNNER QUERY WILL BE GIVEN TO THE OUTER QUERY AS AN INPUT.
    4. FINALLY THE OUTER QUERY WILL EXECTE IT WILL GENERETES THE FINAL RESULT.
    5. IN THE SUBQUERY ALWAYS THE OUTER QUERY WILL BE DEPENDENT ON INNER QUERIES.
    6. WE CAN ABLE TO USE TOTAL 255 INNER QUERIES.
# WHEN AND WHY TO USE THE SUBQUERY
     A. WHEN WE HAVE UNKNOWN VALUE PRESENT IN THE QUESTION WE HAVE TO USE THE SUBQUERY.
     CASE 1. THE DATA TO BE SELECTED(FINAL RESULT ) & THE CONDITION TO BE EXCUTED(BELONGS TO YOUR INNER TABLE) 
     BOTH ARE FROM THE SAME TABLE.
      QUES : WRITE A QUERY TO DISPLAY THE EMPLOYESS WHOSE SALRIES ARE LESS THAN ALLEN.
      SELECT ENAME FROM EMP WHERE SAL < (SELECT SAL FROM EMP WHERE ENAME = 'ALLEN');
     
     CASE 2. THE DATA SELECTED AND THE COLUMN TO BE EXECUTED BOTH ARE FROM THE SAME TABLE.
      QUES: DISPLAY ALL THE EMPLOYEES THE EMPLOYEE WHO ARE WORKING IN SQL DEPARTMENT.
      SELECT ENAME FROM ENAME WHERE DNO = (SELECT DNO FROM DEPT WHERE DNAME = 'SQL');

     QUES : DISPLAY ALL THE DETAILS , THE EMPLOYEE WHO ARE WORKING IN THE SAME DEPARTMENT OF SMITH
            SELECT * FROM EMP WHERE DEPTNO = (SELECT DEPTNO FROM EMP WHERE ENAME = 'SMITH' );
     QUES : DISPLAY THE DEPARTMENT NAME OF SCOTT
            SELECT ENAME FROM DEPT WHERE DNO = (SELECT DEPTNO FROM EMP WHERE ENAME = 'SCOTT');
     QUES : DISPLAY ALL THE DETAILS EMPLOYEES WHOSE SALRIES ARE LESS THAN KING AND HIRED AFTER SMITH.
            SELECT * FROM EMP 
            WHERE SAL < (SELECT SAL FROM EMP WHERE ENAME = 'KING') AND HIREDATE > (SELECT HIREDATE FROM EMP WHERE ENAME  = 'SMITH' ) ;
     QUES : DISPLAY ALL THE DETAILS OF THE EMPLOYEES THE EMPLOYEES WHOSE SALARIES ARE MORE THAN 800 AND WORKING IN THE SAME
            DESIGNATION OF ALLEN AND HIRED AFTER SMITH;
            SELECT * FROM EMP WHERE SAL > 800 AND JOB = (SELECT JOB FROM EMP WHERE ENAME = "ALLEN") AND HIREDATE (SELECT HIREDATE FROM EMP WHERE ENAME = 'SMITH');
    
     QUES : THE ENAME WHO IS EARNING THE MAXIMUM SALARY
             SELECT ENAME FROM EMP
             WHERE SAL = (SELECT ,MAX(SAL) FROM EMP);
     QUES : DEPARTMENT NAME OF ALL THE EMPLOYEES WHO ARE GETTING MAXIUMUM SALARY.
            SELECT DNAME FROM DEPT WHERE DEPTNO = (SELECT DEPTNO FROM EMP WHERE SAL = (SELECT MAX(SAL) FROM EMP));
     QUES : WRITE A QUERY TO DISPLAY THE SECOND MAXIMUM SAL FROM EMP TABLE;
            SELECT SAL , MAX(SAL) FROM EMP 
            WHERE SAL < (SELECT MAX(SAL) FROM EMP);
     QUES : DISPLAY THE EMPLOYEE NAME WHO IS GETTING THE SECOND MAXIMUM SALARY .
     QUES : DIAPLAY THE DEPTNO OF ALL THE EMPLOYEE WHO IS GETTING THE MAXIMUM SALARY.
            SELECT DEPTNO FROM EMP WHERE 
             SAL = (SELECT MAX(SAL ) FROM EMP);
     QUES : DISPLAY THE DEPTNAME OF ALL THE EMPLOYEE WHOSE NAME HAVING 'A' CHARACTER;

            if your inner query giving you a singlr output you can use =
             if your inner query giving you muktiple output you can use special operatot like IN , NOT IN , etc.
     Note : There are two types of subquery :
     SINGLE ROW SUB QUERY : IF THE INNER QUERY GENERATES SINGLE VALUES AS OUTPUT.THESE TYPE OF SUBQUERIES ARE KNOWN AS SRSQ.
      MULTI ROW SUB QUERY : IF THE INNER QUERY GENERATES MORE THAN ONE OUTPUT,THESE TYPE OF SUBQUERY ARE KNOWN AS MRSQ.
      IT IS DIGFFICULT TO USE SPECIAL OPERATORS OR MRF (IN , NOT IN , MAX , MIN ...ETC)

     Ques : WRITE A QUERY TO DISPLAY ALL THE DETAILS OF THE EMPLOYEES WHOSE SALARIES ARE MORE THAN ALL THE EMPLOYEES DEPTNO 10;
            SELECT * FROM EMP WHERE SAL > (SELECT MAX(SAL) FROM EMP WHERE DEPTNO = 30)
             DIAPLAY ALL THE DETAILS OF THE EPLAOYEE  ,THE EMPLOYEES WHOSE SALARIES ARE MORE THAN ANY ONE OF THE EMPLOYEE 
             OF DEPARTMENT NUMBER 10;
            SELECT * FROM EMP WHERE SAL > (SELECT MIN(SAL) FROM EMP WHERE DEPTNO = 30)
     QUES : THE EMPLOYEES ,  THE EMPLOYEES WHOSE HIRED AFTER ALL THE SALESMAN.
           SELECT * FROM EMP 
           WHERE HIREDATE > (SELECT MAX(HIREDATE) FROM EMP WHERE JOB = 'SALESMAN' );
     QUES : DISPLAY THE DETAILS OF THE EMPLOYEE IF GTHE EMPLOYEE HIRED AFTER ANY ONE OF THE SALESMAN.
             SELECT * FROM EMP 
           WHERE HIREDATE > (SELECT MIN(HIREDATE) FROM EMP WHERE JOB = 'SALESMAN' );

     QUES : WRITE A QUERY TO DIAPLAY ALL THE DETAILS OF THE EMPLOYEES THE EMPLOYEES WHOSE SALARIES ARE LESS THAN ALL THE 
            MANAGERS .
            SELECT * FROM EMP
            WHERE SAL < (SELECT MIN(SAL) FROM EMP WHERE JOB = 'MANAGER');

    QUES:  WRITE A QUERY TO DISPLAY ALL THE DETAILS OF THE EMPLOYEES THE EMPLOYEES WHOSE SALARIES ARE LESS THAN ANY ONE 
           OF  THE MANAGERS .

    QUES : DISPLAY ALL THE DETAILS OF THE EMPLOYEE THE EMPLOYEE WHO HIRED  AFTER ANY ONE OF THE SALESMAN;
           SELECT * FROM EMP
           WHERE HIREDATE > (SELECT MIN(HIREDATE) FROM EMP WHERE JOB = 'SALESMAN')
    QUES : DISPLAY ALL THE DETAILS OF THE EMPLOYEE THE EMPLOYEE WHO HIRED AFTER ALL  THE SALESMAN;
           SELECT * FROM EMP
           WHERE HIREDATE > (SELECT MIN(HIREDATE) FROM EMP WHERE JOB = 'SALESMAN')
    QUES : ALL DETAILS , THE EMPLOYEE WHO HIRED AS THE LAST SECOND EMP;
           SELECT * FROM EMP 
           WHERE HIREDATE IN (SELECT MAX(HIREDATE) FROM EMP WHERE HIREDATE < (SELCT MAX(HIREDATE) FROM EMP));
    QUES : DISPLAY THE DEPARTMENRT NAME OF THE ENMLOYEES WHO ARE WORKING AS SALESMAN EARNING COMMISSION MORE THAN SMITH
           AND EARNING SALARY LESS THAN ANY ONE OF THE MANAGAER AND HIRED AS FIRST THIRD EMPLOYEE .
            
  # HIRARCHI BETWEEN THE EMPLOYESS
           

             
             
     
           








# Joins 
   - The process  merging the multiple tables and  fetching the data from multiple tables simultaneously is known as joins.
   - In sql there are five type of joins.
     1. cartesian joins (CROSS JOINS)
     2. Inner join
     3. natural join
     4. self join
     5. outer join ----> 1. Right outer join , Left outer join , Full outer join
     6. if we are joining the multiple tables first it will joins the table (ex: emp , dept , -------emp+dept --- is a result table)
        then if we want to get from only emp tables we can fetch the data else if we want from dept we can fetch and also 
        if we want from both we can get the data.
     7. basically there are theree types of records we will get after joining the tables
        1. error records
        2. matching records
        3. unmatching records
   # cartesian joins..
   - It is the process of fetching the data from multiple table by merging all the records of one table to each and every
     record of remaining table.
   - crossing method : The each and every record from the first table will merge with each and every record of remaining table
   - is known as crossing method.
   - syntax

           SELECT COL_NAME/ EXP /*
           FROM TABLE_NAME1 , TABLENAME2 , ... TABLE_NAMEn
           [WHERE FILTER THE CONDITION]...

   - QUES: DISPLAY ALL THE EMPLOYEES DETAILS AND THERE DEPARTMENT DETAILS.
     - SELECT * FROM EMP , DEPT ;
   - cartesian join will help us to get the data from multiple tables. but it will also fetch error 
     records from multiple tables.
   - It is consider as a drawback of the cartesian joins to overcome this drawback we have use either inner/natural join.
   - Ques : write a query to display the Ename , sal , dept name of smith.
   - select ENAME , SAL , D_NAME FROM EMP , DEPT WHERE ENAME = 'SMITH';


   # INNER JOINS
   - IT IS USE TO GET THE MATCHING RECORDS FROM THE MULTIPLE TABLES.
   - WHERE CONDITION IS MANDATORY IN INNER JOIN.
   - LESS MEMORY IS REQUIRED TO DISPLAY THE DATA.
   - SYNTAX:
          
           SELECT COL_NAME / EXP / *    
           FROM TABLE_NAME1 , TABLE_NAME2, ... TABLENAMEn
            WHERE  INNER_JOIN_CONDITIONS[AND FILTER CONDITIONS]

   - WRITE A QUERY TO DISPLAY ALL THE EMPLOYEE DETAILS AND THEIR DEPARTMENT DETAILS.
       
         SELECT * FROM EMP , DEPT WHERE EMP.DNO IN DEPT.DNO;

   - WRITE A QUERY TO DISPLAY THE SAL , LOCATION AND THE DEPTNAME OF ALL THE EMPLOYEE WHOSE NAME STARTS WITH S.

         SELECT * FROM EMP , DEPT WHERE EMP.DNO IN DEPT.DNO AND ENAME LIKE 'S%';
   - WRITE A QUERY TO DISPLAY THE ENAME ,SAL , LOCATION AND  OF ALL THE EMPLOYEE WHO ARE WORKING IN SALES DEPARTMENT.

         SELECT * FROM EMP , DEPT WHERE EMP.DEPTNO IN DEPT.DEPTNO AND DNAME = 'SALES';
   - WRITE A QUERY TO DISPLAY THE SAL , LOCATION AND THE DEPTNAME OF ALL THE EMPLOYEE WHOSE NAME ENDS WITH R.

          SELECT * FROM EMP , DEPT WHERE EMP.DNO IN DEPT.DNO AND ENAME LIKE '%R'; XXXX
           SELECT * FROM EMP ,EMP.DEPTNO WHERE EMP.DNO IN DEPT.DNO AND ENAME LIKE '%R';
   - JOB , LOCATION & DEPTNO OF ALL THE EMPLOYEE WHO WORKING IN SALES DEPARTMENT.
   - 
             SELECT ENAME , JOB , LOC EMP.DEPTNO FROM EMP , DEPT WHERE EMP.DEPTNO IN DEPT.DEPTNO AND DNAME = 'SALES';
   - WRITE A QUERY TO DISPLAY JOB LOC SAL AND ANNUAL SAL WHO ARE WORKING IN DEPTNO 30;

          SELECT JOB , LOC , SAL , SAL * 12 , FROM EMP, DEPT WHERE EMP.DEPTNO IN DEPT.DEPTNO AND DEPT.DEPTNO IN 30;  

   - IN INNER JOIN ACCESSING THE FOREIGN KEY COLUMN WILL BECOME THE DIFFICULT UNTIL WE ARE NOT ACCESSING WITH TABLE NAME.

# Natural Joins
- THE NATURAL JOINS HAVE TWO BEHAVIOUR 
  1. NATURAL JOIN WILL ACT AS CARTESIAN JOIN.
  2. NATURAL JOIN WILL ACT AS INNER JOIN.
- NATURAL JOIN ACT AS CARTESIAN JOIN
  1. IF THERE IS NOT ANY CONNECTION B/W ALL THE MULTIPLE TABLES IF WE USE A NATURAL JOIN , IN THIS CASE THE NATURAL JOIN
     WILL GIVE A RESULT AS A CARTESIAN JOIN.
- NATURAL JOIN ACT AS INNER JOIN
  1. IF THERE IS A CONNECTION B/W ALL THE MULTIPLE TABLE IN THIS CASE , THE NATURAL JOIN WILL GIVE A RESULT TABLE AS A INNER JOIN
- SYNTAX :

        SELECT COL_NAME /EXP /*
        FROM TABLE_NAME1 , NATURAL JOIN TABLE_NAME2 NATURAL JOIN TABLE_NAMEn
        [WHERE FILTER CONDITION]
        SELECT ENAME , LOC , DEPTNO 
        FROM EMP NATURAL JOIN DEPT;
- NOTE : 
  1. ACCESSING FOREIGN KEY WILL BECOME VERY EASY.
  2. JOIN CONDITION IS NOT REQUIRED ION ORDERED TO GET THE MATCHING RECORDS.
  3. IF WE DON'T KNOW WHETHER THE TABLES ARE CONNECTED WITH EACH OTHER , THEN WE CAN EASILY USE NATURAL JOIN.
  4. QUES:DISPLAY THE EMPLOYEE NAME AND THE LOCATION OF ALL EMPLOYEE , THE EMPLOYEE WHO ARE WORKING IN DEPARTMENT NUMBER 30.
      
         SELECT ENAME , LOC 
         FROM EMP , DEPT 
         WHERE EMP.DEPTNO IN DEPT.DEPTNO AND EMP.DEPTNO = 30;
  

         SELECT ENAME , LOC 
         FROM EMP  NATURAL JOIN DEPT
          WHERE DEPTNO = 30;
  5. QUES : WRITE ENAME , SALARY , DEPTNAME OF ALL THE EMPLOYEE , THE EMPLOYEE WHO ARE WORKING IN NEW-YORK LOC AND EARNING SALARY 
     MORE THAN SMITH.
  
          SELECT ENAME , SAL FROM EMP NATURAL JOIN DEPT 
           WHERE SAL > (SELECT SAL FROM EMP WHERE ENAME = "SMITH") AND LOC = 'NEW YORK';
   
           SELECT * FROM EMP NATURAL JOIN DEPT 
           WHERE SAL > (SELECT SAL FROM EMP WHERE ENAME = "SMITH") AND LOC = 'NEW YORK';
  
# SELF JOIN
- JOINING SAME TABLE ITSELF IS KNOWN AS SELF JOIN.
- HIERARCHICAL  
- SYNTAX :
     
        SELECT COLUMN_NAME / EXP /*
        FROM TABLE_NAME1 ALIAS_NAME , TABLE_NAME2 ALIAS_NAME , TABLE_NAMEn 
        WHERE TABLE_NAME1.COL_NAME IN TABLE_NAME2.COL_NAME AND FILTER CONDITION;

- WAQTD ALL THE EMPLOYEES DETAILS AND THEIR MANAGER DETAILS.
- WATQD EMP_NAME , SAL , EMP_HIRE_DATE , MANAGER_SALARY AND MANAGER_HIRE_DATE.
- WAQTD EMP_NAME AND JOB , MANAGER NAME AND JOB IF EMPLOYEE IS WORKING AS CLERK ? 
- WAQTD THE SMITH MANAGER ? 
- WAQTD EMPLOYEE NAME MANAGER NAME AND MANAGER'S MANAGER NAME IF EMPLOYEE SALARY IS LESS THAN MANAGERS ,MANAGERS SALARY.

# OUTER JOIN
- IT IS USED TO GET THE UNMATCHED RECORD ALONG WITH THE MATCHING RECORD OF MULTIPLE TABLES.
- THERE ARE THREE TYPES OF OUTER JOIN
  1. LEFT OUTER JOIN
  2. RIGHT OUTER JOIN
  3. FULL OUTER JOIN
- LEFT OUTER JOIN
  1. IT IS USED TO PRINT THE MATCHING DATA OF ALL THE TABLE ALONG WITH THE UNMATCHED DATA OF LEFT TABLE.
  2. SYNTAX:
           
           SELECT COL_NAME/EXP/*
           FROM TABLE_NAME[LT], TABLE_NAME2[RT]
           WHERE LT.COL_NAME IN RT.COL_NAME(+) AND FILTER CONDITIONS;
- RIGHT OUTER JOIN
  1. IT IS USED TO GET THE MATCHED DATA FROM BOTH THE TABLE ALONG WITH THE UNMATCHED DATA OF RIGHT TABLE.
  2.             SELECT COL_NAME/EXP/*
           FROM TABLE_NAME[LT], TABLE_NAME2[RT]
           WHERE LT.COL_NAME(+) IN RT.COL_NAME() AND FILTER CONDITIONS;
- FULL OUTER JOIN
  1. IT IS USED TO GET THE MATCHED DATA FROM BOTH THE TABLES ALONG WITH THE UNMATCHED DATA OF BOTH THE TABLE.
 
                  SELECT COL_NAME/EXP/*
           FROM TABLE_NAME[LT] FULL OUTER JOIN  TABLE_NAME2[RT]
            ON LT.COL_NAME IN RT.COL_NAME
            WHERE FILTER CONDITION;
           
 - QUES: DISPLAY ALL THE EMPLOYEE DETAILS AND THEIR DEPARTMENT DETAIL FOR ALL THE EMPLOYEES EVEN THOUGH THEY ARE NOT WORKING IN ANY 
   DEPARTMENT
 - QUES: DISPLAY THE EMPLOYEE DETAILS IN WHICH THE DEPARTMENT THE EMPLOYEES ARE NOT WORKING.
 - QUES: DISPLAY THE EMPLOYEES DETAILS AND THEIR DEPARTMENT DETAILS 
   1. EVEN THOUGH THE EMPLOYEES ARE NOT WORKING IN ANY DEPT
   2. THE DEPARTMENT IN WHICH NO EMPLOYEES ARE WORKING

# SRF - SINGLE ROW FUNCTION
- THE FUNCTION WHICH WILL TAKE N NUMBER OF INPUT AND EXECUTES WHICH WILL GIVE N NUMBER OF OUTPUTS.
- THE FUNCTION IN WHICH THE NUMBER OF INPUT ARE EQUAL TO NUMBER OF OUTPUT.
  1. LENGTH()
  2. UPPER/LOWER.INITCAP
  3. REVERSE()
  4. ROUND()
  5. TRUNC()
  6. SYSDATE()
  7. CURRENT_DATE()
  8. TO_DATE()
  9. TO_CHAR()
  10. NVL()
  11. SUBSTR()
  12. INSTR()
  13. LAST_DAY()
  14. MONTH_BETWEEN()
  15. REPLACE()
- SINGLE ROW FUNCTION WILL ALLOW MULTIPLE COLUMN OR EXPRESSION AS A ARGUMENT.
- SINGLE ROW FUNCTIONS ARE NOT POSSIBLE TO USE HAVING CLAUSE.
- WHERE CLAUSE WE CAN USE SINGLE ROW FUNCTION.
- SINGLE ROW FUNCTION WILL NOT IGNORE THE NULL VALUE.
- IN SELECT CLAUSE ALONG WITH SINGLE ROW FUNCTION WE CAN USE N NUMBERS OF COLUMNS.
- SOME OF THE SINGLE ROW FUNCTION ARE NOT REQUIRED EVEN SINGLE ARGUMENT ALSO.


## # DDL --> DATA DEFINITION LANGUAGE 
- IT IS USED TO CREATE , MODIFY , DESTROYS THE DATABASE OBJECTS...
- BASICALLY THERE ARE 5 COMMANDS IN DDL...
- NORMAL TABLE : TABLE WHICH DOES NOT HAVE ANY PRIMARY KEY AND FOREIGN KEY
- PRIME TABLE : TABLE WHICH CAN  HAVE PRIMARY KEY AND FOREIGN KEY.
- COMPLEX TABLE : 
- 1.CREATE 2. RENAME 3.TRUNCATE 4.DROP(FLASHBACK , PURGE) 5.ALTER (7 OPERATIONS)
- 1. CREATE - IT IS USED TO CREATE A DATABASE OBJECTS
   - SYNTAX :  CREATE : DATABASE OBJECTS
  
   -       CREATE TABLE TABLE_NAME 
           (
             COL_NAME1 DATATYPE [CONSTRAINTS],
             COL_NAME2 DATATYPE [CONSTRAINTS],
             .
             .
             .
             COL_NAMEn DATATYPE [CONSTRAINTS],
             CONSTRAINTS REF_NAME PRIMARY KEY(COL_NAME),
             CONSTRAINT REF_NAME FOREIGN KEY(COL_NAME) REFERENCES PARENT_TAB_NAME(COL_NAME));
         );
   - THE TABLE NAME AND THE COLUMN NAME SHOULD NOT START WITH ANY NUMERIC VALUE / SPECIAL CHARACTERS.
   - THE TABLE NAME / COL NAME SHOULD NOT CONSIST A SPACE BETWEEN THE STRING.
   - THE DATABASE  SHOULD NOT HAVE THE SAME NAME OF MULTIPLE TABLE.
   - THE SINGLE TABLE CAN HAVE ONLY ONE PRIMARY KEY.
   - THE SAME TABLE SHOULD NOT CONSIST OF SAME NAME OF MULTIPLE COLUMN.
   - SQL IS NOT A CASE SENSITIVE VALUE.

- WRITE A QUERY TO CREATE THE STUDENT TABLE WHICH CONSISTS OF ANY 5 COL , USE THE PROPER DATATYPE OF EACH COL , WHICH 
  SHOULD NOT CONSISTS OF ANY PRIMARY KEY AND FOREIGN KEY.
          
         CREATE TABLE STD_DETAILS
         (

           SID_NO NOT NULL,
           SNAME VARCHAR(20),
           AGE NUMBER CHECK(AGE > 18) NOT NULL ,
           GENDER CHAR(1) NOT NULL,
           COURSE VARCHAR(10)


          );
- WRITE A QUERY TO CRETE THE PRODUCT TABLE WHICH CONSISTS OF PID , PNAME , MDATE , EDATE(<2025) , BRAND , PRICE(>0) , DISCOUNT(<100%); 


# Alter
- It is used to modify the structure of the table...
- There are basically 7 operation in Alter
- 1. ADD COLUMN : USE TO ADD THE COLUMN
  - SYNTAX : ALTER TABLE TABLE_NAME ADD COLUMN_NAME DATA-TYPE [CONSTRAINTS];
  - ALTER TABLE EMP ADD COLUMN COMM NUMBER;
  - ALTER TABLE EMP ADD COLUMN MNO NUMBER CHECK(LENGTH(MNO) = 10) UNIQUE;


  2. DROP COLUMN : USE TO DROP THE COLUMN
  - SYNATX : ALTER TABLE TABLE_NAME DROP COLUMN COLUNM_NAME;
  - ALTER TABLE EMP DROP COLUMN MNO;
  - ALTER TABLE EMP DROP COLUMN COMM;



  3. RENAME COLUMN : USE TO CHANGE THE COLUMN NAME.
  - SYNTAX : ALTER TABLE TABLE_NAME RENAME COLUMN OLD_COL_NAME TO NEW_COL_NAME;
  - ALTER TABLE EMP RENAME COLUMN JOIN_DATE TO HIRE_DATE;
  - ALTER TABLE EMP RENAME COLUMN ENAME TO EMPNAME;



  4. CHANGE THE DATATYPE : USE TO CHANGE THE DATA-TYPE OF THE COLUMN;
  - ALTER TABLE TABLE_NAME MODIFY COL_NAME NEW DATA-TYPE;
  - ALTER TABLE EMP MODIFY MNO DATE; EXECUTED;
  - ALTER TABLE EMP MODIFY ENAME NUMBER: ERROR BECAUSE DATA IS ALREADY FILLED IN ENMAE COL WITH TYPE VARCHAR.



  5. DROP CONSTRAINTS : USE TO DROP THE CONSTRAINT
  - SYNTAX : ALTER TABLE TABLE_NAME DROP CONSTRAINT CONSTRAINT_REF_NAME;
  - SELECT * FROM USER CONSTRAINT WHERE TABLE_NAME = "FLIGHT10";
  - ALTER TABLE PASSENGER10 DROP CONSTRAINT SYS_C005607;-->REF_NAME.



  6. ADD CONSTRAINTS : USE TO ADD THE CONSTRAINTS
  - ALTER TABLE TABLE_NAME ADD CONSTRAINT REF_NAME CONSTRAINT_NAME(COL_NAME);
  -  ALTER TABLE EMP ADD CONSTRAINT EID_PK PRIMARY KEY(EID);
  - ALTER TABLE EMP ADD CONSTRAINTS SQL_FK FOREIGN KEY(SID) REFERENCES DEPT(SID)



  7. TO CONVERT NULL TO NOT NULL AND VISE-VERSA
  - SYNTAX : ALTER TABLE TABLE_NAME MODIFY COL_NAME EXISTING DATA-TYPE NULL/NOT NULL;
  - ALTER TABLE TRAINER MODIFY SAL NUMBER NOT NULL;



  8. NOTE : MOST ALTER OPERATION WILL WORK WITH EMPTY TABLE.

                   DDL COMPLETED...

# # DML command
- data mainipulation langyage
- it is used to insert modify and delete the data from table;
- 1. INSERT : IT IS USED TO INSERT THE RECORDS INTO THE TABLE;
- SYNTAX: INSERT INTO TABLE_NAME (V1 , V2 , ..... Vn);
- INSERT INTO TABLE_NAME VALUES(&COL_NAME1 , &COL_NAME2 , $COL_NAMEn  );
- INSERT ALL : INSERT INTO TABLE_NAME1(COL_NAME1 , COL_NAME2 , COL_NAMEn  ) VALUES(V1 , V2 ... Vn);
- INSERT INTO TABLE_NAME2(COL_NAME1 , COL_NAME2 , COL_NAMEn  ) VALUES(V1 , V2 ... Vn);
- INSERT INTO TABLE_NAMEn(COL_NAME1 , COL_NAME2 , COL_NAMEn  ) VALUES(V1 , V2 ... Vn);
- SELECT * FROM DUAL ;
- 2. DELETE : USE TO DELETE THE RECORDS FROM THE TABLE
  - SYNATAX : DELETE FROM TABLE_NAME
              [WHERE CONDITION]; --- OPTIONAL
  - 
- 3. UPDATE : USE TO CHANGE THE VALUES FROM THER TABLE
   - UPDATE TABLE_NAME 
   - SET COL_NAME = VALUE , COL_NAME = VALUE...
   - [WHERE CONDITION ]; ----->  OPTIONAL
   - NOTE : ALL DML OPERATION ARE ALSO KNOWN AS TRANSACTION IN SQL.
   - NOTE2: THESE ARE ALSO KNOWN AS NON AUTOCOMMIT STATEMENT.
   - AUTOCOMMIT : AUTOMATICALLY THE TRANSACTION WILL SAVE.
   - NON AUTOCOMMIT : MANUALLY WE HAVE TO SAVE THE TRANSACTION.
   - DDL IS AUTOCOMMIT OPERATION.

# #TCL
- TRANSACTION CONTROL LANGUAGE
- IT IS USED TO CONTROL THE TRANSACTION BEFORE COMMIT
- THERE ARE 3 COMMANDS IN TCL
- 1. ROLLBACK : USE TO GET BACK THE TRANSACTION BEFORE COMMIT.
     - SYNTAX : ROLLBACK;
- 2. COMMIT : IT IS USED TO SAVES THE TRANSACTION INTO THE DB
    - SYNTAX : COMMIT 
- 3. SAVEPOINT : USE TO CONTROL THE TRANSACTION IN LEVEL WISE
    - SYNTAX : SAVEPOINT SAVEPOINT_NAME;
  NOTE : TO CONTROL THE TRANSACTION BY SAVEPOINTS 
    - ROLLBACK TO SAVEPOINT_NAME ;

# DCL
- DATA CONTROL LANGUAGE
- USE TO CONTROL THE DATA FLOW BETWEEN THE USERS
- THERE ARE 2 COMMANDS IN DCL
- 1. GRANT : USE TO GIVE THE ACCESS TO USERS
   - SYNTAX : GRANT SQL_COMMAND ON TABLE_NAME
      TO USER_NAME;
  2. REVOKE : USE TO GETBACK THE ACCESS FROM THE USER
   - SYNTAX: REVOKE SQL_COMMANDS OPN TABLE_NAME
     FROM  USER_NAME;
  NOTE : TO CHECK THE ACCESS LIST WHICH WE GAVE 
     SELECTS * FROM USER_TAB_PRIVS;

  
