<div align="center">
  <h1> Python by Topic - List Comprehension & Lambda</h1>
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

1. [List Comprehension](#list-comprehension)

    - [Proof of Speed](#proof-of-speed)

    - [Fun Examples](#fun-examples)

2. [Lambda Function](#lambda-function)

    - [Creating a Lambda Function](#creating-a-lambda-function)

    - [Lambda Function Inside Another Function](#lambda-function-inside-another-function)


## List Comprehension

List comprehension in Python is a compact way of creating a list from a sequence. It is a short way to create a new list. List comprehension is considerably faster than processing a list using the for loop.

### Proof of Speed

We will have to do 10,000 repetitions for each as the computer will be able to do either process in a nanosecond. In this example, list comprehension is 66% faster.


```python
import time

# Number of repetitions to make the timing difference more noticeable
repetitions = 100000

tic = time.time()

# Slow way
for _ in range(repetitions):
    language = 'Python'
    lst = list(language) # changing the string to list

toc = time.time()

print(f'Using list took: {toc-tic:.2f}ms')

tic = time.time()

# Second way: list comprehension
for _ in range(repetitions):
    lst = [i for i in language]

tock = time.time()

print(f'List comprehension took: {tock-tic:.2f}ms')

```

    Using list took: 0.02ms
    List comprehension took: 0.02ms


### Fun examples


```python
print([i for i in range(11)]) # Generate numbers from 0 to 10
print([i * i for i in range(11)]) # Mathematical operations
print([(i, i * i) for i in range(11)]) # List of tuples
```

    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    [0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
    [(0, 0), (1, 1), (2, 4), (3, 9), (4, 16), (5, 25), (6, 36), (7, 49), (8, 64), (9, 81), (10, 100)]



```python
print([i for i in range(21) if i % 2 == 0]) # Even numbers
print([i for i in range(21) if i % 2 != 0]) # Odd numbers
```

    [0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
    [1, 3, 5, 7, 9, 11, 13, 15, 17, 19]



```python
# Flattening a three dimensional array
list_of_lists = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
flattened_list = [ number for row in list_of_lists for number in row]
print(flattened_list) 
```

    [1, 2, 3, 4, 5, 6, 7, 8, 9]


## Lambda Function

Lambda function is a small anonymous function without a name. It can take any number of arguments, but can only have one expression. Lambda function is similar to anonymous functions in JavaScript. We need it when we want to write an anonymous function inside another function.

### Creating a Lambda Function

To create a lambda function we use lambda keyword followed by a parameter(s), followed by an expression. See the syntax and the example below. Lambda function does not use return but it explicitly returns the expression.


```python
x = lambda param1, param2, param3: param1 + param2 + param2
print(x(1, 2, 3)) # 5
```

    5


### Example


```python
# Named function
def add_two_nums(a, b):
    return a + b

print(add_two_nums(2, 3))     # 5
# Lets change the above function to a lambda function
add_two_nums = lambda a, b: a + b
print(add_two_nums(2,3))    # 5

# Self invoking lambda function
(lambda a, b: a + b)(2,3) # 5 - need to encapsulate it in print() to see the result in the console

square = lambda x : x ** 2
print(square(3))    # 9
cube = lambda x : x ** 3
print(cube(3))    # 27

# Multiple variables
multiple_variable = lambda a, b, c: a ** 2 - 3 * b + 4 * c
print(multiple_variable(5, 5, 3)) # 22
```

    5
    5
    9
    27
    22


### Lambda Function Inside Another Function

Using a lambda function inside another function.


```python
def power(x):
    return lambda n : x ** n

cube = power(2)(3)   # function power now need 2 arguments to run, in separate rounded brackets
print(cube)          # 8
two_power_of_five = power(2)(5) 
print(two_power_of_five)  # 32
```

    8
    32

