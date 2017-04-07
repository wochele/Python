# Making a Web Page

- [Mapping a URL](#url)
- [Writing a View](#view)
- [Writing a Template](#template)

- Three stages to making a web site
  - Define patterns for URLs
  - Writing views
  - Writing templates
  
<a name="url"></a>
## Mapping a URL

Add base page to urls.py:

```python
from django.conf.urls import include, url
from django.contrib import admin

urlpatterns = [
    url(r'^admin/', include(admin.site.urls)),
    url(r'', include('learning_logs.urls', namespace='learning_logs')), 
]
```

Create `urls.py` in the app:

```python
"""Defines url patterns for learning_logs."""

from django.conf.urls import url

from . import views

urlpatterns = [
    # Home page.
    url(r'^$', views.index, name='index'),
    
    # Show all topics.
    url(r'^topics/$', views.topics, name='topics'),
    
    # Detail page for a single topic.
    url(r'^topics/(?P<topic_id>\d+)/$', views.topic, name='topic'),
]
```

<a name="view"></a>
## Writing a View

A view function takes in information from a request, prepares the data needed to generate a page, 
and then sends the data back to the browser, often by using a template that defines what the page will look like.

```python
from django.shortcuts import render

from .models import Topic

def index(request):
    """The home page for Learning Log."""
    return render(request, 'learning_logs/index.html')

def topics(request):
    """Show all topics."""
    topics = Topic.objects.order_by('date_added')
    context = {'topics': topics}
    return render(request, 'learning_logs/topics.html', context)

def topic(request, topic_id):
    """Show a single topic, and all its entries."""
    topic = Topic.objects.get(id=topic_id)
    entries = topic.entry_set.order_by('-date_added')
    context = {'topic': topic, 'entries': entries}
    return render(request, 'learning_logs/topic.html', context)
```

<a name="template"></a>
## Writing a Template

A template sets up the structure for a web page. The template defines what the page should look like, 
and Django fills in the relevant data each time the page is requested. A template allows you to access 
any data provided by the view

Create a folder in the app called `templates` and a folder under that with the same name as the app

