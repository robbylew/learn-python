<div align="center">
  <h1> Python by Topic - Data Types</h1>
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

- [Data Types](#data-types)

  - [Integer](#integer-or-int)

  - [Float](#float)

  - [String](#string)

  - [Booleans](#booleans)

  - [List](#list)
  
  - [Dictionary](#dictionary-or-dict)

  - [Tuple](#tuple)

  - [Set](#set)

- [Checking Data Types](#checking-data-types)

# Data Types

There are several data types in Python. We will go over them extremely briefly today, and will dive into them in great detail later on.

## Integer or Int

A whole number, or zero.


```python
-3, -2, -1, 0, 1, 2, 3
```

## Float

A decimal number.


```python
3.14, 2.71828, -1.61803
```

## String

A collection of one or more characters under a single or double quote.


```python
'Robert', 'Lewis', '50'
```

Strings can also span multiple lines with a triple quote


```python
'''
All of the characters in here
are strings
1031
'''
```

## Booleans

Similar to 1's and 0's, Booleans can only be one of two values: `True` or `False`


```python
True  #  1 in computer language
False # 0 in computer language
```

## List
An ordered collection which allows to store different data type items. 


```python
[0, 1, 2, 3, 4, 5] # all are the same data types - a list of numbers
['Banana', 'Orange', 'Mango', 'Avocado'] # all the same data type - a list of strings
['Banana', 10, False, 9.81] # different data types in the list - string, int, boolean, float
```

## Dictionary or Dict
An unordered collection of data in a key value pair format.



```python
{
  'first_name': 'Robert',
  'last_name': 'Lewis',
  'country': 'United States',
  'age': 250,
  'is_married': False,
  'skills': ['Python', 'R']
}
```

## Tuple

An ordered collection of different data types, like a list, but tuples cannot be modified once they are created. They are immutable.


```python
('Robert', 'Lewis', 'Brook', 'Adam', 'James') # Names
```

## Set

A collection of data types, similar to a list and a tuple, but unlike the two is an unordered collection of items. Like in Mathematics, set in Python only stores unique items



```python
{2, 4, 3, 5}
{3.14, 9.81, 2.7} # order is not important in set
```


# Checking Data Types



```python

print(type(10))          # Int
print(type(3.14))        # Float
print(type(1 + 3j))      # Complex number
print(type('Robert'))  # String
print(type([1, 2, 3]))   # List
print(type({'name':'Robert'})) # Dictionary
print(type({9.8, 3.14, 2.7}))    # Set
print(type((9.8, 3.14, 2.7)))    # Tuple
```
