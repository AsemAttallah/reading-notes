
# Explain the purpose and basic structure of Django models. How do they help in creating and managing database schema in a Django application?
* 'A model is the single, definitive source of information about your data. It contains the essential fields and behaviors of the data you’re storing. Generally, each model maps to a single database table.

* The basics:
- Each model is a Python class that subclasses django.db.models.Model.
- Each attribute of the model represents a database field.
- With all of this, Django gives you an automatically-generated database-access API'

# Describe the primary features and functionality of the Django Admin interface. How can it be customized to suit the specific needs of a project?
* 'The Django admin application can use your models to automatically build a site area that you can use to create, view, update, and delete records. This can save you a lot of time during development, making it very easy to test your models and get a feel for whether you have the right data.'
* 'The admin application can also be useful for managing data in production, depending on the type of website.'

* Registering models :
 All you must do to add your models to the admin application is to register them by take this code 
    ```
    from .models import Author, Genre, Book, BookInstance

    admin.site.register(Book)
    admin.site.register(Author)
    admin.site.register(Genre)
    admin.site.register(BookInstance) ```

* Creating a superuser : 
* In order to log into the admin site, we need a user account with Staff status enabled. In order to view and create records we also need this user to have permissions to manage all our objects. You can create a "superuser" account that has full access to the site and all needed permissions using manage.py.
```
 python3 manage.py createsuperuser
```
- Once this command completes a new superuser will have been added to the database. Now restart the development server so we can test the login:
```
python3 manage.py runserver
```

* You can further customize the interface to make it even easier to use. Some of the things you can do are:

* List views:
    * Add additional fields/information displayed for each record.
    * Add filters to select which records are listed, based on date or some other selection value (e.g. Book loan status).
    * Add additional options to the actions menu in list views and choose where this menu is displayed on the form.
* Detail views
    * Choose which fields to display (or exclude), along with their order, grouping, whether they are editable, the widget used, orientation etc.
    * Add related fields to a record to allow inline editing (e.g. add the ability to add and edit book records while you're creating their author record).


