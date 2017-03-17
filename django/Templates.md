# Templates
- Create a templates folder in the main project folder and add a folder for each app that needs a template
- Create variable with relative path for the templates folder
    - TEMPLATE_DIR = os.path.join(BASE_DIR, 'templates')
- Update settings.py with templates location 
    - 'DIRS': [TEMPLATE_DIR, ],
    
    
