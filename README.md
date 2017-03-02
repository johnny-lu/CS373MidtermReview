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
 - All of Python's immutable built-in objects are hashable, while no mutable containers (such as lists or dictionaries) are.
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
- l-values are on the left hand side, but can be on either. r-values can only be on the right side. One way of thinking about it is: l-values are objects that persist whereas r-values do not after the expression.
- When you put a list into a tuple, you are putting its address in the tuple. You can still modify the original list, and tuple would be fine with that.

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

`i += j` is the same as `i = i + j` if `i` is an immutable type (e.g. `tuple`, `int`, ... but not `list`) AND `j` is the same type as `i`.
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
 - list: Constructor needs an iterable (over anything).
 - dict: Maps objects "values" to other hashable objects "keys". iterable, not indexable. unordered, no duplicate keys. mutable. not hashable. Constructor needs an iterable (over iterable).
 - tuple: Constructor needs an iterable (over anything). Immutable. Because `tuple` is immutable, calling `copy()` on one returns the address of the same `tuple`.
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
 - int: In Python, if an `int` gets bigger than 8-bytes, then the variable will be an address instead of its value. 
 - float: floating point numeric
 - frozenset: immutable, hashable set. `frozenset` is to `set` as `tuple` is to `list`.
 - range
 - set: Iterable. No duplicates. Mutable. Unordered. Unindexable. Things must be hashable (i.e. immutable objects) by default.
 - str: Constructor needs an iterable (over strings). Immutable.
 - type
 - zip

#### **Operators**
In Python, operators that does shomething should NOT return anything.
- `-` subtraction
- `-=` in place subtraction
- ()
- []
- `**` exponent; `a**b` is the same as saying a to the power of b
- `**=` in place exponent
- `*` multiplication
- `*=` in place multiplication
- `//` floor division. Returns `int` unless `float` was passed. Truncates.
- `/` true division. Always returns `float`.
- `/=` in place true division.
- `&` bitwise `AND`
- `&=` in place bitwise `AND`
- `>>` right bitwise shift
- `>>=` in place right bitwise shift
- `>` greater than
- `>=` greater or equal to
- `<<` left bitwise shift
- `<<=` in place left bitwise shift
- `<` less than
- `<=` less than or equal to
- `%` modulo (remainder after divison)
- `%=` in place modulo
- `^` bitwise exclusive or (`XOR`)
- `^=` in place bitwise exclusive or (`XOR`)
- `+` addition
- `+=` in place addition
- `|` bitwise or
- `|=` in place bitwise or
- `~` bitwise complement ("flips" the bits)
- `and` logical `AND`. If both sides are `true`, then the condition is `true`.
- `not` logical `NOT`. Reverse logical state of its operand.
- `or` logical `OR`. If either side is non-zero, then the condition is `true`.

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
- generators: are iterators.
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
- `*` in a function call unpacks an iterable. Can only do one per call. Must be used before the `**` unpacker. 
- `*` in a parameter list - every parameter that follows it must be called by name.
- `**` in a function call unpacks a dictionary. Can only do one per call. Must be used after the `*` unpacker. 
- `**` in a parameter list is used to take a variable number of arguments. 
- `=` in a function call used to pass keyword arguments (aka call by name). Why? Easier to read (and know what the function is asking for). Must be in the trailing set. Makes code more "brittle" because if the args names are changed, old calls to it passing keyword args have to change, too.
- `=` in a parameter list used to set default values in a function. Must be in the trailing set. If the defaults are not immutable, Python will store the mutable object somewhere and use it the next time you call the function without passing it a keyword arg.
