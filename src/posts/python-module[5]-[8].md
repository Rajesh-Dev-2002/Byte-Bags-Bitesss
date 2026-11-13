---
title: Python-module[5]-[7]
date: 2026-11-08
category: Coding
place: Bengaluru, India
summary: Python-module[5]-[7]
---

## Module 5:Object-Oriented Programming

`Introduction`

Object-Oriented Programming (OOP) is a programming approach based on classes and objects. It helps organize code, reuse functionality, and build large applications efficiently.

Python supports four main OOP principles:


- Encapsulation

- Inheritance

- Polymorphism

- Abstraction

In this module, we will learn how to create classes, work with objects, use methods, and understand the important concepts of OOP.

`1. Classes and Objects`

A class is a blueprint used to create objects. An object is an instance of a class that contains data and behavior.

`Example`

```jsx
class Student:
    name = "Rahul"
    age = 22

student1 = Student()

print(student1.name)
print(student1.age)
```

`Output`
```jsx
Rahul
22
```

`2. Constructors and init()`

A constructor is a special method that is automatically called when an object is created.

In Python, __init__() is commonly used to initialize object attributes.

`Example`

```jsx
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age

student1 = Student("Rahul", 22)

print(student1.name)
print(student1.age)
```

`Output`
```jsx
Rahul
22
```

`3. Instance, Class, and Static Methods`

Python supports three main types of methods.

`A. Instance Method`

An instance method works with object-specific data and uses self.

```jsx
class Student:
    def __init__(self, name):
        self.name = name

    def display(self):
        print("Name:", self.name)

s1 = Student("Rahul")
s1.display()
```
`Output:`
```jsx
Name: Rahul
```
`B. Class Method`

A class method works with class-level data and uses cls.

```jsx
class Student:
    school = "ABC School"

    @classmethod
    def display_school(cls):
        print(cls.school)

Student.display_school()
```

`Output`
```jsx
ABC School
```

`C. Static Method`

A static method does not require self or cls. It is used for utility operations related to a class.

```jsx
class Calculator:
    @staticmethod
    def add(a, b):
        return a + b

print(Calculator.add(10, 20))
```
`Output`
```jsx
30
```
`4. Inheritance`

Inheritance allows one class to acquire the properties and methods of another class.

The existing class is called the parent class, and the new class is called the child class.

`Example`
```jsx
class Animal:
    def eat(self):
        print("Animal is eating")

class Dog(Animal):
    def bark(self):
        print("Dog is barking")

dog = Dog()

dog.eat()
dog.bark()
```
`output`
```jsx
Animal is eating
Dog is barking
```
`Types of Inheritance`

- Single Inheritance

- Multiple Inheritance

- Multilevel Inheritance

- Hierarchical Inheritance

- Hybrid Inheritance

`A. Single Inheritance`

Single inheritance occurs when one child class inherits properties and methods from one parent class.

`Example:`
```jsx
class Parent:
    def display(self):
        print("This is Parent class")

class Child(Parent):
    def show(self):
        print("This is Child class")

obj = Child()
obj.display()
obj.show()
```
`Output`
```jsx
This is Parent class
This is Child class
```
`B. Multiple Inheritance`

Multiple inheritance occurs when one child class inherits properties and methods from two or more parent classes.

`Example:`
```jsx
class Father:
    def father_skill(self):
        print("Father: Driving")

class Mother:
    def mother_skill(self):
        print("Mother: Cooking")

class Child(Father, Mother):
    def child_skill(self):
        print("Child: Programming")

obj = Child()

obj.father_skill()
obj.mother_skill()
obj.child_skill()
```
`Output:`
```jsx
Father: Driving
Mother: Cooking
Child: Programming
```
`C. Multilevel Inheritance`

Multilevel inheritance occurs when a class inherits from another child class, creating a chain of inheritance.

`Example:`
```jsx
class Grandparent:
    def display_grandparent(self):
        print("Grandparent class")

class Parent(Grandparent):
    def display_parent(self):
        print("Parent class")

class Child(Parent):
    def display_child(self):
        print("Child class")

obj = Child()

obj.display_grandparent()
obj.display_parent()
obj.display_child()
```

`Output:`
```jsx
Grandparent class
Parent class
Child class
```

`D. Hierarchical Inheritance`

Hierarchical inheritance occurs when multiple child classes inherit properties and methods from a single parent class.

`Example:`
```jsx
class Animal:
    def eat(self):
        print("Animals can eat")

class Dog(Animal):
    def bark(self):
        print("Dog barks")

class Cat(Animal):
    def meow(self):
        print("Cat meows")

dog = Dog()
cat = Cat()

dog.eat()
dog.bark()

cat.eat()
cat.meow()
```

`Output:`
```jsx
Animals can eat
Dog barks
Animals can eat
Cat meows
```

`E. Hybrid Inheritance`

Hybrid inheritance is a combination of two or more types of inheritance.

`Example:`
```jsx
class A:
    def show_a(self):
        print("Class A")

class B(A):
    def show_b(self):
        print("Class B")

class C(A):
    def show_c(self):
        print("Class C")

class D(B, C):
    def show_d(self):
        print("Class D")

obj = D()

obj.show_a()
obj.show_b()
obj.show_c()
obj.show_d()
```

`Output:`
```jsx
Class A
Class B
Class C
Class D
```
`Difference Between Types of Inheritance`

```jsx
Type                                 Description

Single                               One child inherits from one parent

Multiple                             One child inherits from multiple parents

Multilevel                           Inheritance happens in a chain

Hierarchical                         Multiple children inherit from one parent

Hybrid                               Combination of multiple inheritance types
```

`5. Polymorphism`

Polymorphism means one name or interface can have different behaviors depending on the object.

`Example`

```jsx
class Dog:
    def sound(self):
        print("Dog barks")

class Cat:
    def sound(self):
        print("Cat meows")

dog = Dog()
cat = Cat()

dog.sound()
cat.sound()
```
`Output`
```jsx
Dog barks
Cat meows
```
`6. Encapsulation and Abstraction`

`A.Encapsulation`

Encapsulation means combining data and methods inside a class and controlling access to the data.

Python uses naming conventions to indicate access level :

- Public:name

- Protected:_name

- Private:__name

`Example:`
```jsx
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance

    def get_balance(self):
        return self.__balance

account = BankAccount(5000)

print(account.get_balance())
```
`Output`
```jsx
5000
```
`B. Abstraction`

Abstraction means hiding implementation details and showing only essential functionality.

Python provides the abc module to implement abstraction using abstract classes.

`Example:`
```jsx
from abc import ABC, abstractmethod

class Animal(ABC):

    @abstractmethod
    def sound(self):
        pass

class Dog(Animal):
    def sound(self):
        print("Dog barks")

dog = Dog()
dog.sound()
```

`Output:`
```jsx
Dog barks
```

`7. Method Overriding and Overloading Concepts`

`A. Method Overriding`

Method overriding occurs when a child class provides its own implementation of a method already defined in the parent class.
```jsx
class Animal:
    def sound(self):
        print("Animal makes a sound")

class Dog(Animal):
    def sound(self):
        print("Dog barks")

dog = Dog()
dog.sound()
```

`Output:`
```jsx
Dog barks
```

`B. Method Overloading`

Method overloading means defining multiple methods with the same name but different parameters.

Python does not support traditional method overloading directly. Similar behavior can be achieved using default arguments or *args.
```jsx
class Calculator:
    def add(self, a, b=0, c=0):
        return a + b + c

calc = Calculator()

print(calc.add(10, 20))
print(calc.add(10, 20, 30))
```

`Output:`
```jsx
30
60
```

`8. super() and the self Keyword`

`A. self Keyword`

self represents the current object of a class. It is used to access instance variables and methods.
```jsx
class Student:
    def __init__(self, name):
        self.name = name

    def display(self):
        print(self.name)

s1 = Student("Rahul")
s1.display()
```

`Output:`
```jsx
Rahul
```

`B. super() Function`

super() is used to access methods of a parent class from a child class.
```jsx
class Parent:
    def display(self):
        print("Parent class")

class Child(Parent):
    def display(self):
        super().display()
        print("Child class")

obj = Child()
obj.display()
```
`Output:`
```jsx
Parent class
Child class
```

`9. Dunder Methods and Properties`

`A. Dunder Methods`

Dunder methods are special methods that start and end with double underscores.

`Examples:`

- **__init__()** - Initializes an object.

- **__str__()** - Returns a readable string representation.

- **__len__()** - Defines the behavior of len().

- **__add__()** - Defines addition behavior.

`Example`
```jsx
class Student:
    def __init__(self, name):
        self.name = name

    def __str__(self):
        return self.name

student = Student("Rahul")

print(student)
```

`Output:`
```jsx
Rahul
```
`B. Properties`

Properties allow us to access methods like attributes using the @property decorator.

```jsx
class Student:
    def __init__(self, name):
        self._name = name

    @property
    def name(self):
        return self._name

student = Student("Rahul")

print(student.name)
```

`Output:`
```jsx
Rahul
```
## Module 6: Advanced Python

`Introduction`

Advanced Python concepts help developers write efficient, reusable, and professional applications. They provide better ways to handle errors, manage files, organize code, and automate tasks.

In this module, we will explore important advanced Python features used in real-world development.

`1. Exception Handling`

Exception handling is used to handle runtime errors without stopping the entire program unexpectedly.

Python provides the following keywords:

- **try**

- **except**

- **else**

- **finally**

- **raise**

`Example`
```jsx
try:
    a = 10
    b = 0
    result = a / b

except ZeroDivisionError:
    print("Cannot divide by zero")

finally:
    print("Program completed")
```

`Output:`
```jsx
Cannot divide by zero
Program completed
```

`2. File Handling`

File handling allows Python programs to create, read, write, and modify files.

`Common File Modes`
```jsx
Mode                                 Description

r                                    Read a file

w                                    Write to a file

a                                    Append data

x                                    Create a new file

rb                                   Read a binary file

wb                                   Write a binary file
```

`Example: Writing to a File`
```jsx
with open("sample.txt", "w") as file:
    file.write("Welcome to Python")
```

`Example: Reading a File`
```jsx
with open("sample.txt", "r") as file:
    content = file.read()


print(content)
```

`Output`
```jsx
Welcome to Python
```
`3. Modules and Packages`

`A. Modules`

A module is a Python file containing functions, variables, and classes that can be reused in another Python program.

`Example`
```jsx
import math

print(math.sqrt(25))
print(math.pi)
```
`Output:`
```jsx
5.0
3.141592653589793
```

`B. Packages`

A package is a collection of related Python modules organized inside a directory.

`Example structure:`
```jsx
my_package/
    __init__.py
    calculator.py
    operations.py
```

`Importing a Module`
```jsx
import math

print(math.factorial(5))
```

`Output:`
```jsx
120
```

`4. Iterators and Generators`

`A. Iterators`

An iterator is an object that allows us to access elements one at a time using next().

Python provides iter() and next() functions.

`Example`
```jsx
numbers = [10, 20, 30]

iterator = iter(numbers)

print(next(iterator))
print(next(iterator))
print(next(iterator))
```

`Output:`
```jsx
10
20
30
```

`B. Generators`

A generator is a special type of iterator that produces values one at a time using the yield keyword.

`Example`
```jsx
def numbers():
    yield 10
    yield 20
    yield 30

for num in numbers():
    print(num)
```

`Output:`
```jsx
10
20
30
```

`5. Decorators`

A decorator is a function that modifies or extends the behavior of another function without changing its original code.

`Example`
```jsx
def decorator(func):
    def wrapper():
        print("Before function")
        func()
        print("After function")
    return wrapper

@decorator
def greet():
    print("Hello Python")

greet()
```

`Output:`

```jsx
Before function
Hello Python
After function
```
`6. Regular Expressions`

Regular Expressions **(RegEx)** are used to search, match, and manipulate text based on specific patterns.

Python provides the re module for regular expressions.

`Common RegEx Functions`
```jsx
Function                                  Description

search()                                  Finds the first match

match()                                   Checks for a match at the beginning

findall()                                 Returns all matches

sub()                                     Replaces matched text

split()                                   Splits text using a pattern
```
`Example`
```jsx
import re

text = "My phone number is 9876543210"

result = re.findall(r"\d+", text)

print(result)
```

`Output:`
```jsx
['9876543210']
```
`7. Working with JSON`

JSON **(JavaScript Object Notation)** is a popular format used to exchange data between applications.

Python provides the built-in json module to work with JSON data.

`Common JSON Methods`
```jsx
Method                        Description

json.dumps()                  Converts Python data into a JSON string

json.loads()                  Converts a JSON string into Python data

json.dump()                   Writes JSON data to a file

json.load()                   Reads JSON data from a file
```
`Example`

```jsx
import json

student = {
    "name": "Rahul",
    "age": 22,
    "course": "Python"
}

json_data = json.dumps(student)

print(json_data)
```
`Output:`
```jsx
{"name": "Rahul", "age": 22, "course": "Python"}
```
`8. Virtual Environments and pip`

`A. Virtual Environments`

A virtual environment creates an isolated Python environment for a project. It helps manage project-specific dependencies.

`Creating a Virtual Environment`
```jsx
python -m venv myenv
```

`Activating the Environment`

`Windows:`
```jsx
myenv\Scripts\activate
```
`macOS / Linux:`
```jsx
source myenv/bin/activate
```
`Deactivating the Environment`
```jsx
deactivate
```
`B. pip`

pip is Python's package installer. It is used to install and manage external libraries.

`Common pip Commands`
```jsx
Command                         Description
pip install pandas	      Installs Pandas
pip uninstall pandas	      Uninstalls Pandas
pip list	               Displays installed packages
pip show pandas	               Displays package details
pip freeze	               Lists installed packages and versionsExample
```
`Example`
```jsx
pip install numpy
```
`9. Logging and Debugging`

`A. Logging`

Logging helps developers record events, warnings, and errors during program execution.

Python provides the built-in logging module.

`Logging Levels`
```jsx
Level	           Description
DEBUG	           Detailed debugging information
INFO	           General information
WARNING	           Indicates a potential problem
ERROR	           Indicates an error
CRITICAL	   Indicates a serious problem
```
`Example`
```jsx
import logging

logging.basicConfig(level=logging.INFO)

logging.debug("Debug message")
logging.info("Program started")
logging.warning("Warning message")
logging.error("An error occurred")
```
`Output:`
```jsx
INFO:root:Program started
WARNING:root:Warning message
ERROR:root:An error occurred
```
`B. Debugging`

Debugging is the process of identifying and fixing errors in a program.

`Common debugging techniques:`
- Using print() statements.
- Using breakpoints in VS Code.
- Checking error messages.
- Using Python's built-in pdb debugger.


## Module 7: Practical Python
`Introduction`

Practical Python focuses on applying Python programming concepts to real-world projects and applications.

It helps developers work with databases, APIs, files, testing frameworks, data analysis libraries, and version control systems.

In this module, we will learn how Python is used in practical development environments.

`1. Working with CSV and Excel Files`

Python allows us to read, write, and manipulate CSV and Excel files.

`A. Working with CSV Files`

CSV (Comma-Separated Values) is a file format used to store tabular data.

Python provides the built-in csv module.

`Example: Writing a CSV File`
```jsx
import csv

data = [
    ["Name", "Age"],
    ["Rahul", 22],
    ["Priya", 23]
]

with open("students.csv", "w", newline="") as file:
    writer = csv.writer(file)
    writer.writerows(data)
```
`Example: Reading a CSV File`
```jsx
import csv

with open("students.csv", "r") as file:
    reader = csv.reader(file)

    for row in reader:
        print(row)
```
`Output:`

```jsx
['Name', 'Age']
['Rahul', '22']
['Priya', '23']
```
`B. Working with Excel Files`

Python can work with Excel files using libraries such as Pandas and openpyxl.
`Example`
```jsx
import pandas as pd

data = {
    "Name": ["Rahul", "Priya"],
    "Age": [22, 23]
}

df = pd.DataFrame(data)

df.to_excel("students.xlsx", index=False)
```
**Note:** Install the required libraries before running Excel examples.
```jsx
pip install pandas openpyxl
```
`2. Python with MySQL`

Python can connect to MySQL databases to store, retrieve, update, and delete data.

A popular library for connecting Python with MySQL is mysql-connector-python.

`Installation`
```jsx
pip install mysql-connector-python
```
`Example: Connecting to MySQL`
```jsx
import mysql.connector

connection = mysql.connector.connect(
    host="localhost",
    user="root",
    password="your_password",
    database="student_db"
)

if connection.is_connected():
    print("Database connected successfully")

connection.close()
```
`Output:`
```jsx
Database connected successfully
```
`Example: Fetching Data`
```jsx
import mysql.connector

connection = mysql.connector.connect(
    host="localhost",
    user="root",
    password="your_password",
    database="student_db"
)

cursor = connection.cursor()

cursor.execute("SELECT * FROM students")

for row in cursor.fetchall():
    print(row)

cursor.close()
connection.close()
```
**Note:** Replace the database name, username, password, and table name with your actual MySQL details.

`3. Using APIs and HTTP Requests`

An API (Application Programming Interface) allows two applications to communicate and exchange data.

Python provides the requests library to send HTTP requests.

`Common HTTP Methods`
```jsx
Method	                             Description
GET	                             Retrieves data
POST	                             Sends new data
PUT	                             Updates existing data
PATCH	                             Partially updates data
DELETE	                             Deletes data
```
`Installation`
```jsx
pip install requests
```
`Example: GET Request`
```jsx
import requests

url = "https://jsonplaceholder.typicode.com/posts/1"

response = requests.get(url)

print(response.status_code)
print(response.json())
```
`Output:`
```jsx
200
{'userId': 1, 'id': 1, 'title': '...', 'body': '...'}
```

The title and body contain the full response values returned by the API.

`4. Unit Testing with unittest or pytest`

Unit testing checks whether individual parts of a program work correctly.

Python supports different testing frameworks, including unittest and pytest.

`A. Using unittest`

unittest is a built-in Python testing framework.

`Example`
```jsx
import unittest

def add(a, b):
    return a + b

class TestCalculator(unittest.TestCase):

    def test_add(self):
        self.assertEqual(add(10, 20), 30)

if __name__ == "__main__":
    unittest.main()
```
`Expected Result:`
```jsx
Ran 1 test
OK
```
`B. Using pytest`

pytest is a popular external testing framework.

`Installation`
```jsx
pip install pytest
```
`Example`

Create a file named test_calculator.py.
```jsx
def add(a, b):
    return a + b

def test_add():
    assert add(10, 20) == 30
```
`Run the following command:`
```jsx
pytest
```
`Expected Result:`
```jsx
1 passed
```
`5. NumPy and Pandas Basics`

NumPy and Pandas are popular Python libraries used for numerical computing and data analysis.

`A. NumPy`
NumPy is used to perform mathematical operations on arrays efficiently.

`Installation`
```jsx
pip install numpy
```
`Example`
```jsx
import numpy as np

numbers = np.array([10, 20, 30, 40])

print(numbers)
print(numbers.mean())
print(numbers.max())
```
`Output:`
```jsx
[10 20 30 40]
25.0
40
```
`Common NumPy Functions`
```jsx
Function	                            Description
array()	                                Creates an array
mean()	                                Calculates the average
sum()	                                Calculates the total
max()	                                Returns the maximum value
min()	                                Returns the minimum value
reshape()	                            Changes array shape
```
`B. Pandas`

Pandas is used for data manipulation and analysis. It provides two important data structures: Series and DataFrame.

`Installation`
```jsx
pip install pandas
```
`Example`
```jsx
import pandas as pd

data = {
    "Name": ["Rahul", "Priya", "Amit"],
    "Age": [22, 23, 24]
}

df = pd.DataFrame(data)

print(df)
```
`Output:`
```jsx
    Name  Age
0  Rahul   22
1  Priya   23
2   Amit   24
```
`Common Pandas Functions`
```jsx
Function	                  Description
read_csv()	                  Reads a CSV file
read_excel()	                  Reads an Excel file
head()	                          Displays the first rows
tail()	                          Displays the last rows
info()	                          Shows DataFrame information
describe()	                  Generates statistical information
dropna()	                  Removes missing values
fillna()	                  Fills missing values
```
`6. Git and GitHub for Python Projects`

Git is a version control system used to track changes in code.

GitHub is an online platform used to store, manage, and collaborate on Git repositories.

`Common Git Commands`
```jsx
Command	                            Description
git init	                        Initializes a repository
git status	                        Checks repository status
git add .	                        Stages changes
git commit -m "message"         	Saves changes
git push	                        Uploads changes to GitHub
git pull	                        Downloads and integrates updates
git clone	                        Copies a repository 
```
`Example: Pushing a Python Project`
```jsx
git init
git add .
git commit -m "Initial Python project"
git branch -M main
git remote add origin <repository-url>
git push -u origin main
```
**Note:** If you already have an existing GitHub repository connected to your project, you do not need to repeat the initialization and remote setup commands.

`7. Python Interview Questions and Coding Problems`

Python interview preparation helps developers improve their programming knowledge, problem-solving skills, and coding abilities.

`A. Basic Python Interview Questions`

1. What is Python?
2. What are the main features of Python?
3. What are Python data types?
4. What is the difference between a list and a tuple?
5. What is the difference between == and is?
6. What are functions in Python?
7. What is OOP?
8. What is inheritance?
9. What are decorators?
10. What is exception handling?

`B. Common Python Coding Problems`

`1. Reverse a String`
```jsx
text = "Python"

print(text[::-1])
```
`Output:`
```jsx
nohtyP
```
`2. Check Whether a Number Is Even or Odd`
```jsx
num = 10

if num % 2 == 0:
    print("Even number")
else:
    print("Odd number")
```
`Output:`
```jsx
Even number
```
`3. Find the Factorial of a Number`
```jsx
num = 5
factorial = 1

for i in range(1, num + 1):
    factorial *= i

print(factorial)
```
`Output:`
```jsx
120
```
`4. Check Whether a Number Is Prime`
```jsx
num = 7

if num > 1:
    for i in range(2, num):
        if num % i == 0:
            print("Not Prime")
            break
    else:
        print("Prime Number")
else:
    print("Not Prime")
```
`Output:`
```jsx
Prime Number
```
`5. Find the Largest Number in a List`
```jsx
numbers = [10, 50, 20, 80, 30]

print(max(numbers))
```
`Output:`
```jsx
80
```
