---
title: Crash Course on Python with Projects
author: Sooraj Prasad
date: May 09, 2024
---

# Real World Projects Using Python

Welcome to our GitHub repository dedicated to mastering Python and exploring its advanced features through a variety of projects and libraries! 🚀 Here, we embark on an exciting journey into the world of Python programming, where learning and innovation collide. ✨

Our projects span diverse domains, offering hands-on experience and real-world applications, from web development to data science, machine learning to automation. Each project is a testament to Python's versatility and power, empowering you to tackle any challenge with confidence. 💪

We harness the full potential of Python by leveraging an array of libraries and frameworks, from NumPy and pandas for data manipulation to TensorFlow and PyTorch for machine learning. 📚

Join us in this collaborative journey as we learn, create, and innovate with Python, pushing the boundaries of what's possible and unlocking the limitless potential of this incredible language, one project at a time. 🔍🔧🎨💻📈🔥

## Table of Contents

- [Introduction To Python](#introduction-to-python)
  - [What are Variables?](#what-are-variables)
  - [Simple Types Integers, String and Floats](#simple-types-integers-string-and-floats)
  - [List Data Types](#list-data-types)
  - [Type Attributes](#type-attributes)
  - [How to find out what code you need](#how-to-find-out-what-code-you-need)
  - [Dictionary Data Types](#dictionary-data-types)
  - [Tuple Data Types](#tuple-data-types)
  - [More Operations with Lists](#more-operations-with-lists)
  - [Accessing list item](#accessing-list-item)
  - [Accessing List Slices](#accessing-list-slices)
  - [Accessing items and Slices with Negative indexes](#accessing-items-and-slices-with-negative-indexes)
  - [Accessing Characters and Slices in Strings](#accessing-characters-and-slices-in-strings)
  - [Accessing items in Dictionaries](#accessing-items-in-dictionaries)
  - [Creating your own Functions](#creating-your-own-functions)
  - [Function with multiple arguments](#function-with-multiple-arguments)
  - [if else Condition](#if-else-condition)
  - [User Input](#user-input)
  - [String Formatting](#string-formatting)
  - [For Loops](#for-loops)
  - [While Loop](#while-loop)
  - [List Comprehension](#list-comprehension)
  - [File Processing in Python](#file-processing-in-python)
  - [File Cursor](#file-cursor)
  - [Python Modules](#python-modules)

## Introduction To Python

Let's start by writing our first piece of python code.

In your workspace open a folder where you want to create your python file. Make a new text file and save it as _Filename.py_. Then start writting the given code inside.

```python
# first import a module name datetime
import datetime

print("The date and time is", datetime.datetime.now()) #print function("String",(saperated by comma) module.object.function())
```

Next go to the terminal and type

> python _Filename.py_

hit enter and you will get the date and time something like, The date and time is 2024-04-27 18:34:44.455667

### What are Variables?

Variables are names in python which you can create to store values. Here is an example:

```python
import datetime

mynow = datetime.datetime.now()
mynumber = 7
mytext = "Hello"

print(mynow, mynumber, mytext)
```

Output

> 2024-04-27 18:34:44.455667 7 Hello

**Rules for Python variables:**

- A variable name must start with a letter or the underscore character
- A variable name cannot start with a number
- A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and \_ )
- Variable names are case-sensitive (age, Age and AGE are three different variables)
- A variable name cannot be any of the Python keywords.

### Simple Types Integers, String and Floats

There are two types of declarations one is the _Explicite Type_ and the other is the _Implicite Type_

In python we use the implicite type declaration.

```python
# Explicite type declaration which we don't use
int x =10
str y = "10" #can also use single quotes''
float z = 10.1

#Implicite Type declaration which we use
a = 10
b = "10" #can also use single quotes''
c = 10.1

sum1 = a+a
sum2 = b+b

print(sum1, sum2)
print(type(a), type(b), type(z))
```

Output

> 20 1010 <br>
> <class 'int'><class 'str'><class 'float'>

### List Data Types

There are also compound data type (**Types that are made of different objects**) and the list is the popular one. It can store multiple objects

```python
student_grades = [9.1, 8.8, 7.8]
```

You can create a list of numbers automatically using a range. For example:

```python
list(range(1, 10))
```

That will output:

> [1, 2, 3, 4, 5, 6, 7, 8, 9]

As you can see we just needed to specify the list boundaries inside range(). So, we specified 1and 10. Note that 10 is not included in the list. The generated list always runs up to one number before the upper number. In our example it goes up to 9 since the upper number is 10.

You can also specify a step as a third argument:

```python
list(range(1, 10, 2))
```

That will output:

> [1, 3, 5, 7, 9]

So, the count happens every two items starting from 1 and ending at 9.

### Type Attributes

So we know about list , str , int etc. But what can we do with it. To know that we will use the command after launching python inside our terminal

```bash
dir(str)
dir(list)
dir(int)
```

inside our python shell to get a list of attributes that we can use on the specific types.

Still confused what that attribute does? use the commant `help()` to know what that does for example

```bash
help(str.upper)
```

Output

> Return a copy of the string converted to uppercase.

Use `q` to quit.

### How to find out what code you need

So we know how to find out the attributes or methods of a type above but what if we want to know what other functionalities we can use in python other than the methods.

So for example someone ask us to find the mean or average of the items inside a list. We use the `dir(list)` to find if there is any method that we can use to find the mean but we couldn't find any so what do we do?

well we know that `print()` is a inbuild function which is not an attribute which uses a `.` operator to be used of any type so to find more such functions we use the `dir()` again

Here's how we get all the builtin Functions in Python

```bash
dir(__builtins__)
```

Output

```bash
['ArithmeticError', 'AssertionError', 'AttributeError', 'BaseException', 'BaseExceptionGroup', 'BlockingIOError', 'BrokenPipeError', 'BufferError', 'BytesWarning', 'ChildProcessError', 'ConnectionAbortedError', 'ConnectionError', 'ConnectionRefusedError', 'ConnectionResetError', 'DeprecationWarning', 'EOFError', 'Ellipsis', 'EncodingWarning', 'EnvironmentError', 'Exception', 'ExceptionGroup', 'False', 'FileExistsError', 'FileNotFoundError', 'FloatingPointError', 'FutureWarning', 'GeneratorExit', 'IOError', 'ImportError', 'ImportWarning', 'IndentationError', 'IndexError', 'InterruptedError', 'IsADirectoryError', 'KeyError', 'KeyboardInterrupt', 'LookupError', 'MemoryError', 'ModuleNotFoundError', 'NameError', 'None', 'NotADirectoryError', 'NotImplemented', 'NotImplementedError', 'OSError', 'OverflowError', 'PendingDeprecationWarning', 'PermissionError', 'ProcessLookupError', 'RecursionError', 'ReferenceError', 'ResourceWarning', 'RuntimeError', 'RuntimeWarning', 'StopAsyncIteration', 'StopIteration', 'SyntaxError', 'SyntaxWarning', 'SystemError', 'SystemExit', 'TabError', 'TimeoutError', 'True', 'TypeError', 'UnboundLocalError', 'UnicodeDecodeError', 'UnicodeEncodeError', 'UnicodeError', 'UnicodeTranslateError', 'UnicodeWarning', 'UserWarning', 'ValueError', 'Warning', 'WindowsError', 'ZeroDivisionError', '__build_class__', '__debug__', '__doc__', '__import__', '__loader__', '__name__', '__package__', '__spec__', 'abs', 'aiter', 'all', 'anext', 'any', 'ascii', 'bin', 'bool', 'breakpoint', 'bytearray', 'bytes', 'callable', 'chr', 'classmethod', 'compile', 'complex', 'copyright', 'credits', 'delattr', 'dict', 'dir', 'divmod', 'enumerate', 'eval', 'exec', 'exit', 'filter', 'float', 'format', 'frozenset', 'getattr', 'globals', 'hasattr', 'hash', 'help', 'hex', 'id', 'input', 'int', 'isinstance', 'issubclass', 'iter', 'len', 'license', 'list', 'locals', 'map', 'max', 'memoryview', 'min', 'next', 'object', 'oct', 'open', 'ord', 'pow', 'print', 'property', 'quit', 'range', 'repr', 'reversed', 'round', 'set', 'setattr', 'slice', 'sorted', 'staticmethod', 'str', 'sum', 'super', 'tuple', 'type', 'vars', 'zip']
```

We get a complete list of built in functions and types.
We find a sum and a len function there. If we use `help()` and inside the bracket type the name we will know exactly what thet particular is used for. Use `q` to quit.

So to find the average of numbers inside a list we can do

```python
student_grades = [9.1, 8.8, 7.5]
mysum = sum(student_grades)
length = len(student_grades)
mean = mysum / length
print(mean)
```

Output

> 8.46666666667

There are also libraries made by other developers that has functionalies that are not in python built-in.

### Dictionary Data Types

While a list is a good data structure to store an array of items, it's not good enough where these items have some sort of identity attached to them. A Dictionary is written in `{}` and have a **Key & Value Pair** so for example

```python
# Syntax for writting a dictionary
student_grades = {"John": 8.8, "Jani": 6.7, "Janardan": 7.3}
#To access the values
student_grades.values()
#To access the keys
student_grades.keys()
```

### Tuple Data Types

Tuples are like list with the only significant difference it that tuples are _Immutable_ while lists are _Mutable_. What it means it that you can add or remove items from a list but not from a tuple during the course of the program.

```python
temp1 = [1,4,5] #List
temp2 = (1,3,4) #Tuple
```

**Did You Know?**

> Python is mainly used for automation purposes, web apps, and data science. Many big companies like Instagram, Facebook, and Amazon use Python in different parts of their products. For example, Facebook uses Python to process images.

### More Operations with Lists

Type the command `dir(list)` and it will give a bunch of attributes you can use with the list. For now just ignore the ones that starts and ends with double underscore, they are basically attributes used by Python internally and rarely you're going to have to use them.

Our Main focus will be on these:

> 'append', 'clear', 'copy', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort'

So Here what they do.

```python
#Here is our list that we will experiment on
my_list = [1, 2, 3]

# append(item): Adds a single element to the end of the list.
my_list.append(4)
# Result: my_list is now [1, 2, 3, 4]

#clear(): Removes all elements from the list.
my_list.clear()
# Result: my_list is now []

#copy(): Returns a shallow copy of the list.
my_list = [1, 2, 3]
new_list = my_list.copy()

#count(item): Returns the number of occurrences of the specified item in the list.
my_list = [1, 2, 2, 3, 3, 3]
count = my_list.count(2)
# Result: count is 2

#extend(iterable): Appends the elements of the iterable to the list.
my_list = [1, 2, 3]
my_list.extend([4, 5, 6])
# Result: my_list is now [1, 2, 3, 4, 5, 6]

#index(item, starting index): Returns the index of the first occurrence of the specified item.By default starting index is 0.
my_list = [1, 2, 3, 4, 5]
index = my_list.index(3)
# Result: index is 2

#insert(index, item): Inserts the specified item at the specified index.
my_list = [1, 2, 3]
my_list.insert(1, 4)
# Result: my_list is now [1, 4, 2, 3]

#pop(index): Removes and returns the element at the specified index.
my_list = [1, 2, 3]
popped_item = my_list.pop(1)
# Result: my_list is now [1, 3] and popped_item is 2

#remove(item): Removes the first occurrence of the specified item from the list.
my_list = [1, 2, 3, 2]
my_list.remove(2)
# Result: my_list is now [1, 3, 2]

#reverse(): Reverses the elements of the list in place.
my_list = [1, 2, 3]
my_list.reverse()
# Result: my_list is now [3, 2, 1]

#sort(key=None, reverse=False): Sorts the elements of the list in place.
my_list = [3, 1, 2]
my_list.sort()
# Result: my_list is now [1, 2, 3]
```

### Accessing list item

If you notice there is a method `__getitem__` when we access `dir(list)` now what happens in python is that if we want to access the item at index 1 we will type `my_list[1]` but internally in the background what python is doing is `mylist.__.getitem__(1)` and you get the item at index 1.

### Accessing List Slices

Instead of getting a single item from a list we can get a sliced part of the list like

```python
my_list = [1,2,3,4,5]
my_list[1:4]
# Result : [2,3,4], upper limit is not included

#want to get items starting from the first item
my_list[:2] #Not mentioning will be 0 by default here
# Result : [1,2]

#want to get till the last item
my_list[3:]
# Result : [4,5]
```

### Accessing items and Slices with Negative indexes

If we want to get the last item of the list just write

> `my_list[-1]`

result will be the last item of the list

If you want to get last two items of the list just type

> `my_list[-2:]`

And you get the idea.

### Accessing Characters and Slices in Strings

String behave same as list and has the same slicing method.

```python
myString = 'hello'
myList = ['hello', 0, 2,3]

myString[1] #Result : e
myList[0][2] #Result : l
```

### Accessing items in Dictionaries

To access the values in a dictionary we need the key as indexing won't work here like we did in list.

```python
eng_port = {"rain" : "chuva", "sun" : "sol"}
eng_port["sun"] #Result : 'sol'
```

### Creating your own Functions

Lets create a mean function,

```python
# def fuction_name(parameter(s))
def mean(myList):
    the_mean = sum(myList) / len(myList)
    return the_mean

print(mean([1, 4, 5])) #Function call passing argument(s)
print(type(mean),type(sum))
```

> Output : 3.33335
> <class 'function'> <class 'builtin_function_or_method'>

### Function with multiple arguments

Here's an example,

```python
def area(a,b):
    return a * b

print(area(4, 5))
```

> Output : 20

There are different types of arguments in python, they are:

1. **Positional Arguments (Non-Default):**

   - These are the arguments passed to a function based on their position in the function call. They don't have a default value and must be provided when calling the function.

   ```python
   def greet(name, greeting):
       return f"{greeting}, {name}!"

   print(greet("Alice", "Hello"))  # Output: Hello, Alice!
   ```

2. **Default Arguments:**

   - These are the arguments that have a default value specified in the function definition. If a value is not provided during the function call, the default value will be used.

   ```python
   def greet(name, greeting="Hello"):
       return f"{greeting}, {name}!"

   print(greet("Bob"))  # Output: Hello, Bob!
   ```

3. **Keyword Arguments (Non-Default):**

   - These are the arguments passed to a function using their corresponding parameter names. They don't rely on position and can be passed in any order.

   ```python
   def greet(name, greeting):
       return f"{greeting}, {name}!"

   print(greet(greeting="Hi", name="Charlie"))  # Output: Hi, Charlie!
   ```

4. **Arbitrary Positional Arguments (\*args):**

   - These are used when you want to accept any number of positional arguments. They are captured as a tuple inside the function.

   ```python
   def greet(*names, greeting="Hello"):
       return [f"{greeting}, {name}!" for name in names]

   print(greet("Alice", "Bob"))  # Output: ['Hello, Alice!', 'Hello, Bob!']
   ```

5. **Arbitrary Keyword Arguments (**kwargs):\*\*

   - These are used when you want to accept any number of keyword arguments. They are captured as a dictionary inside the function.

   ```python
   def greet(**kwargs):
       return [f"{kwargs['greeting']}, {name}!" for name in kwargs['names']]

   print(greet(names=["Alice", "Bob"], greeting="Hi"))  # Output: ['Hi, Alice!', 'Hi, Bob!']
   ```

6. **Combining all types:**

   - You can combine all types of arguments in a single function definition. However, the order should be: positional arguments, default arguments, arbitrary positional arguments (\*args), keyword arguments, and arbitrary keyword arguments (\*\*kwargs).

   ```python
   def complex_function(a, b, c=0, *args, d, e=10, **kwargs):
       print(f"a: {a}, b: {b}, c: {c}, d: {d}, e: {e}, args: {args}, kwargs: {kwargs}")

   complex_function(1, 2, d=3)  # Output: a: 1, b: 2, c: 0, d: 3, e: 10, args: (), kwargs: {}
   ```

### Print or Return

If you don't return anything in your function then by default python will return none. Even if you print the value you will still get none, so for example

```python
# def fuction_name(arguments)
def mean(myList):
    the_mean = sum(myList) / len(myList)
    print(the_mean) # printing instead of returning

my_mean = mean([1, 4, 5]) #Function call
print(my_mean)

```

> Output : 3.33335
> None

if we try

> `print(my_mean + 10)`

this will give an error. As it is trying to add a None type to a number.

### if else Condition

In the same program imagine that the value that is pass as an argument can be either a list or a dictionary, how will be manage that. In such situation we will use the help of If Conditinal statement. Here is how

```python
def mean(data):
    if type(data) == dict:
        the_mean = sum(data.values()) / len(data)
    else :
        the_mean = sum(data) / len(data) #for list values

    return the_mean
```

You can also check if your data is dict or not using `isinstance` fuction in python like `isinstance(data, dict)` if that's true it will return `True` otherwise `False` and that is what the if statement checks.

You learned to check for one single condition:

```python
x = 1

if x == 1:
    print("Yes")
else:
    print("No")
```

You can also check if two conditions are met at the same time using an and operator:

```python
x = 1
y = 1

if x == 1 and y==1:
    print("Yes")
else:
    print("No")
```

That will return Yes since x == 1 and y ==1 are both True.

You can also check if one of two conditions are met using an or operator:

```python
x = 1
y = 1

if x == 1 or y==2:
    print("Yes")
else:
    print("No")
```

That will return Yes since at least one of the conditions is True. In this case x == 1 is True.

Note: we can check multiple conditions using else if statement which is written in python like `elif`.

> **Indentation is very important in python, mistake in that can lead to many unwanted errors**

### User Input

You can take the user input while your program runs by using `input()` function. Just take a variable to store and make it equal to `input("Message that you want to show before user gives a input")` and that value will be stored in that variable which you can use where ever you like.

But there is a catch, the input fuction will only take string as an input so even if the user give a number lets say 7 as a input it will automatically be converted into a string '7'.

To handle this situation you can use the type conversion, here's how

```python
def weather(temp):
    if temp > 7:
        return "Warm"
    else:
        return "Cold"

user_input = float(input("Enter Temperature")) #Converted string to float
print(weather(user_input))
```

### String Formatting

- You can format strings with (works both on **Python 2 and 3**):

```python
name = "Sim"
experience_years = 1.5
print("Hi %s, you have %s years of experience." % (name, experience_years))
```

> Output: Hi Sim, you have 1.5 years of experience.

- You can also format strings with (**Python 3 only**):

```python
name = "Sim"
experience_years = 1.5
print("Hi {}, you have {} years of experience".format(name, experience_years))
```

> Output: Hi Sim, you have 1.5 years of experience.

```python
name = 'Sooraj'
age = 23
print(f"Hello, My name is {name} and I'm {age} years old.")
```

> Output: Hello, My name is Sooraj and I'm 23 years old.

### For Loops

We we want to go one by one to each items of a list, a string or a tuple then the easiest way to achieve that is by using the for loop. Here is how

```python
mon_temp = [9.1, 4.5, 8.9]

# Syntax to write a for loop: for variable_for_iteration in list:

for temp in mon_temp:
    print(round(temp))

#for string you can do
for letter in 'hello':
    print(letter)

#or you could have simply store that string in a variable and perform the same to that variable, not an issue
```

Output:

> 9 <br>
> 5 <br>
> 9<br>
> h <br>
> e <br>
> l<br>
> l <br>
> o <br>

Note: If you simply want to perform a task from 1 to n times then it do not mean you need a list of 1-n for that you can simply use the `range()` function in python to achieve that.

```python
for day in range(1, 8):
    distance = 3 + (day - 1) * 0.5
    print(f"Day {day}: Run {distance:.1f} miles")
```

Output:

> Day 1: Run 3.0 miles <br>
> Day 2: Run 3.5 miles <br>
> Day 3: Run 4.0 miles <br>
> Day 4: Run 4.5 miles <br>
> Day 5: Run 5.0 miles <br>
> Day 6: Run 5.5 miles <br>
> Day 7: Run 6.0 miles <br>

But what if you want to itterate over dictionary ?

Well it's similar to itteration over a list but with a small change that you can specify if you want to itterate over items or keys or just values. Here's how

**You can loop over dictionary keys**:

```python
phone_numbers = {"John Smith":"+37682929928","Marry Simpons":"+423998200919"}
for key in phone_numbers.keys():
    print(key)
```

Output:

> John Smith<br>
> Marry Simpsons

**You can loop over dictionary values**:

```python
phone_numbers = {"John Smith":"+37682929928","Marry Simpons":"+423998200919"}
for value in phone_numbers.values():
    print(value)
```

Output:

> +37682929928 <br>
> +423998200919

**You can loop over dictionary items**:

```python
phone_numbers = {"John Smith":"+37682929928","Marry Simpons":"+423998200919"}
for key, value in phone_numbers.items():
    print(key, value)
```

Output: (as tuple)

> ('John Smith', '+37682929928')<br>
> ('Marry Simpons', '+423998200919')

One can also do something like

```python
phone_numbers = {"John Smith": "+37682929928", "Marry Simpons": "+423998200919"}

for pair in phone_numbers.items():
    print("{} has as phone number {}".format(pair[0], pair[1]))
```

Output:

> John Smith has as phone number +37682929928 <br>
> Marry Simpons has as phone number +423998200919

or can put key and value named variable instead

Note : If you simply type `for var_name in dictionary:` and print var_name you will get the keys in that dict one by one, but if you type `for var1 , var2 in dictionary` you will expect it gives you key and value one by one but it will give you an **Error**, in that case `.items()` method is needed.

### While Loop

A while loops run as long as the given condition is true. That means you can get an infinity loop if the condition never becomes false for example

```python
a = 5
while a > 0:
    print("Infinity Loop")
```

Let's look at an example which makes more sence why we use while loop

```python
username = ''

while username != "python": #!= means not equals to
    username = input("Enter username: ")
```

the program will keep running till the user input python, once he does the condition becomes false and the loop ends.

There are two important syntaxs that we can use inside a loop to make it more custom they are:

1. **break:**

   - `break` is used to exit a loop prematurely. When encountered, it immediately terminates the loop and continues with the code that follows the loop.

   ```python
   for i in range(5):
       if i == 3:
           break
       print(i)
   # Output: 0 1 2
   ```

2. **continue:**
   - `continue` is used to skip the current iteration of a loop and move to the next iteration without executing the remaining code in the loop block.
   ```python
   for i in range(5):
       if i == 2:
           continue
       print(i)
   # Output: 0 1 3 4
   ```

In the `break` example, the loop terminates when `i` reaches 3, and the code after the loop is executed.

In the `continue` example, when `i` is equal to 2, the `print(i)` statement is skipped for that iteration, and the loop proceeds to the next iteration.

### List Comprehension

List comprehension is a concise and efficient way to create lists in Python. It allows you to generate a new list by applying an expression to each item in an existing iterable, such as a list, tuple, or range.

Here's the basic syntax of list comprehension:

```python
new_list = [expression for item in iterable if condition]
```

- `expression` is the operation you want to perform on each item in the iterable.
- `item` is a variable representing each element in the iterable.
- `iterable` is the existing iterable (e.g., list, tuple, range) you want to iterate over.
- `condition` is an optional filter that specifies whether to include the item in the new list.

Here's an example to illustrate list comprehension:

```python
# Example 1: Square of numbers from 1 to 5 using list comprehension (only for loop)
squared_numbers = [x ** 2 for x in range(1, 6)]
print(squared_numbers)  # Output: [1, 4, 9, 16, 25]

# Example 2: Filter even numbers from a list using list comprehension (if)
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
even_numbers = [x for x in numbers if x % 2 == 0]
print(even_numbers)  # Output: [2, 4, 6, 8, 10]

# Example 3: Flatten a 2D list using list comprehension (loop within loop)
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
flattened_matrix = [x for row in matrix for x in row]
print(flattened_matrix)  # Output: [1, 2, 3, 4, 5, 6, 7, 8, 9]

# Example 4: Convert even numbers to their squares and odd numbers to their cubes using list comprehension (if-else)
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
modified_numbers = [x ** 2 if x % 2 == 0 else x ** 3 for x in numbers]
print(modified_numbers)  # Output: [1, 4, 27, 16, 125, 36, 343, 64, 729, 100]

```

In each example:

- We define a new list using list comprehension.
- We specify the expression to apply to each item in the iterable (`x ** 2`, `x`, `x for x in row`).
- We iterate over the existing iterable (`range(1, 6)`, `numbers`, `matrix`).
- Optionally, we include a condition to filter items (`if x % 2 == 0`).

List comprehension is not only concise but also often more readable than traditional looping constructs, making your code more compact and expressive.

### File Processing in Python

File processing in Python involves reading from and writing to files. Python provides built-in functions and methods for file handling. Here's a basic overview:

1. Opening a File:

To open a file, you can use the built-in `open()` function. It takes two arguments: the file path and the mode (read, write, append, etc.). The most common modes are:

- `'r'`: Read mode (default). Opens a file for reading.
- `'w'`: Write mode. Opens a file for writing. Creates a new file if it doesn't exist or truncates the file if it exists.
- `'a'`: Append mode. Opens a file for appending data. Creates a new file if it doesn't exist.
- `'b'`: Binary mode. Used for reading or writing binary data.
- `'t'`: Text mode (default). Used for reading or writing text data.

there are more....

2. Reading from a File:

You can read from a file using various methods like `read()`, `readline()`, or `readlines()`.

```python
# Reading from a file
with open('file.txt', 'r') as file:
    content = file.read()
    print(content)
```

3. Writing to a File:

You can write to a file using methods like `write()` or `writelines()`. You may not need to have that file exist at the moment, the open function will create it at runtime. If the file already exist then write method will overwrite the existing file if open in 'w'.

```python
# Writing to a file
with open('file.txt', 'w') as file:
    file.write('Hello, World!\n')
    file.write('This is a new line.')
```

4. Appending to a File:

To append data to an existing file, you can open the file in append mode (`'a'`).

```python
# Appending to a file
with open('file.txt', 'a') as file:
    file.write('\nAppending new content.')
```

5. Closing a File:

It's good practice to close a file after you're done with it. However, using a context manager (`with` statement) automatically closes the file when the block is exited, even if an exception occurs.

```python
# Closing a file manually
file = open('file.txt', 'r')
content = file.read()
file.close()
```

6. Exception Handling:

When working with files, it's important to handle exceptions, especially when dealing with file I/O operations.

```python
try:
    with open('file.txt', 'r') as file:
        content = file.read()
except FileNotFoundError:
    print("File not found!")
except IOError:
    print("Error reading file!")
```

File processing in Python is versatile and allows you to handle various file formats and operations efficiently.

Another useful mode in file proccessing is the **'+'** mode

In file processing, the `'+'` mode in the `open()` function allows you to perform both read and write operations on the same file. It's essentially a combination of `'r+'` (read and write) or `'w+'` (write and read), depending on whether the file is intended to be opened for reading first or writing first.

Here's how the `'+'` mode works with different combinations:

- `'r+'`: Opens the file for both reading and writing. The file must exist; otherwise, an error will be raised. The file pointer is positioned at the beginning of the file.

  ```python
  with open('file.txt', 'r+') as file:
      data = file.read()  # Read data from the file
      file.write('New content')  # Write data to the file
  ```

- `'w+'`: Opens the file for both reading and writing. If the file exists, it will be truncated (emptied). If the file does not exist, a new file will be created. The file pointer is positioned at the beginning of the file.

  ```python
  with open('file.txt', 'w+') as file:
      file.write('New content')  # Write data to the file
      file.seek(0)  # Move the file pointer to the beginning
      data = file.read()  # Read data from the file
  ```

The `'+'` mode allows you to perform read and write operations within the same file object. It's useful when you need to both read from and write to a file without having to close and reopen it for different modes. However, you should be careful with the file pointer position, as it can affect the behavior of read and write operations.

**Extra Note for Deep learners**

Here's how the `with` statement, `as` keyword, and `open()` function work together for file processing:

```python
with open('file.txt', 'r') as file:
    content = file.read()
    # File processing operations...
# File is automatically closed when exiting the block
```

In this example:

- `open('file.txt', 'r')` opens the file named 'file.txt' in read mode and returns a file object.
- The `with` statement creates a context manager that automatically closes the file when the block is exited, even if an exception occurs.
- `as file` assigns the file object returned by `open()` to the variable `file`.
- Inside the block, you can perform file processing operations using the `file` variable.
- Once the block is exited, the file is automatically closed, releasing any system resources associated with it.

Using the `with` statement and the `open()` function in this way ensures that files are properly closed after use, which helps prevent resource leaks and makes code more robust.

### File Cursor

The file cursor, also known as the file pointer or file position indicator, refers to the current position within a file where the next read or write operation will occur.

In Python, when you read from or write to a file, the cursor moves automatically to keep track of the current position within the file. After reading or writing data, the cursor moves to the end of the data that was read or written, ready for the next operation.

You can control the position of the cursor within the file using methods like `seek()` and `tell()`.

- `seek(offset, whence)`: Moves the cursor to a specified position within the file.
  - `offset`: The number of bytes to move the cursor by.
  - `whence`: Specifies the reference point for the offset:
    - `0` (default): From the beginning of the file.
    - `1`: From the current cursor position.
    - `2`: From the end of the file.
- `tell()`: Returns the current position of the cursor within the file.

Here's an example demonstrating the use of `seek()` and `tell()`:

```python
with open('file.txt', 'r') as file:
    # Read the first 10 bytes
    data = file.read(10)
    print(data)  # Output: First 10 bytes of the file

    # Get the current cursor position
    position = file.tell()
    print(position)  # Output: Current position of the cursor

    # Move the cursor to the beginning of the file
    file.seek(0)

    # Read the entire file from the beginning
    content = file.read()
    print(content)  # Output: Entire content of the file
```

In this example:

- We read the first 10 bytes of the file and print them.
- We use `tell()` to get the current position of the cursor.
- We use `seek(0)` to move the cursor to the beginning of the file.
- We read the entire file from the beginning and print its content.

### Python Modules

In Python, a module is a file containing Python code. The code can define functions, classes, and variables that can be imported and used in other Python scripts.

There are three important types of modules that we are concerned about in this section, so let's discuss them one by one:

<ol type="A">
<li> <b>Builtin Modules</b>

Python comes with a rich set of built-in modules that provide various functionalities for tasks ranging from file I/O to mathematics to networking. Here are some commonly used built-in modules in Python:

- **os**: Provides a way to interact with the operating system, including file operations, directory manipulation, and environment variables.

```python
import os
print(os.getcwd())  # Get current working directory
```

- **sys**: Contains system-specific parameters and functions, such as command line arguments and the Python runtime environment.

```python
import sys
print(sys.version)  # Get Python version
```

- **math**: Offers mathematical functions and constants for various mathematical operations.

```python
import math
print(math.sqrt(16))  # Calculate square root
```

- **random**: Provides functions for generating random numbers and selecting random elements from sequences.

```python
import random
print(random.randint(1, 10))  # Generate random integer between 1 and 10
```

- **datetime**: Allows manipulation of dates, times, and time intervals.

```python
import datetime
print(datetime.datetime.now())  # Get current date and time
```

- **json**: Provides functions for encoding and decoding JSON data.

```python
import json
data = {'name': 'John', 'age': 30}
json_string = json.dumps(data)  # Convert dictionary to JSON string
print(json_string)
```

- **re**: Offers support for regular expressions, allowing pattern matching and search operations.

```python
import re
pattern = r'\b\w{5}\b'  # Match words with exactly 5 characters
text = 'Python is a powerful language'
matches = re.findall(pattern, text)
print(matches)
```

- **urllib**: Contains functions for working with URLs, such as opening URLs and parsing URL components.

```python
import urllib.request
response = urllib.request.urlopen('https://www.python.org/')
print(response.read())
```

These are just a few examples of the many built-in modules available in Python. You can explore the Python documentation to discover more built-in modules and their functionalities.

**Here's how you can get a list of all the Inbuilt module in you python enviroment**

- Open a command shell or terminal.
- Run the Python interpreter by typing python or python3 depending on your system configuration.
- Once in the Python interpreter, type the following command:

```python
help('modules')
```

- Press Enter.

This command will display a list of all available built-in modules in Python. You can scroll through the list to see the names of the modules. Keep in mind that this list may be extensive, depending on the Python installation and installed packages.

You can also use this command to search for specific modules by providing a search term:

```python
help('modules regex')
```

This will display a list of modules that contain the word "regex" in their names or documentation. Replace "regex" with any search term you're interested in.

You can check the functionality of a particular module in Python by using the `help()` function or by inspecting the module's documentation. Here are a few methods to do so:

1. **Using the `help()` function:**

   - Open a Python shell or a script.
   - Import the module you want to inspect.
   - Use the `help()` function with the module name as an argument.

   ```python
   import module_name
   help(module_name)
   ```

   **q** to quit the help viewer and return to the Python prompt.

   This will display the documentation for the module, including information about its functions, classes, and other attributes.

2. **Using the `dir()` function:**

   - Open a Python shell or a script.
   - Import the module you want to inspect.
   - Use the `dir()` function with the module name as an argument.

   ```python
   import module_name
   print(dir(module_name))
   ```

   This will display a list of all the attributes (functions, classes, variables) in the module.

3. **Using online documentation:**
   - Many modules have online documentation available, either on the official Python documentation website or on other platforms.
   - You can search for the module name along with "Python documentation" to find the official documentation.

There is another way of getting all the builtin modules in python which is

```python
import sys
sys.builtin_module_names
```

the only major difference between this and `help(modules)` is
Output:

- import sys; sys.builtin_module_names: This code returns a tuple containing the names of all built-in modules available in Python.
- help('modules'): This command displays a list of all available modules, including both built-in modules and third-party modules that are currently importable in the Python environment.

<li> <b>Standard Python Modules</b>

Standard Python modules are modules that come built-in with the Python programming language. These modules are part of the Python Standard Library, which is a comprehensive library of modules and packages that provide functionality for a wide range of tasks, such as file I/O, networking, mathematics, data processing, and more. Standard Python modules are available for use without the need for any additional installation or setup.

Some examples of standard Python modules include:

1. **os**: Provides operating system interfaces for tasks such as file and directory operations, environment variables, and process management.

2. **sys**: Provides access to system-specific parameters and functions, including command-line arguments, Python runtime environment, and interpreter settings.

3. **math**: Contains mathematical functions and constants for tasks such as arithmetic operations, trigonometry, logarithms, and more.

4. **datetime**: Offers classes for working with dates, times, time zones, and time intervals.

5. **random**: Provides functions for generating random numbers, selecting random elements from sequences, and shuffling sequences.

6. **re**: Supports regular expressions for pattern matching and search operations on strings.

7. **json**: Allows encoding and decoding JSON data, facilitating interoperability with JSON-formatted data.

8. **urllib**: Contains functions for working with URLs, such as opening URLs, parsing URL components, and sending HTTP requests.

These are just a few examples of the many standard Python modules available in the Python Standard Library. Standard Python modules are extensively documented and can be readily used in Python scripts and applications to simplify development and streamline common tasks.

<li> <b>Third-Party Modules</b>

Third-party modules in Python are modules developed by individuals or organizations outside of the Python core development team. These modules extend the functionality of Python by providing additional features, tools, and libraries for specific tasks or domains. Unlike standard Python modules, third-party modules are not included in the Python Standard Library and need to be installed separately using package managers like pip.

Some common reasons for using third-party modules include:

1. **Specialized Functionality**: Third-party modules often provide specialized functionality that may not be available in the Python Standard Library. For example, modules for web scraping, data visualization, machine learning, etc.

2. **Community Contributions**: The Python community is vast and diverse, and many developers contribute to the ecosystem by creating and maintaining third-party modules. These modules are often open-source and benefit from community-driven development and support.

3. **Rapid Development**: Using third-party modules can accelerate development by providing pre-built solutions to common problems. Instead of reinventing the wheel, developers can leverage existing modules to quickly implement features and functionalities.

4. **Domain-specific Tools**: Third-party modules cater to specific domains or industries, providing tools and libraries tailored to those needs. For example, modules for scientific computing, game development, finance, etc.

5. **Flexibility and Customization**: Third-party modules offer flexibility and customization options, allowing developers to choose the modules that best suit their project requirements. This modular approach promotes code reuse and modularity.

To use a third-party module in your Python project, you typically need to install it using a package manager like pip. For example:

```bash
pip install module_name
```

Once installed, you can import the module in your Python code and use its functionalities as needed.

```python
import module_name
```

Some popular third-party modules in the Python ecosystem include NumPy, pandas, requests, matplotlib, TensorFlow, Django, Flask, SQLAlchemy, and many more. These modules play a crucial role in expanding the capabilities of Python and empowering developers to build diverse and innovative applications.

<ol type="A">

**Extra Notes on Modules**

- _Builtin objects_ are all objects that are written inside the Python interpreter in C language.

- _Builtin modules_ contain builtins objects.

- Some builtin objects are not immediately available in the global namespace. They are parts of a builtin module. To use those objects the module needs to be imported first. E.g.:

```python
import time
time.sleep(5)
```

- A list of all builtin modules can be printed out with:

```python
import sys
sys.builtin_module_names
```

- _Standard libraries_ is a jargon that includes both builtin modules written in C and also modules written in Python.

- _Standard libraries_ written in Python reside in the Python installation directory as .py files. You can find their directory path with sys.prefix.

- _Packages_ are a collection of .py modules.

- _Third-party libraries_ are packages or modules written by third-party persons (not the Python core development team).

- Third-party libraries can be _installed_ from the terminal/command line:

Windows:

> pip install pandas

Mac and Linux:

> pip3 install pandas

---
