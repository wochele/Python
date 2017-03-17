# Creating an app

Content from [HERE](https://docs.djangoproject.com/en/1.10/intro/tutorial01/)

```
# create app right next to manage.py file so that it can be imported as its own 
#   top-level module, rather than a submodule of mysite
> python manage.py startapp <AppName>

# In settings.py for the project, add the app to the INSTALLED_APPS tuple
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    '<AppName>',
]

# Start project web server and verify no errors

# In project urls.py, add a mapping to the app

# In your app’s directory, create a urls.py file to direct incoming URL strings to views.

# In your app’s views.py, create the required views ensuring that they return a HttpResponseobject or render.
```

