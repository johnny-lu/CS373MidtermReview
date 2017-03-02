# **SWE Midterm Review**
Some notes over Downing's CS373: Software Engineering midterm.

The topics to be reviewed are:

 - [Readings](#readings)
 - [Quizzes](#quizzes)
 - [Python](#python)
 
 
## **Readings**

----------



## **Quizzes**

----------

## **Python**
----------
##### **Subtopics:**

 - [Types](#types)
 - [Operators](#operators)
 - [Methods](#methods)
 - [Functions](#functions)
 - [Concepts](#concepts)
 - [Tokens](#tokens)

#### **Types**
Everything in Python is an object.

 - bool: `True` or `False`. Conditional expressions will accept values of any type, treating special ones like boolean `False`, integer 0 and the empty string `""` as equivalent to False, and all other values as equivalent to True.
 - complex: A complex number is a number of the form `A+Bi` where `i` is the imaginary number, equal to the square root of -1. In Python, a number followed by “j” is treated as an imaginary number. Python displays complex numbers in parentheses when they have a nonzero real part. Unlike Python's other numeric types, complex numbers are made of two parts: the real part and the imaginary part, both of which are represented internally as float values. You can retrieve the two components using `c.real` or `c.imag`.
 
```python
>>> 5j
5j
>>> 1+2.56j
(1+2.5600000000000001j)
>>> a = (7.8064-6j)
>>> a.real
7.8064
>>> a.imag
-6.0
```
 - list
 - dict: Maps objects "values" to other hashable objects "keys". iterable, not indexable. unordered, no duplicate keys. mutable. not hashable
 - tuple
 - map: applies a function to all the items in an input_list. 
```python
map(function_to_apply, list_of_inputs) #example call
items = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x**2, items))
# Output: [1, 4, 9, 16, 25]
````
 - filter: creates a list of elements for which a function returns true.
```python
number_list = range(-5, 5)
less_than_zero = list(filter(lambda x: x < 0, number_list))
print(less_than_zero)

# Output: [-5, -4, -3, -2, -1]
```
 - int
 - float
 - frozenset
 - range
 - set
 - str
 - type
 - zip

#### **Operators**
- -
- -=
- ()
- []
- **
- **=
- *
- *=
- //
- /
- /=
- &
- &=
- >>
- >>=
- >
- >=
- <<
- <<=
- <
- <=
- %
- %=
- ^
- ^=
- +
- +=
- |
- |=
- ~
- and
- not
- or

#### **Methods**
```python
__getitem__
__init__
def __iter__(self):
    return self #returns an iterator, itself.
__len__
__next__
```
#### **Functions**
#### **Concepts**
#### **Tokens**


