# Django Custom User
## What are the key benefits of using a Django Custom User Model, and how does it differ from the default Django User Model?
* 'It's highly recommended to set up a custom user model when starting a new Django project. Without it, you will need to create another model (like UserProfile) and link it to the Django user model with a OneToOneField if you want to add new fields to the user model.'
## Explain the process of creating and implementing a Custom User Model in Django, including the necessary changes to settings.py and the required model fields.
Creating our initial custom user model requires four steps:
* 'update django_project/settings.py'
* 'create a new CustomUser model'
* 'create new UserCreation and UserChangeForm'
* 'update the admin'
* 'In settings.py we'll add the accounts app and use the AUTH_USER_MODEL config to tell Django to use our new custom user model in place of the built-in User model. We'll call our custom user model CustomUser.'

* 'Within INSTALLED_APPS add accounts at the bottom. Then at the bottom of the entire file, add the AUTH_USER_MODEL config.'
* 'update accounts/models.py with a new User model which we'll call CustomUser.'
* 'We need new versions of two form methods that receive heavy use working with users. Stop the local server with Control+c and create a new file in the accounts app called forms.py.'
* 'We'll update it with the following code to largely subclass the existing forms.'

        from django.contrib.auth.forms import UserCreationForm, UserChangeForm

        from .models import CustomUser

        class CustomUserCreationForm(UserCreationForm):

        class Meta:
            model = CustomUser
            fields = ("username", "email")

        class CustomUserChangeForm(UserChangeForm):

        class Meta:
            model = CustomUser
            fields = ("username", "email")
* 'Finally we update admin.py since the Admin is highly coupled to the default User model.'

        from django.contrib import admin
        from django.contrib.auth.admin import UserAdmin

        from .forms import CustomUserCreationForm, CustomUserChangeForm
        from .models import CustomUser

        class CustomUserAdmin(UserAdmin):
            add_form = CustomUserCreationForm
            form = CustomUserChangeForm
            model = CustomUser
            list_display = ["email", "username",]

        admin.site.register(CustomUser, CustomUserAdmin)

* 'And we're done! We can now run makemigrations and migrate for the first time to create a new database that uses the custom user model.'


## What is DjangoX and how does it complement or extend the functionality of Django? Provide an example use case for incorporating DjangoX in a project.

* 'DjangoX is a set of extensions and add-ons for the Django web framework that aims to improve the development experience and provide additional functionality for building web applications.'
* 'It comes with a custom user model by default, email/password authentication instead of Django’s default and outdated username/email/password pattern, and is fully extendable with social authentication like Gmail, Facebook, and more.'