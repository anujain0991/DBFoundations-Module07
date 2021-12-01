# Name: Anu Jain
# Date: 11/30/2021
# Course: IT Foundation of Database Management
# Assignment No.: 7
# GitHub URL: https://github.com/anujain0991/DBFoundations-Module07/

# SQL UDF

# 1.	Explain when you would use a SQL UDF
A user-defined function (UDF) in SQL Server is a programming construct that accepts parameters, does work that typically makes use of the accepted parameters, and returns a type of result.  The result either is a scalar value or result set.

UDFs support modular programming. Once you create a UDF and store it in a database then you can call it any number of times. You can modify the UDF independent of the source code.

UDF can be used in a select, where, or case statement. They can also be used to create Joins.
User-defined functions allow programmers to create their own routines and procedures that the computer can follow; it is the basic building block of any program and also very important for modularity and code reuse since a programmer could create a user-defined function which does a specific process and simply call it every time it is needed. 

There are 2 types of UDFs:
a.	Scalar functions 
b.	Table Valued Functions
- Inline Table valued function
- Multi Statement Table valued function


# 2.	Explain are the differences between scalar, Inline and Multi Statement function.

•	Scalar Valued function 
It accepts zero or more parameters and return a single value. The return type of a scalar function is any data type except text, ntext, image, cursor and timestamp. Scalar functions can be use in a WHERE clause of the SQL Query.
(Source: https://www.c-sharpcorner.com/UploadFile/3194c4/user-defined-functions-in-sql-server/ )


Create Scalar function:

CREATE Function 
RETURNS 
As
Begin
Return
Select  
FROM table_name
WHERE condition;
End

•	Inline table Values function 
It contains a single statement that must be a SELECT statement. The result of the query becomes the return value of the function. There is no need for a BEGIN-END block in an Inline function. It return a table variable.
(Source: https://www.c-sharpcorner.com/UploadFile/3194c4/user-defined-functions-in-sql-server/ )

CREATE Function 
RETURNS Table 
As
Return
Select  
FROM table_name
WHERE condition;


•	Multi Statement Table Valued Function
 A Multi-Statement contains multiple SQL statements enclosed in BEGIN-END blocks. In the function body you can read data from databases and do some operations. In a Multi-Statement Table valued function the return value is declared as a table variable and includes the full structure of the table to be returned. The RETURN statement is without a value and the declared table variable is returned. 
(Source: https://www.c-sharpcorner.com/UploadFile/3194c4/user-defined-functions-in-sql-server/ )

Summary:

In this document, we’ve discussed about SQL UDF and its types.
