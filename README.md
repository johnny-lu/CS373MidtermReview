# **CS 373: Software Engineering Midterm Review**
Some notes over Downing's CS373: Software Engineering midterm.

The topics to be reviewed are:

 - [Readings](#readings)
 - [Quizzes/Lectures](#quizzeslectures)
 - [Python](#python)
 
 
## **Readings**
----------
- _The Open-Closed Principle_: Software entities (classes, modules, functions, etc.) should be open for **extension**, but closed for **modification**.
- _The New Methodology_ – Agile methods are adaptive rather than predictive. Agile methods are people-oriented rather process-oriented.
- _Continuous Integration_ – automate the build, everyone commits to the mainline every day, make your build self-testing, maintain a single-source repository. 
- _UML Basics_: In **composition aggregation**, the relationship between the child’s lifecycle and the parent’s lifecycle is: the child’s lifecycle is dependent on the parent’s and denoted by a filled diamond on the parent’s side.
- _Liskov Substitution Principle_:  Functions that use references to **base classes** must be able to use objects of **derived classes** without knowing it.
- _Extreme Programming_ – discard independent work and rewrite it.



## **Quizzes/Lectures**
----------
Some pieces of information from either quizzes or lectures I think might appear on the test.
- Eager cache – stores (cycle length) during the run before the first read.
- Unit tests = white box, Acceptance tests = black box
- Java has (method) overloading, Python does NOT.
- `==` is for value equality and `is` is for reference equality.
- Calling `iter()` on an iter returns itself.
- How to notice/handle exceptions between two functions?
 - **return** mechanism. Return some value that indicates an error.
 - Write to some **global variable**. In Python, you must declare that a variable is global inside the function to use it.
 - Pass (the address) of a variable to check/write to. 
```python
try:
 ...
except E as e:
 ...
else: # won't run with break, continue, return and only if no exceptions were raised
 ...
finally: # always runs, even with break, continue, or return
 ...
```

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
- assert
- except
- functools.reduce
- issubclass
- iter
- next
- operator.add
- operator.floordiv
- operator.mul
- operator.sub
- operator.truediv
- pass
- print
- raise
- sqrt
- sum
- try
- yield

#### **Concepts**
- assertions
- classes
- closures
- concatenation
- dict comprehensions
- exceptions
- generators
- iterables
- iteration
- iterators
- lambdas: One line functions. Good for when you don’t want to use a function twice in a program.  
```python
lambda argument: manipulate(argument) #blueprint
add = lambda x, y: x + y
print(add(3, 5)) # Output: 8

def f (bf, x, y, z) :
    return bf(x, y) * bf(y, z)

assert f(lambda x, y : x + y, 2, 3, 4) == 35 # (2+3) * (3+4)
```
- list comprehensions
- nested classes
- nested functions
- recursion
- replication
- set comprehensions
- StopIteration

#### **Tokens**
- "*" in a function call
- "*" in a parameter list
- "**" in a function call
- "**" in a parameter list
- "=" in a function call
- "=" in a parameter list
