### Django Templates Explanation

In Django, templates are used to define the structure and presentation of the web pages that your application generates. They allow you to separate the design from the logic by using HTML syntax along with special template tags and filters provided by Django.

#### How Templates Work in Django

Django uses a templating engine called Django Template Language (DTL) which is designed to be simple yet powerful. A template can contain static content like HTML, as well as dynamic content that gets inserted when the template is rendered. 

- **Static Content**: This includes any part of the page that remains unchanged for every request, such as navigation bars and footers.
- **Dynamic Content**: This is data that changes based on the context in which the template is rendered, like user-specific information or database-driven content.

#### Template Tags and Filters

Templates can use special syntax to insert dynamic content:

- **Template Tags**: These are special tokens that do something. They look like `{% tag %}`. For example:
  ```django
  {% if user.is_authenticated %}
      Hello, {{ user.username }}!
  {% endif %}
  ```
- **Filters**: Filters allow you to modify variables for display. You can chain filters together and they are separated by pipes `|`. For example:
  ```django
  {{ some_text|upper }}
  ```

#### Template Inheritance

Django templates support template inheritance, allowing you to build a base "skeleton" template that contains all the common elements of your site, and then define child templates that extend the base template. This makes it easier to maintain consistency across your site.

Here’s an example:

**base.html**
```django
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>{% block title %}My Site{% endblock %}</title>
</head>
<body>
    <header>
        My Website
    </header>
    <div class="content">
        {% block content %}
        <!-- Content goes here -->
        {% endblock %}
    </div>
    <footer>
        © 2023 My Website
    </footer>
</body>
</html>
```

**home.html**
```django
{% extends "base.html" %}

{% block title %}Home Page{% endblock %}

{% block content %}
<p>Welcome to the home page!</p>
{% endblock %}
```

In this example, `home.html` extends `base.html` and overrides the `title` and `content` blocks.

#### Rendering Templates in Views

Templates are rendered by views in Django. Here’s how you might render a template in a view:

```python
from django.shortcuts import render

def home_view(request):
    context = {'user': request.user, 'message': 'Hello World!'}
    return render(request, 'home.html', context)
```

In this example, the `render` function is used to render `home.html`, passing it a context dictionary that contains data for the template.

#Templates #Django