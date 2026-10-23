---
title: Learn Python from Zero to Advanced
date: 2026-10-21
category: coding
summary: Complete Python Tutorial.
---

## Complete course structure
`Module 1: Python Fundamentals`
1. Introduction to Python
2. Installing Python and setting up VS Code or Jupyter Notebook
3. Your first Python program
4. Variables and data types
5. Taking user input with **input()**
6. Type conversion and type casting
7. Operators in Python
8. Comments, indentation, and coding conventions

`Module 2: Conditional Statements and Loops`
1. if, elif, and else
2. Nested conditional statements
3. for loops
4. while loops
5. break, continue, and pass
6. **range()** function
7. Pattern printing and loop-based problems

`Module 3: Python Data Structures`
1. Strings and string methods
2. Lists and list methods
3. Tuples
4. Sets and set operations
5. Dictionaries and dictionary methods
6. Indexing and slicing
7. Mutable vs. immutable objects
8. List, set, and dictionary comprehensions

`Module 4: Functions`
1. Defining and calling functions
2. Parameters and arguments
3. Return statements
4. Default and keyword arguments
5. ****args*** and *****kwargs***
6. Lambda functions
7. Recursion and variable scope

`Module 5: Object-Oriented Programming`
1. Classes and objects
2. Constructors and ***__init__()***
3. Instance, class, and static methods
4. Inheritance
5. Polymorphism
6. Encapsulation and abstraction
7. Method overriding and overloading concepts
8. super() and the self keyword
9. Dunder methods and properties

`Module 6: Advanced Python`
1. Exception handling
2. File handling
3. Modules and packages
4. Iterators and generators
5. Decorators
6. Regular expressions
7. Working with JSON
8. Virtual environments and pip
9. Logging and debugging

`Module 7: Practical Python`
1. Working with CSV and Excel files
2. Python with MySQL
3. Using APIs and HTTP requests
4. Unit testing with unittest or pytest
5. NumPy and Pandas basics
6. Git and GitHub for Python projects
7. Python interview questions and coding problems




## Module 1: Python Fundamentals

Welcome to Module 1! In this module, you will learn the basic concepts of Python programming, from installing Python to writing your first programs.

`Why learn Python?`
- Easy to learn for beginners.
- Used in Artificial Intelligence (AI) and Machine Learning (ML).
- Useful for data analysis and visualization.
- Used in web development and automation.
- Supports object-oriented and procedural programming.

```jsx
print("Hello, World!")
```
Output:
```jsx
Hello, World!
```
## Lesson 2: Installing Python and Setting Up VS Code or Jupyter Notebook

`You can write Python programs using either VS Code or Jupyter Notebook.`
1. Download Python from Python official website.
2. During installation on Windows, select Add Python to PATH.
3. Download Visual Studio Code.
4. Install the Python extension in VS Code.
5. Open a terminal and check your Python installation:

```jsx
python --version
```
For Jupyter Notebook, install it using:

```jsx
pip install notebook
jupyter notebook
```

## Lesson 3: Your First Python Program

The `print()` function displays information on the screen.

```jsx
print("Welcome to Python")
print(100)
print(10 + 20)
```
Output:

```jsx
Welcome to Python
100
30
```
## Lesson 4: Variables and Data Types
A variable stores a value that you can use later in your program.

```jsx
name = "Rajesh"
age = 25
salary = 19000.50
is_working = True

print(name)
print(age)
print(salary)
print(is_working)
```
Common Python data types:
```jsx
Data type	Example
int	        age = 25
float	      price = 99.50
str	        name = "Rajesh"
bool	      is_active = True
list	      numbers = [1, 2, 3]
tuple	      values = (1, 2, 3)
set	        items = {1, 2, 3}
dict	      student = {"name": "Rajesh"}
```
To check a variable's data type:
```jsx
age = 25
print(type(age))
```
Output:
```jsx
<class 'int'>
```

## Lesson 5: Taking User Input with `input()`
The `input() `function accepts information from the user. By default, it returns a string.
```jsx
name = input("Enter your name: ")
print("Hello,", name)
```
Example output:
```jsx
Enter your name: Rajesh
Hello, Rajesh
```
To accept numbers, convert the input:

```jsx
age = int(input("Enter your age: "))
print("Next year, you will be", age + 1)
```
## Lesson 6: Type Conversion and Type Casting
Type conversion changes a value from one data type to another.

```jsx
x = "100"
y = int(x)

print(y + 50)
```
Output:
```jsx
150
```
Common conversion functions:
```jsx
int() — converts a compatible value to an integer.
float() — converts a compatible value to a floating-point number.
str() — converts a value to a string.
bool() — converts a value to a Boolean.
```
Example:
```jsx
price = 99
price_text = str(price)

print(price_text)
print(type(price_text))
```
Output:
```jsx
99
<class 'str'>
```
Note: converting an invalid numeric string, such as `"hello"` to an integer, raises a `ValueError`.
## Lesson 7: Operators in Python
Operators perform calculations and comparisons.

```jsx
Operator type   	       Operators	                 Example
Arithmetic	      +, -, *, /, //, %, **	10 + 5
Comparison	      ==, !=, >, <, >=, <=	10 > 5
Logical	          and, or, not	                 10 > 5 and 5 > 2
Assignment	      =, +=, -=, *=	         x += 2
Membership	      in, not in	                 "a" in "apple"
Identity	        is, is not	         x is None
```
## Lesson 8: Comments, Indentation, and Coding Conventions
Comments explain code and are ignored by the Python interpreter.
```jsx
# This is a single-line comment
print("Learning Python")
```
Indentation defines code blocks in Python. Four spaces per indentation level is the standard convention.

```jsx
age = 20

if age >= 18:
    print("You are eligible")
else:
    print("You are not eligible")
```
Coding conventions:
```jsx
- Use meaningful variable names, such as student_name.
- Use lowercase names with underscores for variables and functions.
- Use consistent four-space indentation.
- Keep code readable and avoid unnecessary repetition.
- Use comments where they clarify the code.
```
## Module 2: Conditional Statements and Loops in Python
`Introduction`

In Python programming, conditional statements and loops are used to control the flow of a program. Conditional statements help us make decisions based on specific conditions, while loops allow us to execute a block of code multiple times.

`For example:`
- We can use an if statement to check whether a student has passed an exam.
- We can use a for loop to print numbers from 1 to 10.
- We can use a while loop to repeat a program until a condition becomes false.

In this module, you will learn how to use conditional statements, loops, control statements, and pattern-printing techniques with practical examples.

1. `if, elif, and else Statements`

Conditional statements allow a program to execute different blocks of code depending on whether a condition is true or false.

`The if Statement`

The if statement executes a block of code when the specified condition is true.

`Example:`

```jsx
age = 20
if age >= 18:
    print("You are eligible to vote.")
```
`Output:`
```jsx
You are eligible to vote.
```
`Explanation:`
- age = 20 stores the person's age.
- age >= 18 checks whether the age is at least 18.
- Since the condition is true, the message is displayed.

`The if-else Statement`

The else statement executes when the if condition is false.

`Example:`
```jsx
number = 7

if number % 2 == 0:
    print("Even number")
else:
    print("Odd number")

```

`Output:`

```jsx 
Odd number
```

The modulus operator % returns the remainder after division. If a number is divisible by 2, it is even; otherwise, it is odd.

`The if-elif-else Statement`

The elif keyword means “else if.” It allows you to check multiple conditions.

`Example:`
```jsx
marks = 85

if marks >= 90:
    print("Grade A+")
elif marks >= 80:
    print("Grade A")
elif marks >= 70:
    print("Grade B")
elif marks >= 60:
    print("Grade C")
else:
    print("Grade D")
```
`Output:`

```jsx
Grade A
```
Python checks the conditions from top to bottom and executes the first matching block.

`Practical Example: Positive, Negative, or Zero`

```jsx 
number = int(input("Enter a number: "))

if number > 0:
    print("Positive number")
elif number < 0:
    print("Negative number")
else:
    print("Zero")
```
This program takes a number from the user and determines whether it is positive, negative, or zero.

`2. Nested Conditional Statements`

A nested conditional statement is an if statement placed inside another if or else statement.

Nested conditions are useful when one decision depends on another decision.

`Example:`
```jsx
age = 22
has_id = True

if age >= 18:
    if has_id:
        print("Entry allowed")
    else:
        print("Please show your ID")
else:
    print("Entry not allowExample:")
```
`Output:`

```jsx 
Entry allowed
```
`Explanation:`

- The outer if checks whether the age is at least 18.
- If the condition is true, the inner if checks whether the person has an ID.
- If both conditions are true, entry is allowed.
`Practical Example: Login Validation`

```jsx
username = input("Enter username: ")
password = input("Enter password: ")

if username == "admin":
    if password == "1234":
        print("Login successful")
    else:
        print("Incorrect password")
else:
    print("Invalid username")
```

This example demonstrates how nested conditions can be used to validate login details. In real applications, passwords should be securely stored and verified rather than hard-coded.

`3. for Loops in Python`

A for loop is used to iterate over a sequence, such as a list, string, or range of numbers.
`Example:`

```jsx
for number in range(1, 6):
    print(number)
```
`Output:`
```jsx
1
2
3
4
5
```
The loop executes five times, assigning the values 1 through 5 to number.

`Iterating Through a List`

```jsx 
fruits = ["Apple", "Banana", "Mango"]

for fruit in fruits:
    print(fruit)
```

`Output:`

```jsx
Apple
Banana
Mango
```

`Iterating Through a String`

```jsx
for character in "Python":
    print(character)
```

This program prints each character of the word Python on a separate line.

`Calculating the Sum of Numbers`

```jsx
total = 0

for number in range(1, 6):
    total += number

print("Total:", total)
```

`Output:`

```jsx
Total: 15
```
The variable total accumulates the values 1, 2, 3, 4, and 5.

`4. while Loops in Python`

A while loop repeatedly executes a block of code as long as its condition remains true.

`Example:`

```jsx
count = 1

while count <= 5:
    print(count)
    count += 1
```
`Output:`

```jsx
1
2
3
4
5
```

`Explanation:`

```jsx
count = 1 initializes the variable.

count <= 5 is the loop condition.

count += 1 increases the value after every iteration.
```

The loop stops when count becomes 6.

`Example: Countdown Program`

```jsx
count = 5

while count >= 1:
    print(count)
    count -= 1

print("Countdown complete!")

```

`Output:`

```jsx
5
4
3
2
1
Countdown complete!
```

`Important Note: Infinite Loops`

An infinite loop occurs when the condition never becomes false.

`For example:`

```jsx
while True:
    print("Running...")
```
This program continues indefinitely unless it is interrupted or a suitable stopping condition is added.

Always ensure that a while loop has a way to terminate when needed.

`5. break, continue, and pass Statements`

Python provides three useful statements to control how code executes inside loops or conditional blocks.

`The break Statement`

The break statement immediately terminates the nearest enclosing loop.

`Example:`
```jsx
for number in range(1, 10):
    if number == 5:
        break

    print(number)
```
`Output:`
```jsx
1
2
3
4
```
When number becomes 5, the loop stops.

`The continue Statement`

The continue statement skips the rest of the current iteration and moves to the next iteration.

`Example:`
```jsx
for number in range(1, 6):
    if number == 3:
        continue

    print(number)
```
`Output:`
```jsx
1
2
4
5
```
The number 3 is skipped, but the loop continues.

`The pass Statement`

The pass statement does nothing. It acts as a placeholder when Python requires a statement syntactically, but you do not want to implement the logic yet.

`Example:`
```jsx
number = 10

if number > 0:
    pass

print("Program completed")
```
`Output:`
```jsx
Program completed
```
`Difference Between break, continue, and pass`
```jsx
Statement          Purpose
break     =>         Terminates the loop immediately.
continue    =>       Skips the current iteration.
pass       =>        Performs no action and allows execution to proceed.
```
`6. The range() Function`

The range() function generates a sequence of integers. It is commonly used with for loops.

Python supports three common forms of range().

`range(stop)`

Starts from 0 and stops before the specified number.
```jsx
for i in range(5):
    print(i)
```
`Output:` 0 1 2 3 4 (each number appears on a separate line).

`range(start, stop)`

Starts from start and stops before stop.
```jsx
for i in range(2, 7):
    print(i)
```
```jsx
Output: 2 3 4 5 6
```

`range(start, stop, step)`

The step specifies how much the number changes each time.
```jsx
for i in range(2, 11, 2):
    print(i)

Output:

2
4
6
8
10
```
`Printing Numbers in Reverse`
```jsx
for i in range(10, 0, -1):
    print(i)

Output: Numbers from 10 down to 1.
```
`Important Points About range()`

- The starting value is included.

- The stopping value is excluded.

- The default starting value is 0 when only stop is provided.

- The default step is 1.

- A negative step can be used to count backwards.

- A step of 0 is not allowed.

`7. Pattern Printing and Loop-Based Problems`

Pattern printing is a useful way to understand nested loops. The outer loop controls the rows, while the inner loop controls the items printed in each row.

`Pattern 1: Right-Angled Star Triangle`

`Code:`
```jsx
for i in range(1, 6):
    for j in range(i):
        print("*", end="")

    print()
```
`Output:`
```jsx
*
**
***
****
*****
```
The outer loop determines the number of rows. The inner loop prints the required number of stars in each row. end="" keeps the stars on the same line, and print() moves to the next line.

`Pattern 2: Number Triangle`

`Code:`
```jsx
for i in range(1, 6):
    for j in range(1, i + 1):
        print(j, end="")

    print()
```
`Output:`
```jsx
1
12
123
1234
12345
```
`Pattern 3: Inverted Star Triangle`

`Code:`
```jsx
for i in range(5, 0, -1):
    for j in range(i):
        print("*", end="")

    print()
```
`Output:`
```jsx
*****
****
***
**
*
```
`Program 4: Multiplication Table`
```jsx
number = int(input("Enter a number: "))

for i in range(1, 11):
    print(number, "x", i, "=", number * i)
```
If the user enters 5, the program displays the multiplication table of 5 from 1 to 10.

`Program 5: Factorial of a Number`

The factorial of a positive integer is the product of all positive integers up to that number. By definition, 0! = 1.
```jsx
number = int(input("Enter a non-negative integer: "))

if number < 0:
    print("Factorial is not defined for negative integers")
else:
    factorial = 1

    for i in range(1, number + 1):
        factorial *= i

    print("Factorial:", factorial)
```
`Example: For input 5, the output is Factorial: 120.`

`Program 6: Sum of Digits`
```jsx
number = int(input("Enter a positive integer: "))
total = 0

while number > 0:
    digit = number % 10
    total += digit
    number //= 10

print("Sum of digits:", total)
```
Example: If the input is 1234, the output is Sum of digits: 10.

The % operator extracts the last digit, while // removes the last digit.

`Program 7: Check Whether a Number Is Prime`

A prime number is a number greater than 1 that has exactly two positive divisors: 1 and itself.
```jsx
number = int(input("Enter a number: "))

if number < 2:
    print("Not a prime number")
else:
    for i in range(2, int(number ** 0.5) + 1):
        if number % i == 0:
            print("Not a prime number")
            break
    else:
        print("Prime number")
```
This program checks for divisors only up to the square root of the number, making it more efficient than checking every smaller number.

`8. Practice Questions`

- Try solving these problems on your own to strengthen your understanding.

- Beginner Level

- Write a program to check whether a number is even or odd.

- Write a program to find the largest of two numbers.

- Print numbers from 1 to 100 using a for loop.

- Print all even numbers between 1 and 50.

- Print the multiplication table of a number entered by the user.

`Intermediate Level`

- Write a program to find the sum of the first N natural numbers.

- Write a program to reverse a number using a while loop.

- Write a program to calculate the factorial of a number.

- Write a program to check whether a number is prime.

- Print a right-angled triangle using numbers and stars.

`Challenge Level`

- Write a program to check whether a number is a palindrome.

- Print the Fibonacci sequence for N terms.

- Print a pyramid pattern using stars.

- Find all prime numbers between 1 and 100.

- Create a simple calculator using if-elif-else statements.

`9. Key Takeaways`

- After completing this module, you should understand:

- How to use if, elif, and else for decision-making.

- How nested conditions work.

- How to iterate over sequences using for loops.

- How to repeat operations using while loops.

- How break, continue, and pass affect program execution.

- How to generate number sequences using range().

- How to solve practical problems using loops and nested loops.

- How to print patterns and write beginner-level programming logic.

`Conclusion`

```jsx
Conditional statements and loops are fundamental concepts in Python programming. They help you build programs that make decisions, repeat tasks, process data, and solve problems efficiently.

Practice each example by running it in VS Code or Jupyter Notebook. Try changing the values, predicting the output, and solving the practice questions independently.

In the next module, you can explore Python Data Structures: Lists, Tuples, Sets, and Dictionaries to learn how to store and manipulate collections of data.
```


> Tip: put every value your effect reads into the dependency array.
