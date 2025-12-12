# Ex04 Places Around Me
# Date:9-12-2025
# AIM
To develop a website to display details about the places around my house.

# DESIGN STEPS
## STEP 1
Create a Django admin interface.

## STEP 2
Download your city map from Google.

## STEP 3
Using <map> tag name the map.

## STEP 4
Create clickable regions in the image using <area> tag.

## STEP 5
Write HTML programs for all the regions identified.

## STEP 6
Execute the programs and publish them.

# CODE
```
map.html

{% load static %}
<html>
    <head>
        <title>NISHANTH JAYAKUMAR</title>
         
    </head>
    <body>
        <center><h1>NISHANTH JAYAKUMAR (25015083)</h1>
<img src="{% static 'map.png' %}" usemap="#image-map"></center>

<map name="image-map">
            <area alt="CINEMAS" title="RAKKI CINEMAS" href="cine.html" coords="1182,351,880,175" shape="rect">
            <area alt="HOSPITAL" title="SIR IVAN STEDFORD HOSPITAL" href="hospital.html" coords="892,173,506,2" shape="rect">
            <area alt="ACADEMY" title="DOLPHIN SPORTS ACADEMY" href="sports.html" coords="691,478,524,319" shape="rect">
            <area alt="RESTARAUNT" title="SS HYDERABAD BIRIYANI" href="rest.html" coords="1178,619,1501,774" shape="rect">
            </map>
        
        
    </body>
</html>
```
```
cine.html 

{% load static %}
<html>
    <head>
        <title>RAKKI CINEMAS</title>
    </head>
    <body bgcolor="purple">
        
       <center>
        <img src="{% static 'rakki.jpeg' %}" width="70%" height="50%">
        <h1>RAKKI CINEMAS</h1></center>
        <h4>Rakki Cinemas is a prominent entertainment destination with multiple screens across the Chennai region. It is a proprietorship owned by Hari Govind and is known for its modern cinematic experience, including 4K projection and Dolby Atmos sound, as well as a new EPIQ screen at its latest location.</h4>
      
    </body>
</html>
```
```
hospital.html

{% load static %}
<html>
    <head>
        <title>SIR IVAN STEDFORD HOSPITAL</title>
    </head>
    <body bgcolor="purple">
        
       <center>
        <img src="{% static 'stedford.jpeg' %}" width="70%" height="50%">
        <h1>SIR IVAN STEDFORD HOSPITAL</h1></center>
        <h4>Sir Ivan Stedeford Hospital, often referred to locally as Stedford Hospital, is a multi-speciality charitable hospital located in Ambattur, Chennai. It provides high-quality healthcare at subsidized rates and is managed by the AMM Foundation, the philanthropic arm of the Murugappa Group. </h4>
      
    </body>
</html>
```
```
rest.html
{% load static %}
<html>
    <head>
        <title>SS BIRIYANI</title>
    </head>
    <body bgcolor="purple">
        
       <center>
        <img src="{% static 'ssbiriyani.webp' %}" width="70%" height="50%">
        <h1>SS BIRIYANI</h1></center>
        <h4>SS Hyderabad Biryani is a very popular restaurant chain in the Chennai area, known for its flavorful, Chennai-influenced Hyderabadi-style biryani.  </h4>
      
    </body>
</html>
```
```
{% load static %}
<html>
    <head>
        <title>DOLPHIN SPORTS ACADEMY</title>
    </head>
    <body bgcolor="purple">
        
       <center>
        <img src="{% static 'dolphin.webp' %}" width="70%" height="50%">
        <h1>DOLPHIN SPORTS ACADEMY</h1></center>
        <h4>Dolphin Sports Academy has several locations in the Chennai area, with prominent facilities in Ambattur and Avadi. They offer coaching and facilities for a wide range of sports.   </h4>
      
    </body>
</html>
```
```
views.py

from django.shortcuts import render,HttpResponse
def fun(request):
    return render(request,'map.html')
def cine(request):
    return render(request,'cine.html')
def hospital(request):
    return render(request,'hospital.html')
def rest(request):
    return render(request,'rest.html')
def sports(request):
    return render(request,'sports.html')
```
```
urls.py
from django.contrib import admin
from django.urls import path
from book import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.fun),
    path('cine',views.cine),
    path('hospital',views.hospital),
    path('rest',views.rest),
    path('sports',views.sports), 
]
```
# OUTPUT
![alt text](<Screenshot 2025-12-12 120100.png>)
![alt text](<Screenshot 2025-12-12 115855.png>)
![alt text](<Screenshot 2025-12-12 115912.png>)
![alt text](<Screenshot 2025-12-12 120025.png>)
![alt text](<Screenshot 2025-12-12 115952.png>)

# RESULT
The program for implementing image maps using HTML is executed successfully.
