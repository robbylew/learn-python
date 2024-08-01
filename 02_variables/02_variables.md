<div align="center">
  <h1> Python by Topic - Variables</h1>
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

1. [Variables](#variables)

    - [Declaring Multiple Variables in a Line](#declaring-multiple-variables-in-a-line)
    
    - [Casting Data Types](#casting-data-types)

# Variables

Variables store data in a computer memory. Mnemonic variables are recommended to use in many programming languages. You should get used to using mnemonic variables. A mnemonic variable is a variable name that can be easily remembered and associated. 

Python Variable Name Rules:
+ A variable must start with a letter or the underscore character
+ A variable name cannot start with a number
+ A variable can only contain alpha-numeric characters and underscores (A-z, 0-9, and _)
+ Variable names are case-sensitive (firstname, Firstname, FirstName, FIRSTNAME)


```python
# Variables in Python
first_name = 'Robert'
last_name = 'Lewis'
country = 'United States'
city = 'Los Angeles'
age = 250
is_married = False
skills = ['Python', 'R']
person_info = {
   'firstname':'Robert',
   'lastname':'Lewis',
   'country':'United States',
   'city':'Los Angeles'
   }
```

### Declaring Multiple Variables in a Line

Multiple variables can also be declared in one line:


```python
first_name, last_name, country, age, is_married = 'Robert', 'Lewis', 'United States', 250, False

print(first_name, last_name, country, age, is_married)
print('First name:', first_name)
print('Last name: ', last_name)
print('Country: ', country)
print('Age: ', age)
print('Married: ', is_married)
```

    Robert Lewis United States 250 False
    First name: Robert
    Last name:  Lewis
    Country:  United States
    Age:  250
    Married:  False


### Casting Data Types

Casting: Converting one data type to another data type. We use `int()`, `float()`, `str()`, `list`, `set`. 


```python
# int to float
num_int = 10
print('num_int',num_int)         # 10
num_float = float(num_int)
print('num_float:', num_float)   # 10.0

# float to int
gravity = 9.81
print(int(gravity))             # 9

# int to str
num_int = 10
print(num_int)                  # 10
num_str = str(num_int)
print(num_str)                  # '10'

# str to int or float
num_str = '10.6'
print('num_int', int(float(num_str)))      # 10
print('num_float', float(num_str))  # 10.6

# str to list
first_name = 'Robert'
print(first_name)               # 'Robert'
first_name_to_list = list(first_name)
print(first_name_to_list)   
```

    num_int 10
    num_float: 10.0
    9
    10
    10
    num_int 10
    num_float 10.6
    Robert
    ['R', 'o', 'b', 'e', 'r', 't']

