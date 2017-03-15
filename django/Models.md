# Models

### Setting up the database

```
# Initialize the Database
> python manage.py migrate

# Create superuser to manage the database - username, email, password
> python manage.py createsuperuser
```

### Changing a model

```
# Register the model changes
> python manage.py makemigrations <AppName>

# Run migrate again
> python manage.py migrate
```

### Viewing the model from the admin interface

```
# Edit admin.py in the app

from django.contrib import admin
from rango.models import Category, Page

admin.site.register(Category)
admin.site.register(Page)
```




