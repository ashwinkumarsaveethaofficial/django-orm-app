# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![Table](https://user-images.githubusercontent.com/120731469/210124041-bc3a6584-ba24-4988-9a7d-27584c4e1225.jpeg)


## DESIGN STEPS

### STEP 1:
Create a Django app Go to the app directory In models.py create two classes And
save the models.py
### STEP 2:
Go to admins.py And put the two class in admins.py from the models.py And save
the ﬁle
### STEP 3:
Start the Django server Then move to admin page
## PROGRAM
```python
from django.db import models
from django.contrib import admin

class Employee (models.Model):
    unique_number=models.CharField(max_length=20,primary_key=True)
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    job=models.CharField(max_length=100)

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('unique_number','name','age','email','job')
```
```
### File: Admin.py
python
from django.contrib import admin
from .models import Employee,EmployeeAdmin

admin.site.register(Employee,EmployeeAdmin)
```

## OUTPUT
![1st](https://user-images.githubusercontent.com/120731469/210124049-34927acc-820a-4856-a94e-5cf31a0035d7.png)

### Primary Key Verification
![primary](https://user-images.githubusercontent.com/120731469/210124064-655f8bf8-88e3-44d1-bd6c-820525000b87.png)


## RESULT
The result for orm is successful.
