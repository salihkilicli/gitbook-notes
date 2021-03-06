---
description: Here is some basic information about the Python programming language.
---

# Basics

In this chapter code blocks used often. `>>>` symbol is used to denote the commands entered into the interpreter. `...` denotes an indented code block following a `for`  or `while` loop \(will mention later\) or a conditional statement. The rest of the lines represent outputs of the Python interpreter.

### Installing Python

Most of the computers already come with **Python** installed. In order to check whether you already have up to date version of Python, go to the command line \(terminal in Mac, cmd in Windows\) and type Python, the prompt will show the version of Python you have.

```python
>>> username$ python
Python 3.7.7 (default, Mar 26 2020, 10:32:53) 
```

If you don't have up to date version of Python, you can go install the one compatible with your device [here](https://www.python.org/downloads/). Moreover, if you are going to learn Python and use it for Data Science, probably the best option is to download [Anaconda](https://www.anaconda.com/products/individual) \(or light version [Miniconda](https://docs.conda.io/en/latest/miniconda.html)\) distribution as it comes with most of the up to date Machine Learning libraries included along with the most common Python and R interpreters \(JupyterLab, Jupyter Notebook, PyCharm, RStudio, Spider, VSCode, etc.\).

My personal favorites are Jupyter Notebook \(or JupyterLab\) and VSCode for Python, RStudio for R. Now, assuming you already have an interpreter let's dive into the basic commands of Python.

### Print

The first command everybody should learn is `print()`. It simply prints the provided string/variable to the console.

{% hint style="info" %}
**String:** Anything written between 2 apostrophes `(' ')`or quotation marks `(" ") is` called a string, and if one of the words requires an apostrophe we can use quotation marks to represent the string \(see the last example below\).
{% endhint %}

{% hint style="success" %}
**Examples:** `'Hello!'` 

         `"I love programming!"`

         `"We are going to eat breakfast at Denny's."`
{% endhint %}

{% hint style="danger" %}
**Warning**: Combining and apostrophe or quotation marks will give an error.

**Incorrect:** `'error1"  or  "error2'`
{% endhint %}

{% hint style="warning" %}
**`Note:`**`'` and `"` used to create a string in the same line, while `"""` can be used for block comments consisting of multiple lines.
{% endhint %}

```python
# Block Commenting Example - often used in function descriptions
""" This is generally use to explain how some code block and/or a 
function works, especially when the explanation of the code cannot be
fitted in one line. """
```

```python
>>> print('Hello World! This is Salih!')
Hello World! This is Salih.

>>> print("I am an Applied Mathematician!")
I am an Applied Mathematician!

>>> print("This is an erratic string')
Error
```

### Variables

To create a variable use  `=`   sign followed by a variable name and then assign it to any value you want. You can print the value of the variable using `print()`  function.

```python
>>> a = 5
>>> b = 'This is a string.'
>>> print(a)
5

>>> print(b)
This is a string.
```

### Data Types

Use `type()` command to check the data type of a variable. The list of data types below is mainly taken from the [w3schools.com](https://www.w3schools.com/python/python_datatypes.asp). Putting a pound `#` symbol before typing anything converts the code line into a comment line in Python.

* **Text type:** String \(`str`\)

```python
# String Example
>>> s = 'This is a string'
>>> print(type(s))
<class 'str'>
```

* **Numeric Types:** Integer \(`int`\), Float \(`float`\), Complex \(`complex`\)

```python
# Integer Example          # Other commands giving the same results
>>> i = 5                  # i = int(5)
>>> print(type(i))
<class 'int'>

# Float Example
>>> f = 3.0                # f = float(3)
>>> print(type(f))
<class 'float'>

# Complex Example          # j is used to denote complex i in Python
>>> c = 1 + 3j             # c = complex(1, 3)
>>> print(type(c))
<class 'complex'>
```

Note: `int(3.5)` gives the integer part of the float, i.e., $$3$$, whereas `float(3)` yields $$3.0$$. Complex `i` is denoted by `j` in Python since `i` often used to denote an **index** for iteration in a loop.

* **Sequence Types:** List \(`list`\), Tuple \(`tuple`\), Range \(`range`\)

```python
# List Example                 # Notice list can hold different types
>>> l = ['a', 1, 2.0, 3 + 0j]  # l = list(['a', 1, 2.0, 3 + 0j])
>>> print(type(l))
<class 'list'>

# Tuple Example                # Tuples can store different types too
>>> t = (1, 'a', 2.0, 5j)      # t = tuple((1, 'a', 2.0, 5j)) 
>>> print(type(t))
<class 'tuple'>

# Range Example                 # This is actually a generator!
>>> r = range(5)                # Printing will not give the sequence
>>> print(type(r))              # print(r) -> range(0, 5)
<class 'range'>
```

Lists and tuples can store different types of data types. However, the main difference between a `list` and a `tuple` is that the lists are **mutable** \(i.e., the elements can be reassigned\) while the latter is **immutable** \(i.e., the elements cannot be reassigned or changed\). The `range` function is mainly used to create integer sequences in the following format `range(start=0, stop, step).` Some examples are given below:

```python
>>> list(range(5))        # since range is a generator (will see later)
[0, 1, 2, 3, 4]           # list() gives the range in a list format
              
>>> list(range(0, 10, 2)) # Notice range doesn't include stop point
[0, 2, 4, 6, 8]

```

* **Mapping Type \(Hash Table\):** Dictionary \(`dict`\)

```python
# Dictionary Example            # Consists of key:value pairs
>>> d = {1:'a', 2:'b'}          # d = dict({1:'a', 2:'b'}) 
>>> print(type(d))              
<class 'dict'>x
```

Dictionaries consist of `key:value` pairs and are **mutable** objects in Python.

* **Set Types:** Set **\(**`set`, or `frozenset`\)

```python
# Set Example                   # no repetitive elements
>>> st = {1, 2, 2, 3, 3,'Kivi'} # st = set((1, 2, 2, 3, 3, 'Kivi')) 
>>> print(type(st))             # print(st) -> {1, 2, 3, 'Kivi'}  
<class 'set'>

# Frozenset Example             # immutable set (el. cannot be changed)
>>> fs = {1, 2, 2, 3, 3, 3}     # fs = frozenset((1, 2, 2, 3, 3, 3)) 
>>> print(type(fs))              
<class 'dict'>
```

Sets are collections of unordered distinct objects. The main difference between a `set` and a `frozenset` is that `set` is **mutable** while `frozentset` is **immutable**. Also, sets cannot contain mutable objects, as a result, only a `frozenset` can be an element of either set.

* **Boolean Type:** Boolean \(`bool`\)

```python
# Boolean Example
>>> T = True
>>> print(type(T))
<class 'bool'>

>>> F = False
>>> print(type(F))
<class 'bool'>
```

* **None Type:** None

```python
# None Example
>>> n = None
>>> print(type(n))
<class 'NoneType'>
```





