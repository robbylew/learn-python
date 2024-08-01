<div align="center">
  <h1> Python by Topic - Sets</h1>
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

1. [Creating a Set](#creating-a-set)

2. [Set Methods](#set-methods)

# Sets

A Set is a unordered data collection that contains un-indexed distinct elements.


### Creating a Set

We can use the `set()` built-in function or use curly brackets `{}`


```python
st = set()
st2 = {'item1', 'item2', 'item3', 'item4'}
```

### Set Methods

| Method | Shortcut | Description |
| --- | :-: | --- |
| <a href="https://www.w3schools.com/python/ref_set_add.asp">`add()`</a> | | Adds an element to the set |
| <a href="https://www.w3schools.com/python/ref_set_clear.asp">`clear()`</a> | | Removes all the elements from the set |
| <a href="https://www.w3schools.com/python/ref_set_copy.asp">`copy()`</a> | | Returns a copy of the set |
| <a href="https://www.w3schools.com/python/ref_set_difference.asp">`difference()`</a> | `-` | Returns a set containing the difference between two or more sets |
| <a href="https://www.w3schools.com/python/ref_set_difference_update.asp">`difference_update()`</a> | `-=` | Removes the items in this set that are also included in another, specified set |
| <a href="https://www.w3schools.com/python/ref_set_discard.asp">`discard()`</a> | | Remove the specified item |
| <a href="https://www.w3schools.com/python/ref_set_intersection.asp">`intersection()`</a> | `&` | Returns a set, that is the intersection of two other sets | 
| <a href="https://www.w3schools.com/python/ref_set_intersection_update.asp">`intersection_update()`</a> | `&=` | Removes the items in this set that are not present in other, specified set(s) | 
| <a href="https://www.w3schools.com/python/ref_set_isdisjoint.asp">`isdisjoint()`</a> | | Returns whether two sets have an intersection or not | 
| <a href="https://www.w3schools.com/python/ref_set_issubset.asp">`issubset()`</a> | `<=` | Returns whether another set contains this set or not | 
| | `<` | Returns whether all items in this set is present in other, specified set(s) | 
| <a href="https://www.w3schools.com/python/ref_set_issuperset.asp">`issuperset()`</a> | `>=` | Returns whether this set contains another set or not |
| | `>` | Returns whether all items in other, specified set(s) is present in this set | 
| <a href="https://www.w3schools.com/python/ref_set_pop.asp">`pop()`</a> | | Removes an element from the set |
| <a href="https://www.w3schools.com/python/ref_set_remove.asp">`remove()`</a> | | Removes the specified element |
| <a href="https://www.w3schools.com/python/ref_set_symmetric_difference.asp">`symmetric_difference()`</a> | `^` | Returns a set with the symmetric differences of two sets |
| <a href="https://www.w3schools.com/python/ref_set_symmetric_difference_update.asp">`symmetric_difference_update()`</a> | `^=` | Inserts the symmetric differences from this set and another |
| <a href="https://www.w3schools.com/python/ref_set_union.asp">`union()`</a> | `\|` | Returns a set containing the union of sets |
| <a href="https://www.w3schools.com/python/ref_set_update.asp">`update()`</a> | `\|=` | Updates the set with the union of this set and others |

