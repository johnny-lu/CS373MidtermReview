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

 - dict
 - filter
 - float
 - frozenset
 - int
 - list
 - map
 - range
 - set
 - str
 - tuple
 - type
 - zip

#### **Operators**
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


