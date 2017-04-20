# Forms

https://docs.djangoproject.com/en/dev/topics/forms/#form-objects

GET requests - Only read data from the server
POST requests - Usually info submitted through a form

### Model Forms

Any page that lets a user enter and submit information on a web page is a form, even if it doesn’t look like one.

The simplest way to build a form in Django is to use a ModelForm, which uses the information from the models we 
defined in Chapter 18 to auto-matically build a form

forms.py
```python
from django import forms

from .models import Topic, Entry

class TopicForm(forms.ModelForm):
    class Meta:
        model = Topic
        fields = ['text']
        labels = {'text': ''}

class EntryForm(forms.ModelForm):
    class Meta:
        model = Entry
        fields = ['text']
        labels = {'text': ''}
        widgets = {'text': forms.Textarea(attrs={'cols': 80})}
```       
 ### Regular forms
 
 
