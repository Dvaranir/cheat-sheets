**To create new blank model:**
```python
python manage.py startapp “Model name”
```

**To install model in project you need to add model into settings.py INSTALLED_APPS list**

**To add model in admin panel:**

1) You need to import it in admin.py

2) admin.site.register(“IMPORTED_MODEL_NAME”)

**To generate migrations from models:**
```python
python manage.py makemigrations
```

**To insert migrations in db:**
```python
python manage.py migrate
```

**To display field model name in db:**
```python
def __str__(self):
        return self.”MODEL_FIELD”
```