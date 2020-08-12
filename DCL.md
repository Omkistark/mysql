# DCL
### GRANT:  
GRANt privilege_type [(column_list)] [, priv_type [(column_list)]] ...  
    ON [object_type] priv_level  
    TO user [auth_option] [, user [auth_option]] ...  
    [REQUIRE {NONE | tls_option [[AND] tls_option] ...}]  
    [WITH {GRANT OPTION | resource_option} ...];  
    
GRANT privilege ON objects/'*' TO 'username'@'localhost';  

for checking, use:  
SHOW GRANTS FOR finley localhost];  

### REVOKE:  
REVOKE priv_type [(column_list)]  
      [, priv_type [(column_list)]] ...  
    ON [object_type] privilege_level  
    FROM user [, user] ... 
