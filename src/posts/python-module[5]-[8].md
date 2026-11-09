---
title: Python-module[5]-[8]
date: 2026-11-08
category: Coding
place: Bengaluru, India
summary: Python-module[5]-[8]
---

## Module 5:Object-Oriented Programming

`Introduction`

Object-Oriented Programming (OOP) is a programming approach based on classes and objects. It helps organize code, reuse functionality, and build large applications efficiently.

Python supports four main OOP principles:

.Encapsulation

.Inheritance

.Polymorphism

.Abstraction

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

.Single Inheritance

.Multiple Inheritance

.Multilevel Inheritance

.Hierarchical Inheritance

.Hybrid Inheritance

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

Python uses naming conventions to indicate access levels:

. Public:name

. Protected:_name

. Private:__name

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

. __init__() - Initializes an object.

. __str__() - Returns a readable string representation.

. __len__() - Defines the behavior of len().

. __add__() - Defines addition behavior.

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