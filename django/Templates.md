# Templates

- A template sets up the structure for a web page

- Create a templates folder in the app folder and add a folder for each app that needs a template
- Create variable with relative path for the templates folder in settings.py
    - TEMPLATE_DIR = os.path.join(BASE_DIR, 'templates')
- Update settings.py with templates location 
    - 'DIRS': [TEMPLATE_DIR, ],
    
### Template inheritance

- Create a template called `base.html` containing stuff to repeat on each page

### Template Tags
   
- `{% extends "ll_app/base.html" %}` - Used by child to specify file to inherit from
- `{% url 'll_app:index' %}` - URL in specified urls.py file
- `{% block content %}{% endblock content %}` - Block to be defined by child, does not have to define each

