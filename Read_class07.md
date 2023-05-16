# Explain the concept of variable scope in Python and describe the difference between local and global scope. Provide an example illustrating the usage of both.

* ## 'The concept of scope rules how variables and names are looked up in your code. It determines the visibility of a variable within the code. The scope of a name or variable depends on the place in your code where you create that variable.'

* ## There are two general scopes:
    <br/> Global scope: The names that you define in this scope are available to all your code.
    * example:

             x=10

    <br/>Local scope: The names that you define in this scope are only available or visible to the code within the scope.
    * example:

                if x>1:
                     x=10
# How do the global and nonlocal keywords work in Python, and in what situations might you use them?

* ## global and nonlocal are similar, to make the variable (x) which is local scope globally you write for example(global x) after that you can access and make a changes on variable (x) which is global scope.

* ## For nonlocal variable which is for example in nested function the same we add nonlocal before variable (x) for example(nonlocal x) then we can access and make a changes on variable (x) which is local scope (top level of function not on nested).


# In your own words, describe the purpose and importance of Big O notation in the context of algorithm analysis. 

* ## one of benifit to Big O notation to be attention what will happen in long sequenses,when O(n^3) it is actually bigger than O(n) and important thing we should know that this comparision it is not depend on the start value of each sequense but it is depend on the type of increasing if it constant of not.

# Based on the Rolling Dice Example, explain how you would simulate a dice roll using Python. Describe how you would use code to calculate the probability of rolling a specific number (e.g., the probability of rolling a 6) over a large number of trials.

```python
import random
count = 0

def roll():
    return random.randint(1,6)

    for i in range(1, max_number_of_repeating):
       if roll() == 6:
            count += 1
    
    propability(6)=(1/6)*max_number_of_repeating
    return propability(6)
```
