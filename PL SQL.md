## PL in SQL  
** Stored Procedure					** Function  
* call procedurename  			* functionname(arglist)  
* returns 0 or more values	* returns only one value  
* Precompiled								* Not precompiled  
*	Not usable in query				* Usable in query  
* Out parameter							* Can't use out parameter  

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
