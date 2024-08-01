<div align="center">
  <h1> Python by Topic - Functions</h1>
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

1. [Defining a Function](#defining-a-function)

    - [Declaring and Calling a Function](#declaring-and-calling-a-function)

    - [Function with Default Parameters](#function-with-default-parameters)

    - [Function with Arbitrary Number of Arguments](#function-with-arbitrary-number-of-arguments)


# Functions

So far we have seen many built-in Python functions. In this section, we will focus on custom functions. What is a function? Before we start making functions, let us learn what a function is and why we need them?

## Defining a Function

A function is a reusable block of code or programming statements designed to perform a certain task. To define or declare a function, Python provides the `def` keyword. The following is the syntax for defining a function. The function block of code is executed only if the function is called or invoked.

### Declaring and Calling a Function

When we make a function, we call it declaring a function. When we start using the it, we call it calling or invoking a function. Function can be declared with or without parameters.

```python
# Declaring a function
def function_name():
    code
    
# Calling a function
function_name()
```

### Function with Default Parameters

Sometimes we pass default values to parameters, when we invoke the function. If we do not pass arguments when calling the function, their default values will be used.


```python
# Declaring a function
def function_name(param = value):
    code
        
# Calling function
function_name()
function_name(arg)
```

### Function with Arbitrary Number of Arguments

If we do not know the number of arguments we pass to our function, we can create a function which can take arbitrary number of arguments by adding `*` before the parameter name.

```python
# Declaring a function
def function_name(*args):
    code
    
# Calling function
function_name(param1, param2, param3,..)
```
