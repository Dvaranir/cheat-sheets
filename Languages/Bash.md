## Find all files and folders that are not containing "STRING" in name and print it
```bash
find . ! -name "*STRING*" -print
```
## Clean all files except some
```bash
#! /bin/bash
shopt -s extglob
rm -v !("FILENAME_TO_KEEP"|".gitignore")
```

