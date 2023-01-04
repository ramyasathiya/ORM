# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![Entity Relationship Diagram](./er.png)

## DESIGN STEPS

### STEP 1:
Clone the GitHub repository into Theia IDE

### STEP 2:
Create a new app

### STEP 3:
Write programs for models.py and admin.py and migrate them into myapp

### STEP 4:
Create an Employee database.

## PROGRAM
```
admin.py

from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)

models.py

from django.db import models
from django.contrib import admin
class Employee(models.Model):
    eid=models.CharField(primary_key="eid",max_length=20,help_text="Employee ID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')
```

## OUTPUT
![OUTPUT](./out.png)

## RESULT
The program for implementing Django ORM web Application has been executed successfully