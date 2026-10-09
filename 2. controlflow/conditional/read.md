# Python Programming Language

# Control Flow: Conditional Statements

## Introduction

Control flow determines the order in which statements are executed in a Python program.

Conditional statements allow a program to make decisions based on specific conditions. Depending on whether a condition is `True` or `False`, Python executes the appropriate block of code.

In this tutorial, we will learn about:

1. `if` statements
2. `if-else` statements
3. `if-elif-else` statements
4. Nested conditional statements
5. Practical examples
6. Common mistakes and best practices

---

## 1. The `if` Statement

The `if` statement evaluates a condition and executes a block of code only when the condition is `True`.

### Syntax

```python
if condition:
    # Code executes when the condition is True
```

### Example

```python
age = 20

if age >= 18:
    print("You are eligible to vote.")
```

**Output:**

```text
You are eligible to vote.
```

**Explanation:**

* The variable `age` contains the value `20`.
* Python checks whether `age >= 18`.
* The condition is `True`, so the indented statement executes.

If the condition is `False`, the code inside the `if` block will not execute.

---

## 2. The `if-else` Statement

The `if-else` statement allows a program to choose between two possible paths.

* The `if` block executes when the condition is `True`.
* The `else` block executes when the condition is `False`.

### Syntax

```python
if condition:
    # Executes when the condition is True
else:
    # Executes when the condition is False
```

### Example: Voting Eligibility

```python
age = 16

if age >= 18:
    print("You are eligible to vote.")
else:
    print("You are a minor.")
```

**Output:**

```text
You are a minor.
```

**Explanation:**

Since the age is `16`, the condition `age >= 18` is `False`. Therefore, Python executes the `else` block.

---

## 3. The `if-elif-else` Statement

The `elif` statement means **else if**. It allows us to check multiple conditions in a program.

Python checks the conditions from top to bottom. The first condition that evaluates to `True` has its corresponding block executed. The remaining conditions are skipped.

If none of the conditions is true, the `else` block executes.

### Syntax

```python
if condition1:
    # Code for condition1
elif condition2:
    # Code for condition2
else:
    # Code when all conditions are False
```

### Example: Classifying Age Groups

```python
age = 17

if age < 13:
    print("You are a child.")
elif age < 18:
    print("You are a teenager.")
else:
    print("You are an adult.")
```

**Output:**

```text
You are a teenager.
```

**Explanation:**

1. `age < 13` is `False`.
2. `age < 18` is `True`.
3. Python prints `"You are a teenager."` and skips the `else` block.

You can use multiple `elif` statements whenever you need to check additional conditions.

---

## 4. Nested Conditional Statements

A nested conditional statement is a conditional statement placed inside another conditional statement.

Nested statements are useful when a program needs to make a decision inside another decision.

### Syntax

```python
if condition1:
    if condition2:
        # Code when both conditions are True
    else:
        # Code when condition1 is True but condition2 is False
else:
    # Code when condition1 is False
```

### Example: Checking Positive, Negative, Even, or Odd

The following program checks whether a number is positive and whether it is even or odd. It also handles zero and negative numbers.

```python
number = int(input("Enter a number: "))

if number > 0:
    print("The number is positive.")

    if number % 2 == 0:
        print("The number is even.")
    else:
        print("The number is odd.")

elif number < 0:
    print("The number is negative.")

else:
    print("The number is zero.")
```

### Sample Execution 1

Input:

```text
Enter a number: 12
```

Output:

```text
The number is positive.
The number is even.
```

### Sample Execution 2

Input:

```text
Enter a number: 11
```

Output:

```text
The number is positive.
The number is odd.
```

### Sample Execution 3

Input:

```text
Enter a number: -1
```

Output:

```text
The number is negative.
```

### Sample Execution 4

Input:

```text
Enter a number: 0
```

Output:

```text
The number is zero.
```

**Explanation:**

* The outer conditional checks whether the number is positive, negative, or zero.
* If the number is positive, the nested `if-else` checks whether it is even or odd.
* The modulus operator (`%`) returns the remainder. A positive number is even when `number % 2 == 0`.

---

## 5. Practical Example: Checking Leap Years

A leap year generally has 366 days instead of 365 days.

The leap-year rules are:

* A year divisible by 400 is a leap year.
* A year divisible by 100 but not by 400 is not a leap year.
* A year divisible by 4 but not by 100 is a leap year.
* All other years are not leap years.

### Example Program

```python
year = int(input("Enter the year: "))

if year % 400 == 0:
    print(year, "is a leap year.")
elif year % 100 == 0:
    print(year, "is not a leap year.")
elif year % 4 == 0:
    print(year, "is a leap year.")
else:
    print(year, "is not a leap year.")
```

### Sample Execution 1

Input:

```text
Enter the year: 2024
```

Output:

```text
2024 is a leap year.
```

### Sample Execution 2

Input:

```text
Enter the year: 2022
```

Output:

```text
2022 is not a leap year.
```

### Sample Execution 3

Input:

```text
Enter the year: 2000
```

Output:

```text
2000 is a leap year.
```

### Sample Execution 4

Input:

```text
Enter the year: 1900
```

Output:

```text
1900 is not a leap year.
```

**Explanation:**

The program uses the modulus operator to check divisibility. Checking divisibility by 400 and 100 before divisibility by 4 ensures that century years are handled correctly.

---

## 6. Practical Project: Simple Calculator

A calculator is a useful project for practising conditional statements and arithmetic operators.

The program accepts two numbers and an operation from the user. It then performs the selected operation using `if`, `elif`, and `else`.

### Example Program

```python
num1 = float(input("Enter the first number: "))
num2 = float(input("Enter the second number: "))

operation = input(
    "Enter an operation (+, -, *, /, %): "
)

if operation == "+":
    result = num1 + num2

elif operation == "-":
    result = num1 - num2

elif operation == "*":
    result = num1 * num2

elif operation == "/":
    if num2 != 0:
        result = num1 / num2
    else:
        result = "Cannot divide by zero."

elif operation == "%":
    if num2 != 0:
        result = num1 % num2
    else:
        result = "Cannot calculate modulus by zero."

else:
    result = "Invalid operation."

print("Result:", result)
```

### Sample Execution

Input:

```text
Enter the first number: 12
Enter the second number: 24
Enter an operation (+, -, *, /, %): +
```

Output:

```text
Result: 36.0
```

**Explanation:**

* `float()` converts the user's input into a floating-point number.
* `input()` accepts the operation.
* `if-elif-else` selects the correct calculation.
* A nested `if-else` prevents division by zero.

---

## 7. Practical Example: Ticket Pricing Based on Age

Conditional statements can also be used in real-world applications to calculate ticket prices.

For this example, the pricing rules are:

* Children under 5 years old: Free
* Children under 12 years old: $10
* Students under 17 years old: $12
* All other customers: $15

### Example Program

```python
age = int(input("Enter your age: "))
is_student = input("Are you a student? (yes/no): ").lower()

if age < 5:
    price = 0

elif age < 12:
    price = 10

elif age < 17 and is_student == "yes":
    price = 12

else:
    price = 15

print("Ticket price: $", price)
```

### Sample Execution

Input:

```text
Enter your age: 15
Are you a student? (yes/no): yes
```

Output:

```text
Ticket price: $ 12
```

**Explanation:**

The program uses `if-elif-else` to select a price and the logical operator `and` to check both the age and student status.

The conditions are evaluated in order, so the age ranges must be arranged carefully.

---

## 8. Common Mistakes to Avoid

1. **Missing a colon:** Always add `:` after `if`, `elif`, and `else`.
2. **Incorrect indentation:** Keep statements inside the correct conditional block.
3. **Using `=` instead of `==`:** Use `==` to compare two values.
4. **Incorrect condition order:** Put more specific conditions before broader conditions when necessary.
5. **Forgetting the `else` block:** Use `else` when you need to handle all remaining cases.
6. **Incorrect leap-year logic:** A year divisible by 100 is not automatically a leap year.
7. **Ignoring division by zero:** Check the denominator before division or modulus operations.
8. **Using too many nested statements:** Prefer clear conditions and `elif` where appropriate.

---

## 9. Best Practices

* Use meaningful variable names such as `age`, `year`, and `ticket_price`.
* Keep indentation consistent, preferably four spaces per level.
* Write clear and simple conditions.
* Use `elif` to handle multiple alternative conditions.
* Test your program with different inputs, including boundary values.
* Handle invalid input and exceptional cases when developing larger programs.
* Avoid unnecessary nesting to make code easier to read and maintain.

---

## 10. Practice Exercises

Try solving the following exercises independently before checking any solutions.

1. Write a program to check whether a person is eligible to vote.
2. Write a program to classify a person as a child, teenager, or adult.
3. Write a program to determine whether a number is positive, negative, or zero.
4. Check whether a positive number is even or odd.
5. Write a program to check whether a year is a leap year.
6. Create a simple calculator using `if`, `elif`, and `else`.
7. Calculate ticket prices based on age and student status.
8. Write a program to find the largest of three numbers.
9. Write a program to assign grades based on marks.
10. Test your programs with boundary values such as `0`, `4`, `5`, `12`, `17`, and `18`.

---

## Conclusion

Conditional statements are an essential part of Python control flow. They allow programs to make decisions and execute different blocks of code depending on the conditions.

In this tutorial, we learned about:

* The `if` statement
* The `if-else` statement
* The `if-elif-else` statement
* Nested conditional statements
* Leap-year checking
* A simple calculator
* Age-based ticket pricing
* Common mistakes and best practices

Practising these examples will help you understand decision-making in Python and prepare you for more advanced programming concepts.

**Next Topic:** Loops in Python — `for` loops and `while` loops.
