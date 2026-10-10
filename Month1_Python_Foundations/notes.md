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

Append this section to your GitHub notes:

````markdown
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
