## PL in SQL  
* * * Stored Procedure ***  
call procedurename  
returns 0 or more values   
Precompiled  						 
Not usable in query  
Out parameter    
  
####  Procedures + Cursors + Exception Handeling:  
DELIMITER //  
CREATE PROCEDURE procedure_name(IN argument datatype,..,OUT parameter_name datatype)  
BEGIN  
DECLARE variable_name datatype [DEFAULT defaultvalue]   
.
.
.
DECLARE c1 CURSOR FOR SELECT 

-- Any query  
-- To use OUT use 'INTO'  i.e SELECT column_name INTO parameter_name from table_name ...  
END //  
DELIMITER ;  
  
CALL procedure_name(in_arg1,in_arg2, ... ,@outarg1,@outarg2, ...);  
SELECT @outarg1,@outarg2,.... ;  
  
  

* * * Fuction ***  
functionname(arglist)  
returns only one value  
Not precompiled  
Usable in query  
Can't use out parameter  
#### Functions Syntax:  
DELIMITER //
CREATE FUNCTION functionname (parameter1 datatype1,...) returns datatype DETERMINISTIC  
BEGIN  
DECLARE ..  
-- Loops,cnditions blah blah  
-- Select into statements  
RETURN datatype;  
END//  

SELECT functionname(arglist) FROM tablename;  
  
  
##### Conditional statements  
IF condition THEN SET var=value;  
ELSE IF condition THEN SET var=value;  
.  
.  
.  
ELSE  SET something;  
END IF;  

  
CASE varname  
WHEN value1 THEN  
	SET var=somevalue;  
WHEN value2 THEN  
	SET var=somevalue;
WHEN value3 THEN  
	SET var=somevalue;  
ELSE 
	SET var=someval;
END CASE;  

WHILE condition DO  
SET assignment  
END WHILE  

