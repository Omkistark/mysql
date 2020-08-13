# DML:  
* * * Note: Contents within '[' and ']' are optional  
  
### 1>SELECT  
SELECT [DISTINCT/ALL(default)] */column_name1/column_epression1 [[AS] alias_name] , ...  
FROM table_name [alias] , ...  
[WHERE condition ]  
[GROUP BY column_name_1,column_name2,...]  
[HAVING condtion]  
[ORDER BY column_name_1,column_name2,... [ASC(default)/DESC]] ;  

  
#### Common expressions:  
LENGTH(string)  
STRCMP(string1,string2)  
CURDATE()  
DAY(date)  
DAYNAMEE(date)  
MONTH(date)  
YEAR(date)  
DATEDIFF(date1,date2)  
* * The HAVING clause is used in the SELECT statement to specify filter conditions for a group of rows or aggregates. The HAVING clause is often used with the GROUP BY clause to filter groups based on a specified condition. If the GROUP BY clause is omitted, the HAVING clause behaves like the WHERE clause.  
#### Common Conditions (WHERE)
1. Comparison (Works with check too!): =,<,>,<=,>=,<>  
2.Range: BETWEEN, NOT BETWEEN  
3.null: IS NULL, IS NOT NULL  
4.Membership: IN (), NOT IN ()  
5.Pattern Matching: LIKE '', NOT LIKE ''  
        -> '' contains _ , % , specifically mentioned characters  
        -> _ Indicates any alphanumeric value  
        -> % Indicates zero or more alphanumeric values  
  
#### Aggregate functions :  
MIN(), MAX(), SUM(), AVG(), COUNT()  

#### 1a>Cartesian product first step in join internally  
SELECT var1.colname1,var2.colname2 FROM tablename1 var1,tablename2 var2;  

#### 1b>Inner/Equi/Simple Join (Gives matching rows based on condition)  
condition denotes any expression like comparison.  
SELECT colname1,colname2 ... FROM tablename1 INNER JOIN tablename2 ON condition;  
SELECT colname1,colname2 ... FROM tablename1, tablename2 WHERE condition;  
  
SELECT column1,column2.column3,... 
FROM ((table-name1 INNER JOIN table-name2 ON condition1)
INNER JOIN table-name3 ON condition2);  

#### 1c>Left Outer Join (Gives matching rows and non matching rows from on leftside) 
SELECT column_name1,column_name2, ... FROM table_name1 LEFT JOIN table_name2 ON condition;  

#### 1d>Right Outer Join (Gives matching rows and non matching rows from on rightside)  
SELECT column_name1,column_name2, ... FROM table_name1 RIGHT JOIN table_name2 ON condition;  

#### 1e>Self Join (Useful in case of unary relation)  
SELECT obj1.column_name1 [AS Alias1],  
       obj2.column_name2 [As Alias2]  
FROM table_name1 obj1 INNER/LEFT/RIGHT JOIN table_name1 obj2 ON condition;   
  

### 2>INSERT INTO  
Not all column values :  
INSERT INTO table_name (column_name_1,column_name_2, ...)
VALUES (value-corresponding-to-col-1,value-corresponding-to-col-2, ...);
  
All column values:  
INSERT INTO table_name VALUES (value1,value2, ...);  

### 3>UPDATE  
UPDATE table_name SET column_name [WHERE condition];  

### 4>DELETE FROM  
DELETE FROM table_name [WHERE condition];
  
