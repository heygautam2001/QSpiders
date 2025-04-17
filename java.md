## history of java 
java was introduced in the year of 1991 by james gosling.
He along with his team was working in the company names sun-microsystem. He faced some issue like 
security
platform architecture etc.
**currently oracle is the owner of java.
**Java was developed mainly to build internet best/based application.
**java has two parent
1. C - from c it has taken syntax excluding pointers.
2.  C++ - from c++ OPPS concept.

## Programming language
- programming language is used to interact with the machine,
- A language whiuch is used to write the program is called a programming language
- Based on human understanding it is classified in three types:
1. High level language : A language which is completely understandable by human but not by machine is called 
  high level language  - java , c++ , c , python.
2. Mid?Intermediate level : A language which nethier completely understandable by human nor by machine 
  is called as mid level language - Bytecode
3. Low level/Binary/Machine level language : A language which is not understyandable by human 
   but completely understandable by machine 
  ex: 0's and 1's


## compiler 
It a software Which is used to convert high level language into low level language.

## Features of java
1. It is simple as compare to c
2. It is plateform Independent
3. It is secure
4. It has high performance
5. It is an efficient language
6. It supports OPPS
7. It supports multithreding(Multitasking)
8. It is portable
9. It is Robus (Widely Used)
10.   It has a large community support
11. It is strictly typed language 
12. It is case sensative
13. It is architectural neutral language
14. It is secure
15. Highly performance
16. Good memory management because of garbage collector

## Ques : Why java is platform independent language ?

## sourceCode ----> Compiler(JavaC)---->ByteCode(platformIndependent) -----> JVM(pleteformDependent) ----> 1.Windows 2.Mac 3.Linux 

1. java is a two-step compilation based language it means compiler and interpreter both will work.
2. First compiler will work and convert java source code into ByteCode(mid level code).
3. After that JVM will take this bytecode as an input and convert it into the machine code.
4. It means it doent matter from which platform we are getting the byteCode we will get the same output on all the plateform.
5. This is the reason why java is plateform dependent language.

## Why java is secure ?
1. Because it does not support pointer that is  why we cannot get actual location of memory . so we cannot get the access the actual 
address of a memory variable.
2. jvm is responsible to convert bytecode into machine code
3. Before executing the bytecode it will check 
 - whether the bytecode is geberated by the valid compiler or not
 - whether the bytecode is properly structured or not 
 - Whether the bytecode is properly structured or not 
 - if it finds any problem it stops executing the bytecode.

## Why java is high performance ?
 - JVM executes the bytecode line by line 
 - suppose we invoke a function multiple times then - inside jvm we have a component known as JIT compiler will
   directly execute the bytecode into machine code.

## Java souurce file
- A file which contains instructions of java language is known as java source file.
- its extention will be .java

  ______________
## JDK - Java Development Kit 
- It contains all the necessary tools to develop a java program
-  Hierarchy of JDK
- JDK -----> JRE ------> JVM 
- JRE (JAVA RUNTIME ENVIRONMENT)
  1. It provides a run time environment to execute a java program

- JVM 
  1. JAVA VIRTUAL MACHINE 
  2. It is an interpreter which is resposible for execute a java program 

- 3 steps to execute a java program
  1. Create a source file - create source file by using normal text editor notepad , 
  2. We can also use advance code editor vsCode , eclipse , intelligIdea.
  3. To create a source file we just need to create a file by any one the editor and save it by .java extention.
  4. Compile the source file - we need to compile the source file after the successfuly compilation ,
     compiler will generate bytecode file with name .class file 
  5. During the compilation the compiler will check rules and regulation (Syntax and semantics ).
  6. If compiler finds any mistake or error the compiler will throw an error and compiler will not generate .class
     file
  7. Syntax for the compilation
     1. javac source-file Name.java
     2. Ex : javac name.java
  8. Execution the .class file - In this stage we need to give .class file as an input to the
     JVM will execute this and give us output.
  9. syntax for the execution:-
     1. java className
     2. javaSourceFile -----> compilation ---> .classFile ------> JVM -----> output

## # Basic structure of java program.
- First we need to create a file and save it with .java extension
  inside the file we can write our java instruction
- Inside a file we can create a class
  1. class - it is a predefined word 
  2. it must be written in the lowercase 
  3. it is used to create a class block
  4. class Demo {  Class-Block }
  5. file name and class name can be different ... It is not necessary to have same name class and file  
  6. Inside the class we can have the following components
     1. method
     2. variable
     3. constructor 
     4. static Initializer
     5. non static Initializer
     6. class
