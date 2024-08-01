# Operators

<div align="center">
  <h1> Python by Topic - Operators</h1>
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

1. [Assignment Operators](#assignment-operators)

    - [Examples](#assignment-operator-examples)

2. [Arithmetic Operators](#arithmetic-operators)

    - [Examples](#arithmetic-operators-examples)

3. [Comparison Operators](#comparison-operators)

    - [Examples](#comparison-operators-examples)
    
4. [Logical Operators](#logical-operators)

    - [Examples](#logical-operators-examples)

## Assignment Operators

To assign values to varaibles we use **Assignment Operators**

![assignment_operators.png](03_operators_files/assignment_operators.png)

### Assignment Operator Examples


```python
x = 5
print(x)  # 5

x += 3
print(x)  # 8

x -= 2
print(x)  # 6

x *= 4
print(x)  # 24

x /= 2
print(x)  # 12.0

x %= 5
print(x)  # 2.0

x //= 2
print(x)  # 1.0

x **= 3
print(x)  # 1.0

x = int(x)
x &= 5
print(x)  # 1

x |= 3
print(x)  # 3

x ^= 2
print(x)  # 1

x >>= 1
print(x)  # 0

x <<= 2
print(x)  # 0
```

    5
    8
    6
    24
    12.0
    2.0
    1.0
    1.0
    1
    3
    1
    0
    0


## Arithmetic Operators

If you want to do arithmetics with variables, we use **Arithmetic Operators**

![arithmetic_operators.png](03_operators_files/arithmetic_operators.png)

### Arithmetic Operators Examples:


```python
# Arithmetic Operations in Python
# Integers

print('Addition: ', 1 + 2)        # 3
print('Subtraction: ', 2 - 1)     # 1
print('Multiplication: ', 2 * 3)  # 6
print ('Division: ', 4 / 2)       # 2.0  Division in Python gives floating number
print('Division: ', 6 / 2)        # 3.0         
print('Division: ', 7 / 2)        # 3.5
print('Division without the remainder: ', 7 // 2)   # 3,  gives without the floating number or without the remaining
print ('Division without the remainder: ',7 // 3)   # 2
print('Modulus: ', 3 % 2)         # 1, Gives the remainder
print('Exponentiation: ', 2 ** 3) # 9 it means 2 * 2 * 2

# Floating numbers
print('Floating Point Number, PI', 3.14)
print('Floating Point Number, gravity', 9.81)

# Complex numbers
print('Complex number: ', 1 + 1j)
print('Multiplying complex numbers: ',(1 + 1j) * (1 - 1j))
```

    Addition:  3
    Subtraction:  1
    Multiplication:  6
    Division:  2.0
    Division:  3.0
    Division:  3.5
    Division without the remainder:  3
    Division without the remainder:  2
    Modulus:  1
    Exponentiation:  8
    Floating Point Number, PI 3.14
    Floating Point Number, gravity 9.81
    Complex number:  (1+1j)
    Multiplying complex numbers:  (2+0j)


## Comparison Operators

To compare a variable to another, we use **Comparison Operators**

![comparison_operators.png](03_operators_files/comparison_operators.png)

In addition to the above comparison operator Python uses:

+ `is`: Returns true if both variables are the same object(x is y)

+ `is not`: Returns true if both variables are not the same object(x is not y)

+ `in`: Returns True if the queried list contains a certain item(x in y)

+ `not in`: Returns True if the queried list doesn't have a certain item(x in y)


### Comparison Operators Examples:


```python
print(3 > 2)     # True, because 3 is greater than 2
print(3 >= 2)    # True, because 3 is greater than 2
print(3 < 2)     # False,  because 3 is greater than 2
print(2 < 3)     # True, because 2 is less than 3
print(2 <= 3)    # True, because 2 is less than 3
print(3 == 2)    # False, because 3 is not equal to 2
print(3 != 2)    # True, because 3 is not equal to 2
print(len('mango') == len('avocado'))  # False
print(len('mango') != len('avocado'))  # True
print(len('mango') < len('avocado'))   # True
print(len('milk') != len('meat'))      # False
print(len('milk') == len('meat'))      # True
print(len('tomato') == len('potato'))  # True
print(len('python') > len('dragon'))   # False


# Comparing something gives either a True or False

print('True == True: ', True == True)
print('True == False: ', True == False)
print('False == False:', False == False)


print('1 is 1:', 1 == 1)                      # True - because the data values are the same
print('1 is not 2:', 1 != 2)                  # True - because 1 is not 2
print('R in Robert:', 'R' in 'Robert')        # True - R is found in the string
print('B in Robert:', 'B' in 'Robert')        # False - there is no uppercase B
print('coding in "coding for all":', 'coding' in 'coding for all')  # True - because "coding for all" has the word "coding"
print('a in an:', 'a' in 'an')                # True
print('4 is 2 ** 2:', 4 == 2 ** 2)            # True - 4 is equal to 2 raised to the power of 2
```

    True
    True
    False
    True
    True
    False
    True
    False
    True
    True
    False
    True
    True
    False
    True == True:  True
    True == False:  False
    False == False: True
    1 is 1: True
    1 is not 2: True
    R in Robert: True
    B in Robert: False
    coding in "coding for all": True
    a in an: True
    4 is 2 ** 2: True


## Logical Operators

Last but certainly not least, Python allows for the use of keyword in conditional statements, called **Logical Operators**

![logical_operators.png](03_operators_files/logical_operators.png)

### Logical Operators Examples:


```python
print(3 > 2 and 4 > 3) # True - because both statements are true
print(3 > 2 and 4 < 3) # False - because the second statement is false
print(3 < 2 and 4 < 3) # False - because both statements are false
print('True and True: ', True and True)
print(3 > 2 or 4 > 3)  # True - because both statements are true
print(3 > 2 or 4 < 3)  # True - because one of the statements is true
print(3 < 2 or 4 < 3)  # False - because both statements are false
print('True or False:', True or False)
print(not 3 > 2)     # False - because 3 > 2 is true, then not True gives False
print(not True)      # False - Negation, the not operator turns true to false
print(not False)     # True
print(not not True)  # True
print(not not False) # False
```

    True
    False
    False
    True and True:  True
    True
    True
    False
    True or False: True
    False
    False
    True
    True
    False

