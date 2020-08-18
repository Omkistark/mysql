## PL in SQL  
* * * Stored Procedure ***  
call procedurename  
returns 0 or more values   
Precompiled  						 
Not usable in query  
Out parameter  
* * * Fuction    
functionname(arglist)  
returns only one value  
Not precompiled  
Usable in query  
Can't use out parameter  
  
####  Procedures:  
DELIMITER //
CREATE PROCEDURE procedure_name(IN argument datatype,..,OUT parameter_name datatype)
BEGIN  
DECLARE variable_name datatype DEFAULT defaultvalue
-- Any query  
-- To use OUT use 'INTO'  i.e SELECT column_name INTO parameter_name from table_name ...  
END //  
DELIMITER ;  
  
CALL procedure_name(col1,@something);  
SELECT @something;
  
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

#### Functions:  
