<div align="center">
  <h1> Python by Topic - Conditionals & Loops </h1>
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

1. [Conditionals](#conditionals)

    - [If](#if)

    - [If Else](#if-else)

    - [If Elif Else](#if-elif-else)

    - [Short Hand](#short-hand)

    - [Nested Conditions](#nested-conditions)

    - [And](#and)

    - [Or](#or)

2. [Loops](#loops)

    - [While Loops](#while-loops)

    - [For Loops](#for-loops)

    - [For Else](#for-else)

    - [Break](#break)

    - [Continue](#continue)

    - [Pass](#pass)


# Conditionals and Loops

## Conditionals

By default, statements in Python script are executed sequentially from top to bottom. If the processing logic require so, the sequential flow of execution can be altered in two way:

- Conditional execution: a block of one or more statements will be executed if a certain expression is true

- Repetitive execution: a block of one or more statements will be repetitively executed as long as a certain expression is true. In this section, we will cover _if_, _else_, _elif_ statements. The comparison and logical operators we learned in previous sections will be useful here.

### If

In python, and other programming languages, they key word `if` is used to check if a condition is true and to execute the block code.. Remember the indentation after the colon. 

```python
if condition:
    this part of code runs for truthy conditions
```

### If Else

If condition is true the first block will be executed, if not the else condition will run.

```python
if condition:
    this part of code runs for truthy conditions
else:
     this part of code runs for false conditions
```

### If Elif Else

In our daily life, we make decisions on daily basis. We make decisions not by checking one or two conditions but multiple conditions. As similar to life, programming is also full of conditions. We use _elif_ when we have multiple conditions.

```python
if condition:
    code
elif condition:
    code
else:
    code
````

### Short Hand

```python
code if condition else code
```

### Nested Conditions

```python
if condition:
    code
    if condition:
    code
````

### And

Instead of nesting if statements, which we can do, we can use the logical operator and

```python
if condition and condition:
    code
````

### Or

Same as and, except we use it for a either or conditional.

```python
if condition or condition:
    code
```

## Loops

In order to handle repetitive task programming languages use loops. Python programming language also provides the following types of two loops:

+ while loop

+ for loop

### While Loops

We use the reserved word while to make a while loop. It is used to execute a block of statements repeatedly until a given condition is satisfied. When the condition becomes false, the lines of code after the loop will be continued to be executed.

```python
while condition:
    code goes here
```

If we are interested to run block of code once the condition is no longer true, we can use else.

```python
while condition:
    code goes here
else:
    code goes here
```

#### For Loops

A for keyword is used to make a for loop, similar with other programming languages, but with some syntax differences. Loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).

```python
for iterator in data_type:
    code goes here
```

### For Else

If we want to execute some message when the loop ends, we use else.

```python
for iterator in range(start, end, step):
    do something
else:
    print('The loop ended')
```

#### Break

We use break when we like to get out of or stop the loop.

```python
# while loop
while condition:
    code goes here
    if another_condition:
        break
    
# for loop
for iterator in sequence:
    code goes here
    if condition:
        break
```

#### Continue

With the continue statement we can skip the current iteration, and continue with the next

```python
# while loop
while condition:
    code goes here
    if another_condition:
        continue
    
# for loop
for iterator in sequence:
    code goes here
    if condition:
        continue
```

#### Pass

In python when statement is required (after semicolon), but we don't like to execute any code there, we can write the word pass to avoid errors. Also we can use it as a placeholder, for future statements.

```python
for number in range(6):
    pass
```
