# django getting started

[Writing first django project](https://docs.djangoproject.com/en/1.10/intro/tutorial01/)

Install python version 3.5.3 (latest that works with Django)

### Install Virtualenv

```
pip install virtualenv
```

### Create virtual env

```
virtualenv <sitename>
```

### Activate the environment

```
env_mysite\scripts\activate
```

### Install django

```
pip install django

# Verify install
django-admin --version

# If not working on Windows 10, perform the following updates on the main install
python -m pip install -U pip setuptools virtualenv
```

### Create a project

change to folder where the project will be

```
django-admin startproject mysite
```

### Create database table

```
python manage.py migrate 
```



