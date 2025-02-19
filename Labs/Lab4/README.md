# Lab 4
## Django and Flask
### Instructions: 
- Go to the GitHub repository and review lesson 4.
- Install Django & Django REST framework. Use the default database (SQLite).
- Start Django project "stevens," run server, and view app.
- Start Django REST project "mycpu," run server, and view app.
- Install Flask if no module named 'flask'
- Run Flask server via hello_world.py and view app
- Document results to your GitHub repository

--- 
## Installing Django & Django REST framework
The following commands were executed in my terminal to install Django and Django REST framework: 
- `pip3 install -U setuptools` 
- `pip3 install -U django`
- `pip3 install -U djangorestframework`
- `pip3 install -U django-filter`
- `pip3 install -U markdown`
- `pip3 install -U requests`
![Django and Django REST terminal installation 1](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/lab4installD1.png)
![Django and Django REST terminal installation 2](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/lab4installD2.png)

---
## Starting Django project
I started a Django project named "stevens" by executing the following command in my terminal:
`django-admin startproject stevens`
![Django project start in terminal](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/lab4projectStevens.png)

Then, I started a Django app called myapp by executing the following command:
`python3 manage.py startapp myapp`
![Django app start in terminal](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/lab4makeApp.png)
After starting the app I used `python3 manage.py migrate` to migrate the database. This ensured SQLite was set up properly for my project

Next, I edited settings.py in ~/stevens/stevens to add an asterisk to ALLOWED_HOSTS and 'myapp' to INSTALLED_APPS. I did this by using: `nano settings.py`
![Django settings.py edit in terminal](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/usednanotoeditsettings.png)

Then I copied files from the GitHub lesson4/stevens repository. 
1. I copied urls.py to ~/stevens/stevens by:
- `cp ~/iot/lesson4/stevens/urls.py .`
3. I copied admin.py, models.py, and views.py to ~/stevens/myapp by:
- `cp ~/iot/lesson4/stevens/admin.py .`, 
- `cp ~/iot/lesson4/stevens/models.py .`
- `cp ~/iot/lesson4/stevens/views.py .`
4. I copied index.html by:
 - `mkdir static templates`
- `cd templates`
- `mkdir myapp`
- `cd myapp`
- `cp ~/iot/lesson4/stevens/index.html .`
![Django file copies](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/cpslab4.png)

Next, I enabled google maps API. To do this, I obtained an API key from the google cloud console and replaced "YOUR_API_KEY" in index.html with the API key. This was done using: `nano index.html`
![API in index.html](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/APIchangeinindex.png)

Then I copied static files from the GitHub repository:
- `cp ~/iot/lesson4/static/favicon.ico .`
- `mkdir myapp`
- `cd myapp`
- `cp ~/iot/lesson4/static/*css .`
- `cp ~/iot/lesson4/static/*js .`
![static files copying](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/lab4cpsset2.png)

Before running the server I ran the commands `python3 manage.py makemigrations myapp` and `python3 manage.py migrate` to update the database

Then I ran the Django server with `python3 manage.py runserver`
![django server](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/djangoserverruncode.png)

While the server was running, I went to http://127.0.0.1:8000/admin, and logged in with my admin credentials. I added in data regarding date/time, temperature, longitude, and latitude and clicked save.
Then I visited the Django app by going to http://127.0.0.1:8000.

The app is shown below: 
![django app](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/IMG_9879.jpg)


---
## Starting Django REST project
I started a Django project named "stevens" by executing the following command in my terminal:
`django-admin startproject stevens`
Then, I started a Django app called myapp by executing the following command:
`python3 manage.py startapp myapp`
Next, I edited settings.py in ~/mycpu/myvpu to add an asterisk to ALLOWED_HOSTS and add 'myapp'& 'rest_framework' to INSTALLED_APPS. I did this by using: `nano settings.py`
Then I copied some necessary files:
I copied urls.py to ~/mycpu/mycpu by doing: `cp ~/iot/lesson4/mycpu/urls.py .`
I copied admin.py, models.py, views.py, & serializers.py to ~/mycpu/myapp by doing the following commands:
- `cp ~/iot/lesson4/mycpu/admin.py .`
- `cp ~/iot/lesson4/mycpu/models.py .`
- `cp ~/iot/lesson4/mycpu/views.py .`
- `cp ~/iot/lesson4/mycpu/serializers.py .` </br>
Once these files were copied I changed the default password 'admin' in views.py with `nano views.py`. Then I copied index.html by executing the following commands:
- `mkdir static templates`
- `cd templates`
- `mkdir myapp`
- `cd myapp`
- `cp ~/iot/lesson4/mycpu/index.html .` </br>
After index.html was copied. I edited the file to add a Google Maps API key using `nano index.html`
Next I copied static files by executing the following commands in the static directory:
- `cp ~/iot/lesson4/static/*css .`
- `cp ~/iot/lesson4/static/*js .` </br>
Then I changed directories to mycpu and copied controller.py by using the command: `cp ~/iot/lesson4/mycpu/controller.py .`. Again, I changed the default password 'admin' in controller.py by using `nano controller.py`.

Before running the server I executed the following commands to help the server and database be properly configured:
- `pip3 install -U psutil`
- `python3 manage.py makemigrations myapp`
- `python3 manage.py migrate`
- `python3 manage.py createsuperuser` </br>

Then I ran the Django server by executing: `python3 manage.py runserver`. Initially I went to  http://127.0.0.1:8000/admin and logged in with my Django administration username and password. On this website I added in location data for Stevens. Then, in HTML form, I posted 2024 to the DT List at http://127.0.0.1:8000/dt, 20 to the Cpu list at http://127.0.0.1:8000/cpu, and 20 to the Mem List at http://127.0.0.1:8000/mem. After doing all of this, in a seperate terminal window I ran controller.py in the mycpu directory with `python3 controller.py`. With this and the Django server still running, I viewed the app at  http://127.0.0.1:8000/home. </br>

The app looked like this: 
![mycpu Django app](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/cpulab4.jpg)

Below are screenshots that show my steps taken in the terminal: 
![terminal steps 1](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/RESTuptomigrations.png)
![terminal steps 2](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/RESTuptoserverrun.png)
![terminal controller step](https://github.com/ardensentak/CPE322/blob/main/Labs/Lab4/lab4images/controllerlab4.png)

---
## Installing Flask
---

## Running Flask server
---

## Summary

