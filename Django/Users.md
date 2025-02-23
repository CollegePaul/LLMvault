### Users in Django

In Django, the user authentication system is a robust framework that handles users, groups, permissions, and cookie-based user sessions. This system includes a default `User` model which you can use out of the box or extend to fit your needs.

#### Default User Model

Django comes with a built-in `User` model located in `django.contrib.auth.models`. This model includes fields like `username`, `password`, `email`, `first_name`, and `last_name`.

Here’s how you can create a user using Django’s shell:

```bash
python manage.py shell
```

Then, inside the shell:

```python
from django.contrib.auth.models import User

# Create a new user
user = User.objects.create_user('username', 'email@example.com', 'password123')

# Update additional fields
user.first_name = 'John'
user.last_name = 'Doe'
user.save()
```

#### Extending the Default User Model

If you need to add extra fields to the default user model, it’s best to extend the `AbstractUser` class. Here is an example of how to do this:

First, define a new user model in one of your apps' `models.py` files:

```python
from django.contrib.auth.models import AbstractUser

class CustomUser(AbstractUser):
    age = models.PositiveIntegerField(null=True, blank=True)
```

Next, you need to tell Django to use this new model by adding or updating the following line in your project’s settings file (`settings.py`):

```python
AUTH_USER_MODEL = 'myapp.CustomUser'
```

Replace `'myapp.CustomUser'` with the path to your custom user model.

After making these changes, make sure to run migrations:

```bash
python manage.py makemigrations myapp
python manage.py migrate
```

#### User Authentication Views

Django provides several views out of the box for handling authentication tasks such as login, logout, and password management. You can use them directly or customize them according to your needs.

For example, to include a login view in your project, you can update one of your URL configuration files like this:

```python
from django.urls import path
from django.contrib.auth import views as auth_views

urlpatterns = [
    path('login/', auth_views.LoginView.as_view(), name='login'),
]
```

This will create a login page at the `/login/` URL.

#Users #Django