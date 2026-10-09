# Python Programming Language

# Getting Started with VS Code

## Python Loops

### 1. Introduction

Loops are used to execute a block of code repeatedly. They help reduce code duplication and make programs more efficient.

In Python, the main types of loops are:

* `for` loop
* `while` loop

Python also provides loop control statements:

* `break`
* `continue`
* `pass`

Other important concepts include nested loops, the `range()` function, and practical programming problems.

---

## 2. The `for` Loop

A `for` loop is used to iterate over a sequence of elements, such as numbers, strings, lists, and other iterable objects.

### Syntax

```python
for variable in iterable:
    # Code to execute
```

### Example 1: Using `range()`

```python
for i in range(5):
    print(i)
```

**Output:**

```text
0
1
2
3
4
```

The `range(5)` function generates numbers from `0` to `4`. The stop value `5` is excluded.

### Example 2: Specifying Start and Stop Values

```python
for i in range(1, 6):
    print(i)
```

**Output:**

```text
1
2
3
4
5
```

Here, `range(1, 6)` generates numbers from `1` to `5`.

### Example 3: Using a Step Value

The `range()` function accepts three parameters:

```python
range(start, stop, step)
```

* `start`: The starting value. The default is `0`.
* `stop`: The ending boundary, which is excluded.
* `step`: The increment or decrement between values. The default is `1`.

**Example:**

```python
for i in range(1, 10, 2):
    print(i)
```

**Output:**

```text
1
3
5
7
9
```

The step value `2` skips every other number.

### Example 4: Counting Backward

```python
for i in range(10, 0, -1):
    print(i)
```

**Output:**

```text
10
9
8
7
6
5
4
3
2
1
```

A negative step value allows the loop to count backward.

### Example 5: Iterating Through a String

A string is a sequence of characters. A `for` loop can access each character individually.

```python
text = "Python"

for character in text:
    print(character)
```

**Output:**

```text
P
y
t
h
o
n
```

This approach can also be used with longer sentences and paragraphs.

---

## 3. The `while` Loop

A `while` loop repeatedly executes a block of code as long as its condition is `True`.

### Syntax

```python
while condition:
    # Code to execute
```

### Example 1: Printing Numbers from 0 to 4

```python
count = 0

while count < 5:
    print(count)
    count = count + 1
```

**Output:**

```text
0
1
2
3
4
```

**How it works:**

1. The variable `count` starts at `0`.
2. The condition `count < 5` is checked.
3. If the condition is `True`, the current value is printed.
4. The count is increased by `1`.
5. The loop stops when `count` becomes `5`.

**Important:** Always make sure that a `while` loop can eventually become false. Otherwise, it may run indefinitely.

### Example 2: Checking for an Even Number

The modulo operator `%` returns the remainder after division.

```python
count = 0

while count % 2 == 0:
    print(count)
    count = count + 1
```

**Output:**

```text
0
```

Initially, `0 % 2 == 0` is true. After printing `0`, the count becomes `1`. The condition is then false, so the loop stops.

---

## 4. Loop Control Statements

Loop control statements change how a loop executes.

### 4.1 The `break` Statement

The `break` statement immediately terminates the nearest enclosing loop.

**Example:**

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

**Output:**

```text
0
1
2
3
4
```

When `i` becomes `5`, the `break` statement terminates the loop. Therefore, `5` is not printed.

### 4.2 The `continue` Statement

The `continue` statement skips the remaining statements in the current iteration and moves to the next iteration.

**Example: Printing Odd Numbers**

```python
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)
```

**Output:**

```text
1
3
5
7
9
```

When `i` is even, the `continue` statement skips the `print()` statement. Only odd numbers are printed.

### 4.3 The `pass` Statement

The `pass` statement does nothing. It acts as a placeholder when a statement is syntactically required but the code has not been implemented yet.

**Example:**

```python
for i in range(5):
    if i == 3:
        pass
    print(i)
```

**Output:**

```text
0
1
2
3
4
```

Unlike `break` and `continue`, `pass` does not terminate the loop or skip the current iteration.

It is also useful when defining an empty function temporarily:

```python
def my_function():
    pass
```

### Difference Between `break`, `continue`, and `pass`

| Statement  | Purpose                                                 |
| ---------- | ------------------------------------------------------- |
| `break`    | Terminates the nearest enclosing loop.                  |
| `continue` | Skips the remaining code in the current iteration.      |
| `pass`     | Does nothing and allows execution to continue normally. |

---

## 5. Nested Loops

A nested loop is a loop placed inside another loop.

The inner loop completes its iterations for each iteration of the outer loop.

### Example

```python
for i in range(3):
    for j in range(2):
        print(f"i = {i}, j = {j}")
```

**Output:**

```text
i = 0, j = 0
i = 0, j = 1
i = 1, j = 0
i = 1, j = 1
i = 2, j = 0
i = 2, j = 1
```

**Explanation:**

* The outer loop runs three times.
* The inner loop runs twice for every outer-loop iteration.
* Therefore, the `print()` statement executes six times.

The expression `f"i = {i}, j = {j}"` is an **f-string**. It allows variables to be inserted into a string using curly braces `{}`.

---

## 6. Practical Example 1: Sum of the First 10 Natural Numbers

### Using a `while` Loop

```python
n = 10
total = 0
count = 1

while count <= n:
    total = total + count
    count = count + 1

print("Sum =", total)
```

**Output:**

```text
Sum = 55
```

**Explanation:**

1. `n` specifies the number of natural numbers.
2. `total` stores the running sum.
3. `count` starts at `1`.
4. Each iteration adds `count` to `total`.
5. The count increases until it exceeds `n`.

### Using a `for` Loop

```python
n = 10
total = 0

for i in range(1, n + 1):
    total = total + i

print("Sum =", total)
```

**Output:**

```text
Sum = 55
```

Both programs calculate:

`1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + 10 = 55`

Notice that `range(1, n + 1)` is used because the stop value is excluded.

---

## 7. Practical Example 2: Find Prime Numbers Between 1 and 100

A **prime number** is an integer greater than `1` that has exactly two positive divisors: `1` and itself.

Examples: `2`, `3`, `5`, `7`, and `11`.

The following program uses nested loops and the `break` statement to identify prime numbers.

```python
for num in range(2, 101):
    is_prime = True

    for i in range(2, num):
        if num % i == 0:
            is_prime = False
            break

    if is_prime:
        print(num)
```

**Output:**

```text
2
3
5
7
11
13
17
19
23
29
31
37
41
43
47
53
59
61
67
71
73
79
83
89
97
```

**Explanation:**

1. The outer loop checks each number from `2` through `100`.
2. The variable `is_prime` initially assumes that the number is prime.
3. The inner loop checks whether any number from `2` to `num - 1` divides it evenly.
4. If `num % i == 0`, the number is not prime, so `is_prime` becomes `False`.
5. The `break` statement stops checking that number once a divisor is found.
6. If `is_prime` remains `True`, the number is printed.

**Note:** This is a beginner-friendly solution. More efficient methods can reduce the number of divisibility checks.

---

## 8. Common Mistakes in Python Loops

### Mistake 1: Forgetting the Colon

Incorrect:

```python
for i in range(5)
    print(i)
```

Correct:

```python
for i in range(5):
    print(i)
```

### Mistake 2: Incorrect Indentation

Python uses indentation to define the body of a loop.

Incorrect:

```python
for i in range(5):
print(i)
```

Correct:

```python
for i in range(5):
    print(i)
```

### Mistake 3: Forgetting to Update a `while` Loop Variable

Incorrect:

```python
count = 0

while count < 5:
    print(count)
```

The condition remains true because `count` never changes.

Correct:

```python
count = 0

while count < 5:
    print(count)
    count += 1
```

### Mistake 4: Misunderstanding the `range()` Stop Value

```python
for i in range(1, 5):
    print(i)
```

This prints `1`, `2`, `3`, and `4`, not `5`.

To include `5`, use `range(1, 6)`.

### Mistake 5: Confusing `pass` with `continue`

* `pass` does nothing.
* `continue` skips the remaining statements in the current iteration.
* `break` exits the nearest enclosing loop.

---

## 9. Practice Exercises

Try solving these problems independently before checking the solutions.

1. Print numbers from `1` to `20` using a `for` loop.
2. Print all even numbers between `1` and `50`.
3. Print numbers from `10` down to `1`.
4. Calculate the sum of the first `n` natural numbers.
5. Print the multiplication table of a number entered by the user.
6. Count the number of vowels in a string.
7. Use `break` to stop a loop when the number reaches `7`.
8. Use `continue` to print numbers from `1` to `20`, excluding multiples of `3`.
9. Use nested loops to print a rectangle of stars.
10. Print all prime numbers between `1` and `100`.

---

## 10. Key Takeaways

* A `for` loop iterates over an iterable such as a string, list, or range.
* A `while` loop repeats as long as its condition remains true.
* The `range()` function generates a sequence of integers.
* `break` terminates the nearest enclosing loop.
* `continue` skips the current iteration.
* `pass` acts as a placeholder and performs no operation.
* Nested loops are useful when working with combinations, patterns, and multidimensional data.
* Indentation and correct loop conditions are essential in Python.

## Conclusion

Loops are an important part of Python programming because they allow us to execute code repeatedly without writing the same statements multiple times.

By practising `for` loops, `while` loops, loop control statements, and nested loops, we can solve problems such as calculating sums, checking prime numbers, processing strings, and generating patterns.

Understanding these concepts provides a strong foundation for working with Python data structures, including lists, tuples, sets, and dictionaries.

**Next topic:** Python data structures and iteration using lists and dictionaries.
