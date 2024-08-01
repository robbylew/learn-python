<div align="center">
  <h1> Python by Topic - Lists</h1>
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

1. [How to Create a List](#how-to-create-a-list)

    - [Using the built-in `list()` function](#using-the-built-in-list-function)

    - [Using Square Brackets `[]`](#using-square-brackets-)

2. [Accessing List Items Using Positive Indexing](#accessing-list-items-using-positive-indexing)

3. [Accessing List Items Using Negative Indexing](#accessing-list-items-using-negative-indexing)

4. [List Methods](#list-methods)

# Lists

Remember there are four collection data types in Python:

+ List: A collection that is ordered and modifiable(mutable). Allows duplicate members.

+ Tuple: A collection which is ordered and unmodifiable(immutable). Allows duplicate members.

+ Set: A collection which is unordered, un-indexed and unmodifiable, but we can add new items to the set. Duplicate members are not allowed.

+ Dictionary: A collection which is unordered, changeable(modifiable) and indexed. No duplicate members.


So a list is a dollection of different data types that is ordered and modifiable(mutable). It can be both empty or have a varying amount of data types. It can have duplicate members.

## How to create a List

In Python we can create lists in two ways:

### Using the built-in `list()` function:


```python
new_list = list()
```

### Or using square brackets, `[]`


```python
new_list = []
```

We use `len()` to find the length of a list


```python
fruits = ['banana', 'orange', 'mango', 'lemon']

# Print the list and its length
print('Fruits:', fruits)
print('Number of fruits:', len(fruits))
```

    Fruits: ['banana', 'orange', 'mango', 'lemon']
    Number of fruits: 4


Lists can have varying data types, and can also contain different type of collection data type:


```python
 lst = ['Robert', 250, True, {'country':'United States', 'city':'Los Angeles'}] # list containing different data types
```

### Accessing List Items Using Positive Indexing

We access each item in a list using their index. A list index starts from 0. The picture below shows clearly where the index starts

![list_index.png](../images/list_index.png)


```python

fruits = ['banana', 'orange', 'mango', 'lemon']
first_fruit = fruits[0] # we are accessing the first item using its index
print(first_fruit)      # banana
second_fruit = fruits[1]
print(second_fruit)     # orange
last_fruit = fruits[3]
print(last_fruit) # lemon
# Last index
last_index = len(fruits) - 1
last_fruit = fruits[last_index]
```

    banana
    orange
    lemon



### Accessing List Items Using Negative Indexing

Negative indexing means beginning from the end, -1 refers to the last item, -2 refers to the second last item.

![list_negative_indexing.png](../images/list_negative_indexing.png)



```python
fruits = ['banana', 'orange', 'mango', 'lemon']
first_fruit = fruits[-4]
last_fruit = fruits[-1]
second_last = fruits[-2]
print(first_fruit)      # banana
print(last_fruit)       # lemon
print(second_last)      # mango
```

    banana
    lemon
    mango


## List Methods

| Function | Description |
| :-: | :-- |
| <a href="https://www.w3schools.com/python/ref_list_append.asp">append()</a> |Adds an element at the end of the list 
| <a href="https://www.w3schools.com/python/ref_list_clear.asp">clear()</a>	| Removes all the elements from the list
| <a href="https://www.w3schools.com/python/ref_list_copy.asp">copy()</a> |	Returns a copy of the list
| <a href="https://www.w3schools.com/python/ref_list_count.asp">count()</a> |	Returns the number of elements with the specified value
| <a href="https://www.w3schools.com/python/ref_list_extend.asp">extend()</a> |	Add the elements of a list (or any iterable), to the end of the current list
| <a href="https://www.w3schools.com/python/ref_list_index.asp">index()</a> |	Returns the index of the first element with the specified value
| <a href="https://www.w3schools.com/python/ref_list_insert.asp">insert()</a> |	Adds an element at the specified position
| <a href="https://www.w3schools.com/python/ref_list_pop.asp">pop()</a> |	Removes the element at the specified position
| <a href="https://www.w3schools.com/python/ref_list_remove.asp">remove()</a> |	Removes the first item with the specified value
| <a href="https://www.w3schools.com/python/ref_list_reverse.asp">reverse()</a> |	Reverses the order of the list
| <a href="https://www.w3schools.com/python/ref_list_sort.asp">sort()</a> |	Sorts the list
