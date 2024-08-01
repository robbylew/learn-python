<div align="center">
  <h1> Python by Topic - Dictionaries</h1>
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

1. [Creating a Dictionary](#creating-a-dictionary)

2. [Accessing Dictionary Items](#accessing-dictionary-items)

3. [Adding Items to a Dictionary](#adding-items-to-a-dictionary)

4. [Other Useful Methods](#other-useful-methods)

# Dictionaries

A dicitonary is an unordered, mutable paired (key: value) data type

### Creating a Dictionary

You can create a dictioanry using the built-in `dict()` function or with squiggly brackets `{}`


```python
empty_dict = dict()
my_dict = {
  'first_name': 'Robert',
  'last_name': 'Lewis',
  'country': 'United States',
  'is_married': False,
  'skills': ['Python', 'Javascript', 'R'],
  'age': 230
}
```

### Accessing Dicitonary Items

You can access Dictionary items by referring to its key name


```python
print(my_dict['first_name'])
```

    Robert


We will raise an error if the key doesn't exist


```python
print(my_dict['date'])
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    Cell In[3], line 1
    ----> 1 print(my_dict['date'])


    KeyError: 'date'


So we can use the `get()` method to avoid this error


```python
print(my_dict.get('date')) # None
print(my_dict.get('first_name')) # Robert
```

    None
    Robert


### Adding Items to a Dictionary

You can add key: value pairs to a dictionary


```python
my_dict['dogs_name'] = 'Hannah'
my_dict['skills'].append('Django')
print(my_dict.get('dogs_name'))
print(my_dict.get('skills'))
```

    Hannah
    ['Python', 'Javascript', 'R', 'Django']


### Other useful Methods

| Method | Description |
| --- | --- |
| <a href="https://www.w3schools.com/python/ref_dictionary_clear.asp">`clear()`</a> | Removes all the elements from the dictionary |
| <a href="https://www.w3schools.com/python/ref_dictionary_copy.asp">`copy()`</a> | Returns a copy of the dictionary |
| <a href="https://www.w3schools.com/python/ref_dictionary_fromkeys.asp">`fromkeys()`</a> | Returns a dictionary with the specified keys and value |
| <a href="https://www.w3schools.com/python/ref_dictionary_items.asp">`items()`</a> | Returns a list containing a tuple for each key-value pair |
| <a href="https://www.w3schools.com/python/ref_dictionary_keys.asp">`keys()`</a> | Returns a list containing the dictionary's keys |
| <a href="https://www.w3schools.com/python/ref_dictionary_pop.asp">`pop()`</a> | Removes the element with the specified key |
| <a href="https://www.w3schools.com/python/ref_dictionary_popitem.asp">`popitem()`</a> | Removes the last inserted key-value pair |
| <a href="https://www.w3schools.com/python/ref_dictionary_setdefault.asp">`setdefault()`</a> | Returns the value of the specified key. If the key does not exist: insert the key, with the specified value |
| <a href="https://www.w3schools.com/python/ref_dictionary_update.asp">`update()`</a> | Updates the dictionary with the specified key-value pairs |
| <a href="https://www.w3schools.com/python/ref_dictionary_values.asp">`values()`</a> | Returns a list of all the values in the dictionary |

