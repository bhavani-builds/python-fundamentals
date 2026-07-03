# 🐍 Python Control Flow Assignments

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Status](https://img.shields.io/badge/status-completed-brightgreen.svg)]()
[![License](https://img.shields.io/badge/license-MIT-lightgrey.svg)]()

A collection of beginner-to-intermediate Python programs covering **conditional statements** and **loops**, presented in a Q&A / assignment format. Each solution is self-contained, well-commented, and ready to run.

---

## 📚 Table of Contents

- [About](#about)
- [Module 2: Control Flow Assignments](#module-2-control-flow-assignments)
  - [Lesson 2.1 — Conditional Statements](#lesson-21--conditional-statements)
  - [Lesson 2.2 — Loops](#lesson-22--loops)
- [How to Run](#how-to-run)
- [Concepts Covered](#concepts-covered)
- [Contributing](#contributing)
- [License](#license)

---

## About

This repository walks through core Python control-flow concepts — `if`/`elif`/`else`, `for` loops, `while` loops, `break`, `continue`, and `pass` — through 15 short, focused assignments. Each entry follows a **Q&A format**: the question (assignment prompt) is followed by a working answer (code solution).

---

## Module 2: Control Flow Assignments

### Lesson 2.1 — Conditional Statements

#### Q1. Simple `if` Statement
**Question:** Write a program that asks the user to input a number and prints whether the number is positive.

**Answer:**
```python
number = float(input("Enter a number: "))
if number > 0:
    print("The number is positive.")
```

---

#### Q2. `if-else` Statement
**Question:** Write a program that asks the user to input a number and prints whether the number is positive or negative.

**Answer:**
```python
number = float(input("Enter a number: "))
if number > 0:
    print("The number is positive.")
else:
    print("The number is negative.")
```
**Sample Output:**
```
The number is positive.
```

---

#### Q3. `if-elif-else` Statement
**Question:** Write a program that asks the user to input a number and prints whether the number is positive, negative, or zero.

**Answer:**
```python
number = float(input("Enter a number: "))
if number > 0:
    print("The number is positive.")
elif number < 0:
    print("The number is negative.")
else:
    print("The number is zero.")
```

---

#### Q4. Nested `if` Statement
**Question:** Write a program that asks the user to input a number and prints whether the number is positive and even, positive and odd, or negative.

**Answer:**
```python
number = float(input("Enter a number: "))
if number > 0:
    if number % 2 == 0:
        print("The number is positive and even.")
    else:
        print("The number is positive and odd.")
else:
    print("The number is negative.")
```

---

### Lesson 2.2 — Loops

#### Q5. `for` Loop
**Question:** Write a program that prints all the numbers from 1 to 10 using a `for` loop.

**Answer:**
```python
for i in range(1, 11):
    print(i)
```

---

#### Q6. `while` Loop
**Question:** Write a program that prints all the numbers from 1 to 10 using a `while` loop.

**Answer:**
```python
i = 1
while i <= 10:
    print(i)
    i += 1
```

---

#### Q7. Nested Loops
**Question:** Write a program that prints a 5x5 grid of asterisks (`*`) using nested loops.

**Answer:**
```python
for i in range(5):
    for j in range(5):
        print("*", end=" ")
    print()
```

---

#### Q8. `break` Statement
**Question:** Write a program that asks the user to input numbers until they input 0. The program should print the sum of all the input numbers.

**Answer:**
```python
total = 0
while True:
    number = float(input("Enter a number (0 to stop): "))
    if number == 0:
        break
    total += number
print(f"The sum of all the numbers is {total}.")
```

---

#### Q9. `continue` Statement
**Question:** Write a program that prints all the numbers from 1 to 10 except 5 using a `for` loop and `continue` statement.

**Answer:**
```python
for i in range(1, 11):
    if i == 5:
        continue
    print(i)
```

---

#### Q10. `pass` Statement
**Question:** Write a program that defines an empty function using the `pass` statement.

**Answer:**
```python
def empty_function():
    pass

# Calling the empty function
empty_function()
```

---

#### Q11. Combining Loops and Conditionals
**Question:** Write a program that asks the user to input a number and prints all the even numbers from 1 to that number using a `for` loop.

**Answer:**
```python
number = int(input("Enter a number: "))
for i in range(1, number + 1):
    if i % 2 == 0:
        print(i)
```

---

#### Q12. Factorial Calculation
**Question:** Write a program that calculates the factorial of a number input by the user using a `while` loop.

**Answer:**
```python
number = int(input("Enter a number: "))
factorial = 1
i = 1
while i <= number:
    factorial *= i
    i += 1
print(f"The factorial of {number} is {factorial}.")
```

---

#### Q13. Sum of Digits
**Question:** Write a program that calculates the sum of the digits of a number input by the user using a `while` loop.

**Answer:**
```python
number = int(input("Enter a number: "))
sum_of_digits = 0
while number > 0:
    digit = number % 10
    sum_of_digits += digit
    number = number // 10
print(f"The sum of the digits is {sum_of_digits}.")
```

---

#### Q14. Prime Number Check
**Question:** Write a program that checks if a number input by the user is a prime number using a `for` loop.

**Answer:**
```python
number = int(input("Enter a number: "))
is_prime = True
if number <= 1:
    is_prime = False
else:
    for i in range(2, int(number ** 0.5) + 1):
        if number % i == 0:
            is_prime = False
            break
if is_prime:
    print(f"{number} is a prime number.")
else:
    print(f"{number} is not a prime number.")
```

---

#### Q15. Fibonacci Sequence
**Question:** Write a program that prints the first `n` Fibonacci numbers, where `n` is input by the user.

**Answer:**
```python
n = int(input("Enter the number of Fibonacci numbers to print: "))
a, b = 0, 1
count = 0
while count < n:
    print(a)
    a, b = b, a + b
    count += 1
```

---

## How to Run

1. Make sure you have **Python 3.x** installed.
2. Copy any code block into a `.py` file, e.g. `assignment_1.py`.
3. Run it from your terminal:
   ```bash
   python assignment_1.py
   ```
4. Follow the input prompts as instructed.

---

## Concepts Covered

| Concept | Assignments |
|---|---|
| `if` / `if-else` / `if-elif-else` | Q1 – Q3 |
| Nested conditionals | Q4 |
| `for` loop | Q5, Q7, Q9, Q11, Q14, Q15 |
| `while` loop | Q6, Q8, Q12, Q13, Q15 |
| `break` | Q8, Q14 |
| `continue` | Q9 |
| `pass` | Q10 |
| Combining loops & conditionals | Q11, Q12, Q13, Q14 |

---

## Contributing

Contributions are welcome! If you'd like to add alternate solutions or additional assignments:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/new-assignment`)
3. Commit your changes
4. Open a pull request

---

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
