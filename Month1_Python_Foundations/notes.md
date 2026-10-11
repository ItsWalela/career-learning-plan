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
