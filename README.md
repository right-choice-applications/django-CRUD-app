# django-CRUD-app
CRUD application written in python and django. This application is connected to MySQL database. With this application we can perform all CRUD methods on the employee table of MySQL.


After importing the project folder into PyCharm, Use the terminal to enter following command. Make sure you are in the same folder where manage.py file exist.

STEP-1: DjangoProject\adithyadjango>python manage.py runserver
STEP-2: Visit http://127.0.0.1:8000/show
It will display CRUD Application.

Prerequisites:
Requirements for creating a Django application
1. PyCharm
2. Xampp (For working with any database related projects)
3. PYTHON installed
4. PIP installed
   PIP : A package management system used to install and manage software packages written in Python.
   PIP installs packages
   PIP is already installed in python environment

How to verify PIP installed or not?
  CMD:  Pip --version
How to upgrade PIP version
  CMD:  Python -m pip install --upgrade pip

Django Installation from pycharm.
Django requires pip to start installation. For Python 3.4 and higher versions pip3 is used to manage packages.
Django can be installed either from pycharm terminal or command prompt.

How to install Django
  Type “pip install django” in cmd

How to check or verify Django Version or installation
  Type “Django-admin version” in cmd

Django Project Directory setup using Pycharm 
  1. Open pycharm and click on create new project
  2. In pycharm local terminal type the following command
      django-admin startproject myprojectname
This command will the following packages and files. The outer directory is just a container for the application. We can rename it further.
 a. manage.py: It is a command-line utility which allows us to interact with the project in various ways and also used to manage an application that we will see later on in this tutorial.
b. __init__.py: It is an empty file that tells to the Python that this directory should be considered as a Python package.
c. settings.py: This file is used to configure application settings such as database connection, static files linking etc.
d. urls.py: This file contains the listed URLs of the application. In this file, we can mention the URLs and corresponding actions to perform the task and display the view.
e. wsgi.py: It is an entry-point for WSGI-compatible web servers to serve Django project.
	Initially, this project folder is a default draft which contains all the required files and folders for creating a django application.

Creating django Application directory.
Type the following command in the terminal
    CMD: python manage.py startapp mywebappname
A directory (mywebappname) will be created, and it is the actual application package name which we'll need to use to import module inside the application.
NOTE: To create mywebapp make sure you are in the directory of your project. Only when terminal can use “manage.py” file to create the webapp. Else displays an error saying manage.py file is not found.

Running the django project
Django project has a built-in development server which is used to run application instantly without any external web server and can be accessed at localhost with port 8000. It means we don't need of Apache or another web server to run the application in development mode.
To run the application, we can use the following command
  CMD: python manage.py runserver

Django Virtual environment setup
The virtual environment is an environment which is used by Django to execute an application. It is recommended to create and execute a Django application in a separate environment.
Python provides a tool virtualenv to create an isolated Python environment. We will use this tool to create a virtual environment for our Django application.
How to install virtual environment in windows, type in cmd
		Virtualenv env
How to activate virtual environment, type in cmd
project folder source\projectname\venv\Scripts\activate
OUTPUT:
(venv)    C:\Users\PUBLIC.ADITHYAPC\PycharmProjects\BharathDjango\bharathpython>

After completing the directory structure and Virtual environment, now we can work on the development of django crud application.

Creating CRUD Application in Django
Create a database djangodb in mysql, and configure into the settings.py file of django project. (myprojectname)
Using the link following from settings.py file https://docs.djangoproject.com/en/2.2/ref/settings/#databases
We can connect to other database backends, such as MySQL, Oracle, or PostgreSQL and some additional connection parameters will be required as below.
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'djangoproject',
        'USER': 'admin',
        'PASSWORD': 'rightchoice',
        'HOST': '127.0.0.1',
        'PORT': '3306',
    }
}
Note: Create a database with name “djangoproject” in mysql, with username  “admin” and password ”rightchoice”.

