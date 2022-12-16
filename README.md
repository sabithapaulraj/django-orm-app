# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![Screenshot (60)](https://user-images.githubusercontent.com/118343379/207867577-fe26a3c6-45a7-44c2-bd5a-d7dafd8e5ced.png)


>>>>>>> 4ad5f7603170cdcb3ffcc918e291a068e2fe3af3
## DESIGN STEPS

### STEP 1:

Create a new Django project using  "django-admin startproject",get into the project terminal  and use "python3 manage.py startapp" command.
 
### STEP 2:

Define a model for the golf club membership in the models.py.Allow host access and add the app name under installed apps in settings.py

### STEP 3:

Register the models with the Django admin site. In admin.py under app folder,register the models with Django admin site.


### STEP 4:

Run the python manage.py makemigrations and python manage.py migrate commands to create the necessary database tables for the golf club membership model.Run the Server using "python3 manage.py runserver 0:80" command.


## PROGRAM

#IN models.py:-
```
from django.db import models
from django.contrib import admin

# Create your models here.
class GolfClubMember(models.Model):
    member_id = models.CharField(max_length=8,primary_key=True)
    name =models.CharField(max_length=100)
    phone_number = models.IntegerField()
    email = models.EmailField()
    membership_type = models.CharField(max_length=100)
    validity = models.IntegerField()

class GolfClubAdmin(admin.ModelAdmin):
    list_display = ('member_id','name','phone_number','membership_type','validity')
 ```

#IN admin.py:-
```
from django.contrib import admin
from .models import GolfClubMember,GolfClubAdmin

admin.site.register(GolfClubMember,GolfClubAdmin)
```


## OUTPUT

![Screenshot (62)](https://user-images.githubusercontent.com/118343379/208137890-4c11d1d6-35d7-42fd-908e-27b140887060.png)
![Screenshot (63)](https://user-images.githubusercontent.com/118343379/208137977-b1a0c0f4-2f97-46b4-88be-98fbf765a279.png)
![Screenshot (64)](https://user-images.githubusercontent.com/118343379/208138078-302d2d6f-0805-43e4-9a31-bdae14142a07.png)
![Screenshot (65)](https://user-images.githubusercontent.com/118343379/208138134-bfd853ad-48c1-4975-a931-5b857f8c753e.png)
![Screenshot (66)](https://user-images.githubusercontent.com/118343379/208138177-0a0546de-0894-4319-8261-7279687071f3.png)




## RESULT

Successfully developed a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).
