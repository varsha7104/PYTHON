# Python Programming Language

# Operators in Python

## Introduction

Operators in Python are special symbols or keywords used to perform different operations on variables and values.

They help us perform mathematical calculations, compare values, and make logical decisions in programs.

For example:

```python
a = 10
b = 15

result = a + b
print(result)
```

**Output:**

```text
25
```

In this example, `+` is an arithmetic operator that adds two numbers.

## Types of Operators in Python

Python provides several types of operators:

1. Arithmetic Operators
2. Comparison Operators
3. Logical Operators

---

## 1. Arithmetic Operators

Arithmetic operators are used to perform mathematical calculations such as addition, subtraction, multiplication, and division.

Let's use two variables:

```python
a = 10
b = 15
```

### Arithmetic Operators Table

| Operator | Name           | Example  | Result             |
| -------- | -------------- | -------- | ------------------ |
| `+`      | Addition       | `a + b`  | `25`               |
| `-`      | Subtraction    | `a - b`  | `-5`               |
| `*`      | Multiplication | `a * b`  | `150`              |
| `/`      | Division       | `a / b`  | `0.666...`         |
| `//`     | Floor Division | `a // b` | `0`                |
| `%`      | Modulus        | `a % b`  | `10`               |
| `**`     | Exponentiation | `a ** b` | `1000000000000000` |

### Example Program

```python
a = 10
b = 15

addition = a + b
subtraction = a - b
multiplication = a * b
division = a / b
floor_division = a // b
modulus = a % b
exponentiation = a ** b

print("Addition:", addition)
print("Subtraction:", subtraction)
print("Multiplication:", multiplication)
print("Division:", division)
print("Floor Division:", floor_division)
print("Modulus:", modulus)
print("Exponentiation:", exponentiation)
```

**Output:**

```text
Addition: 25
Subtraction: -5
Multiplication: 150
Division: 0.6666666666666666
Floor Division: 0
Modulus: 10
Exponentiation: 1000000000000000
```

### Understanding Division and Floor Division

Python provides two different division operators.

**Normal Division (`/`)**

Normal division returns the quotient, generally as a floating-point number.

```python
print(21 / 5)
```

Output:

```text
4.2
```

**Floor Division (`//`)**

Floor division rounds the quotient down to the nearest integer for integer operands when the result is non-negative.

```python
print(21 // 5)
```

Output:

```text
4
```

Note: Floor division rounds down mathematically, rather than simply removing the decimal part. For example, `-21 // 5` returns `-5`.

### Understanding the Modulus Operator

The modulus operator (`%`) returns the remainder after division.

```python
print(10 % 5)
print(21 % 5)
```

Output:

```text
0
1
```

Explanation:

* `10 % 5` returns `0` because 10 is exactly divisible by 5.
* `21 % 5` returns `1` because the remainder is 1.

The modulus operator is commonly used to check whether a number is even or odd.

```python
number = 7

if number % 2 == 0:
    print("Even number")
else:
    print("Odd number")
```

Output:

```text
Odd number
```

### Understanding Exponentiation

The exponentiation operator (`**`) raises a number to a power.

```python
print(2 ** 3)
print(10 ** 2)
```

Output:

```text
8
100
```

Here, `2 ** 3` means \(2 \times 2 \times 2\).

---

## 2. Comparison Operators

Comparison operators compare two values and return a Boolean result: `True` or `False`.

Let's use the following variables:

```python
a = 10
b = 10
c = 15
```

### Comparison Operators Table

| Operator | Meaning                  | Example  | Result |
| -------- | ------------------------ | -------- | ------ |
| `==`     | Equal to                 | `a == b` | `True` |
| `!=`     | Not equal to             | `a != c` | `True` |
| `>`      | Greater than             | `c > a`  | `True` |
| `<`      | Less than                | `a < c`  | `True` |
| `>=`     | Greater than or equal to | `a >= b` | `True` |
| `<=`     | Less than or equal to    | `a <= b` | `True` |

### Example Program

```python
a = 10
b = 10
c = 15

print(a == b)
print(a != c)
print(c > a)
print(a < c)
print(a >= b)
print(a <= b)
```

**Output:**

```text
True
True
True
True
True
True
```

### Important: Equal to (`==`) vs Assignment (`=`)

These two operators have different purposes.

* `=` assigns a value to a variable.
* `==` compares two values to check whether they are equal.

Example:

```python
a = 10

print(a == 10)
```

Output:

```text
True
```

### Comparing Strings

Python string comparisons are case-sensitive.

```python
str1 = "Python"
str2 = "Python"
str3 = "python"

print(str1 == str2)
print(str1 == str3)
```

Output:

```text
True
False
```

The second comparison returns `False` because uppercase `P` and lowercase `p` are different characters.

---

## 3. Logical Operators

Logical operators combine conditions or reverse a Boolean value.

Python provides three logical operators:

1. `and`
2. `or`
3. `not`

### A. AND Operator

The `and` operator returns `True` only when both conditions are true.

| Condition 1 | Condition 2 | Result  |
| ----------- | ----------- | ------- |
| `True`      | `True`      | `True`  |
| `True`      | `False`     | `False` |
| `False`     | `True`      | `False` |
| `False`     | `False`     | `False` |

Example:

```python
x = True
y = True

print(x and y)
```

Output:

```text
True
```

Another example:

```python
age = 25
has_id = False

print(age >= 18 and has_id)
```

Output:

```text
False
```

Although the age condition is true, `has_id` is false. Therefore, the complete condition is false.

### B. OR Operator

The `or` operator returns `True` when at least one condition is true. It returns `False` only when both conditions are false.

| Condition 1 | Condition 2 | Result  |
| ----------- | ----------- | ------- |
| `True`      | `True`      | `True`  |
| `True`      | `False`     | `True`  |
| `False`     | `True`      | `True`  |
| `False`     | `False`     | `False` |

Example:

```python
x = True
y = False

print(x or y)
```

Output:

```text
True
```

Another example:

```python
is_weekend = False
is_holiday = True

print(is_weekend or is_holiday)
```

Output:

```text
True
```

The result is true because at least one condition is true.

### C. NOT Operator

The `not` operator reverses a Boolean value.

* `not True` returns `False`.
* `not False` returns `True`.

Example:

```python
x = True
y = False

print(not x)
print(not y)
```

Output:

```text
False
True
```

---

## 4. Practical Project: Simple Calculator

We can combine arithmetic operators and user input to create a simple calculator.

The program accepts two numbers and displays their addition, subtraction, multiplication, division, modulus, and exponentiation results.

```python
num1 = float(input("Enter the first number: "))
num2 = float(input("Enter the second number: "))

print("Addition:", num1 + num2)
print("Subtraction:", num1 - num2)
print("Multiplication:", num1 * num2)

if num2 != 0:
    print("Division:", num1 / num2)
    print("Floor Division:", num1 // num2)
    print("Modulus:", num1 % num2)
else:
    print("Division, floor division, and modulus by zero are undefined.")

print("Exponentiation:", num1 ** num2)
```

### Sample Execution

Input:

```text
Enter the first number: 12
Enter the second number: 5
```

Output:

```text
Addition: 17.0
Subtraction: 7.0
Multiplication: 60.0
Division: 2.4
Floor Division: 2.0
Modulus: 2.0
Exponentiation: 248832.0
```

Note: `float()` allows the user to enter decimal numbers as well as whole numbers. Division by zero must be handled to avoid an error in division-related operations.

---

## 5. Common Mistakes to Avoid

1. Using `=` instead of `==` when comparing values.
2. Confusing `/` with `//`.
3. Assuming `%` returns the quotient instead of the remainder.
4. Forgetting that string comparisons are case-sensitive.
5. Assuming `and` returns `True` when only one condition is true.
6. Forgetting to handle division by zero.
7. Confusing `^` with exponentiation. In Python, use `**` for powers; `^` is the bitwise XOR operator.

---

## 6. Practice Exercises

Try to solve these exercises on your own.

1. Write a program to perform all seven arithmetic operations on two numbers.
2. Check whether a number is even or odd using the modulus operator.
3. Compare two numbers using all six comparison operators.
4. Write a program that checks whether a person is between 18 and 60 years old using `and`.
5. Write a program that checks whether a person can enter using either a valid pass or a special permission, using `or`.
6. Use the `not` operator to reverse a Boolean value.
7. Create a calculator that accepts two numbers and displays the results of arithmetic operations.

---

## Conclusion

Operators are essential in Python programming because they allow us to perform calculations, compare values, and combine conditions.

In this tutorial, we learned about:

* Arithmetic operators
* Comparison operators
* Logical operators
* Division, floor division, modulus, and exponentiation
* A practical calculator project

Understanding these operators will help you write more effective Python programs and build more advanced projects.

**Next Topic:** Continue learning Python with the next topic in the series.
