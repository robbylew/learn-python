<div align="center">
  <h1> Python by Topic - Higher Order Functions</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/robbylew/">
    <img src="https://img.shields.io/badge/LinkedIn-robbylew-blue?style=flat-square&logo=linkedin">
  </a>

  <a class="header-badge" target="_blank" href="https://twitter.com/roberthedev">
    <img src="https://img.shields.io/badge/Twitter-roberthedev-blue?style=flat-square&logo=X">
  </a>

<a class="header-badge" target="_blank" href="https://robertlewis.dev">
  <img src="https://img.shields.io/badge/Website-robertlewis.dev-blue?style=flat-square&logo=github">
</a>

<sub>Author:
<a href="https://www.linkedin.com/in/robbylew/" target="_blank">Robert Lewis</a><br>
<small> First Edition: August, 2024</small>
</sub>
</div>

# Table of Contents

1. [Function as a Parameter](#function-as-a-parameter)

2. [Function as a Return Value](#function-as-a-return-value)

3. [Python Closures](#python-closures)

4. [Python Decorators](#python-decorators)

    - [Creating Decorators](#creating-decorators)

    - [Applying Multiple Decorators to a Single Function](#applying-multiple-decorators-to-a-single-function)

    - [Accepting Parameters in Decorator Functions](#accepting-parameters-in-decorator-functions)

5. [Built-in Higher Order Functions](#built-in-higher-order-functions)

    - [map()](#map)

    - [filter()](#filter)

    - [reduce()](#reduce)


# Higher Order Functions

In Python functions are treated as first class citizens, allowing you to perform the following operations on functions:

+ A function can take one or more functions as parameters

+ A function can be returned as a result of another function

+ A function can be modified
 
+ A function can be assigned to a variable

In this section, we will cover:

1. Handling functions as parameters

2. Returning functions as return value from another functions

3. Using Python closures and decorators


### Function as a Parameter



```python
def sum_numbers(nums):  # normal function
    return sum(nums)    # a sad function abusing the built-in sum function :<

def higher_order_function(f, lst):  # function as a parameter
    summation = f(lst)
    return summation
result = higher_order_function(sum_numbers, [1, 2, 3, 4, 5])
print(result)       # 15
```

    15


### Function as a Return Value


```python
def square(x):          # a square function
    return x ** 2

def cube(x):            # a cube function
    return x ** 3

def absolute(x):        # an absolute value function
    if x >= 0:
        return x
    else:
        return -(x)

def higher_order_function(type): # a higher order function returning a function
    if type == 'square':
        return square
    elif type == 'cube':
        return cube
    elif type == 'absolute':
        return absolute

result = higher_order_function('square')
print(result(3))       # 9
result = higher_order_function('cube')
print(result(3))       # 27
result = higher_order_function('absolute')
print(result(-3))      # 3
```

    9
    27
    3


## Python Closures 

Python allows a nested function to access the outer scope of the enclosing function. This is is known as a Closure. Let us have a look at how closures work in Python. 

In Python, closure is created by nesting a function inside another encapsulating function and then returning the inner function. See the example below.


```python
def add_ten():
    ten = 10
    def add(num):
        return num + ten
    return add

closure_result = add_ten()
print(closure_result(5))  # 15
print(closure_result(10))  # 20
```

    15
    20


## Python Decorators

A decorator is a design pattern in Python that allows a user to add new functionality to an existing object without modifying its structure. Decorators are usually called before the definition of a function you want to decorate.

### Creating Decorators

To create a decorator function, we need an outer function with an inner wrapper function.


```python
# Normal function
def greeting():
    return 'Welcome to Python'
def uppercase_decorator(function):
    def wrapper():
        func = function()
        make_uppercase = func.upper()
        return make_uppercase
    return wrapper
g = uppercase_decorator(greeting)
print(g())          # WELCOME TO PYTHON

## Let us implement the example above with a decorator

'''This decorator function is a higher order function
that takes a function as a parameter'''
def uppercase_decorator(function):
    def wrapper():
        func = function()
        make_uppercase = func.upper()
        return make_uppercase
    return wrapper
@uppercase_decorator
def greeting():
    return 'Welcome to Python'
print(greeting())   # WELCOME TO PYTHON

```

    WELCOME TO PYTHON
    WELCOME TO PYTHON


### Applying Multiple Decorators to a Single Function


```python

'''These decorator functions are higher order functions
that take functions as parameters'''

# First Decorator
def uppercase_decorator(function):
    def wrapper():
        func = function()
        make_uppercase = func.upper()
        return make_uppercase
    return wrapper

# Second decorator
def split_string_decorator(function):
    def wrapper():
        func = function()
        splitted_string = func.split()
        return splitted_string

    return wrapper

@split_string_decorator
@uppercase_decorator     # order with decorators is important in this case - .upper() function does not work with lists
def greeting():
    return 'Welcome to Python'
print(greeting())   # WELCOME TO PYTHON
```

    ['WELCOME', 'TO', 'PYTHON']


### Accepting Parameters in Decorator Functions

Most of the time we need our functions to take parameters, so we might need to define a decorator that accepts parameters.


```python
def another_dec(function):
    def wrapper(para1, para2, para3):
        function(para1, para2, para3)
        print("I also love to walk my dog")
    return wrapper

def decorator_with_parameters(function):
    def wrapper_accepting_parameters(para1, para2, para3):
        function(para1, para2, para3)
        print("I live in {}".format(para3))
    return wrapper_accepting_parameters

@another_dec
@decorator_with_parameters
def print_full_name(first_name, last_name, country):
    print("I am {} {}. I love to teach.".format(
        first_name, last_name, country))

print_full_name("Robert", "Lewis", 'United States')
```

    I am Robert Lewis. I love to teach.
    I live in United States
    I also love to walk my dog


## Built-in Higher Order Functions

Some of the built-in higher order functions that we cover in this part are `map()`, `filter`, and `reduce`. Lambda function can be passed as a parameter and the best use case of lambda functions is in functions like `map`, `filter` and `reduce`.

### map()

The `map()` function is a built-in function that takes a function and iterable as parameters.

```python
    map(function, iterable)
```


```python
# Example 1

numbers = [1, 2, 3, 4, 5] # iterable
def square(x):
    return x ** 2
numbers_squared = map(square, numbers)
print(list(numbers_squared))    # [1, 4, 9, 16, 25]
# Lets apply it with a lambda function
numbers_squared = map(lambda x : x ** 2, numbers)
print(list(numbers_squared))    # [1, 4, 9, 16, 25]
```

    [1, 4, 9, 16, 25]
    [1, 4, 9, 16, 25]



```python
# Example 2

numbers_str = ['1', '2', '3', '4', '5']  # iterable
numbers_int = map(int, numbers_str)
print(list(numbers_int))    # [1, 2, 3, 4, 5]
```

    [1, 2, 3, 4, 5]



```python
# Example 3

names = ['Robert', 'Lewis', 'James', 'Adams']  # iterable

def change_to_upper(name):
    return name.upper()

names_upper_cased = map(change_to_upper, names)
print(list(names_upper_cased))    # ['ROBERT', 'LEWIS', 'JAMES', 'ADAMS']

# Let us apply it with a lambda function
names_upper_cased = map(lambda name: name.upper(), names)
print(list(names_upper_cased))    # ['ROBERT', 'LIDIYA', 'JAMES', 'ADAMS']
```

    ['ROBERT', 'LEWIS', 'JAMES', 'ADAMS']
    ['ROBERT', 'LEWIS', 'JAMES', 'ADAMS']


What actually map does is iterating over a list. For instance, it changes the names to upper case and returns a new list.

### filter()

The `filter()` function calls the specified function which returns boolean for each item of the specified iterable (list). It filters the items that satisfy the filtering criteria.

```python
filter(function, iterable)
````


```python
# Example 1

# Lets filter only even nubers
numbers = [1, 2, 3, 4, 5]  # iterable

def is_even(num):
    if num % 2 == 0:
        return True
    return False

even_numbers = filter(is_even, numbers)
print(list(even_numbers))       # [2, 4]
```

    [2, 4]



```python
# Example 2

numbers = [1, 2, 3, 4, 5]  # iterable

def is_odd(num):
    if num % 2 != 0:
        return True
    return False

odd_numbers = filter(is_odd, numbers)
print(list(odd_numbers))       # [1, 3, 5]
```

    [1, 3, 5]



```python
# Example 3

# Filter long name
names = ['Robbylew', 'Robert', 'Lewis', 'Adams']  # iterable
def is_name_long(name):
    if len(name) > 7:
        return True
    return False

long_names = filter(is_name_long, names)
print(list(long_names))         # ['Robbylew']
```

    ['Robbylew']


### reduce()

The `reduce()` function is defined in the functools module and we should import it from this module. Like map and filter it takes two parameters, a function and an iterable. However, it does not return another iterable, instead it returns a single value. 


```python
from functools import reduce
# Example 1

numbers_str = ['1', '2', '3', '4', '5']  # iterable
def add_two_nums(x, y):
    return int(x) + int(y)

total = reduce(add_two_nums, numbers_str)
print(total)    # 15
```

    15

