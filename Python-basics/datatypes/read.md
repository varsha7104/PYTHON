# Python Programming Language

# Getting Started with VS Code

## Python Data Types

### Introduction

Data types are an important concept in programming. They define the kind of value a variable can store and the operations that can be performed on that value.

Python provides several built-in data types, including integers, floating-point numbers, strings, and Boolean values.

Python is a dynamically typed language, so we do not need to explicitly declare the data type of a variable.

## 1. Importance of Data Types

Data types are important for the following reasons:

* They help classify different kinds of data.
* They determine which operations can be performed on values.
* They help prevent errors caused by incompatible data types.
* They help programmers write clear and reliable code.
* They influence how data is represented and stored in memory.

## 2. Integer Data Type (`int`)

The `int` data type is used to represent whole numbers without decimal points.

**Example:**

```python
age = 35

print(age)
print(type(age))
```

**Output:**

```text
35
<class 'int'>
```

Other examples of integers include:

```python
a = 10
b = -20
c = 0
```

## 3. Floating-Point Data Type (`float`)

The `float` data type is used to represent numbers containing a decimal point.

**Example:**

```python
height = 5.11

print(height)
print(type(height))
```

**Output:**

```text
5.11
<class 'float'>
```

Other examples of floating-point numbers include:

```python
price = 99.99
temperature = 36.5
value = -2.75
```

## 4. String Data Type (`str`)

The `str` data type is used to store text. Strings can be written using single quotes or double quotes.

**Example:**

```python
name = "Krish"

print(name)
print(type(name))
```

**Output:**

```text
Krish
<class 'str'>
```

Additional examples:

```python
first_name = "Python"
message = 'Hello World'
```

Strings provide several built-in methods, such as `upper()`, `lower()`, `replace()`, `split()`, and `count()`.

**Example:**

```python
text = "hello"

print(text.upper())
print(text.capitalize())
```

**Output:**

```text
HELLO
Hello
```

## 5. Boolean Data Type (`bool`)

The `bool` data type represents one of two values: `True` or `False`.

Boolean values are commonly used in comparisons and conditional statements.

**Example 1: Assigning Boolean Values**

```python
is_student = True
is_employed = False

print(is_student)
print(type(is_student))
```

**Output:**

```text
True
<class 'bool'>
```

**Example 2: Using Boolean Conditions**

```python
a = 10
b = 10

result = a == b

print(result)
print(type(result))
```

**Output:**

```text
True
<class 'bool'>
```

The `==` operator checks whether two values are equal and returns a Boolean result.

**Example 3: Using the `bool()` Function**

```python
print(bool(0))
print(bool(1))
print(bool(""))
print(bool("Python"))
```

**Output:**

```text
False
True
False
True
```

In Python, zero and empty strings are considered false in Boolean contexts, while nonzero numbers and non-empty strings are considered true.

## 6. Type Checking

The built-in `type()` function identifies the data type of a value or variable.

**Example:**

```python
age = 35
height = 5.11
name = "Krish"
is_student = True

print(type(age))
print(type(height))
print(type(name))
print(type(is_student))
```

**Output:**

```text
<class 'int'>
<class 'float'>
<class 'str'>
<class 'bool'>
```

## 7. Type Conversion

Type conversion means converting a value from one data type to another compatible data type.

Common conversion functions include:

| Function  | Purpose                                                |
| --------- | ------------------------------------------------------ |
| `int()`   | Converts a compatible value to an integer              |
| `float()` | Converts a compatible value to a floating-point number |
| `str()`   | Converts a value to a string                           |
| `bool()`  | Converts a value to a Boolean                          |

### Example: Converting an Integer to a String

```python
result = "Hello" + str(5)

print(result)
```

**Output:**

```text
Hello5
```

The `str()` function converts the integer `5` into a string, allowing it to be concatenated with `"Hello"`.

## 8. Common Errors with Data Types

Python does not allow every operation between different data types.

### Example 1: Adding a String and an Integer

The following code produces a `TypeError`:

```python
result = "Hello" + 5

print(result)
```

**Reason:** The `+` operator cannot concatenate a string and an integer directly.

### Correct Approach

```python
result = "Hello" + str(5)

print(result)
```

**Output:**

```text
Hello5
```

### Example 2: Converting Invalid Text to an Integer

```python
value = int("Hello")
```

This produces a `ValueError` because `"Hello"` does not represent a valid integer.

A valid example is:

```python
value = int("25")

print(value)
```

**Output:**

```text
25
```

## 9. Overview of Basic Data Types

| Data Type | Example             | Description            |
| --------- | ------------------- | ---------------------- |
| `int`     | `age = 35`          | Whole numbers          |
| `float`   | `height = 5.11`     | Floating-point numbers |
| `str`     | `name = "Krish"`    | Text                   |
| `bool`    | `is_student = True` | True or false values   |

Python also supports advanced built-in data types, including lists, tuples, sets, and dictionaries. These will be covered in future tutorials.

## 10. Practice Exercises

1. Create an integer variable to store your age.
2. Create a float variable to store your height.
3. Create a string variable to store your name.
4. Create a Boolean variable called `is_student`.
5. Print the data type of each variable using `type()`.
6. Convert the integer `100` into a string.
7. Correct the error in `"Python" + 10`.
8. Compare two numbers using `==` and print the result.

## Conclusion

Understanding Python data types is essential for writing effective programs. The `int`, `float`, `str`, and `bool` data types are the basic building blocks of Python programming.

Learning type checking, type conversion, and common data type errors will help you write more reliable code.

**Next Topic:** Python Operators.
