# Python Essential Training Notes

## 1. First Python Program

Python files use the `.py` extension. A basic script is often named `hello.py`.

To print text to the terminal, use:

```python
print("Hello, World!")
```

The text inside the quotes is called a string. The quotes are required so Python knows the value is text.

Comments start with `#` and are ignored by Python when the program runs:

```python
# This is a comment
print("Hello, World!")
```

### Running a Python file

1. Save the file.
2. Open the terminal.
3. Change to the folder containing the file:

```bash
cd path/to/folder
```

4. Run the script:

```bash
python hello.py
```

### Example

```python
# Welcome to the training
print("Hello, welcome to the training session!")
```

### Key Takeaways
- Python files end with `.py`
- Use `print()` to display output
- Strings must be wrapped in quotes
- `#` creates comments
- You run Python files from the terminal using `python filename.py`

---

## 2. Jupyter Notebooks

Jupyter Notebook is a web-based tool for writing and running Python code. It is part of the Project Jupyter ecosystem and is commonly used for data science, experiments, reports, and teaching.

### File Type
Notebook files use the `.ipynb` extension.

### Why Use Jupyter?
- Great for learning and testing code
- Shows code and output together
- Useful for reports and visualizations
- Easy to share and export

### How It Works
- Open Jupyter Notebook in the browser
- It starts a local web application on your computer
- You create or open notebooks and write code in cells

### Cells
A notebook is made of cells. Each cell can contain:
- Python code
- Markdown text

To run a code cell, use:

```text
Shift + Enter
```

### Command Mode vs Edit Mode
- Click outside a cell to enter Command Mode
- Click inside a cell to enter Edit Mode

### Common Shortcuts
- `A` = add a cell above
- `B` = add a cell below
- `D` + `D` = delete selected cell
- `M` = convert cell to Markdown
- `Y` = convert cell to code

### Markdown Example

```markdown
# Python

## Welcome to the Training
- This is a bullet point
- This is another bullet point
```

### Example Code

```python
print("Welcome to the training")
```

```python
print((151 + 9) / 20)
```

### VS Code Support
Jupyter notebooks can also be opened and edited in Visual Studio Code, which supports notebook editing and execution similar to the browser version.

### Key Takeaways
- Jupyter is useful for interactive Python work
- Notebooks are made of cells
- Use `Shift + Enter` to run code
- You can mix code and markdown in the same notebook
- Notebooks are easy to share in GitHub and other platforms

---

## 3. CoderPad

CoderPad is the coding platform used for the challenges in this course. It is built into the LinkedIn Learning course website and keeps the instructions, answer area, and test output in one place.

### How to Use It
1. Click the challenge to open it
2. Read the instructions carefully
3. Write your solution in the answer panel
4. Run the tests
5. Check the console output for errors

### Interface Layout
- Instructions panel: explains the task
- Answer panel: where you write code
- Test code panel: shows values used to validate the solution
- Console output: displays print statements and errors

### Important Reminder
You are expected to solve the challenge, not just hard-code the answer. The console output helps you debug and understand errors.

### Best Practices
- Read the problem before coding
- Review examples and expected output
- Test small ideas before finalizing
- Use hints when needed
- Focus on learning, not just passing

### Key Takeaways
- CoderPad is used for coding challenges in this course
- It combines instructions and testing in one environment
- The console output is important for debugging
- The goal is to practice problem-solving and improve coding skills

---

# Variables and Types

## Variables
- A variable is a name that refers to a value.
- Use `=` to assign a value to a variable:

```python
x = 5
name = "Ryan"
```

- Use `print()` to display a variable’s value. In a Jupyter Notebook, the value of the last expression in a cell is also displayed automatically.

```python
print(x)
```

## Variable Naming Rules
- Names can contain letters, numbers, and underscores.
- Names cannot start with a number.
- Names are case-sensitive: `name` and `Name` are different variables.
- Python convention is to use lowercase names, often with underscores: `first_name`.
- Avoid spaces and special characters in variable names.

## Common Python Types

| Type | Description | Example |
|---|---|---|
| `int` | Whole number | `5` |
| `float` | Decimal number | `1.5` |
| `complex` | Complex number; uses `j` for the imaginary part | `2j` |
| `str` | Text (string) | `"Hello"` |
| `bool` | Boolean value: true or false | `True`, `False` |

Use `type()` to check a value’s type:

```python
type(5)       # int
type(1.5)     # float
type("Ryan")  # str
```

## Working with Strings
- Strings can use single or double quotes.
- The `+` operator joins strings; this is called concatenation.
- Joining strings that contain digits still produces text:

```python
"1" + "1"  # "11"
```

- A string cannot be directly added to a number. Convert the value to a string first if needed:

```python
"Age: " + str(5)
```

## Booleans and Comparisons
- Boolean values must be capitalized: `True` and `False`.
- Use `==` to compare values. It returns a Boolean.
- A single `=` assigns a value; `==` checks whether values are equal.

```python
x = 5       # Assignment
x == 5      # Comparison; evaluates to True
1 == 2      # Evaluates to False
```

## Key Takeaways
- Variables store or refer to values.
- `=` assigns a value, while `==` compares values.
- Python values have different types, such as `int`, `float`, `str`, and `bool`.
- Use `type()` to inspect a value’s type.
- Read error messages carefully; they often explain what needs fixing.
````

````

---
# Data Structures

Data structures store and organize multiple values. Python’s common built-in structures include lists, sets, tuples, and dictionaries.

## Lists

- Lists use square brackets: `[]`
- They are ordered and can be changed after creation.
- Lists can contain different types of values, including other lists.
- Use `len()` to get the number of items.

```python
my_list = [1, "hello", True]
print(len(my_list))  # 3

my_list.append(4)
print(my_list)
```

## Sets

- Sets use curly braces: `{}`.
- They contain unique values; duplicate values are removed.
- Sets are unordered, so don’t rely on their display order.
- Use `set()` to create an empty set; `{}` creates an empty dictionary.

```python
my_set = {1, 1, 2, 2}
print(my_set)       # {1, 2}
print(len(my_set))  # 2

empty_set = set()
```

## Tuples

- Tuples are ordered and use parentheses: `()`.
- They cannot be changed after creation.
- Use a trailing comma for a tuple with one item.

```python
my_tuple = (1, 2, 3)
print(len(my_tuple))  # 3

single_item = (1,)
```

## Dictionaries

- Dictionaries store key-value pairs and use curly braces.
- Access a value using its key.
- Keys must be unique. Assigning a value to an existing key replaces its previous value.
- Modern Python dictionaries preserve insertion order.

```python
my_dict = {
    "apple": "a red fruit",
    "bear": "a large animal"
}

print(my_dict["apple"])
my_dict["apple"] = "a fruit that can also be green"
```

## Quick Comparison

| Structure | Syntax | Ordered? | Can be changed? | Allows duplicates? |
|---|---|---|---|---|
| List | `[1, 2]` | Yes | Yes | Yes |
| Set | `{1, 2}` | No | Yes | No |
| Tuple | `(1, 2)` | Yes | No | Yes |
| Dictionary | `{"key": "value"}` | Yes, insertion order | Yes | Keys must be unique |

## Key Takeaways

- Use a **list** for an ordered collection that may change.
- Use a **set** when you need unique values.
- Use a **tuple** for an ordered collection that should remain unchanged.
- Use a **dictionary** to look up values by key.
- `len()` returns the number of items in a collection.
````
````
---

# Operators

Operators perform actions on values and variables. They can calculate results, compare values, or check conditions.

## Arithmetic Operators

| Operator | Operation | Example | Result |
|---|---|---|---|
| `+` | Addition | `1 + 1` | `2` |
| `-` | Subtraction | `5 - 2` | `3` |
| `*` | Multiplication | `3 * 4` | `12` |
| `/` | Division | `20 / 5` | `4.0` |
| `**` | Exponentiation | `5 ** 2` | `25` |
| `%` | Modulus (remainder) | `20 % 6` | `2` |

In Python, `/` returns a float, even when the result is a whole number. The `%` operator is useful for finding remainders.

## String Operators

- `+` joins strings together (concatenation).
- `*` repeats a string a specified number of times.
- You cannot directly add a string and a number; convert one type if needed.

```python
"Hello, " + "Python"  # "Hello, Python"
"ha" * 3              # "hahaha"
"Age: " + str(5)      # "Age: 5"
```

## Comparison Operators

Comparison operators return `True` or `False`.

| Operator | Meaning |
|---|---|
| `==` | Equal to |
| `!=` | Not equal to |
| `<` | Less than |
| `<=` | Less than or equal to |
| `>` | Greater than |
| `>=` | Greater than or equal to |

```python
4 < 5    # True
5 <= 5   # True
1 == 2   # False
```

Remember: `=` assigns a value; `==` compares values.

## Logical Operators

Logical operators combine or reverse Boolean values:

- `and` is `True` only when both conditions are true.
- `or` is `True` when at least one condition is true.
- `not` reverses a Boolean value.

```python
True and False  # False
True or False   # True
not True        # False
```

## Membership Operators

Use `in` and `not in` to check whether a value appears in a collection or string.

```python
2 in [1, 2, 3]           # True
10 not in [1, 2, 3]      # True
"cat" in "my pet cat"    # True
```

For strings, membership checks for a substring, so `"cat" in "catatonic"` is also `True`.

## Identity Operators

- `is` checks whether two references point to the same object.
- `is not` checks whether they point to different objects.
- To compare values for equality, use `==`.

## Key Takeaways

- Arithmetic operators perform calculations.
- `+` and `*` can also join and repeat strings.
- Comparison, logical, membership, and identity operators produce Boolean results.
- Pay attention to data types; incompatible operations can raise a `TypeError`.
- Read error messages to help understand and fix problems.
````

````
---

# Control Flow

Control flow determines which parts of a program run and how many times they run. Python uses conditionals and loops to control execution.

## `if` and `else`

An `if` statement runs its indented code block when its condition is true. An `else` block runs when the condition is false.

```python
is_ready = True

if is_ready:
    print("Ready!")
else:
    print("Not ready yet.")
```

Python uses a colon (`:`) to begin a block. Indentation defines which statements belong to that block.

You can use `elif` to check another condition:

```python
score = 75

if score >= 90:
    print("Excellent")
elif score >= 60:
    print("Passed")
else:
    print("Try again")
```

## `for` Loops

A `for` loop runs once for each item in an iterable, such as a list.

```python
numbers = [1, 2, 3, 4, 5]

for number in numbers:
    print(number)
```

The loop variable (`number` here) refers to the current item during each iteration. You can choose its name.

## `while` Loops

A `while` loop repeats as long as its condition is true. Update the condition inside the loop so it eventually becomes false.

```python
count = 0

while count < 5:
    print(count)
    count += 1
```

If the condition never becomes false, the loop can run indefinitely. This is called an infinite loop.

## Key Takeaways

- `if`, `elif`, and `else` let a program choose between actions.
- Indentation is required and determines the structure of Python code blocks.
- Use a `for` loop to process items in an iterable.
- Use a `while` loop when repetition depends on a condition.
- Make sure `while` loops can eventually stop.
````


````
---

# Functions

A function is a reusable block of code that performs a task. It can accept input values, called **arguments**, and return a result.

## Defining and Calling a Function

Use the `def` keyword to define a function. Indent the function body, and call the function by writing its name followed by parentheses.

```python
def multiply_by_three(value):
    return value * 3

result = multiply_by_three(4)
print(result)  # 12
```

- `value` is a **parameter**: a name listed in the function definition.
- `4` is an **argument**: the value passed when calling the function.
- `return` sends a result back to the code that called the function.

A function can have multiple parameters:

```python
def multiply(first, second):
    return first * second

print(multiply(3, 4))  # 12
```

## Functions Without a Return Value

Some functions perform an action rather than returning a result. For example, a function can modify a mutable object such as a list:

```python
def append_four(items):
    items.append(4)

numbers = [1, 2, 3]
append_four(numbers)
print(numbers)  # [1, 2, 3, 4]
```

If a function does not explicitly return a value, Python returns `None` by default. The `print()` function displays output but also returns `None`.

```python
result = print("Hello")
print(result)  # None
```

`None` represents the absence of a value. It has its own type, `NoneType`.

## Naming Functions

- Use descriptive, lowercase names.
- Separate words with underscores, as in `multiply_by_three`.
- Function names follow the same basic naming rules as variable names.

## Key Takeaways

- Define functions with `def`.
- Pass inputs through parameters and arguments.
- Use `return` to send a result back.
- Functions can also perform actions without returning a value.
- A function without a `return` statement returns `None`.
````


````
---

# Classes and Objects

A **class** is a blueprint for creating objects. It groups related data (attributes) and behavior (methods) together. An **object** is an instance created from a class.

## Defining a Class

Class names conventionally use `PascalCase`. The `__init__` method runs when a new instance is created and initializes its attributes.

```python
class Dog:
    def __init__(self, name):
        self.name = name
        self.legs = 4

    def speak(self):
        print(f"{self.name} says bark!")
```

- `self` refers to the current instance.
- `self.name` and `self.legs` are attributes belonging to that instance.
- `speak()` is a method: a function defined inside a class.

## Creating and Using Objects

Call the class to create an instance, then access its attributes and methods with dot notation.

```python
my_dog = Dog("Rover")
another_dog = Dog("Buddy")

print(my_dog.name)  # Rover
my_dog.speak()      # Rover says bark!
another_dog.speak() # Buddy says bark!
```

Each instance has its own attribute values.

## Key Takeaways

- A class describes the data and behavior its objects will have.
- An object is an instance of a class.
- `__init__` initializes a new instance.
- `self` refers to the current instance.
- Use `PascalCase` for class names and lowercase `snake_case` for methods and variables.
````


````
---

# About the Challenges

Coding challenges are an opportunity to practice writing programs independently. Feeling stuck at first is normal—watching code and creating it yourself are different skills.

## A Helpful Approach

1. Read the problem carefully and identify what it asks for.
2. Work through a few examples by hand.
3. Break the task into smaller steps.
4. Write a small amount of code, then run and test it.
5. Read error messages and use them to debug.
6. Review hints or other learning resources when needed.
7. Revisit course videos or notebook examples if a concept is unclear.

## Keep Practicing

- Give yourself time; learning to program takes practice.
- Experiment with code and modify examples.
- Start with small exercises, such as writing a function that returns `"Hello"`.
- Focus on understanding the process, not just finishing the challenge.

## Key Takeaway

Challenges are for learning. Working through confusion, testing ideas, and correcting mistakes are all part of building programming skills.
````

````
---

# Factorials

The factorial of a non-negative integer `n`, written `n!`, is the product of all positive integers from `1` through `n`.

```text
5! = 5 × 4 × 3 × 2 × 1 = 120
0! = 1
```

Factorials are undefined for negative integers. In this example, invalid inputs return `None`.

## Iterative Solution

A loop multiplies a running total by each number from `1` through the input.

```python
def factorial(number):
    if not isinstance(number, int) or number < 0:
        return None

    result = 1
    counter = 1

    while counter <= number:
        result *= counter
        counter += 1

    return result
```

The result starts at `1`, so the loop does not need to run for `0`; the function correctly returns `0! = 1`.

## Recursive Solution

Recursion occurs when a function calls itself. A recursive function needs a **base case** to stop the calls.

```python
def factorial_recursive(number):
    if not isinstance(number, int) or number < 0:
        return None

    if number == 0:
        return 1

    return number * factorial_recursive(number - 1)
```

For example:

```text
factorial_recursive(3)
= 3 × factorial_recursive(2)
= 3 × 2 × factorial_recursive(1)
= 3 × 2 × 1 × factorial_recursive(0)
= 3 × 2 × 1 × 1
= 6
```

## Key Takeaways

- `0!` is `1`.
- Factorials are only defined for non-negative integers.
- An iterative solution uses a loop to build the result.
- A recursive solution calls itself and needs a base case.
- Recursive calls use additional memory; for very large numbers, an iterative approach avoids recursion-depth limits.
````


````
---

# Integers and Floats

Python’s `int` type represents whole numbers, while `float` represents numbers with a fractional part. Mixing integers and floats in arithmetic usually produces a float. The `/` operator always returns a float.

```python
20 / 4       # 5.0
2 + 1.5      # 3.5
2 * 1.5      # 3.0
```

## Converting Between Types

Use `int()` and `float()` to convert values. This is often called **casting**.

```python
int(8.9)     # 8
float(5)     # 5.0
```

`int()` does not round; it removes the fractional part, moving toward zero. To round to the nearest value, use `round()`:

```python
round(4.9)       # 5
round(4.678, 2)  # 4.68
```

## Floating-Point Precision

Floats are stored as finite-precision binary approximations. Some decimal values cannot be represented exactly, which can produce results that look unexpected:

```python
1.2 - 1.0  # May display as 0.19999999999999996
```

For approximate calculations, rounding the result for display can help:

```python
round(1.2 - 1.0, 2)  # 0.2
```

For calculations where exact decimal values matter—such as money—consider Python’s `decimal.Decimal` type instead of relying on floats.

## Key Takeaways

- `/` always returns a float.
- Mixing `int` and `float` values in arithmetic generally produces a float.
- `int()` truncates; it does not round.
- Use `round(value, decimal_places)` when you need rounding.
- Floats are approximate, so avoid assuming every decimal calculation is exact.
````


````
---

# Other Types of Numbers

Python’s `int()` can convert numeric strings to integers. It can also parse strings written in another number base.

```python
int("100")       # 100
int("100", 2)    # 4: binary 100 is decimal 4
int("1ab", 16)   # 427: hexadecimal 1ab is decimal 427
```

When specifying a base, the first argument must be a string. The base must be between 2 and 36.

## The `Decimal` Type

The `decimal` module provides `Decimal` for decimal arithmetic where exact decimal representation matters, such as financial calculations.

```python
from decimal import Decimal, getcontext

price = Decimal("3.14")
total = Decimal("1.20") + Decimal("1.00")
print(total)  # 2.20
```

Create `Decimal` values from strings to avoid carrying inexact float representations. For example, `Decimal(3.14)` captures the approximation already present in the float; prefer `Decimal("3.14")`.

You can set the decimal context’s precision with `getcontext().prec`. Precision is the number of significant digits used in calculations, not the number of digits after the decimal point.

```python
getcontext().prec = 4

result = Decimal(1) / Decimal(3)
print(result)  # 0.3333
```

## Choosing a Number Type

- Use `int` for whole numbers.
- Use `float` for most general-purpose decimal calculations.
- Use `Decimal` when exact base-10 decimal arithmetic is important.
- Round values appropriately when displaying them to users.
````

````
---

# Booleans

Booleans have two values: `True` and `False`. Python also treats other values as truthy or falsy when evaluating conditions.

## Truthy and Falsy Values

Common falsy values include:

- `False`
- Numeric zero, such as `0`, `0.0`, and `0j`
- Empty strings and collections, such as `""`, `[]`, `{}`, and `()`
- `None`

Most other values are truthy. For example, `-1` and the string `"False"` are truthy. A string is falsy only when it is empty; even `" "` is truthy.

Use `bool()` to check a value’s truthiness:

```python
bool(0)       # False
bool(-1)      # True
bool("")      # False
bool("False") # True
bool([])      # False
```

Conditions use these same rules:

```python
items = [1, 2]

if items:
    print("The list has items")
```

## Writing Clear Boolean Logic

Use `and`, `or`, and `not` to combine conditions. Parentheses can make the intended logic easier to read.

```python
weather_is_nice = False
have_umbrella = True

if have_umbrella or weather_is_nice:
    print("Go for a walk")
else:
    print("Stay inside")
```

For the equivalent “stay inside” condition, both conditions must be false:

```python
if not have_umbrella and not weather_is_nice:
    print("Stay inside")
```

This follows De Morgan’s law:

```python
not (have_umbrella or weather_is_nice)
# equivalent to:
(not have_umbrella) and (not weather_is_nice)
```

## Key Takeaways

- Empty values and numeric zero are falsy; most other values are truthy.
- The string `"False"` is truthy because it is not empty.
- Python evaluates `not` before `and`, and `and` before `or`.
- Use parentheses when they make complex conditions clearer.
- Test Boolean logic with different combinations of inputs.
````

````
---

# Strings

Strings store text. Python provides tools to access parts of a string, format output, and work with multiline text.

## Indexing and Slicing

String indexes start at `0`. Use square brackets to access a character or slice:

```python
name = "My name is Ryan Mitchell"

name[0]      # "M"
name[1]      # "y"
name[0:7]    # "My name"
name[11:]    # "Ryan Mitchell"
name[:7]     # "My name"
```

A slice includes the start index but excludes the stop index. Leaving out the start or stop uses the beginning or end of the string. Slicing works similarly with lists.

Use `len()` to get the number of characters in a string, or the number of items in a list:

```python
len(name)
```

## Formatting Strings

F-strings are a readable way to insert variables and expressions into text. Put `f` before the opening quote and expressions inside `{}`.

```python
number = 5

f"My number is {number}"
f"Twice that is {number * 2}"
```

You can format numbers inside the braces. For example, `:.2f` displays a number with two digits after the decimal point:

```python
import math

f"Pi is {math.pi:.2f}"  # "Pi is 3.14"
```

The older `str.format()` method is another option:

```python
"Pi is {:.2f}".format(math.pi)
```

## Multiline Strings

Triple quotes allow strings to span multiple lines. Newlines inside the string are preserved.

```python
message = """This is a
multiline string."""
print(message)
```

Use a backslash (`\`) to escape a character when needed, such as including a quote that would otherwise end the string.

## Key Takeaways

- Strings use zero-based indexes.
- Slices include the start and exclude the stop.
- Use f-strings to insert values and format output.
- Triple quotes support multiline strings.
- `len()` returns the length of a string or collection.
````

````
---

# Bytes

A `bytes` object is an immutable sequence of byte values. Each byte contains 8 bits and can represent a value from `0` to `255`. Bytes are commonly used for file data and network communication.

## Creating Bytes

Calling `bytes()` with an integer creates that many zero-valued bytes—not a byte containing that integer.

```python
empty_data = bytes(4)
print(empty_data)  # b'\x00\x00\x00\x00'
```

To convert text into bytes, encode it using a character encoding such as UTF-8:

```python
text = "🙂"
data = text.encode("utf-8")
print(data)  # UTF-8 bytes
```

The `b` prefix in a displayed value indicates that it is a bytes object.

## Decoding Bytes

To convert bytes back to text, decode them using the same encoding:

```python
decoded_text = data.decode("utf-8")
print(decoded_text)  # 🙂
```

The encoding must match the data. Decoding with the wrong encoding, or with invalid byte sequences, can raise an error.

## Mutable Bytes: `bytearray`

`bytes` objects cannot be changed after creation. Use `bytearray` when you need mutable byte data:

```python
mutable_data = bytearray(data)
mutable_data[0] = 0xF1
```

Each `bytearray` element must be an integer from `0` through `255`. Changing bytes that represent encoded text may make the sequence invalid for that encoding.

## Key Takeaways

- `bytes` stores immutable binary data; `bytearray` is mutable.
- Use `.encode("utf-8")` to convert text to bytes.
- Use `.decode("utf-8")` to convert UTF-8 bytes back to text.
- `bytes(n)` creates `n` zero-valued bytes.
````


````
---

# Solution: Converting Hex to Decimal

Hexadecimal (base 16) uses digits `0–9` and letters `a–f`, where `a` through `f` represent values `10` through `15`.

Each digit’s value depends on its position. For example:

```text
1ab₁₆ = 1 × 16² + 10 × 16¹ + 11 × 16⁰ = 427₁₀
```

## Using Python’s Built-in Conversion

Python can convert a hexadecimal string directly to a decimal integer:

```python
int("1ab", 16)  # 427
```

## Converting Manually

To handle any length, process digits from left to right. For each digit, multiply the current total by `16`, then add the digit’s value.

```python
HEX_VALUES = {
    "0": 0, "1": 1, "2": 2, "3": 3,
    "4": 4, "5": 5, "6": 6, "7": 7,
    "8": 8, "9": 9, "a": 10, "b": 11,
    "c": 12, "d": 13, "e": 14, "f": 15,
}

def hex_to_decimal(hex_num):
    if not isinstance(hex_num, str) or not hex_num:
        return None

    converted = 0

    for char in hex_num.lower():
        if char not in HEX_VALUES:
            return None
        converted = converted * 16 + HEX_VALUES[char]

    return converted
```

For `"1ab"`, the running total is:

```text
0 × 16 + 1 = 1
1 × 16 + 10 = 26
26 × 16 + 11 = 427
```

## Key Takeaways

- Hexadecimal is base 16; each position represents a power of `16`.
- `int(value, 16)` is Python’s built-in way to convert hexadecimal strings.
- When implementing the conversion yourself, validate each character.
- Start with simpler cases, identify the pattern, then generalize to strings of any length.
````

````
---

# Lists

Lists are ordered, mutable collections. Like strings, they support indexing, slicing, and `len()`.

## Slicing

The general syntax is `list[start:stop:step]`. The start is included; the stop is excluded.

```python
numbers = [1, 2, 3, 4, 5]

numbers[2:]       # [3, 4, 5]
numbers[::2]      # [1, 3, 5]
numbers[::-1]     # [5, 4, 3, 2, 1]
len(numbers)      # 5
```

Leaving out the start or stop uses the beginning or end of the list. A negative step moves through the list in reverse.

## Creating Sequences with `range()`

`range()` represents an ordered sequence of integers, commonly used in loops. Convert it to a list to see or store all its values.

```python
for number in range(5):
    print(number)  # 0 through 4

numbers = list(range(10))
```

## Modifying Lists

Lists are mutable, so methods can add or remove items:

```python
numbers = [1, 2, 3]

numbers.append(4)       # Add to the end
numbers.insert(1, 10)   # Insert at index 1
numbers.remove(10)      # Remove the first matching value
last_item = numbers.pop()  # Remove and return the last item
```

`remove()` raises a `ValueError` if the value is not present. `pop()` removes the last item by default, or an item at a specified index.

## Aliasing and Copying

Assigning one list variable to another does not copy the list; both variables refer to the same object. Use `.copy()` for a separate, shallow copy.

```python
original = [1, 2, 3]
alias = original
copy = original.copy()

original.append(4)

print(alias)  # [1, 2, 3, 4]
print(copy)   # [1, 2, 3]
```

## Key Takeaways

- Lists are ordered and mutable.
- Slicing uses `[start:stop:step]`; the stop index is excluded.
- `range()` is useful for generating integer sequences.
- Use `append()`, `insert()`, `remove()`, and `pop()` to modify lists.
- Assignment creates another reference; `.copy()` creates a shallow copy.
````

````
---

# Tuples and Sets

## Sets

A set is a mutable collection of unique, hashable values. Sets do not support indexing or slicing, and their iteration order is not guaranteed.

```python
letters = {"a", "b", "c"}
also_letters = set(("a", "b", "c"))
```

Use `set()` to create an empty set; `{}` creates an empty dictionary.

Sets are useful for removing duplicates, but converting a list to a set may change its order:

```python
values = ["a", "b", "b", "c"]
unique_values = set(values)
```

Add items with `.add()`. Check membership with `in`. Use `.discard()` to remove an item without an error if it is missing; `.remove()` raises a `KeyError` if it is missing. `.pop()` removes and returns an arbitrary item.

```python
letters.add("d")
"a" in letters  # True
letters.discard("z")
```

## Tuples

A tuple is an ordered, immutable sequence. It supports indexing and slicing, but you cannot add, remove, or reassign its elements.

```python
coordinates = (10, 20, 30)
coordinates[0]  # 10
```

Commas create tuples; parentheses are usually added for clarity. A one-item tuple needs a trailing comma:

```python
single_item = ("a",)
```

Functions that return multiple comma-separated values return a tuple. You can unpack those values into variables:

```python
def get_values():
    return 1, 2, 3

a, b, c = get_values()
```

## Key Takeaways

- Sets contain unique values and do not support indexing.
- Use sets for membership checks and removing duplicates when order is unimportant.
- Tuples are ordered and immutable.
- Tuple unpacking assigns sequence values to multiple variables.
````

````
---

# Dictionaries

A dictionary (`dict`) stores key-value pairs. Use keys to look up, add, or update values. Keys must be unique and hashable; values can be any type. A trailing comma after the final pair is optional but commonly used.

```python
animals = {
    "a": "aardvark",
    "b": "bear",
}

animals["a"]          # "aardvark"
animals["d"] = "dog"  # Add a key-value pair
animals["a"] = "antelope"  # Update a value
```

Accessing a missing key with square brackets raises a `KeyError`. Use `.get()` to provide a default instead:

```python
animals.get("e")             # None if "e" is missing
animals.get("e", "elephant")  # "elephant" if "e" is missing
```

Use `in` to check whether a key exists, and `len()` to count the pairs:

```python
"a" in animals
len(animals)
```

## Keys, Values, and Items

`.keys()`, `.values()`, and `.items()` return dictionary views. These are iterable and reflect changes to the dictionary. Convert a view to a list if you need a list:

```python
list(animals.keys())
list(animals.values())
list(animals.items())  # List of (key, value) pairs
```

## Dictionaries of Lists

A dictionary can map keys to lists. Check whether a key exists before creating its list:

```python
animals_by_letter = {"b": ["bear"]}

if "c" not in animals_by_letter:
    animals_by_letter["c"] = []

animals_by_letter["c"].append("cat")
```

For this pattern, `collections.defaultdict` can create a default list automatically:

```python
from collections import defaultdict

animals_by_letter = defaultdict(list)
animals_by_letter["e"].append("elephant")
animals_by_letter["e"].append("emu")
```

Pass the `list` type—not `list()`—so a new list is created whenever a missing key is accessed.

## Key Takeaways

- Dictionaries map unique keys to values.
- Use `dictionary[key]` to access a value, or `.get()` when a key might be missing.
- Assigning to a key adds it if it is new or updates it if it already exists.
- Dictionary views provide iterable access to keys, values, or key-value pairs.
- `defaultdict(list)` is useful for collecting multiple values under each key.
````

````
---

# List Comprehensions

A list comprehension builds a new list by transforming or filtering items from an iterable. Its basic form is:

```python
[expression for item in iterable]
```

For example, double each number in a list:

```python
numbers = [1, 2, 3, 4, 5]
doubled = [number * 2 for number in numbers]
# [2, 4, 6, 8, 10]
```

## Filtering Items

Add an `if` condition after the `for` clause to include only items that meet a condition:

```python
numbers = list(range(100))
multiples_of_ten = [number for number in numbers if number % 10 == 0]
# [0, 10, 20, ..., 90]
```

## Processing Strings

`str.split()` separates a string into a list. With no argument, it splits on whitespace; pass a separator to split on something specific.

```python
text = "My name is Ryan Mitchell. I live in Boston."
words = text.split()
sentences = text.split(".")
```

You can clean each word as you build a list:

```python
def clean_word(word):
    return word.replace(".", "").lower()

cleaned_words = [clean_word(word) for word in text.split()]
short_words = [
    clean_word(word)
    for word in text.split()
    if len(clean_word(word)) < 3
]
```

## Nested List Comprehensions

A comprehension can be nested to create a list of lists—for example, grouping cleaned words by sentence:

```python
sentences = text.split(".")
words_by_sentence = [
    [clean_word(word) for word in sentence.split()]
    for sentence in sentences
]
```

Nested comprehensions can become difficult to read. Use regular loops when they make the logic clearer.

## Key Takeaways

- Use `[expression for item in iterable]` to transform items.
- Add `if condition` to filter items.
- `split()` turns a string into a list of parts.
- Nested comprehensions can build nested lists, but readability matters.
````

````
---

# Dictionary Comprehensions

A dictionary comprehension creates a dictionary from an iterable. Its basic form is:

```python
{key_expression: value_expression for item in iterable}
```

For example, create a dictionary from a list of key-value tuples:

```python
animal_list = [("a", "aardvark"), ("b", "bear"), ("c", "cat")]

animals = {item[0]: item[1] for item in animal_list}
```

Because each tuple has two values, you can unpack them directly in the comprehension:

```python
animals = {key: value for key, value in animal_list}
```

The number of variables used for unpacking must match the number of values in each tuple.

## Working with Dictionary Items

The `.items()` method returns an iterable view of a dictionary’s key-value pairs. Convert it to a list if needed:

```python
pairs = list(animals.items())
```

You can also use `.items()` to transform a dictionary into a list of dictionaries:

```python
animal_records = [
    {"letter": key, "name": value}
    for key, value in animals.items()
]
```

## Key Takeaways

- Dictionary comprehensions use `{key: value for item in iterable}`.
- Unpack tuples in the `for` clause when it improves readability.
- `.items()` provides iterable key-value pairs.
- Comprehensions can transform data into a different structure.
````

````
---

# Solution: Encoding ASCII Art

Run-length encoding represents consecutive repeated characters as `(character, count)` pairs. For example, `"aaabb"` becomes `[("a", 3), ("b", 2)]`. This can compact strings with repeated characters, such as ASCII art.

## Encoding

Track the current character and how many times it appears consecutively. When the character changes, save the previous run and start counting the new one.

```python
def encode_string(text):
    if not text:
        return []

    encoded = []
    previous = text[0]
    count = 0

    for char in text:
        if char != previous:
            encoded.append((previous, count))
            previous = char
            count = 0

        count += 1

    encoded.append((previous, count))
    return encoded
```

The final append is needed because the last run has no following character to signal a change.

## Decoding

For each pair, repeat the character by its count and join the results:

```python
def decode_string(encoded):
    return "".join(char * count for char, count in encoded)
```

## Example

```python
original = "aaabbcccc"
encoded = encode_string(original)
decoded = decode_string(encoded)

print(encoded)  # [('a', 3), ('b', 2), ('c', 4)]
print(decoded)  # aaabbcccc
```

## Key Takeaways

- Run-length encoding stores consecutive runs as `(character, count)` pairs.
- Remember to save the final run after the loop.
- Decoding repeats each character by its count and joins the pieces.
- Test both a larger input and small cases, including an empty string and a single repeated character.
````

````
---

# If and Else

Conditional statements run code depending on whether a Boolean condition is true.

```python
if condition:
    # Runs when condition is true
elif another_condition:
    # Runs when the first condition is false
    # and this condition is true
else:
    # Runs if no preceding condition is true
```

A conditional block has one `if`, may have multiple `elif` branches, and may end with one optional `else`.

## Example: FizzBuzz

Check divisibility by `15` before checking `3` or `5`, since multiples of `15` also match those conditions.

```python
for number in range(1, 101):
    if number % 15 == 0:
        print("FizzBuzz")
    elif number % 3 == 0:
        print("Fizz")
    elif number % 5 == 0:
        print("Buzz")
    else:
        print(number)
```

A new `if` starts a separate conditional block; it does not continue the preceding `if`/`elif`/`else` chain.

## Conditional Expressions

For a simple choice between two values, Python supports a one-line conditional expression:

```python
number = 3
result = "Fizz" if number % 3 == 0 else number
```

Its general form is:

```python
value_if_true if condition else value_if_false
```

You can chain conditional expressions, but long chains can be hard to read. Prefer regular `if`/`elif`/`else` blocks when there are several cases.

## Key Takeaways

- Use `if` for the first condition, optional `elif` branches for alternatives, and an optional final `else`.
- Conditions are checked in order; the first true branch runs.
- Use `%` to check for a remainder, such as divisibility.
- Conditional expressions are useful for short, simple choices.
````

````
---

# While Loops

A `while` loop repeats its body as long as its condition is true. Make sure the condition can eventually become false, or the loop may run indefinitely.

```python
count = 0

while count < 3:
    print(count)
    count += 1
```

## Loop Control Statements

- `break` exits the innermost loop immediately.
- `continue` skips the rest of the current iteration and starts the next one.
- `pass` does nothing; it can serve as a placeholder where Python requires a statement.

```python
while True:
    command = input("Enter a command (or 'quit'): ")

    if command == "quit":
        break

    if not command:
        continue

    print(f"You entered: {command}")
```

## Waiting Until a Time

A loop that repeatedly checks the clock can waste CPU time. Use `time.sleep()` between checks. A deadline based on `datetime` also handles minute and hour changes correctly.

```python
from datetime import datetime, timedelta
from time import sleep

deadline = datetime.now() + timedelta(seconds=2)

while datetime.now() < deadline:
    sleep(0.1)

print("Two seconds have passed.")
```

## Key Takeaways

- Use `while` when repetition depends on a condition rather than a fixed number of iterations.
- Update the condition’s state so the loop can finish.
- `break` exits a loop; `continue` skips to its next iteration; `pass` is a no-op.
- Avoid busy-waiting when waiting for time or another event.
````

````
---

# For Loops

A `for` loop iterates over the items in an iterable, such as a list, string, dictionary, or `range`.

```python
numbers = [1, 2, 3, 4]

for number in numbers:
    print(number)
```

You can unpack items while iterating over key-value pairs:

```python
animal_lookup = {"a": "aardvark", "b": "bear"}

for letter, animal in animal_lookup.items():
    print(letter, animal)
```

## Loop Control

- `pass` does nothing; use it as a placeholder.
- `continue` skips the rest of the current iteration.
- `break` exits the innermost loop.

```python
for number in range(10):
    if number == 2:
        continue
    if number == 5:
        break
    print(number)  # Prints 0, 1, 3, 4
```

## The `for`-`else` Pattern

A loop’s `else` block runs only if the loop finishes without encountering `break`. This is useful for searching: break when you find a match; otherwise, handle the “not found” case in `else`.

For example, test which numbers below 100 are prime:

```python
for number in range(2, 100):
    for factor in range(2, int(number ** 0.5) + 1):
        if number % factor == 0:
            break
    else:
        print(number, "is prime")
```

The inner `else` belongs to the `for factor` loop. It runs when no factor was found and the loop did not break. The square-root limit is sufficient because any composite number has a factor no greater than its square root.

## Key Takeaways

- Use `for` to iterate over an iterable.
- `break`, `continue`, and `pass` work in both `for` and `while` loops.
- A loop’s `else` runs if the loop completes without `break`.
- `range(start, stop)` includes `start` but excludes `stop`.
````

````
---

# Solution: Finding Primes Faster

To find primes more efficiently, keep a list of primes found so far and use those as possible factors for each new candidate. You only need to test factors up to the candidate’s square root: if a number has a larger factor, it must also have a smaller factor.

```python
def primes_below(limit):
    primes = []

    for candidate in range(2, limit):
        is_prime = True

        for factor in primes:
            if factor * factor > candidate:
                break
            if candidate % factor == 0:
                is_prime = False
                break

        if is_prime:
            primes.append(candidate)

    return primes
```

The function returns primes less than `limit`. For each candidate, it checks only previously found primes and stops once their squares exceed the candidate.

## Key Takeaways

- Reuse known primes as candidate factors instead of checking every number.
- Factors only need to be checked up to the square root.
- Optimize when it meaningfully improves performance, while keeping the code readable.
````

````
---

# The Anatomy of a Function

A function groups reusable behavior. Define one with `def`, give it parameters, and use `return` to send a result back to the caller.

```python
def perform_operation(num1, num2, operation="sum"):
    if operation == "sum":
        return num1 + num2
    elif operation == "multiply":
        return num1 * num2
    else:
        raise ValueError(f"Unknown operation: {operation}")

result = perform_operation(2, 3)  # Uses the default: sum
product = perform_operation(2, 3, operation="multiply")
```

## Arguments and Parameters

- **Parameters** are names in the function definition.
- **Arguments** are values passed when calling the function.
- Positional arguments are assigned by order.
- Keyword arguments are assigned by name and can make calls clearer.
- Parameters with default values are optional. They must follow required parameters.

```python
def greet(name, message="Hello"):
    print(f"{message}, {name}!")

greet("Ava")
greet("Ava", message="Welcome")
```

## Variable-Length Arguments

Use `*args` to collect extra positional arguments into a tuple, and `**kwargs` to collect extra keyword arguments into a dictionary.

```python
def show_arguments(*args, **kwargs):
    print(args)
    print(kwargs)

show_arguments(1, 2, name="Ava")
# args: (1, 2)
# kwargs: {"name": "Ava"}
```

These names are conventions; the `*` and `**` provide the behavior.

## Returning Results

`return` ends the function and sends a value back. A function without a `return` statement returns `None`.

```python
def perform_operation(*args, operation="sum"):
    if operation == "sum":
        return sum(args)
    elif operation == "multiply":
        from math import prod
        return prod(args)
    else:
        raise ValueError(f"Unknown operation: {operation}")

perform_operation(1, 2, 3)                       # 6
perform_operation(2, 3, 4, operation="multiply") # 24
```

`sum()` is a built-in function; `math.sum()` does not exist. `math.prod()` multiplies the items in an iterable.

## Key Takeaways

- Functions are defined with `def` and may return values with `return`.
- Defaults make parameters optional; keyword arguments identify values by name.
- `*args` collects extra positional arguments into a tuple.
- `**kwargs` collects extra keyword arguments into a dictionary.
- Keep functions readable and validate unsupported inputs when appropriate.
````

````
---

# Variables and Scope

A variable’s **scope** determines where it can be accessed. Variables defined inside a function are local to that function; variables defined at module level are global.

```python
message = "Global value"

def greet():
    name = "Ava"  # Local to greet
    print(message)  # Reads the global variable
    print(name)

greet()
```

Python looks up names using the LEGB order: **Local**, **Enclosing**, **Global**, then **Built-in**. A function can read a global variable, but assigning to a name inside a function makes it local by default.

```python
count = 0

def update():
    global count
    count += 1
```

Use `global` sparingly; passing values into a function and returning results is usually easier to understand.

## Inspecting Names

`locals()` returns a dictionary of names available in the current local scope. `globals()` returns the module’s global namespace dictionary. These are useful for inspection, but generally shouldn’t replace explicit variables or parameters.

```python
def show_values(value):
    extra = "local"
    print(locals())

show_values(42)
```

A function defined inside another function is local to its enclosing function and can access names from that enclosing scope.

```python
def outer():
    message = "Enclosing value"

    def inner():
        print(message)

    inner()
```

## Key Takeaways

- Function parameters and variables assigned inside a function are local by default.
- Functions can read names from enclosing and global scopes.
- `global` allows a function to reassign a module-level name; use it cautiously.
- `locals()` and `globals()` expose scope dictionaries for inspection.
- Inner functions can access variables in their enclosing function.
````

````
---

# Functions as Variables

In Python, functions are objects. You can assign them to variables, store them in collections, pass them to other functions, and call them later.

## Store Functions in a List

A list of functions can represent a sequence of operations. Call each function in turn to transform some data:

```python
def strip_text(text):
    return text.strip()

def lowercase(text):
    return text.lower()

operations = [strip_text, lowercase]

text = "  Hello, Python!  "
for operation in operations:
    text = operation(text)

print(text)  # hello, python!
```

This pattern makes it easy to change or reorder processing steps.

## Lambda Functions

A `lambda` creates a small anonymous function containing a single expression. The expression’s value is returned automatically.

```python
add_three = lambda value: value + 3
print(add_three(5))  # 8
```

Lambdas are often useful when a function is needed briefly as an argument. For example, `sorted()` accepts a `key` function that determines what value to sort by:

```python
records = [
    {"number": 3},
    {"number": 1},
    {"number": 2},
]

sorted_records = sorted(records, key=lambda record: record["number"])
```

Use a regular `def` function instead when the logic needs multiple statements or a descriptive reusable name.

## Key Takeaways

- Functions can be stored, passed as arguments, and called through variables.
- Lists of functions can define configurable processing steps.
- `lambda` is for short, single-expression functions.
- Functions such as `sorted()` can accept another function as an argument.
- Function internals such as `__code__` are generally for specialized inspection, not everyday use.
````

````
---

# Solution: Sum of Triangles

The *nth triangular number* is the sum of integers from 1 through `n`. Two consecutive triangular numbers add up to a square:

```text
n² = triangle(n) + triangle(n - 1)
```

For example, `4² = 10 + 6 = 16`.

## Recursive Implementation

A triangular number can be defined recursively: add `n` to the previous triangular number. The base case stops the recursion.

```python
def triangle(n):
    if n <= 0:
        return 0
    return n + triangle(n - 1)

def square_from_triangles(n):
    return triangle(n) + triangle(n - 1)

print(square_from_triangles(4))  # 16
```

Each recursive function needs a base case; otherwise, it keeps calling itself. Recursion is useful for expressing problems this way, though an iterative approach may be preferable for large inputs because Python limits recursion depth.

## Related Pattern: Factorial

The same recursive structure can calculate a factorial:

```python
def factorial(n):
    if n <= 1:
        return 1
    return n * factorial(n - 1)
```

The key difference is the operation: triangular numbers add each step, while factorials multiply.

## Key Takeaways

- A triangular number is the sum `1 + 2 + ... + n`.
- Two consecutive triangular numbers sum to `n²`.
- Recursive functions need a base case and a step that moves toward it.
- Similar recursive structures can solve different problems by changing the operation and base case.
````
