# Ex02 Django ORM Web Application
# Date:23.04.2025
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
admin.py
~~~
from django.contrib import admin
from .models import book,bookadmin
admin.site.register(book,bookadmin)
~~~

models.py
~~~
from django.db import models
from django.contrib import admin
class book(models.Model):
    Book_name=models.CharField(max_length=100)
    Author=models.CharField(max_length=100)
    Co_author=models.CharField(max_length=100)
    Book_code=models.IntegerField()
    Publisher=models.CharField(max_length=100)
    MRP=models.IntegerField()
class bookadmin(admin.ModelAdmin):
    list_display=("Book_name","Author","Co_author","Book_code","Publisher","MRP")
~~~

urls.pr
~~~
from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),
]
~~~
# OUTPUT
![image](https://github.com/user-attachments/assets/3bfb222b-5855-4269-ad47-ef032dc66b54)

![image](https://github.com/user-attachments/assets/7290b2d8-48bf-408c-9336-f2abe6e3c3ee)


![image](https://github.com/user-attachments/assets/feaca524-3c58-47e9-a28f-6254dfd0bd3b)


# RESULT
Thus the program for creating a database using ORM hass been executed successfully
