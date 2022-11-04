**To create virtual env:**
```python
python -m venv “NAME_OF_ENVIROMENT”
```

**To deactivate virtual env:**
```python
deactivate
```

**Generate absolute path to folder**
```python
os.path.expanduser("~/Library/Mail/")
```

**Change execution directory**
```python
os.chdir(PATH_TO_DIRECTORY)
```
**Find folder or file in current directory with part name**
**Returns array**
```python
glob.glob(PART_NAME_STRING)
```