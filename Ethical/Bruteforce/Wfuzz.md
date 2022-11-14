### Standart query
```bash
wfuzz -c -z file,PATH_TO_FILE -d *REQUEST* URL
```
### Example
```bash
wfuzz -c -z file,/usr/share/wordlists/wfuzz/Injections/SQL.txt -d *username=1&password=FUZZ* 10.115.97.129/index.php
```
