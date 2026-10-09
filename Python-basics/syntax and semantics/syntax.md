# Python Programming Language

# Python Syntax and Semantics

This README introduces the basic rules of Python syntax and semantics, based on the lesson transcript. It covers comments, case sensitivity, indentation, line continuation, multiple statements on one line, variable assignment, type inference, and common errors.

## 1. Syntax vs. Semantics

### Syntax

**Syntax** is the set of rules that determines how symbols and statements must be arranged to form correctly structured code.

In simple terms, syntax is about writing code in the correct format.

```python
print("Hello World")
```

### Semantics

**Semantics** refers to the meaning or interpretation of code — what the code is intended to do when it runs.

- **Syntax**: How the code is written.
- **Semantics**: What the code means or does.

---

## 2. Comments in Python

Comments explain code and are not executed as Python instructions.

### Single-Line Comments

Use `#` to write a single-line comment.

```python
# This is a single-line comment
print("Hello World")
```

### Multi-Line Notes

For longer explanations, you can use multiple single-line comments:

```python
# Welcome to the Python course.
# We are learning basic Python syntax.
# This is an example of comments.
```

Triple-quoted strings can also span multiple lines:

```python
"""
Welcome to the Python course.
This is a multi-line string.
"""
```

**Note:** Triple quotes create a string literal, not a true comment. They are commonly used for docstrings when placed in suitable locations, such as at the start of a module, function, or class. For ordinary comments, use `#`.

---

## 3. Python Is Case-Sensitive

Python treats uppercase and lowercase letters as different characters in identifiers.

```python
name = "Krish"
Name = "Nick"

print(name)
print(Name)
```

Output:

```text
Krish
Nick
```

`name` and `Name` are two different variables because their capitalization differs.

**Remember:** Use consistent capitalization when naming and using variables.

---

## 4. Indentation in Python

**Indentation** is the whitespace at the beginning of a line. Python uses indentation to define blocks of code, such as the body of an `if` statement, loop, function, or class.

Python commonly uses four spaces for each indentation level.

```python
age = 32

if age > 30:
    print(age)

print("Outside the if block")
```

The first `print()` is indented, so it belongs to the `if` block. The second `print()` is not indented, so it runs outside the block.

Unlike languages that use braces to define blocks, Python relies on indentation.

### Nested Indentation

Each nested block needs another indentation level.

```python
if True:
    print("Inside the first block")

    if False:
        print("This line will not run")

print("Outside the if blocks")
```

The line inside `if False` does not execute because the condition is false.

### Indentation Errors

A block statement such as `if` must have an indented body.

Incorrect:

```python
age = 32

if age > 30:
print(age)
```

Correct:

```python
age = 32

if age > 30:
    print(age)
```

Consistent indentation is essential in Python.

---

## 5. Line Continuation

A long statement can be split across lines. One way is to use a backslash (`\`) at the end of a line.

```python
total = 1 + 2 + 3 + \
        4 + 5 + 6

print(total)
```

Output:

```text
21
```

For longer calculations, parentheses are generally preferred because they allow implicit line continuation:

```python
total = (
    1 + 2 + 3 +
    4 + 5 + 6
)

print(total)
```

---

## 6. Multiple Statements on One Line

Python allows multiple simple statements on one line by separating them with semicolons (`;`).

```python
x = 5; y = 10; z = x + y

print(z)
```

Output:

```text
15
```

Although this is valid, writing one statement per line is usually easier to read and maintain.

---

## 7. Variable Assignment

A variable stores a reference to a value. In Python, you do not normally need to declare a variable's type in advance.

```python
age = 32
name = "Chris"

print(age)
print(name)
```

Python determines the type of each value at runtime.

### Checking a Variable's Type

Use the `type()` function:

```python
age = 32
name = "Chris"

print(type(age))
print(type(name))
```

The first value has type `int` (integer), and the second has type `str` (string).

---

## 8. Type Inference and Dynamic Typing

Python determines the type of a value at runtime. This is often described as type inference. Python is also dynamically typed, meaning a variable name can be assigned values of different types at different times.

```python
var = 10
print(type(var))

var = "Krish"
print(type(var))
```

The first `type()` call reports `int`; the second reports `str`.

The variable name `var` can refer to an integer first and a string later.

---

## 9. Common Errors

### IndentationError

This occurs when Python expects an indented block but does not find one.

```python
if age > 30:
    print(age)
```

Make sure the body of the statement is indented consistently.

### NameError

A `NameError` can occur when you use a variable name that has not been defined.

Incorrect:

```python
a = b
```

If `b` has not been defined, Python raises a `NameError`.

Correct example:

```python
b = 10
a = b

print(a)
```

Output:

```text
10
```

A `NameError` is a runtime error, not a syntax error.

---

## 10. Key Takeaways

- **Syntax** describes the rules for writing correctly structured code.
- **Semantics** describes the meaning and behavior of code.
- Use `#` for single-line comments.
- Triple-quoted text is a string literal; it is not technically a comment.
- Python is case-sensitive: `name` and `Name` are different identifiers.
- Indentation defines code blocks; four spaces per level is the common convention.
- Long statements can be continued with a backslash, though parentheses are often clearer.
- Semicolons can separate multiple simple statements on one line, but separate lines are more readable.
- Python determines value types at runtime and supports dynamic typing.
- `IndentationError` and `NameError` are different errors with different causes.

---

## Practice Examples

Try to predict the output before running each example.

### Example 1: Case Sensitivity

```python
city = "Visakhapatnam"
City = "Hyderabad"

print(city)
print(City)
```

### Example 2: Indentation

```python
age = 32

if age > 30:
    print("Age is greater than 30")

print("Program finished")
```

### Example 3: Dynamic Typing

```python
value = 10
print(type(value))

value = "Python"
print(type(value))
```

### Example 4: Multiple Statements

```python
x = 5; y = 10; z = x + y
print(z)
```

---

## Conclusion

Understanding syntax and semantics is an important first step in learning Python. Practice writing comments, using consistent indentation, naming variables carefully, and reading error messages. These basics will help you write clearer Python programs and prepare for topics such as variables, data types, and operators.
