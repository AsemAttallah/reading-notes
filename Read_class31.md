# Django REST Framework & Docker
## What are the key components of a Docker container, and how do they help streamline the development and deployment of applications?
### 'Docker containers include everything an application needs to run, including:
* the code
* a runtime
* libraries
* environment variables
* configuration files'
### 'A Docker container consists of three main parts:

* 'the Dockerfile, used to build the image.'
* 'the image itself, a read-only template with instructions for creating a Docker container'
* 'the container, a runnable instance created from an image (you can create, start, stop, move or delete a container using the Docker API or CLI)'

## Describe the primary steps involved in building a library website using Django, including essential components like models, views, and templates.
1. adding Django REST Framework 
```
python -m pip install djangorestframework~=3.13.0
```
2. add rest_framework in django_project/settings.py file in INSTALLED_APPS
```
# django_project/settings.py
INSTALLED_APPS = [
    "django.contrib.admin",
    "django.contrib.auth",
    "django.contrib.contenttypes",
    "django.contrib.sessions",
    "django.contrib.messages",
    "django.contrib.staticfiles",
    # 3rd party
    "rest_framework",  # new
    # Local
    "books.apps.BooksConfig",
]
```
3.  create apis app 
```
python manage.py startapp apis
```
4. add it to INSTALLED_APPS
5. create a migration file and run migrate to update the database
6. Adding an API endpoint is just like configuring a traditional Django URL route
```
# django_project/urls.py
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path("admin/", admin.site.urls),
    path("api/", include("apis.urls")),  # new
    path("", include("books.urls")),
]
```
7. Then create a new file called apis/urls.py,Then create a new file called apis/urls.py
```
# apis/urls.py
from django.urls import path

from .views import BookAPIView

urlpatterns = [
    path("", BookAPIView.as_view(), name="book_list"),
]
```
8. Update the apis/views.py file so it looks like the following:

```
# apis/views.py
from rest_framework import generics

from books.models import Book
from .serializers import BookSerializer


class BookAPIView(generics.ListAPIView):
    queryset = Book.objects.all()
    serializer_class = BookSerializer
```
9. create a new file called apis/serializers.py and update it as follows:
```
# apis/serializers.py
from rest_framework import serializers

from books.models import Book


class BookSerializer(serializers.ModelSerializer):
    class Meta:
        model = Book
        fields = ("title", "subtitle", "author", "isbn")
```

## Can you explain the primary differences between Django and Django REST framework?
* 'The most important takeaway is that Django creates websites containing webpages, while Django REST Framework creates web APIs which are a collection of URL endpoints containing available HTTP verbs that return JSON.'