# Python Programming Language

# Getting Started with VS Code

## Python Variables

### Introduction

Variables are fundamental elements of programming used to store data that can be accessed and manipulated throughout a program.

In Python, variables are created automatically when a value is assigned to them. We do not need to declare their data types explicitly.

**Example:**

```python
a = 100
print(a)
```

**Output:**

```text
100
```

## 1. Declaring and Assigning Variables

In Python, we use the assignment operator (`=`) to assign values to variables.

```python
age = 32
height = 6.1
name = "Krish"
is_student = True

print(age)
print(height)
print(name)
print(is_student)
```

**Output:**

```text
32
6.1
Krish
True
```

Variables can store different types of values, including integers, floating-point numbers, strings, and Boolean values.

## 2. Variable Naming Conventions

Variable names should be meaningful and follow Python's naming rules.

### Rules for Naming Variables

* A variable name must begin with a letter or an underscore (`_`).
* It can contain letters, numbers, and underscores.
* A variable name cannot begin with a number.
* Variable names are case-sensitive.
* Python keywords cannot be used as variable names.
* Use descriptive names to make code easier to understand.

### Valid Variable Names

```python
first_name = "Krish"
last_name = "Nick"
age1 = 25
_student = True
```

### Invalid Variable Names

```python
# 1age = 25       # Cannot start with a number
# first-name = "Krish"  # Hyphens are not allowed
# first name = "Krish"  # Spaces are not allowed
```

### Case Sensitivity

Python treats uppercase and lowercase letters as different characters.

```python
name = "Krish"
Name = "Nick"

print(name)
print(Name)
```

**Output:**

```text
Krish
Nick
```

## 3. Types of Variables

Python is a dynamically typed language. This means that the type of a variable is determined at runtime.

Some common data types are:

| Data Type | Description     | Example             |
| --------- | --------------- | ------------------- |
| `int`     | Integer numbers | `age = 25`          |
| `float`   | Decimal numbers | `height = 6.1`      |
| `str`     | Text values     | `name = "Krish"`    |
| `bool`    | Boolean values  | `is_student = True` |

**Example:**

```python
age = 25
height = 6.1
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

## 4. Type Checking and Type Conversion

### Type Checking

The `type()` function is used to identify the data type of a variable.

```python
height = 6.1

print(type(height))
```

**Output:**

```text
<class 'float'>
```

### Type Conversion

Type conversion means converting a value from one data type to another.

Python provides functions such as:

* `int()` — converts a compatible value to an integer.
* `float()` — converts a compatible value to a floating-point number.
* `str()` — converts a value to a string.
* `bool()` — converts a value to a Boolean.

**Example 1: Integer to String**

```python
age = 25

age_str = str(age)

print(age_str)
print(type(age_str))
```

**Output:**

```text
25
<class 'str'>
```

**Example 2: String to Integer**

```python
number = "25"

converted_number = int(number)

print(converted_number)
print(type(converted_number))
```

**Output:**

```text
25
<class 'int'>
```

A string containing non-numeric text, such as `"Krish"`, cannot be directly converted into an integer.

**Example 3: Float to Integer**

```python
height = 5.11

converted_height = int(height)

print(converted_height)
```

**Output:**

```text
5
```

When converting a positive floating-point number to an integer using `int()`, Python removes the decimal portion rather than rounding the number.

**Example 4: Integer to Float**

```python
number = 5

converted_number = float(number)

print(converted_number)
```

**Output:**

```text
5.0
```

## 5. Dynamic Typing in Python

Python allows a variable to refer to values of different data types during program execution.

```python
var = 10
print(var, type(var))

var = "Hello"
print(var, type(var))

var = 3.14
print(var, type(var))
```

**Output:**

```text
10 <class 'int'>
Hello <class 'str'>
3.14 <class 'float'>
```

This feature is known as **dynamic typing**.

## 6. Taking User Input

The `input()` function is used to receive input from the user.

By default, `input()` returns the entered value as a string.

**Example 1: Taking String Input**

```python
name = input("Enter your name: ")

print("Your name is:", name)
```

**Example 2: Taking Integer Input**

```python
age = int(input("Enter your age: "))

print("Your age is:", age)
print(type(age))
```

**Example 3: Taking Float Input**

```python
height = float(input("Enter your height: "))

print("Your height is:", height)
```

Type conversion is necessary when numeric input needs to be used in mathematical calculations.

## 7. Practical Example: Simple Calculator

The following program takes two numbers from the user and performs basic arithmetic operations.

```python
num1 = float(input("Enter the first number: "))
num2 = float(input("Enter the second number: "))

sum_result = num1 + num2
difference = num1 - num2
product = num1 * num2

print("Sum:", sum_result)
print("Difference:", difference)
print("Product:", product)

if num2 != 0:
    quotient = num1 / num2
    print("Quotient:", quotient)
else:
    print("Division by zero is not allowed.")
```

**Example Output:**

```text
Enter the first number: 56
Enter the second number: 10
Sum: 66.0
Difference: 46.0
Product: 560.0
Quotient: 5.6
```

This example demonstrates variables, user input, type conversion, arithmetic operators, and basic conditional statements.

## 8. Common Mistakes to Avoid

* Using a number at the beginning of a variable name.
* Using spaces or hyphens in variable names.
* Forgetting that variable names are case-sensitive.
* Assuming that `input()` automatically returns an integer.
* Converting non-numeric strings directly into integers.
* Dividing a number by zero.
* Confusing assignment (`=`) with comparison (`==`).

## 9. Key Takeaways

* Variables store values used in a program.
* Python variables do not require explicit type declarations.
* Variable names must follow Python's naming rules.
* The `type()` function identifies a variable's data type.
* Type conversion changes a value into a compatible data type.
* Python supports dynamic typing.
* The `input()` function accepts user input as a string by default.
* Variables can be used to perform calculations and build practical applications.

## 10. Practice Exercises

1. Create variables to store your name, age, height, and student status.
2. Print the data type of each variable using `type()`.
3. Convert a numeric string into an integer.
4. Take two numbers from the user and calculate their sum.
5. Build a calculator that performs addition, subtraction, multiplication, and division.

## Conclusion

Variables are one of the most important concepts in Python programming. Understanding variable declaration, naming conventions, data types, type conversion, dynamic typing, and user input provides a strong foundation for learning more advanced Python concepts.

**Next Topics:** Python Data Types and Python Operators.
