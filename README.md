# How to install Django and create a Django project

## Prerequisite

Make sure you get Python3 and pip3 installed, you can check that via: 

```bash
python3 --version
pip3 --version
```

## Step 1

Create a virtual environment

```bash
python3 -m venv example_venv
```

## Step 2 

Activate this virtual environment

```bash
source example_venv/bin/activate
```

## Step 3

Install Django

```bash
cd example_venv
python -m pip install Django
```

## Check

Meanwhile, you can check the version AND source of python AND version of Django

```bash
python --version
which python
python -m django --version
```

## Step 4 

Make a directory called "src" in the home directory and store the Django project code inside it

```bash
mkdir src
cd src
```

## Step 5

Create a Django project

```bash
django-admin startproject example_django
```

## Step 6

Run your Django project

```bash
python manage.py runserver
```

Then you can start the server at http://127.0.0.1:8000/

# Build a application called 'poll'

## build application within the same directory as manage.py
```bash
python manage.py startapp polls
```

## run migrations for apps in INSTALLED_APPS of settings.py

```bash
python manage.py migrate
```

## Activate application into project
After add poll application into the project(settings.py->INSTALLED_APPS), you need let Django know

```bash
python manage.py makemigrations polls
```

## Create those model tables in your database
The migrate command takes all the migrations that haven’t been applied and runs them against your database - essentially, synchronizing the changes you made to your models with the schema in the database.
```bash
python manage.py migrate
```

## check what sql that migration would run

```bash
python manage.py sqlmigrate polls 0001
```

## three-step guide to making model changes

1. Change your models (in models.py).
2. Run python manage.py makemigrations to create migrations for those changes
3. Run python manage.py migrate to apply those changes to the database.

## Invoke python shell and you can try api via python to create/save/manipulate data object for models

after enter python shell, you can use Django's predefined APIs to interact with database migrated by model
```bash
python manage.py shell
```

## Creating an admin user

```bash
python manage.py createsuperuser
```
Enter your desired username and press enter
```bash
Username: admin
```
You will then be prompted for your desired email address
```bash
Email address: admin@example.com
```
The final step is to enter your password. You will be asked to enter your password twice, the second time as a confirmation of the first
```bash
Password: **********
Password (again): *********
Superuser created successfully.
```