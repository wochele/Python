# Admin

## Setting up the admin site

'''python
# Create superuser
> python manage.py createsuperuser

# Update admin.py
from <AppName>.models import <ModelName>

admin.site.register(<ModelName>)
'''



