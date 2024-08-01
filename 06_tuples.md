<div align="center">
  <h1> Python by Topic - Tuples</h1>
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

1. [Creating a Tuple](#creating-a-tuple)

    - [Using the built-in `tuple()` function](#using-the-built-in-tuple-function)

    - [Using Round Brackets `()`](#using-round-brackets-)

2. [Tuple Length](#tuple-length)

3. [Joining Tuples](#joining-tuples)

4. [Deleting Tuples](#deleting-tuples)

5. [Indexing and Splitting Tuples](#indexing-and-splitting-tuples)

6. [Changing Tuples to Lists](#changing-tuples-to-lists)

7. [Additional Tuple Methods](#additional-tuple-methods)


# Tuples

A tuple is an immutable ordered data structure. Once a tuple is created, it cannot be edited.

## Creating a Tuple

### Using the built-in `tuple()` function


```python
empty_tuple = tuple()
```

### Or using round brackets, `()`


```python
empty_tuple = ()
```

## Tuple Length

As with lists, we can use `len()` to get a tuples length.


```python
fruit_tuple = ('Apples', 'Bananas', 'Oranges')
print(len(fruit_tuple))
```

    3


## Joining Tuples

We can join two or more tuples using + operator


```python
# syntax
tpl1 = ('item1', 'item2', 'item3')
tpl2 = ('item4', 'item5','item6')
tpl3 = tpl1 + tpl2
print(tpl3)
```

    ('item1', 'item2', 'item3', 'item4', 'item5', 'item6')


### Deleting Tuples

Although you can't delete specific variabls, you can delete the entire tuple


```python
# syntax
tpl1 = ('item1', 'item2', 'item3')
del tpl1
```

### Indexing and Splitting Tuples

Tuples follow the same structure as with Lists when it comes to positive and negative indexing. Same with Slicing.

### Changing Tuples to Lists

You can change a Tuple to a List using the `list()` function


```python
random_tuple = ('item1', 'item2', 'item3','item4')
random_list = list(random_tuple)
random_list[0] = 'item0'
print(random_list)
```

    ['item0', 'item2', 'item3', 'item4']


## Additional Tuple Methods

| Method | Description |
| :-: | :-: |
| <a href="https://www.w3schools.com/python/ref_tuple_count.asp"> `count()` </a> | Returns the number of times a specified value occurs in a tuple |
| <a href="https://www.w3schools.com/python/ref_tuple_index.asp"> `index()` </a> | Searches the tuple for a specified value and returns the position of where it was found |

