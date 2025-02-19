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

---
## Installing Flask
---

## Running Flask server
---

## Summary

