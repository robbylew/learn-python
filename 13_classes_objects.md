<div align="center">
  <h1> Python by Topic - Classes & Objects</h1>
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

1. [Creating a Class](#creating-a-class)

2. [Creating an Object](#creating-an-object)

3. [Class Constructor](#class-constructor)

4. [Object Methods](#object-methods)

5. [Object Default Methods](#object-default-methods)

6. [Method to Modify Class Default Values](#method-to-modify-class-default-values)

7. [Inheritance](#inheritance)

8. [Overriding Parent Method](#overriding-parent-method)



# Classes and Objects

Python is an object oriented programming language. Everything in Python is an object, with its properties and methods. A number, string, list, dictionary, tuple, set etc. used in a program is an object of a corresponding built-in class. We create class to create an object. A class is like an object constructor, or a "blueprint" for creating objects. We instantiate a class to create an object. The class defines attributes and the behavior of the object, while the object, on the other hand, represents the class.

We have been working with classes and objects right from the beginning of this challenge unknowingly. Every element in a Python program is an object of a class. Let us check if everything in python is a class:


```python
num = 10
print(type(num))
str = 'hi'
print(type(str))
bool = True
print(type(bool))
lis = [1, 2, 3]
print(type(lis))
tupl = (1, 2, 3)
print(type(tupl))
dict = {'1': 1, '2': 2}
print(type(dict))
st = set() 
print(type(st))
```

    <class 'int'>
    <class 'str'>
    <class 'bool'>
    <class 'list'>
    <class 'tuple'>
    <class 'dict'>
    <class 'set'>


## Creating a Class 

To create a class we need the key word class followed by the name and colon. Class name should be CamelCase.

```python
class ClassName:
   code goes here
```

### Example:


```python
class Person:
  pass
print(Person)
```

    <class '__main__.Person'>


## Creating an Object

We can create an object by calling the class.


```python
p = Person()
print(p)
```

    <__main__.Person object at 0x10571bdd0>


## Class Constructor
In the examples above, we have created an object from the Person class. However, a class without a constructor is not really useful in real applications. Let us use constructor function to make our class more useful. Like the constructor function in Java or JavaScript, Python has also a built-in `init()` constructor function. The init constructor function has self parameter which is a reference to the current instance of the class 


```python
class Person:
      def __init__ (self, name):
        # self allows to attach parameter to the class
          self.name = name

p = Person('Robert')
print(p.name)
print(p)
```

    Robert
    <__main__.Person object at 0x10574af30>


Let us add more parameters to the constructor function.


```python
class Person:
  def __init__(self, firstname, lastname, age, country, city):
    self.firstname = firstname
    self.lastname = lastname
    self.age = age
    self.country = country
    self.city = city
    
p = Person('Robert', 'Lewis', 250, 'United States', 'Los Angeles')
print(p.firstname)
```

    Robert


## Object Methods

Objects can have methods. The methods are functions which belong to the object.


```python
class Person:
      def __init__(self, firstname, lastname, age, country, city):
          self.firstname = firstname
          self.lastname = lastname
          self.age = age
          self.country = country
          self.city = city
      def person_info(self):
        return f'{self.firstname} {self.lastname} is {self.age} years old. He lives in {self.city}, {self.country}'

p = Person('Robert', 'Lewis', 250, 'United States', 'Los Angeles')
print(p.person_info())
```

    Robert Lewis is 250 years old. He lives in Los Angeles, United States


## Object Default Methods

Sometimes, you may want to have a default values for your object methods. If we give default values for the parameters in the constructor, we can avoid errors when we call or instantiate our class without parameters. Let's see how it looks:


```python
class Person:
      def __init__(self, firstname='Robert', lastname='Lewis', age=250, country='United States', city='Los Angeles'):
          self.firstname = firstname
          self.lastname = lastname
          self.age = age
          self.country = country
          self.city = city

      def person_info(self):
        return f'{self.firstname} {self.lastname} is {self.age} years old. He lives in {self.city}, {self.country}.'

p1 = Person()
print(p1.person_info())
p2 = Person('John', 'Doe', 30, 'Nomanland', 'Noman city')
print(p2.person_info())
```

    Robert Lewis is 250 years old. He lives in Los Angeles, United States.
    John Doe is 30 years old. He lives in Noman city, Nomanland.


## Method to Modify Class Default Values

In the example below, the person class, all the constructor parameters have default values. In addition to that, we have skills parameter, which we can access using a method. Let us create add_skill method to add skills to the skills list.


```python
class Person:
      def __init__(self, firstname='Robert', lastname='Lewis', age=250, country='United States', city='Los Angeles'):
          self.firstname = firstname
          self.lastname = lastname
          self.age = age
          self.country = country
          self.city = city
          self.skills = []

      def person_info(self):
        return f'{self.firstname} {self.lastname} is {self.age} years old. He lives in {self.city}, {self.country}.'
      def add_skill(self, skill):
          self.skills.append(skill)

p1 = Person()
print(p1.person_info())
p1.add_skill('HTML')
p1.add_skill('CSS')
p1.add_skill('JavaScript')
p2 = Person('John', 'Doe', 30, 'Nomanland', 'Noman city')
print(p2.person_info())
print(p1.skills)
print(p2.skills)
```

    Robert Lewis is 250 years old. He lives in Los Angeles, United States.
    John Doe is 30 years old. He lives in Noman city, Nomanland.
    ['HTML', 'CSS', 'JavaScript']
    []


## Inheritance 

Using inheritance we can reuse parent class code. Inheritance allows us to define a class that inherits all the methods and properties from parent class. The parent class or super or base class is the class which gives all the methods and properties. Child class is the class that inherits from another or parent class. Let us create a student class by inheriting from person class.


```python
class Student(Person):
    pass


s1 = Student('Robert', 'Jameson', 30, 'Finland', 'Helsinki')
s2 = Student('James', 'Edwards', 28, 'England', 'London')
print(s1.person_info())
s1.add_skill('JavaScript')
s1.add_skill('React')
s1.add_skill('Python')
print(s1.skills)

print(s2.person_info())
s2.add_skill('Organizing')
s2.add_skill('Marketing')
s2.add_skill('Digital Marketing')
print(s2.skills)

```

    Robert Jameson is 30 years old. He lives in Helsinki, Finland.
    ['JavaScript', 'React', 'Python']
    James Edwards is 28 years old. He lives in London, England.
    ['Organizing', 'Marketing', 'Digital Marketing']


We did not call the `init()` constructor in the child class. If we didn't call it then we can still access all the properties from the parent. But if we do call the constructor we can access the parent properties by calling super.
We can add a new method to the child or we can override the parent class methods by creating the same method name in the child class. When we add the `init()` function, the child class will no longer inherit the parent's `init()` function.

## Overriding Parent Method


```python
class Student(Person):
    def __init__ (self, firstname='Robert', lastname='Lewis',age=250, country='United States', city='Los Angeles', gender='male'):
        self.gender = gender
        super().__init__(firstname, lastname,age, country, city)
    def person_info(self):
        gender = 'He' if self.gender =='male' else 'She'
        return f'{self.firstname} {self.lastname} is {self.age} years old. {gender} lives in {self.city}, {self.country}.'

s1 = Student('Robert', 'Jameson', 30, 'Finland', 'Helsinki', 'male')
s2 = Student('James', 'Edwards', 28, 'England', 'London', 'female')
print(s1.person_info())
s1.add_skill('JavaScript')
s1.add_skill('React')
s1.add_skill('Python')
print(s1.skills)

print(s2.person_info())
s2.add_skill('Organizing')
s2.add_skill('Marketing')
s2.add_skill('Digital Marketing')
print(s2.skills)
```

    Robert Jameson is 30 years old. He lives in Helsinki, Finland.
    ['JavaScript', 'React', 'Python']
    James Edwards is 28 years old. She lives in London, England.
    ['Organizing', 'Marketing', 'Digital Marketing']


We can use `super()` built-in function or the parent name Person to automatically inherit the methods and properties from its parent. In the example above we override the parent method. The child method has a different feature, it can identify, if the gender is male or female and assign the proper pronoun(He/She).
