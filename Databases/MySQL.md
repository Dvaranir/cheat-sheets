## Enter MySQL
```bash
mysql -u 'username' -p 'password if needed'
```
## Show connection settings
```mysql
SHOW variables like "%character%";
SHOW variables like "%collation%";
```
## Set proper connection settings
```mysql
SET character_set_client = 'utf8mb4';
SET character_set_connection = 'utf8mb4';
SET character_set_results = 'utf8mb4';
SET collation_connection = 'utf8mb4_unicode_ci';
```