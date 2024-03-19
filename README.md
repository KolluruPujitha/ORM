# Ex02 Django ORM Web Application
## Date:18-03-2024 

## AIM
To develop a Django application to store and retrieve data from a Railway database using Object Relational Mapping(ORM).

## Entity Relationship Diagram



![WhatsApp Image 2024-03-18 at 18 59 50_2a725946](https://github.com/KolluruPujitha/ORM/assets/150231340/2c636500-afa3-4fbe-8466-ef061a09a856)


## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 Railways

## PROGRAM
```
models.py

from django.db import models
from django.contrib import admin

# Create your models here.
class Railway(models.Model):
    train_no = models.IntegerField(primary_key=True)
    train_name = models.CharField(max_length=50)
    start_date = models.DateTimeField()
    end_date = models.DateTimeField()
    start_station_code = models.CharField(max_length=10)
    end_station_code = models.CharField(max_length=10)

class RailwayAdmin(admin.ModelAdmin):
    list_display = ('train_no', 'train_name', 'start_date', 'end_date', 'start_station_code', 'end_station_code')


admin.py

from django.contrib import admin
from .models import Railway, RailwayAdmin
# Register your models here.
admin.site.register(Railway, RailwayAdmin)

```
## OUTPUT

![Screenshot 2024-03-15 141326](https://github.com/KolluruPujitha/ORM/assets/150231340/4a90ea97-6317-4cb7-b6e3-17d6d02e6579)



## RESULT
Thus the program for creating a database using ORM hass been executed successfully
