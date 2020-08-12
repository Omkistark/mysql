# DDL:  
### Commonly used data types  
int  
decimal  
numeric  
float  
date  
datetime  
char  
varchar(limit)  
  
### 1>	CREATE:  
CREATE DATABASE database_name;  
CREATE TABLE table_name(column1 datatype1 constraints, column2 datatype2 constraints ...);  
Duplicate a table:  CREATE TABLE newtablename AS SELECT * FROM original_table;  
Create a new User:  CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';  
  
Constraints for a database:  
-PRIMARY KEY  
-FOREIGN KEY  
-NOT NULL  
-CHECK  
-DEFAULT  
-UNIQUE  
  
### 2> DROP:  
DROP DATABASE database_name;  
DROP TABLE table_name;  
  
### 3>ALTER:  
ADD column/columns:  
ALTER TABLE table_name ADD column_name datatype;  
ALTER TABLE table_name ADD column_name1 datatype1 constraints, ADD column_name2 datatype2 constraints... ;  

Add constraints:  
PRIMARY KEY:  
ALTER TABLE table_name ADD CONSTRAINT indexname PRIMARY KEY (columnn_name1,columnn_name2);    
FOREIGN KEY:  
ALTER TABLE table_name ADD FOREIGN KEY (column_name) REFERENCES referenced_table_name(referenced_column_name);    
FOREIGN KEY:  
ALTER TABLE table_name ADD CONSTRAINT indexname FOREIGN KEY (column_name) REFERENCES referenced_table_name(referenced_column_name);    
NOT NULL:  
ALTER TABLE table_name MODIFY column_name datatype NOT NULL;  
UNIQUE:  
ALTER TABLE table_name ADD UNIQUE (column_name1,column_name2 ...);  
UNIQUE:  
ALTER TABLE table_name ADD CONSTRAINT indexname UNIQUE (column_name1,column_name2 ...);  
DEFAULT:  
ALTER TABLE tablename ALTER column_name SET DEFAULT value;  

Remove constraints:  
PRIMARY KEY:  
ALTER TABLE table_name DROP PRIMARY KEY;  
FOREIGN KEY:  
ALTER TABLE Orders DROP FOREIGN KEY indexname;  
NOT NULL:  
ALTER TABLE table_name MODIFY column_name datatype new_constraints;
UNIQUE:  
ALTER TABLE table_name DROP INDEX indexname;  
DEFAULT:  
ALTER TABLE table_name ALTER column_name DROP DEFAULT;  

Drop column:  
ALTER TABLE table_name DROP COLUMN column_name;  

Modify Definition:   
ALTER TABLE table_name MODIFY column_name datatype CONSTRAINTS [ FIRST / AFTER column_name];  

Rename:  
ALTER TABLE old_table_name RENAME new_table_name;  
  
### 4>TRUNCATE:  
TRUNCATE TABLE table_name;  
