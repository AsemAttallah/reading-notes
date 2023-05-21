# What is the basic syntax of Python list comprehension, and how does it differ from using a for loop to create a list? Provide an example of a list comprehension that squares the elements in a given list of integers.

* ## The basic syntax of Python list comprehension :
      my_new_list = [ expression for item in list ]
## it's consist of :
- 'The expression we’d like to carry out. expression inside the square brackets' . 
- 'The object that the expression will work on. item inside the square brackets' .
- 'We need an iterable list of objects to build our new list from. list inside the square brackets' .
## In list comprehension I can create a new list in one line of code which more readable and compact and need less time.
## To create a list in python with list comprehension just I need to follow this formated <code> my_new_list = [ expression for item in list ] </code> . But if I want to ceate a list using loopsI need to iterate for each value and append each one to the empty list that I created before to get the required list .

## Example:
        old_list = [1, 2, 3, 4]
        my_new_list = [item**2 for item in old_list]
        output after print(my_new_list): [1, 4, 9, 16]

# What is a decorator in Python?

* ## 'decorator is a function that takes another function and extends the behavior of the latter function without explicitly modifying it' .


# Explain the concept of decorators in Python. How do they work, and what are some common use cases for them? Provide an example of a simple decorator function from the reading.

* ## decorator is a function that takes another function as argument called (higher-order functions) so it is seems dealing with any other argument,that is mean I can return this function as output and make many think on it.

* Example :
    ```python
    def parent(num):
        def first_child():
            return "Hi, I am Emma"

        def second_child():
            return "Call me Liam"

        if num == 1:
            return first_child
        else:
            return second_child
    ```