How to install Django and create a Django project

(Prerequisite) make sure you get Python3 and pip3 installed, you can check that via: 
$ python3 --version
$ pip3 --version

(Step 1) create a virtual environment
$ python3 -m venv example_venv

(Step 2) activate this virtual environment
$ source example_venv/bin/activate

(Step 3) install Django
$ cd example_venv
$ python -m pip install Django

Meanwhile, you can check the version AND source of python AND version of Django
$ python --version
$ which python
$ python -m django --version

(Step 4) make a directory called "src" in the home directory and store the Django project code inside it
$ mkdir src
$ cd src

(Step 5) create a Django project
$ django-admin startproject example_django
