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