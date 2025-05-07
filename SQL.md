
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






## special operator in sql
   - These Operators are used to perform the special type of task in sql.
   - There are 4 set of special operators
   - IN and NOT IN
   - BETWEEN , NOT BETWEEN
   - IS , IS NOT
   - LIKE ,  NOT LIKE
   - these all the operators are not mandatory we can also solve the queries by using n no. of different
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
   
   - BETWEEN VS NOT BETWEEN
     - These are the special operators which are help us to solve the range value queries.
     - syntax : 
     - WHERE COL_NAME /EXP BETWEEN / NOT BETWEEN LOWER_VALUE AND HIGHER_VALUE;
     - QUES : write a query to display all the details of the employees , the employee whose salary are between 1600 to 3000.
     - select * from emp where salary > 1600 AND salary < 3000;
     - select * from emp where salary between 1601 and 2999 ;
     - Ques : Display all the details of employees whose salary are in the range of 1600 and 3000;
     - select * from emp where salary between 1600 and 3000;
     - ques : Display all the details from , the employee who hired 1980 to 1987.
     - ques: Display all the details of the employees who hired in the range of 1980 and 1987.
     - Display all the details of employee , the employee who hired during the year of 1981.
     - Display all the details except all the employees , the employees whose salaries are in  between 1600 to 3000.
     - Display all the details if the employees except all the employees , the employees whose salary are in the range of 
       1600 to 3000;
   - IS Vs IS NOT
     - These are the special operator which are used to compare null values. 
     - Ques : write a query to display all the details of employees the employees who are earning the commission
     - Ques : Display all the details of the employees , the employees who are not earning the commission.
   
   - LIKE VS NOT LIKE 
     - It is used to perform the pattern matching operations.
     - Syntax:
     - WHERE COL_NAME/EXP LIKE/NOT LIKE 'PATTERN'
     - To create a pattern the two special characters we have to use '%' , "_";
     - % : the percentage will allow any type of characters , n number of characters.
     - _ : the underscore will allow any type of characters but only one digit of characters.
     - Ques : Display all tye details of the employees , the employees whose names end with r characters.
     - select * from emp where ename like '%R';
     - Ques : Diaplay all the details of the employees , the employee whose name having 'a' character
     - select * from emp where ename like '%A%';
     - Ques : Display all the details of employee , the employees who hired in the dec.
     - SELECT * FROM EMP WHERE HIREDATE LIKE '%DEC%';
     - Display all the details of employee , the employees whose name having last second character in the E.
     - SELECT * FROM EMP WHERE ENAME LIKE '%E_';
     - Display all the details of employees . the employees whose name starts with a character and starts with p character.
     - Display all the details of employees , except all the employees whose name not starts with A and B;
     - SELECT * FROM EMP WHERE ENAME NOT LIKE 'A%' AND ENAME NOT LIKE 'B%';
     - Display all the details of employees whose name starts with vowels;
     - SELECT * FROM EMPLOYEES WHERE ENAME LIKE 'A%' AND ENAME NOT LIKE '%E_'
     - Display all the details of employees whose name not starts with vowels.
     - Display all the details of employees , 

     select emp.* sal*12 "Annual Salary" , sal*6 "Halfturn salary" from emp where dept IN(10 , 20);

  ##  Functions
      - The set of instructions which are help is to perform the specific task is known as
        functions.
      - In general there are two types of functions--> 1.userdefined 2.InBuilt


      - user-defined : A functions that are defined by users according to their requirements are known as 
        user defined functions.
      - we can do modifications in user defined function.
      - only the person who create the functions can used it. 
        static
      - security will be more.
      



      - InBuilt : the functions which are peredefined in the software are known as bnuiltIn functions , inbuilt functions and pre-defined
        functions.
      - we cannot do modifications in user defined function.
      - Everyone can use builtIn functions . 
      - Dynamic 
      - security will be less.
      - Inbuilt Functions ---> 1.Single row function , 2.Multi row function.


     single row functiuons
      The functons in which yhe number of inputs are equal to no of outputs are knoe as single row functions.
      The single row functions executes line  by line or row by row.
       1) length()
       2) upper()
       3.) substrings() ......ETC
     Multi row functions.
       The functions which gives only one output , on multiple input..
       It executes group by group.
       After the aggregation the execution takes place , hence these function also known as aggregate functions. 
       AVG()
       MAX()
       MIN()
       SUM()
       COUNT()
   ## Rules of multi row functions.
      1)syntax:
             MRF_NAME(COL_NAME/EXPRESSION)
             MAX(SAL/SAL*12) , MIN(SAL/SAL*12) , .....
      2. ALLL THE MRF WILL ALLOWS ONLY COLUMN/EXP AS ARGUMENT
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




     5. IN SELECT CLAUSE ALONG WITH MULTIROW FUNCTION IT IS DIFFICULT TO USE THE COLUMNS / EXPRESSION
        WE CAN USE IF WE ARE USING THE GROUP BY CLAUSE

     6. MULTIROW FUNCTION WILL IGNORES  NULL VALUE.

    7. AMONG ALL THE MULTIROW FUNCTIONS ONLY THE COUNT FUNCTION WILL ALLOW THE '*' AS A ARGUMENT.

      QUES: WRITE A QUERY TO DISPLAY THE TOTAL SALARY AND THE NUMBER OF EMPLOYEES WHO ARE 
      WORKING AS A MANAGER.
     
      QUES: WRITE A QUERY TO DISPLAY THE NUMBER OF EMPLOYEES WORKING IN DEPTNO 10 AND 30.
       
      QUES : DISPLAY THE NUMBER OF EMPLOYEE WHO ARE WORKING IN EACH DEPARTMENT FOR THE DEPARTMENTNO 10 AND 30
     
## group by clause.
    - IT IS USED TO CONVERT THE RECORD INTO GROUPS BASED ON THE COLUMNS
    - SYNTAX
      SELECT MRF / GROUP EXPRESSIONS FROM TABLE_NAME 
      [WHERE FILTER CONDITIONS] ---- OPTIONAL
      GROUP BY COL_NAME;
      1.THE FROM CLAUSE WILL EXECUTE FIRST..
      2.AFTER THE FORM CLAUSE IF WE ARE USING THE WHERE CLAUSE IT EIOLL EXECUTE SECOND ELSE THE GROUP BY CLAUSE EXECUTE SECOND
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
             WHERE JOB = 'CLERK'
             GROUP BY JOB;

      QUES : WERITE A QUERY TO DISPLAY THE NUMMBER OF EMPLOYEE WORKING AS A MANAGER IN EACH DEPARTMENT.
             SELECT COUNT(*) , DEPTNO FROM EMP
             WHERE JOB = 'MANAGER'
             GROUP BY DEPTNO;


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
         HAVING GROUP FILTER COMNSITION
      - 1.FROM CLAUSE  WILL EXECUTE FIRST.
      - 2.IF WE ARE USING WHERE CLAUSE WHERE WILL EXECIUTE SECOND ELSE GROUP BY WILL EXECUTE
      - 3.GROUP BY WILL EXECUTE ROW BY ROW
      - 4.AFTER EXECITIOON OF A GROUP BY CLAUSE THE RECORDS ARE GIONG TO CONVERT AS A GROUP
      - 5.AFTER THE GROUP BY CLAUSE THE HAVING CKLAUSE WILL EXEXUTE AN IT WILL APPLY THE FILTERATION METHOD ON THE GROUPS.
      - 6.FINALLY THE SELECT CLAUSE WILL EXECUTRE AND IT WILL PRINT THE FINAL RESULT.

      - QUES: WRITE A QUERY TO DISPLAY THE DEPARTMENT NUMBER IN WHICH MORE THE TWO EMPLOYEES ARE WORKING.
         SELECT DEPTNO 
         FROM EMP 
         GROUP BY DEPTNO
         HAVING COUNT(*) > 2;
     - QUES : WRITE A QUERY TO DISPLAY THE JOB OF THE EMPLOYEE ATLEAST 3 EMPLLOYEES ARE WORKING.
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
    - NOTE : WE CAN CREATE A GROUP FOR ANY TYPE OF COILUMN BUT MOST OF THE CASES IF WE CREATES THE GROUP THE COLUMN WHICH CONSISTS OF REPEATED
            DATA THOSE GROUP WILL BE USEFUL







# Joins 
   - The process of fetching the data from multiple tables simultaneously is known as joins.
   - In sql there are five type of joins.
     1. cartesian joins (CROSS JOINS)
     2. Inner join
     3. natural join
     4. self join
     5. outer join ----> 1. Right outer join , Left outer join , Full outer join
   # cartesian joins..
   - it is the process of fetching the data from multiple table by merging all the records of one table to each and every
     record of remaining table.
   - syntax

          SELECT COL_NAME/ EXP /*
           FROM TABLE_NAME1 , TABLENAME2 , ... TABLE_NAMEn
           [WHERE FILTER THE CONDITION]..
   - QUES: DISPLAY ALL THE EMPLOYEES DETAILS AND THERE DEPARTMENT DETAILS.
     - SELECT * FROM EMP , DEPT ;
   - cartesian join will help us to get the data from multiple tables. but it will also fetch error 
     records from multiple tables.
   - It is consider as a drawback of the cartesian joins to overcome this drawback we have use either inner/natural join.
   - Ques : write a query to display the Ename , sal , dept name of smith.
   - select ENAME , SAL , D_NAME FROM EMP , DEPT WHERE ENAME = 'SMITH';


   # INNER JOINS
   - IT IS USE TO GET THE MATCHING RECORDS FROM THE MULTIPLE TABLES.
   - SYNTAX:
          
           SELECT COL_NAME / EXP / *    
           FROM TABLE_NAME1 , TABLE_NAME2, ... TABLENAMEn
            WHERE  INNER_JOIN_CONDITIONS[AND FILTER CONDITIONS]

   - WRITE A QUERY TO DISPLAY ALL THE EMPLOYEE DETAILS AND THEIR DEPARTMENT DETAILS.
       
         SELECT * FROM EMP , DEPT WHERE EMP.DNO IN DEPT.DNO;

   - WRITE A QUERY TO DISPLAY THE SAL , LOCATION AND THE DEPTNAME OF ALL THE EMPLOYEE WHOSE NAME STARTS WITH S.

         SELECT * FROM EMP , DEPT WHERE EMP.DNO IN DEPT.DNO AND ENAME LIKE 'S%';
   - WRITE A QUERY TO DISPLAY THE ENAME ,SAL , LOCATION AND  OF ALL THE EMPLOYEE WHO ARE WOPRKING IN SALES DEPARTMENT.

         SELECT * FROM EMP , DEPT WHERE EMP.DEPTNO IN DEPT.DEPTNO AND DNAME = 'SALES';
   - WRITE A QUERY TO DISPLAY THE SAL , LOCATION AND THE DEPTNAME OF ALL THE EMPLOYEE WHOSE NAME ENDS WITH R.

          SELECT * FROM EMP , DEPT WHERE EMP.DNO IN DEPT.DNO AND ENAME LIKE '%R'; XXXX
           SELECT * FROM EMP ,EMP.DEPTNO WHERE EMP.DNO IN DEPT.DNO AND ENAME LIKE '%R';

   - IN INNER JOIN ACCESSING THE FOREIGN KEY COLUMN WILL BECOME THE DIFFICULT UNTIL WE ARE NOT ACCESSING WITH TABLE NAME.