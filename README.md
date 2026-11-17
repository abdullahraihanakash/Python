# Python A to Z — Complete Learning Guide

Welcome! This README is a practical, beginner-friendly guide to **Python**, from your first program to professional development topics. You can read it from top to bottom, copy the examples, run them on your computer, and use the exercises to practise.

The examples use modern Python 3. Some advanced syntax is marked with the minimum Python version it needs. When in doubt, use a recent stable Python 3 release and check the official documentation.

> **How to learn:** Do not only read the code. Type it yourself, run it, change a few values, deliberately make mistakes, and try to explain the result in your own words.

---

## Table of Contents

- [1. What Is Python?](#1-what-is-python)
- [2. What Can You Build with Python?](#2-what-can-you-build-with-python)
- [3. Install Python and Choose an Editor](#3-install-python-and-choose-an-editor)
- [4. Run Your First Python Program](#4-run-your-first-python-program)
- [5. Python Syntax, Indentation, and Comments](#5-python-syntax-indentation-and-comments)
- [6. Variables and Naming Rules](#6-variables-and-naming-rules)
- [7. Built-in Data Types](#7-built-in-data-types)
- [8. Type Conversion and User Input](#8-type-conversion-and-user-input)
- [9. Operators](#9-operators)
- [10. Strings](#10-strings)
- [11. Conditional Statements](#11-conditional-statements)
- [12. Loops](#12-loops)
- [13. Lists](#13-lists)
- [14. Tuples](#14-tuples)
- [15. Sets](#15-sets)
- [16. Dictionaries](#16-dictionaries)
- [17. Comprehensions and Unpacking](#17-comprehensions-and-unpacking)
- [18. Functions](#18-functions)
- [19. Scope and Namespaces](#19-scope-and-namespaces)
- [20. Modules and Imports](#20-modules-and-imports)
- [21. Packages and Virtual Environments](#21-packages-and-virtual-environments)
- [22. Working with Files and Folders](#22-working-with-files-and-folders)
- [23. Handling Errors and Exceptions](#23-handling-errors-and-exceptions)
- [24. Object-Oriented Programming (OOP)](#24-object-oriented-programming-oop)
- [25. Iterators and Generators](#25-iterators-and-generators)
- [26. Decorators](#26-decorators)
- [27. Context Managers](#27-context-managers)
- [28. Type Hints](#28-type-hints)
- [29. Useful Python Standard-Library Modules](#29-useful-python-standard-library-modules)
- [30. Working with JSON and CSV](#30-working-with-json-and-csv)
- [31. Dates and Times](#31-dates-and-times)
- [32. Regular Expressions](#32-regular-expressions)
- [33. Working with APIs and HTTP](#33-working-with-apis-and-http)
- [34. Databases with SQLite](#34-databases-with-sqlite)
- [35. Testing Your Code](#35-testing-your-code)
- [36. Debugging and Logging](#36-debugging-and-logging)
- [37. Concurrency and Asynchronous Python](#37-concurrency-and-asynchronous-python)
- [38. Performance and Memory](#38-performance-and-memory)
- [39. Security Best Practices](#39-security-best-practices)
- [40. Code Style and Professional Practices](#40-code-style-and-professional-practices)
- [41. Python Project Structure](#41-python-project-structure)
- [42. Git and GitHub Workflow](#42-git-and-github-workflow)
- [43. Common Beginner Mistakes](#43-common-beginner-mistakes)
- [44. Practice Problems](#44-practice-problems)
- [45. Project Ideas](#45-project-ideas)
- [46. A Python Learning Roadmap](#46-a-python-learning-roadmap)
- [47. Quick Reference Cheat Sheet](#47-quick-reference-cheat-sheet)
- [48. Glossary](#48-glossary)
- [49. Official Learning Resources](#49-official-learning-resources)

---

## 1. What Is Python?

**Python** is a high-level, general-purpose programming language. It is popular because its syntax is readable and it can be used for many different kinds of software.

A programming language lets us write instructions that a computer can execute. Python code is normally run by the Python interpreter.

### Why learn Python?

- **Readable syntax:** Python code often looks close to everyday language.
- **Versatile:** It is used in web development, automation, data analysis, AI, and more.
- **Large ecosystem:** Many free libraries and tools are available.
- **Cross-platform:** Python programs can run on Windows, macOS, and Linux.
- **Strong community:** Many learning resources and examples are available.

### Is Python compiled or interpreted?

Python is commonly called an interpreted language because you normally run source code through the Python interpreter. In the standard implementation, CPython usually compiles source code to bytecode first and then executes that bytecode in its virtual machine. The exact implementation can differ between Python implementations.

---

## 2. What Can You Build with Python?

| Area | What you can build | Common tools |
|---|---|---|
| Web development | Websites and REST APIs | Django, Flask, FastAPI |
| Data analysis | Reports, charts, data cleaning | pandas, NumPy, Matplotlib |
| Artificial intelligence | Machine learning and AI applications | scikit-learn, PyTorch, TensorFlow |
| Automation | File organisers, repetitive-task scripts | `pathlib`, `shutil`, `os`, `requests` |
| Desktop applications | Desktop utilities and tools | Tkinter, PySide |
| Testing | Automated software tests | `unittest`, pytest |
| Networking | Network tools and clients | `socket`, `asyncio`, `requests` |
| Games | Simple 2D games and prototypes | Pygame |

Python is not always the best choice for every job. For example, a browser's front-end normally uses JavaScript or TypeScript. Choose a language and tools based on the problem you need to solve.

---

## 3. Install Python and Choose an Editor

### Install Python

1. Open the official download page: <https://www.python.org/downloads/>.
2. Download a stable Python 3 release for your operating system.
3. On Windows, enable **Add Python to PATH** in the installer when that option is shown.
4. Complete the installation.
5. Open a new terminal and check the installation.

Commands to check Python:

```bash
# Windows launcher
py --version

# Common command on macOS and Linux
python3 --version

# This command may also work on Windows
python --version
```

The output should show a Python 3 version.

### Choose a code editor

- **Visual Studio Code:** A popular editor. Install the Python extension from Microsoft.
- **PyCharm:** An IDE with many Python development features.
- **IDLE:** A simple editor included with many Python installations.

Official downloads:

- Python: <https://www.python.org/downloads/>
- Visual Studio Code: <https://code.visualstudio.com/>
- PyCharm: <https://www.jetbrains.com/pycharm/>

### Check that Python and pip work

```bash
# Windows
py --version
py -m pip --version

# macOS / Linux
python3 --version
python3 -m pip --version
```

Using `python -m pip` or `py -m pip` helps ensure that pip belongs to the Python interpreter you are using.

---

## 4. Run Your First Python Program

Create a file named `hello.py`:

```python
print("Hello, World!")
```

Run it from the terminal:

```bash
# Windows
py hello.py

# macOS / Linux
python3 hello.py
```

Output:

```text
Hello, World!
```

`print()` displays information in the terminal.

### The Python interactive shell

Run `py` on Windows or `python3` on macOS/Linux without a filename. You will enter the Python interactive shell, where you can test expressions one at a time.

```pycon
>>> 10 + 5
15
>>> print("Python is fun")
Python is fun
```

Enter `exit()` to leave the shell.

---

## 5. Python Syntax, Indentation, and Comments

Python uses indentation (spaces at the start of a line) to group statements into blocks. Use **four spaces** per indentation level. Do not mix tabs and spaces.

```python
age = 20

if age >= 18:
    print("You are an adult.")
    print("You can continue.")

print("This line is outside the if block.")
```

### Comments

A comment is text for people reading the code. Python does not execute it as a statement.

```python
# This is a single-line comment.
price = 100  # This is an inline comment.
```

Use comments to explain *why* something is done when the reason is not obvious. Avoid comments that only repeat the code.

### Docstrings

A docstring describes a module, class, or function. It is written as a string, commonly with triple quotes.

```python
def calculate_area(width, height):
    """Return the area of a rectangle."""
    return width * height
```

---

## 6. Variables and Naming Rules

A **variable** is a name that refers to an object or value.

```python
name = "Akash"
age = 21
height = 1.75
is_learning = True

print(name)
print(age)
```

Python is dynamically typed: you do not normally write a variable's type when assigning it. The type belongs to the value, and a name can later refer to a different type of object.

```python
value = 10
value = "ten"  # Allowed, but avoid confusing type changes in real projects.
```

### Naming rules

- A name can contain letters, numbers, and underscores.
- A name cannot start with a number.
- Names are case-sensitive: `age` and `Age` are different names.
- Do not use Python keywords such as `class`, `if`, or `for` as variable names.
- Use descriptive `snake_case` names for variables and functions.

```python
student_name = "Raihan"
total_price = 450
is_logged_in = False
```

Use `PascalCase` for class names, for example `StudentProfile`.

### Constants

Python does not enforce constants in the same way some languages do. By convention, write names that should not be reassigned in `UPPER_SNAKE_CASE`.

```python
MAX_LOGIN_ATTEMPTS = 5
PI_APPROXIMATION = 3.14159
```

---

## 7. Built-in Data Types

A data type describes the kind of value an object represents.

| Type | Meaning | Example |
|---|---|---|
| `int` | Whole number | `25` |
| `float` | Decimal number | `3.14` |
| `complex` | Complex number | `2 + 3j` |
| `str` | Text | `"Python"` |
| `bool` | True or false | `True` |
| `list` | Ordered, changeable collection | `[1, 2, 3]` |
| `tuple` | Ordered, unchangeable collection | `(1, 2, 3)` |
| `set` | Collection of unique items | `{1, 2, 3}` |
| `dict` | Key-value mapping | `{"name": "Akash"}` |
| `range` | Sequence of integers | `range(5)` |
| `NoneType` | Absence of a value | `None` |

Use `type()` to inspect an object's type:

```python
age = 21
name = "Akash"

print(type(age))   # <class 'int'>
print(type(name))  # <class 'str'>
```

Use `isinstance()` when you need to test whether an object belongs to a type or a class hierarchy:

```python
print(isinstance(21, int))  # True
print(isinstance("21", int))  # False
```

### Mutable and immutable objects

- **Mutable:** The object can be changed after it is created. Examples include lists, dictionaries, and sets.
- **Immutable:** The object cannot be changed after it is created. Examples include integers, floats, strings, and tuples (although a tuple may contain a mutable object).

This difference matters when objects are shared between variables or passed to functions.

---

## 8. Type Conversion and User Input

### Type conversion

Convert values with functions such as `int()`, `float()`, `str()`, and `bool()`.

```python
age_text = "21"
age_number = int(age_text)
price = float("19.99")
message = str(100)

print(age_number + 1)  # 22
print(price)           # 19.99
print(message)         # 100
```

Not every value can be converted. For example, `int("hello")` raises a `ValueError`.

### Get input from a user

`input()` reads a line of text and returns a string.

```python
name = input("Enter your name: ")
print(f"Welcome, {name}!")
```

Convert numeric input before doing arithmetic:

```python
age = int(input("Enter your age: "))
print(f"Next year, you will be {age + 1}.")
```

For a real application, validate input and handle conversion errors rather than assuming that every user enters a valid number.

---

## 9. Operators

Operators perform actions on values.

### Arithmetic operators

| Operator | Meaning | Example result |
|---|---|---|
| `+` | Addition | `8 + 2` → `10` |
| `-` | Subtraction | `8 - 2` → `6` |
| `*` | Multiplication | `8 * 2` → `16` |
| `/` | Division (returns a float) | `8 / 2` → `4.0` |
| `//` | Floor division | `9 // 2` → `4` |
| `%` | Remainder | `9 % 2` → `1` |
| `**` | Power | `2 ** 3` → `8` |

### Comparison operators

```python
x = 10

print(x == 10)  # Equal to: True
print(x != 5)   # Not equal to: True
print(x > 5)    # Greater than: True
print(x < 5)    # Less than: False
print(x >= 10)  # Greater than or equal to: True
print(x <= 10)  # Less than or equal to: True
```

### Logical operators

```python
age = 22
has_id = True

print(age >= 18 and has_id)  # Both conditions must be true.
print(age < 18 or has_id)    # At least one condition must be true.
print(not has_id)            # Reverses a Boolean value.
```

### Assignment operators

```python
score = 10
score += 5  # Same as score = score + 5
score -= 2  # Same as score = score - 2
score *= 2  # Same as score = score * 2
score /= 2  # Same as score = score / 2
```

Other useful operators:

- `in` and `not in` check membership.
- `is` and `is not` check object identity, not value equality.
- `&`, `|`, `^`, `~`, `<<`, and `>>` are bitwise operators.

Use `==` to compare values. Use `is None` to check for `None`:

```python
result = None

if result is None:
    print("No result was returned.")
```

---

## 10. Strings

A string (`str`) is text. You can use single quotes, double quotes, or triple quotes.

```python
first_name = "Abdullah"
last_name = 'Raihan'
message = """This is a
multi-line string."""
```

### Indexing and slicing

Python uses zero-based indexing. A negative index counts from the end.

```python
language = "Python"

print(language[0])    # P
print(language[-1])   # n
print(language[0:2])  # Py
print(language[2:])   # thon
print(language[:3])   # Pyt
print(language[::-1]) # nohtyP
```

The ending position in a slice is not included.

### Common string methods

```python
text = "  learn Python programming  "

print(text.lower())
print(text.upper())
print(text.title())
print(text.strip())
print(text.replace("Python", "JavaScript"))
print(text.find("Python"))
print("apple,banana,mango".split(","))
print(" ".join(["Hello", "World"]))
print("Python".startswith("Py"))
print("Python".endswith("on"))
```

Strings are immutable. Methods such as `replace()` return a new string; they do not change the original string.

### f-strings

Use f-strings to insert values into text. They are usually the clearest choice for formatted output.

```python
name = "Akash"
age = 21
price = 1250.5

print(f"My name is {name} and I am {age} years old.")
print(f"Price: {price:.2f}")  # Two digits after the decimal point.
```

### Escape characters

```python
print("First line\nSecond line")
print("Name:\tAkash")
print("She said, \"Hello!\"")
```

A raw string is useful for text containing backslashes, such as many file paths and regular expressions:

```python
path = r"C:\Users\Admin\Documents"
print(path)
```

---

## 11. Conditional Statements

Conditional statements let a program choose which code to execute.

```python
age = 20

if age >= 18:
    print("Adult")
elif age >= 13:
    print("Teenager")
else:
    print("Child")
```

Python checks the conditions from top to bottom and executes the first matching branch.

### Truthy and falsy values

In a condition, some values behave like `False`: `False`, `None`, numeric zero, and empty collections or strings. Most other values behave like `True`.

```python
username = ""

if username:
    print("Username provided")
else:
    print("Username is empty")
```

### Conditional expression

For a small choice, you can use a conditional expression:

```python
age = 19
status = "Adult" if age >= 18 else "Minor"
print(status)
```

Do not use nested conditional expressions when a normal `if` statement would be easier to read.

### `match` statement (Python 3.10+)

`match` compares a value against patterns. It can be useful when there are several clear cases.

```python
command = "start"

match command:
    case "start":
        print("Starting...")
    case "stop":
        print("Stopping...")
    case "pause":
        print("Pausing...")
    case _:
        print("Unknown command")
```

---

## 12. Loops

Loops repeat instructions.

### `for` loop

A `for` loop visits items in an iterable, such as a list, string, or range.

```python
for number in [1, 2, 3, 4, 5]:
    print(number)
```

### `range()`

`range()` produces a sequence of integers. The stop value is not included.

```python
for number in range(5):
    print(number)  # 0, 1, 2, 3, 4

for number in range(1, 6):
    print(number)  # 1, 2, 3, 4, 5

for number in range(10, 0, -2):
    print(number)  # 10, 8, 6, 4, 2
```

### `while` loop

A `while` loop repeats while its condition is true.

```python
count = 1

while count <= 5:
    print(count)
    count += 1  # Update the value so the loop can eventually finish.
```

Be careful: a loop whose condition never becomes false can run forever.

### `break` and `continue`

- `break` exits the nearest loop.
- `continue` skips the rest of the current iteration and moves to the next one.

```python
for number in range(1, 8):
    if number == 3:
        continue
    if number == 6:
        break
    print(number)
```

### `else` with loops

A loop's `else` block runs when the loop finishes normally, but not when it is ended by `break`.

```python
for number in range(3):
    print(number)
else:
    print("Loop completed without break.")
```

### `enumerate()` and `zip()`

```python
names = ["Asha", "Raihan", "Mina"]

for index, name in enumerate(names, start=1):
    print(index, name)

names = ["Asha", "Raihan"]
scores = [90, 85]

for name, score in zip(names, scores):
    print(f"{name}: {score}")
```

---

## 13. Lists

A list is an ordered, mutable collection. It can contain values of different types, although using one main type is often easier to maintain.

```python
fruits = ["apple", "banana", "mango"]
print(fruits[0])  # apple
print(fruits[-1]) # mango
```

### Change a list

```python
fruits = ["apple", "banana"]

fruits[1] = "orange"       # Change an item.
fruits.append("mango")     # Add one item at the end.
fruits.extend(["grape", "kiwi"])  # Add several items.
fruits.insert(0, "lemon")  # Insert at an index.
fruits.remove("orange")    # Remove the first matching value.
last_item = fruits.pop()    # Remove and return the last item.
del fruits[0]              # Delete by index.
fruits.clear()             # Remove all items.
```

### Useful list operations

```python
numbers = [4, 1, 8, 2]

print(len(numbers))
print(min(numbers))
print(max(numbers))
print(sum(numbers))
print(8 in numbers)

numbers.sort()               # Sorts the original list.
print(numbers)

new_numbers = sorted([4, 1, 8, 2])  # Returns a new sorted list.
```

### Copying a list

Assignment does not make a copy; it creates another reference to the same list.

```python
original = [1, 2, 3]
reference = original
reference.append(4)
print(original)  # [1, 2, 3, 4]

copy_of_list = original.copy()
copy_of_list.append(5)
print(original)       # [1, 2, 3, 4]
print(copy_of_list)   # [1, 2, 3, 4, 5]
```

`.copy()` makes a shallow copy. For nested mutable objects, learn about `copy.deepcopy()` in the `copy` module.

### Sorting with a key

```python
students = [
    {"name": "Asha", "score": 88},
    {"name": "Raihan", "score": 95},
    {"name": "Mina", "score": 81},
]

students.sort(key=lambda student: student["score"], reverse=True)
print(students)
```

---

## 14. Tuples

A tuple is an ordered collection that cannot be structurally changed after it is created.

```python
coordinates = (10, 20)
print(coordinates[0])
print(len(coordinates))
```

A one-item tuple needs a comma:

```python
one_item = (10,)
not_a_tuple = (10)
```

### Tuple unpacking

```python
person = ("Akash", 21, "Bangladesh")
name, age, country = person

print(name)
print(age)
print(country)
```

Tuples are useful for fixed groups of values. A tuple can contain a mutable object, but that does not make the tuple itself structurally mutable.

---

## 15. Sets

A set is an unordered collection of unique, hashable items. It is useful for removing duplicates and performing mathematical set operations.

```python
numbers = {1, 2, 2, 3, 3, 3}
print(numbers)  # Contains each value only once.

empty_set = set()  # {} creates an empty dictionary, not an empty set.
```

### Set methods and operations

```python
fruits = {"apple", "banana"}
fruits.add("mango")
fruits.update(["orange", "grape"])
fruits.discard("banana")  # Does not raise an error if absent.

first = {1, 2, 3}
second = {3, 4, 5}

print(first | second)  # Union
print(first & second)  # Intersection
print(first - second)  # Difference
print(first ^ second)  # Symmetric difference
```

Set order is not a reliable display order. Sort a set when you need ordered output:

```python
print(sorted({5, 2, 8, 1}))
```

---

## 16. Dictionaries

A dictionary (`dict`) stores key-value pairs. Keys must be hashable and unique.

```python
student = {
    "name": "Akash",
    "age": 21,
    "department": "CSE",
}

print(student["name"])
print(student.get("email"))  # Returns None when the key is missing.
```

### Add, update, and delete values

```python
student["email"] = "akash@example.com"  # Add a key.
student["age"] = 22                     # Update a key.
student.update({"city": "Dhaka"})

removed_age = student.pop("age")
del student["city"]
```

### Loop through a dictionary

```python
for key in student:
    print(key)

for value in student.values():
    print(value)

for key, value in student.items():
    print(key, value)
```

### Check whether a key exists

```python
if "name" in student:
    print("Name is available")
```

### Nested dictionaries

```python
users = {
    1: {"name": "Asha", "active": True},
    2: {"name": "Raihan", "active": False},
}

print(users[1]["name"])
```

---

## 17. Comprehensions and Unpacking

Comprehensions provide a compact way to create collections.

### List comprehension

```python
squares = [number ** 2 for number in range(1, 6)]
print(squares)  # [1, 4, 9, 16, 25]

even_squares = [number ** 2 for number in range(10) if number % 2 == 0]
print(even_squares)
```

### Set and dictionary comprehensions

```python
unique_lengths = {len(word) for word in ["cat", "dog", "python"]}

squares = {number: number ** 2 for number in range(1, 4)}

print(unique_lengths)
print(squares)
```

### Generator expression

A generator expression produces values one at a time instead of building a complete list immediately.

```python
square_values = (number ** 2 for number in range(1, 6))

for value in square_values:
    print(value)
```

### Unpacking

```python
first, second, third = [10, 20, 30]
print(first, second, third)

first, *middle, last = [1, 2, 3, 4, 5]
print(first)   # 1
print(middle)  # [2, 3, 4]
print(last)    # 5

numbers = [1, 2, 3]
more_numbers = [0, *numbers, 4]

profile = {"name": "Akash", "age": 21}
updated_profile = {**profile, "city": "Dhaka"}
```

---

## 18. Functions

A function is a reusable block of code. Define it with `def` and call it by using its name.

```python
def greet():
    print("Hello!")

greet()
```

### Parameters and arguments

A parameter is a name in a function definition. An argument is the value passed when calling the function.

```python
def greet_user(name):
    print(f"Hello, {name}!")

greet_user("Akash")
```

### Return values

`return` sends a result back to the caller and ends that function call.

```python
def add(a, b):
    return a + b

result = add(10, 5)
print(result)  # 15
```

A function without an explicit return value returns `None`.

### Default parameters

```python
def greet(name, message="Welcome"):
    return f"{message}, {name}!"

print(greet("Akash"))
print(greet("Asha", "Good morning"))
```

Avoid mutable default arguments such as `items=[]`. The same default list would be reused between calls. Use `None` instead:

```python
def add_item(item, items=None):
    if items is None:
        items = []
    items.append(item)
    return items
```

### Positional and keyword arguments

```python
def create_profile(name, age, city):
    return {"name": name, "age": age, "city": city}

profile = create_profile("Akash", 21, city="Dhaka")
print(profile)
```

### `*args` and `**kwargs`

- `*args` collects extra positional arguments into a tuple.
- `**kwargs` collects extra keyword arguments into a dictionary.

```python
def calculate_total(*prices):
    return sum(prices)

print(calculate_total(100, 200, 50))


def show_profile(**details):
    for key, value in details.items():
        print(f"{key}: {value}")

show_profile(name="Akash", age=21, city="Dhaka")
```

### Lambda functions

A lambda is a small anonymous function containing one expression. Use `def` for complex logic or reusable functions that need a clear name.

```python
square = lambda number: number ** 2
print(square(5))

students = [("Asha", 90), ("Raihan", 95)]
students.sort(key=lambda student: student[1])
```

### Recursion

A recursive function calls itself. It needs a base case so it can stop.

```python
def factorial(number):
    if number < 0:
        raise ValueError("Number must not be negative")
    if number <= 1:  # Base case
        return 1
    return number * factorial(number - 1)

print(factorial(5))  # 120
```

For very deep repetition, a loop is often safer because Python limits recursion depth.

---

## 19. Scope and Namespaces

**Scope** describes where a name can be accessed.

Python commonly follows the **LEGB** lookup rule:

1. **Local:** Inside the current function.
2. **Enclosing:** Inside an enclosing function.
3. **Global:** At the module level.
4. **Built-in:** Names provided by Python, such as `print` and `len`.

```python
message = "global"

def show_message():
    message = "local"
    print(message)

show_message()  # local
print(message)  # global
```

`global` and `nonlocal` can change bindings in outer scopes, but use them carefully. Passing values to functions and returning results is often easier to test.

```python
def make_counter():
    count = 0

    def increment():
        nonlocal count
        count += 1
        return count

    return increment

counter = make_counter()
print(counter())  # 1
print(counter())  # 2
```

---

## 20. Modules and Imports

A **module** is a Python file that contains code you can import and reuse.

Suppose you have two files in the same folder.

`math_tools.py`:

```python
def add(a, b):
    return a + b
```

`main.py`:

```python
import math_tools

print(math_tools.add(10, 5))
```

### Different import styles

```python
import math
print(math.sqrt(25))

from math import pi, sqrt
print(pi)
print(sqrt(36))

import math as mathematics
print(mathematics.factorial(5))
```

Avoid `from module import *` in most projects because it can make it unclear where a name came from.

### The `__name__` check

When a Python file is run directly, its `__name__` is set to `"__main__"`. When imported, its `__name__` is normally the module's name.

```python
def main():
    print("Program started")

if __name__ == "__main__":
    main()
```

This lets a file work both as an importable module and as a program.

---

## 21. Packages and Virtual Environments

A **package** is a way to organise related Python modules. A project often uses packages to keep code manageable.

### Create a virtual environment

A virtual environment gives a project its own Python package installation area. This helps prevent dependency conflicts between projects.

From your project folder:

```bash
# Windows
py -m venv .venv

# macOS / Linux
python3 -m venv .venv
```

Activate it:

```bash
# Windows Command Prompt
.venv\Scripts\activate.bat

# Windows PowerShell
.venv\Scripts\Activate.ps1

# macOS / Linux
source .venv/bin/activate
```

If PowerShell blocks activation because of its execution policy, use Command Prompt or follow the official Python documentation for your system's policy. Do not change security settings without understanding the effect.

When the environment is active, your terminal usually shows `(.venv)`.

Deactivate it:

```bash
deactivate
```

### Install and manage packages with pip

```bash
# Install a package
python -m pip install requests

# Show installed packages
python -m pip list

# Show package information
python -m pip show requests

# Upgrade a package
python -m pip install --upgrade requests

# Uninstall a package
python -m pip uninstall requests
```

On Windows, use `py -m pip` if `python` does not point to the intended interpreter. On macOS/Linux, use `python3 -m pip` when appropriate.

### Record dependencies

```bash
python -m pip freeze > requirements.txt
python -m pip install -r requirements.txt
```

A `requirements.txt` file records package requirements for an environment. For larger projects, learn modern project metadata and dependency management through the Python Packaging User Guide.

### Keep the virtual environment out of Git

Add this to `.gitignore`:

```gitignore
.venv/
__pycache__/
*.py[cod]
.env
.pytest_cache/
.coverage
```

Do not upload `.env` files containing passwords or API keys.

---

## 22. Working with Files and Folders

Python can read, write, create, rename, and delete files.

### Read a text file

```python
with open("notes.txt", "r", encoding="utf-8") as file:
    content = file.read()

print(content)
```

### Write a text file

```python
with open("notes.txt", "w", encoding="utf-8") as file:
    file.write("Learning Python is useful.\n")
```

- `"r"`: read an existing file.
- `"w"`: write; replaces existing content or creates a file.
- `"a"`: append to the end.
- `"x"`: create a new file and fail if it already exists.
- `"b"`: binary mode, such as `"rb"` or `"wb"`.
- `"+"`: allow both reading and writing in supported modes.

### Read a file line by line

```python
with open("notes.txt", "r", encoding="utf-8") as file:
    for line in file:
        print(line.rstrip())
```

### Use `pathlib` for paths

`pathlib` provides an object-oriented way to work with file paths and is usually a good first choice for new code.

```python
from pathlib import Path

project_folder = Path("my_project")
project_folder.mkdir(exist_ok=True)

file_path = project_folder / "notes.txt"
file_path.write_text("Hello from pathlib!", encoding="utf-8")

content = file_path.read_text(encoding="utf-8")
print(content)
print(file_path.exists())
```

### Useful path operations

```python
from pathlib import Path

path = Path("data/report.txt")
print(path.name)    # report.txt
print(path.stem)    # report
print(path.suffix)  # .txt
print(path.parent)  # data
```

Use `shutil` for higher-level file copying and directory operations. Be especially careful with code that deletes files or folders.

---

## 23. Handling Errors and Exceptions

An **exception** is an event that interrupts normal execution. Handle expected problems so a program can respond clearly.

### `try` and `except`

```python
try:
    number = int(input("Enter a number: "))
    print(100 / number)
except ValueError:
    print("Please enter a valid whole number.")
except ZeroDivisionError:
    print("You cannot divide by zero.")
```

### `else` and `finally`

- `else` runs when the `try` block completes without an exception.
- `finally` runs whether an exception occurred or not. It is commonly used for cleanup, although a `with` statement is often better for managing resources.

```python
try:
    number = int("25")
except ValueError:
    print("Invalid number")
else:
    print("Converted:", number)
finally:
    print("Finished")
```

### Raise an exception

Use `raise` when a function cannot continue with invalid input or an invalid state.

```python
def withdraw(balance, amount):
    if amount <= 0:
        raise ValueError("Amount must be greater than zero")
    if amount > balance:
        raise ValueError("Insufficient balance")
    return balance - amount
```

### Create a custom exception

```python
class InsufficientBalanceError(Exception):
    """Raised when an account does not have enough money."""


def withdraw(balance, amount):
    if amount > balance:
        raise InsufficientBalanceError("Not enough money")
    return balance - amount
```

### Good exception-handling habits

- Catch only exceptions you can handle meaningfully.
- Prefer a specific exception over a bare `except:`.
- Do not hide errors silently.
- Keep error messages useful but do not expose secrets or sensitive internal details.
- Use `raise` without an argument inside an `except` block to re-raise the current exception.

---

## 24. Object-Oriented Programming (OOP)

Object-Oriented Programming organises code around **objects** that combine data and behaviour.

Important terms:

- **Class:** A blueprint for creating objects.
- **Object:** An instance of a class.
- **Attribute:** Data stored on an object or class.
- **Method:** A function defined in a class.
- **Constructor:** The initialisation process, commonly implemented with `__init__`.

### Create a class and object

```python
class Student:
    def __init__(self, name, age):
        self.name = name  # Store data on this object.
        self.age = age

    def introduce(self):
        print(f"My name is {self.name}. I am {self.age} years old.")


student_one = Student("Akash", 21)
student_one.introduce()
```

`self` refers to the current instance. Python passes it automatically when you call an instance method through an object.

### Instance attributes and class attributes

```python
class Employee:
    company = "Example Technologies"  # Shared class attribute.

    def __init__(self, name):
        self.name = name  # Instance attribute.

first = Employee("Asha")
second = Employee("Raihan")

print(first.company)
print(second.name)
```

### Inheritance

Inheritance lets a class reuse or extend behaviour from another class.

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print("Some sound")


class Dog(Animal):
    def speak(self):
        print(f"{self.name} says woof!")


dog = Dog("Buddy")
dog.speak()
```

Use inheritance when there is a genuine “is-a” relationship. Composition (putting one object inside another) is often more flexible.

### `super()`

`super()` lets a class call a method from the next class in the method resolution order.

```python
class Person:
    def __init__(self, name):
        self.name = name


class Developer(Person):
    def __init__(self, name, language):
        super().__init__(name)
        self.language = language
```

### Encapsulation and properties

Python uses naming conventions rather than strict private access control. A leading underscore means “internal use by convention.” Double leading underscores trigger name mangling in many class contexts; they do not create absolute privacy.

Use `property` when attribute access needs controlled behaviour:

```python
class Temperature:
    def __init__(self, celsius):
        self.celsius = celsius

    @property
    def celsius(self):
        return self._celsius

    @celsius.setter
    def celsius(self, value):
        if value < -273.15:
            raise ValueError("Temperature cannot be below absolute zero")
        self._celsius = value


temperature = Temperature(25)
print(temperature.celsius)
temperature.celsius = 30
```

### Polymorphism

Different objects can provide methods with the same name. Code can use the method without needing to know the exact class.

```python
class Cat:
    def speak(self):
        return "Meow"

class Dog:
    def speak(self):
        return "Woof"

for animal in [Cat(), Dog()]:
    print(animal.speak())
```

### Class methods and static methods

```python
class User:
    user_count = 0

    def __init__(self, name):
        self.name = name
        User.user_count += 1

    @classmethod
    def total_users(cls):
        return cls.user_count

    @staticmethod
    def is_valid_name(name):
        return isinstance(name, str) and bool(name.strip())


user = User("Akash")
print(User.total_users())
print(User.is_valid_name("Asha"))
```

### Special methods (dunder methods)

Special methods have names such as `__init__`, `__str__`, and `__len__`. They let your objects work with Python's built-in operations.

```python
class Book:
    def __init__(self, title, pages):
        self.title = title
        self.pages = pages

    def __str__(self):
        return self.title

    def __len__(self):
        return self.pages


book = Book("Learn Python", 250)
print(book)       # Uses __str__
print(len(book))  # Uses __len__
```

### Dataclasses

For classes mainly used to store data, `dataclasses` can reduce repeated code.

```python
from dataclasses import dataclass

@dataclass
class Product:
    name: str
    price: float
    in_stock: bool = True


product = Product("Keyboard", 45.5)
print(product)
```

---

## 25. Iterators and Generators

An **iterable** is an object you can loop over. An **iterator** produces items one at a time with `next()`.

```python
numbers = [10, 20, 30]
iterator = iter(numbers)

print(next(iterator))  # 10
print(next(iterator))  # 20
print(next(iterator))  # 30
```

Calling `next()` after the iterator is exhausted raises `StopIteration`.

### Create a generator with `yield`

A generator function uses `yield` to produce values one at a time. Its execution can continue from where it last yielded a value.

```python
def count_up_to(limit):
    number = 1
    while number <= limit:
        yield number
        number += 1

for value in count_up_to(3):
    print(value)
```

Generators can process large sequences without building the entire result in memory at once. They are usually consumed only once.

---

## 26. Decorators

A decorator wraps a function or class to add or change behaviour without rewriting its original code. Decorators are commonly used for logging, timing, access checks, and framework features.

```python
from functools import wraps


def log_call(function):
    @wraps(function)
    def wrapper(*args, **kwargs):
        print(f"Calling {function.__name__}")
        result = function(*args, **kwargs)
        print("Call finished")
        return result
    return wrapper


@log_call
def add(a, b):
    return a + b


print(add(2, 3))
```

`@log_call` is equivalent to assigning `add = log_call(add)`. `functools.wraps` preserves useful metadata from the original function.

---

## 27. Context Managers

A context manager manages setup and cleanup around a block of code. The `with` statement is the common way to use one.

```python
with open("notes.txt", "w", encoding="utf-8") as file:
    file.write("The file closes automatically when the block ends.")
```

The file is closed even if an error occurs inside the block.

You can create a context manager with a class implementing `__enter__` and `__exit__`, or with `contextlib`:

```python
from contextlib import contextmanager

@contextmanager
def simple_session():
    print("Start")
    try:
        yield
    finally:
        print("Clean up")


with simple_session():
    print("Doing some work")
```

---

## 28. Type Hints

Type hints document the types a function expects and returns. Editors and static type-checking tools can use them to find possible mistakes. Python does not normally enforce annotations at runtime.

```python
def add(a: int, b: int) -> int:
    return a + b


def greet(name: str) -> str:
    return f"Hello, {name}!"
```

### Common annotations

```python
from typing import Optional

names: list[str] = ["Asha", "Raihan"]
scores: dict[str, int] = {"Asha": 90, "Raihan": 95}
coordinates: tuple[float, float] = (23.8, 90.4)
unique_ids: set[int] = {1, 2, 3}

# Optional means that the value may be None.
email: Optional[str] = None
```

With Python 3.10+, `str | None` can be used instead of `Optional[str]`:

```python
def find_email(user_id: int) -> str | None:
    return None
```

For more complex types, explore `typing` and a static type checker such as mypy or Pyright.

---

## 29. Useful Python Standard-Library Modules

The **standard library** is a collection of modules included with Python. You can use these without installing a separate package.

| Module | Common use |
|---|---|
| `math` | Mathematical functions |
| `random` | Random values and selections |
| `statistics` | Basic statistical calculations |
| `decimal` | Decimal arithmetic when decimal precision matters |
| `fractions` | Rational numbers |
| `datetime` | Dates and times |
| `time` | Time-related functions and delays |
| `pathlib` | File-system paths |
| `os` | Operating-system interfaces and environment variables |
| `shutil` | Higher-level file operations |
| `sys` | Interpreter and system information |
| `json` | JSON encoding and decoding |
| `csv` | CSV files |
| `re` | Regular expressions |
| `collections` | Specialised collection types |
| `itertools` | Tools for creating and combining iterators |
| `functools` | Higher-order functions and decorators |
| `dataclasses` | Classes for storing structured data |
| `subprocess` | Running external programs |
| `logging` | Application logs |
| `sqlite3` | SQLite database access |
| `unittest` | Built-in testing framework |
| `argparse` | Command-line argument parsing |
| `hashlib` | Cryptographic hash functions |
| `secrets` | Secure random values for secrets and tokens |
| `asyncio` | Asynchronous I/O |

Example:

```python
import math
import random

print(math.sqrt(81))
print(random.choice(["red", "green", "blue"]))
```

Use `secrets`, not the ordinary `random` module, when you need security-sensitive random tokens.

---

## 30. Working with JSON and CSV

### JSON

JSON is a text format commonly used to exchange structured data between applications. Python's `json` module converts between JSON and Python objects.

```python
import json

user = {
    "name": "Akash",
    "age": 21,
    "skills": ["Python", "HTML", "CSS"],
}

# Convert a Python object to a JSON string.
json_text = json.dumps(user, indent=4)
print(json_text)

# Convert a JSON string back to a Python object.
loaded_user = json.loads(json_text)
print(loaded_user["name"])
```

Read and write JSON files:

```python
import json
from pathlib import Path

file_path = Path("user.json")

with file_path.open("w", encoding="utf-8") as file:
    json.dump(user, file, indent=4)

with file_path.open("r", encoding="utf-8") as file:
    saved_user = json.load(file)
```

### CSV

CSV (comma-separated values) is a common format for spreadsheet-like data.

```python
import csv

rows = [
    ["name", "score"],
    ["Asha", 90],
    ["Raihan", 95],
]

with open("scores.csv", "w", newline="", encoding="utf-8") as file:
    writer = csv.writer(file)
    writer.writerows(rows)

with open("scores.csv", "r", newline="", encoding="utf-8") as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
```

For CSV data with named columns, explore `csv.DictReader` and `csv.DictWriter`.

---

## 31. Dates and Times

Use `datetime` to work with dates and times.

```python
from datetime import date, datetime, timedelta

# Current local date and time according to the computer.
now = datetime.now()
today = date.today()

print(now)
print(today)

# Create a specific date.
birthday = date(2005, 5, 10)

# Add seven days.
next_week = today + timedelta(days=7)
print(next_week)

# Format a date/time as text.
print(now.strftime("%Y-%m-%d %H:%M:%S"))
```

Use `strptime()` to parse text into a date/time:

```python
from datetime import datetime

text = "2026-11-17"
parsed_date = datetime.strptime(text, "%Y-%m-%d")
print(parsed_date)
```

For applications that work across time zones, learn about timezone-aware datetimes and `zoneinfo`. A naive datetime does not contain timezone information.

---

## 32. Regular Expressions

A **regular expression** (regex) is a pattern used to search, match, or replace text. Python provides the `re` module.

```python
import re

text = "Contact us at help@example.com"
pattern = r"[\w.-]+@[\w.-]+\.\w+"

match = re.search(pattern, text)
if match:
    print(match.group())
```

Useful functions:

- `re.search()` finds the first match anywhere in the text.
- `re.match()` checks for a match at the beginning.
- `re.fullmatch()` checks whether the whole string matches.
- `re.findall()` returns all matches.
- `re.sub()` replaces matching text.
- `re.compile()` creates a reusable pattern object.

Example replacement:

```python
import re

text = "My phone number is 123-456-7890"
cleaned = re.sub(r"\D", "", text)
print(cleaned)  # 1234567890
```

Regex is powerful, but complex patterns can be difficult to read. For validation of important data, combine clear rules with proper validation rather than relying on a complicated regex alone.

---

## 33. Working with APIs and HTTP

An **API** (Application Programming Interface) is a way for software systems to communicate. A web API commonly uses HTTP requests and returns data such as JSON.

Common HTTP methods:

| Method | Typical purpose |
|---|---|
| `GET` | Read a resource |
| `POST` | Create a resource or submit data |
| `PUT` | Replace a resource |
| `PATCH` | Partially update a resource |
| `DELETE` | Delete a resource |

### Call an API with `requests`

`requests` is a popular third-party HTTP library. Install it inside your virtual environment:

```bash
python -m pip install requests
```

Example using a public test API:

```python
import requests

url = "https://jsonplaceholder.typicode.com/posts/1"

try:
    response = requests.get(url, timeout=10)
    response.raise_for_status()  # Raise an error for HTTP 4xx/5xx responses.
    post = response.json()
    print(post["title"])
except requests.exceptions.Timeout:
    print("The request took too long.")
except requests.exceptions.RequestException as error:
    print(f"Request failed: {error}")
```

Important API habits:

- Set a timeout so a request does not wait forever.
- Check the HTTP status code or call `raise_for_status()`.
- Validate the returned data; do not assume every response has the expected structure.
- Read the API's documentation and respect its rate limits and terms.
- Keep API keys secret. Do not put them directly in source code or commit them to Git.

For built-in HTTP features, Python also includes modules such as `urllib.request` and `http.client`.

---

## 34. Databases with SQLite

A database stores data in a structured way. SQLite is a lightweight relational database included with Python through the `sqlite3` module. It stores a database in a file and does not require a separate database server.

### Create a table and insert data

```python
import sqlite3

connection = sqlite3.connect("students.db")

try:
    cursor = connection.cursor()

    cursor.execute("""
        CREATE TABLE IF NOT EXISTS students (
            id INTEGER PRIMARY KEY AUTOINCREMENT,
            name TEXT NOT NULL,
            age INTEGER NOT NULL
        )
    """)

    cursor.execute(
        "INSERT INTO students (name, age) VALUES (?, ?)",
        ("Akash", 21),
    )

    connection.commit()
finally:
    connection.close()
```

### Read data safely

```python
import sqlite3

with sqlite3.connect("students.db") as connection:
    cursor = connection.execute(
        "SELECT id, name, age FROM students WHERE age >= ?",
        (18,),
    )
    for row in cursor.fetchall():
        print(row)
```

Always use parameterised queries (`?` placeholders with SQLite) for values supplied by users. Do not build SQL by joining untrusted strings into a query; that can cause SQL injection.

Learn SQL fundamentals such as `SELECT`, `INSERT`, `UPDATE`, `DELETE`, `JOIN`, primary keys, foreign keys, indexes, and transactions alongside Python database programming.

---

## 35. Testing Your Code

Testing checks whether code behaves as expected. Tests help prevent bugs when you change a program.

### A simple test with `assert`

```python
def add(a, b):
    return a + b

assert add(2, 3) == 5
assert add(-1, 1) == 0
```

`assert` is useful for development checks, but Python can disable assertions in optimised mode. Do not use `assert` to validate untrusted user input or enforce security rules.

### Use the built-in `unittest` framework

Create `test_math_tools.py`:

```python
import unittest


def multiply(a, b):
    return a * b


class TestMathTools(unittest.TestCase):
    def test_multiply_two_numbers(self):
        self.assertEqual(multiply(3, 4), 12)

    def test_multiply_by_zero(self):
        self.assertEqual(multiply(10, 0), 0)


if __name__ == "__main__":
    unittest.main()
```

Run it:

```bash
python -m unittest
```

### pytest

`pytest` is a popular third-party testing framework. Install it with:

```bash
python -m pip install pytest
```

Example `test_add.py`:

```python
def add(a, b):
    return a + b


def test_add():
    assert add(2, 3) == 5
```

Run:

```bash
python -m pytest
```

Good tests cover normal cases, edge cases, and expected failures. Keep tests repeatable and avoid depending on external services when a small mock or test double will work.

---

## 36. Debugging and Logging

**Debugging** means finding and fixing the cause of a problem.

### Read error messages and tracebacks

When Python raises an exception, it usually displays a traceback. Read the last line first to identify the exception type and message, then inspect the lines above it to locate where the error happened.

Common tools:

- `print()` for quick checks.
- `breakpoint()` to pause execution in the debugger.
- An editor's debugger to step through code and inspect values.
- `pdb`, Python's built-in debugger.

Example:

```python
def divide(a, b):
    breakpoint()  # The debugger pauses here when this line runs.
    return a / b

print(divide(10, 2))
```

Remove unnecessary breakpoints before committing finished code.

### Use logging instead of many print statements

```python
import logging

logging.basicConfig(
    level=logging.INFO,
    format="%(asctime)s %(levelname)s: %(message)s",
)

logging.debug("Detailed debugging information")
logging.info("Application started")
logging.warning("A non-fatal issue occurred")
logging.error("An operation failed")
```

Common levels, from least to most severe: `DEBUG`, `INFO`, `WARNING`, `ERROR`, and `CRITICAL`.

Do not log passwords, access tokens, private user data, or other secrets.

---

## 37. Concurrency and Asynchronous Python

Concurrency helps a program make progress on more than one task during the same period. It is useful for tasks such as network requests, file operations, and background work. The right approach depends on the workload.

### Threading

Threads are often useful for I/O-bound work, where a program spends time waiting for an external operation.

```python
import threading
import time


def worker(name):
    print(f"{name} started")
    time.sleep(1)
    print(f"{name} finished")


thread = threading.Thread(target=worker, args=("Worker 1",))
thread.start()
thread.join()  # Wait for this thread to finish.
print("Main program finished")
```

When multiple threads change shared data, protect shared state appropriately. Race conditions can otherwise occur.

### Multiprocessing

The `multiprocessing` module runs work in separate processes. It can be useful for CPU-bound tasks that need to use multiple processor cores.

```python
from multiprocessing import Process


def worker():
    print("Work running in a separate process")


if __name__ == "__main__":
    process = Process(target=worker)
    process.start()
    process.join()
```

The `if __name__ == "__main__":` guard is especially important for portable multiprocessing programs.

### Asynchronous programming with `asyncio`

`asyncio` supports concurrent I/O using `async` and `await`. It is useful when you have many I/O operations and compatible asynchronous libraries.

```python
import asyncio


async def fetch_data():
    print("Starting a task")
    await asyncio.sleep(1)  # Simulate waiting for I/O.
    print("Task completed")
    return {"status": "success"}


async def main():
    result = await fetch_data()
    print(result)


if __name__ == "__main__":
    asyncio.run(main())
```

Key ideas:

- `async def` defines a coroutine function.
- Calling it creates a coroutine object; it does not run it to completion by itself.
- `await` pauses the coroutine while an awaitable operation completes.
- `asyncio.run()` starts and manages an event loop for a top-level asynchronous program.

Do not use `asyncio` automatically for every program. Normal synchronous code is simpler when concurrency is not needed.

---

## 38. Performance and Memory

Write clear code first. Measure performance before trying to optimise it.

### Big-O basics

Big-O notation describes how an algorithm's work grows as its input grows.

| Complexity | Common example |
|---|---|
| `O(1)` | Average dictionary lookup by key |
| `O(log n)` | Binary search in sorted data |
| `O(n)` | One pass through a list |
| `O(n log n)` | Typical efficient comparison sorting |
| `O(n²)` | Comparing every pair in a simple nested loop |

These are common complexity descriptions, not guarantees for every implementation or input.

### Measure execution time

```python
from timeit import timeit

elapsed = timeit("sum(range(1000))", number=1000)
print(f"Elapsed: {elapsed:.6f} seconds")
```

### Practical performance habits

- Choose an appropriate data structure. A set is often useful for repeated membership checks.
- Avoid repeating expensive work unnecessarily.
- Use generators when you need to process large streams of values.
- Use built-in operations when they express the task clearly.
- Profile real workloads before making changes.
- Consider memory use as well as execution time.

Tools to explore: `timeit`, `cProfile`, and `tracemalloc`.

---

## 39. Security Best Practices

Security should be part of development from the beginning.

1. **Protect secrets:** Keep passwords, API keys, and tokens out of source code and Git.
2. **Use environment variables:** Load configuration and secrets from the environment or a secure secret manager.
3. **Validate input:** Treat data from users, files, APIs, and databases as untrusted.
4. **Use parameterised SQL:** Never assemble SQL values from untrusted strings.
5. **Keep dependencies updated:** Use trusted packages and review what you install.
6. **Handle errors safely:** Do not reveal passwords, secret keys, or sensitive internal details in error messages.
7. **Use HTTPS:** Protect network traffic when communicating with web services.
8. **Limit permissions:** Give programs and users only the access they need.
9. **Avoid unsafe deserialisation:** Never load untrusted data with `pickle`; unpickling can execute code.
10. **Use secure randomness:** Use the `secrets` module for passwords reset tokens, authentication tokens, and other security-sensitive random values.

### Read an environment variable

```python
import os

api_key = os.getenv("API_KEY")

if not api_key:
    raise RuntimeError("API_KEY is not configured")
```

For local development, a `.env` file can be used with a suitable package such as `python-dotenv`. Keep `.env` in `.gitignore`, and provide a safe `.env.example` containing placeholder values only.

---

## 40. Code Style and Professional Practices

Readable code is easier to debug, review, test, and maintain.

### Follow PEP 8

PEP 8 is the Python style guide. Common conventions include:

- Use four spaces for indentation.
- Use `snake_case` for variables and functions.
- Use `PascalCase` for classes.
- Keep lines reasonably short and format code consistently.
- Separate top-level functions and classes with blank lines.
- Use meaningful names.
- Avoid unused imports and unnecessary complexity.

Official guide: <https://peps.python.org/pep-0008/>.

### Example of readable code

```python
def calculate_discount(price: float, discount_percent: float) -> float:
    """Return the final price after applying a percentage discount."""
    if price < 0:
        raise ValueError("Price cannot be negative")

    if not 0 <= discount_percent <= 100:
        raise ValueError("Discount must be between 0 and 100")

    discount = price * (discount_percent / 100)
    return price - discount
```

### Helpful development tools

| Tool | Purpose |
|---|---|
| Ruff | Linting and code formatting |
| Black | Code formatting |
| mypy | Static type checking |
| Pyright | Static type checking |
| pytest | Testing |
| pre-commit | Run checks before commits |
| coverage.py | Measure test coverage |

These are optional third-party tools. Choose a small set that fits your project instead of installing every tool at once.

---

## 41. Python Project Structure

A small project can begin with one file. As it grows, separate responsibilities into modules and folders.

Example structure:

```text
my-python-project/
│
├── src/
│   └── my_app/
│       ├── __init__.py
│       ├── main.py
│       └── helpers.py
│
├── tests/
│   └── test_helpers.py
│
├── .venv/                 # Local virtual environment; do not commit.
├── .gitignore
├── README.md
└── requirements.txt       # Use when your project needs it.
```

This is one possible layout, not a rule for every project. Larger distributable packages may use a `pyproject.toml` file and a packaging configuration.

### Example `helpers.py`

```python
def make_greeting(name: str) -> str:
    return f"Hello, {name}!"
```

### Example `main.py`

```python
from my_app.helpers import make_greeting


def main():
    print(make_greeting("Python learner"))


if __name__ == "__main__":
    main()
```

When using a `src/` layout, install the project into the active environment (often in editable mode during development) or configure your development workflow so Python can import the package correctly. Learn more in the Python Packaging User Guide.

---

## 42. Git and GitHub Workflow

Git tracks changes to your code. GitHub hosts Git repositories and makes it easier to share work and collaborate.

Common commands:

```bash
# Start tracking a project
git init

# Check changed files
git status

# Stage changes
git add .

# Save a version of your work
git commit -m "Add Python practice examples"

# See commit history
git log --oneline

# Add a remote repository
git remote add origin https://github.com/USERNAME/REPOSITORY.git

# Push the main branch
git push -u origin main
```


A common daily workflow is:

1. Pull the latest changes when collaborating.
2. Create a branch for a feature or fix.
3. Make a small, focused change.
4. Run the program and tests.
5. Review `git diff` and `git status`.
6. Commit with a clear message.
7. Push the branch and open a pull request when working with a team.

Do not commit `.venv`, `__pycache__`, local databases containing private information, `.env`, or secret files.

---

## 43. Common Beginner Mistakes

| Mistake | Why it happens | Better approach |
|---|---|---|
| Using `=` instead of `==` in a comparison | Assignment and comparison look similar | Use `=` to assign and `==` to compare |
| Forgetting indentation | Python uses indentation for code blocks | Use four spaces consistently |
| Adding numbers to text without conversion | `input()` returns a string | Convert with `int()` or `float()` when appropriate |
| Using `is` to compare normal values | Identity is confused with equality | Use `==` for value comparison |
| Forgetting that list indexes start at zero | Indexing convention is unfamiliar | First item is at index `0` |
| Changing a list while looping over it | Items may be skipped or processing may become confusing | Build a new list or iterate over a copy |
| Using a mutable default argument | Default objects are created once | Use `None` and create a new object inside the function |
| Catching every exception silently | Errors are hidden | Catch specific exceptions and handle them clearly |
| Forgetting to close files | Resources remain open longer than needed | Use `with open(...)` |
| Installing packages globally for every project | Dependencies can conflict | Use a virtual environment per project |
| Hardcoding API keys | Secrets can leak into source control | Use environment variables or a secret manager |
| Writing all code in one huge file | Responsibilities become mixed | Split related code into modules when needed |

### Understand the difference between `==` and `is`

```python
first = [1, 2]
second = [1, 2]
third = first

print(first == second)  # True: same values
print(first is second)  # False: different list objects
print(first is third)   # True: the same object
```

---

## 44. Practice Problems

Try solving these without looking at a solution first. Start with a working version, then improve the code.

### Beginner

1. Print your name, country, and favourite programming language.
2. Ask for two numbers and print their sum, difference, product, and quotient. Handle division by zero.
3. Ask for an age and print whether the person is a child, teenager, or adult.
4. Print the multiplication table for a number from 1 to 10.
5. Find the largest of three numbers.
6. Count the number of vowels in a string.
7. Reverse a string without using a built-in reverse method.
8. Find the sum of all even numbers from 1 to 100.

### Intermediate

9. Check whether a word is a palindrome.
10. Remove duplicate values from a list while preserving the original order.
11. Find the second-largest unique number in a list.
12. Count how often each word appears in a sentence using a dictionary.
13. Create a function that checks whether a number is prime.
14. Create a number-guessing game with a limited number of attempts.
15. Read a text file and count its lines, words, and characters.
16. Store student names and scores in a dictionary and calculate the average score.

### Advanced

17. Build a contact book with add, search, update, and delete operations.
18. Write a program that reads a CSV file and produces a summary report.
19. Create a class for a bank account with deposit and withdrawal methods.
20. Write unit tests for a calculator module.
21. Use an API to fetch JSON data and handle network errors.
22. Build a SQLite application that stores and searches tasks.
23. Write a generator that reads a large file one line at a time.
24. Build an asynchronous program that runs several independent I/O tasks.

### Suggested way to practise

For each problem:

1. Write down the input, expected output, and rules.
2. Break the problem into small steps.
3. Write pseudocode before complex code.
4. Implement the simplest correct solution.
5. Test normal, boundary, and invalid inputs.
6. Refactor names and functions to improve readability.

---

## 45. Project Ideas

Build projects in increasing difficulty. A finished, well-documented small project is more valuable for learning than many unfinished tutorials.

| Level | Project | Skills you practise |
|---|---|---|
| Beginner | Calculator | Input, conditions, functions |
| Beginner | Unit converter | Numbers, functions, validation |
| Beginner | Number guessing game | Loops, conditions, `random` |
| Beginner | To-do list in the terminal | Lists, functions, file storage |
| Beginner | Password generator | Strings, loops, `secrets` |
| Intermediate | Contact book | Dictionaries, CRUD operations, JSON |
| Intermediate | Expense tracker | CSV/JSON, dates, reports |
| Intermediate | Quiz application | Functions, data structures, file handling |
| Intermediate | File organiser | `pathlib`, `shutil`, error handling |
| Intermediate | Weather/API client | HTTP, JSON, environment variables |
| Intermediate | Library management system | OOP, SQLite, testing |
| Advanced | REST API | FastAPI or Django, HTTP, database design |
| Advanced | Uptime monitoring tool | HTTP checks, scheduling, persistence, logging |
| Advanced | Web scraper | HTTP, HTML parsing, responsible rate limiting |
| Advanced | Data analysis dashboard | pandas, data visualisation, reporting |
| Advanced | Machine-learning project | Data preparation, model training, evaluation |

For every project, try to include a clear README, setup instructions, example usage, tests, and a `.gitignore` file. Never publish real credentials or private user data.

---

## 46. A Python Learning Roadmap

Follow these stages in order. Move forward when you can write and explain small programs without copying every line.

### Stage 1 — Foundations

- Install Python and run scripts.
- Learn variables, data types, operators, and input/output.
- Practise strings and type conversion.
- Use conditions and loops.
- Work with lists, tuples, sets, and dictionaries.

**Goal:** Build a calculator, quiz, and number-guessing game.

### Stage 2 — Core Programming

- Write functions and understand arguments and return values.
- Learn scope, modules, imports, and exceptions.
- Read and write files.
- Use comprehensions and common standard-library modules.
- Understand mutable and immutable objects.

**Goal:** Build a contact book and a file-based to-do application.

### Stage 3 — Intermediate Python

- Learn OOP, inheritance, composition, and dataclasses.
- Use iterators, generators, decorators, and context managers.
- Add type hints.
- Work with JSON, CSV, dates, and regular expressions.
- Create virtual environments and install packages.

**Goal:** Build a tested application that stores data and has a clean project structure.

### Stage 4 — Professional Development

- Use Git and GitHub confidently.
- Learn testing, debugging, logging, and code review.
- Learn SQL and database design.
- Work with HTTP APIs.
- Learn security fundamentals and environment configuration.
- Use formatting, linting, and type-checking tools.

**Goal:** Build and publish a documented API or automation tool.

### Stage 5 — Choose a Specialisation

Choose a direction based on the problems you want to solve:

- **Backend development:** HTTP, REST APIs, FastAPI/Django, SQL, authentication, deployment.
- **Data analysis:** NumPy, pandas, visualisation, statistics, SQL.
- **AI and machine learning:** linear algebra, statistics, data preparation, scikit-learn, PyTorch or TensorFlow.
- **Automation:** file systems, APIs, scheduling, browser automation, reliability.
- **Testing and quality:** pytest, test design, mocking, CI, coverage.

You do not need to learn every framework. Strong fundamentals make it easier to learn new tools when a project requires them.

---

## 47. Quick Reference Cheat Sheet

### Output and input

```python
print("Hello")
name = input("Name: ")
```

### Variables and conversion

```python
age = 21
age = int("21")
price = float("9.99")
text = str(100)
```

### Conditions

```python
if condition:
    pass
elif another_condition:
    pass
else:
    pass
```

### Loops

```python
for item in collection:
    print(item)

while condition:
    break
```

### Functions

```python
def function_name(parameter):
    return parameter
```

### Collections

```python
items = [1, 2, 3]                 # List
fixed_items = (1, 2, 3)           # Tuple
unique_items = {1, 2, 3}          # Set
person = {"name": "Akash"}       # Dictionary
```

### File handling

```python
from pathlib import Path

path = Path("notes.txt")
path.write_text("Hello", encoding="utf-8")
content = path.read_text(encoding="utf-8")
```

### Exception handling

```python
try:
    result = 10 / 2
except ZeroDivisionError:
    print("Cannot divide by zero")
```

### Import a module

```python
import math
print(math.sqrt(16))
```

### Run a script

```bash
# Windows
py main.py

# macOS / Linux
python3 main.py
```

### Install a package

```bash
python -m pip install package_name
```

---

## 48. Glossary

| Term | Easy meaning |
|---|---|
| Algorithm | A step-by-step method for solving a problem |
| Argument | A value passed to a function call |
| API | A defined way for software to communicate |
| Class | A blueprint for creating objects |
| Compiler | A program or tool that translates code into another form |
| Data type | The kind of value an object represents |
| Debugging | Finding and fixing problems in code |
| Exception | An event that interrupts normal program execution |
| Function | A reusable block of code |
| IDE | An application that provides tools for software development |
| Iterable | An object that can provide its items one at a time |
| Iterator | An object that returns the next item when requested |
| Library | Reusable code that a program can use |
| List | An ordered, mutable collection |
| Method | A function associated with a class or object |
| Module | A Python file that can be imported |
| Object | A value with identity, type, and data/behaviour |
| Parameter | A name in a function definition |
| Package | A way to organise related modules |
| PEP 8 | The commonly used Python style guide |
| pip | Python's package installer |
| Recursion | A function calling itself |
| Scope | Where a name can be accessed |
| Script | A file containing instructions to run |
| SQL | A language for working with relational databases |
| Tuple | An ordered collection that cannot be structurally changed |
| Virtual environment | An isolated Python package environment for a project |

---

## 49. Official Learning Resources

Use official documentation as your main reference. Tutorials and videos are useful, but documentation helps you confirm exact behaviour and discover details.

- **Python downloads:** <https://www.python.org/downloads/>
- **Official Python tutorial:** <https://docs.python.org/3/tutorial/>
- **Python language reference:** <https://docs.python.org/3/reference/>
- **Python standard library:** <https://docs.python.org/3/library/>
- **Python HOWTO guides:** <https://docs.python.org/3/howto/>
- **Python FAQ:** <https://docs.python.org/3/faq/>
- **Python style guide (PEP 8):** <https://peps.python.org/pep-0008/>
- **Python Packaging User Guide:** <https://packaging.python.org/>
- **Python Package Index (PyPI):** <https://pypi.org/>
- **Visual Studio Code Python guide:** <https://code.visualstudio.com/docs/languages/python>

---

## Final Advice

Learning Python is not about memorising every keyword or library. It is about learning how to break problems into steps, choose suitable data structures, write clear functions, test your work, and keep improving your solutions.

**A good learning routine:** learn one concept, write a small example, solve two or three exercises, and use that concept in a project. Keep your projects on GitHub with clear documentation so other people can understand what you built.

Happy coding! 🐍
