# Django CRUD and Forms
## How do Django Forms facilitate user input handling, and what are some key components of creating a form using the Django framework?

1. 'Display the default form the first time it is requested by the user'.

2. 'Receive data from a submit request and bind it to the form : Binding data to the form means that the user-entered data and any errors are available when we need to redisplay the form'.
3. 'Clean and validate the data : 
* Cleaning the data performs sanitization of the input fields, such as removing invalid characters that might be used to send malicious content to the server, and converts them into consistent Python types.
* Validation checks that the values are appropriate for the field (for example, that they are in the right date range, aren't too short or too long, etc.)'.
4. 'If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.'
5. 'If all data is valid, perform required actions (such as save the data, send an email, return the result of a search, upload a file, and so on).'
6. 'Once all actions are complete, redirect the user to another page'.

* To create a form in Django, you need to :
1. Create a forms.py file in the application. The forms.py file is similar to models.py; all fields used in the form will be declared here under a form class.
2. Create a view method for the form in the views.py file.
3. Formulate an HTML file for displaying the form.
4. Tag the view in urls.py file.
5. Create a model form by subclassing the ModelForm.
6. Add the novalidate property to the form to disable HTML5 validation temporarily for testing server validation.
7. Use form.is_valid() to check if the form is valid.
8. Use form.save() to save form values into the database.
9. Use redirect() to redirect to a path.

## Explain the purpose of Django Templates in web development and describe how template inheritance can be utilized to improve code reusability and maintainability.
* 'Django templates are used to separate the design from the python code and allow developers to create HTML files that can be rendered dynamically based on user input or database queries123. A template in Django is basically written in HTML, CSS, and Javascript in a .html file1.'

## Describe the function of Django Views in handling HTTP requests, and outline the differences between function-based views and class-based views.
* 'Django views facilitate processing the HTTP requests and providing HTTP responses. When a page is requested, Django creates an HttpRequest object that contains metadata about the request. Then Django loads the appropriate view, passing the HttpRequest as the first argument to the view function. The business logic of handling the requests is done by Django Views, which is why Django supplies the request to the view function, so the code can access the request data and choose what actions it should take and which response it should send back.'
* 'URL mappers to forward the supported URLs (and any information encoded in the URLs) to the appropriate view functions.'
* 'View functions to get the requested data from the models, create HTML pages that display the data, and return the pages to the user to view in the browser.'
* 'Templates to use when rendering data in the views.'

* 'Function-based views are simple to use and beginners can easy understand them. It helps to understand the core concept of the Django fundamentals. FBV provides the advantages to understand the django concept from scratch. Django project usually have the CRUD operations, so we need to implement same code for the multiple times unnecessarily and that's why the Django class-based views come into the scenario. The class based-views reduces the code repetition and takes cares of the basic operations such as deleting and adding item. It is slightly hard to get the concept of class-based views for beginners. You should go through the documentation, and you will have study properly. If you have a clear idea about the function based views, you can move to the class based views.'