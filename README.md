# Ex02 Django ORM Web Application
## Date: 25-09-2024
## Name: Roseline B

## AIM
To develop a Django application to store and retrieve data from a Bank database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![image](https://github.com/user-attachments/assets/4c0876f3-435b-4c90-8bcd-e45f456fcf34)


## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 customers.

## PROGRAM
```
admin.py

from django.contrib import admin

# Register your models here.
from .models import bankloan,bankloanAdmin
admin.site.register(bankloan,bankloanAdmin)
```
```
models.py

from django.db import models

# Create your models here.
from django.contrib import admin
class bankloan(models.Model):
    accno=models.IntegerField(primary_key=True);
    name=models.CharField(max_length=100);
    loanamt=models.IntegerField();
    loanlimit=models.IntegerField();
    phoneno=models.IntegerField();

class bankloanAdmin(admin.ModelAdmin):
    list_display=('accno','name','loanamt','loanlimit','phoneno')
```

## OUTPUT
![image](https://github.com/user-attachments/assets/b015d139-d919-48c8-8893-6b367b21c362)



## RESULT
Thus the program for creating a database using ORM hass been executed successfully
