# 1 Object-Oriented Programming (OOP) in Python

## Definition
Object-Oriented Programming (OOP) is a programming paradigm that organizes code into **classes** and **objects**, enabling better structure, reusability, and modularity.  
A **class** is a blueprint, and an **object** is an instance created from that blueprint.

## Basic Example of Class and Object

```python
class Person:
    def __init__(self, name, age):   # Constructor
        self.name = name             # Attribute
        self.age = age

    def greet(self):                 # Method
        print(f"Hello, my name is {self.name}.")

# Creating an object
p1 = Person("Hima", 20)
p1.greet()
```
---
# OOP Concepts in Python

## 1.1 Encapsulation
Encapsulation means **bundling data (attributes)** and **methods (functions)** into a single unit (class) and restricting direct access to the internal data.

### Example:
```python
class Student:
    def __init__(self, name, grade):
        self.__name = name     # Private attribute
        self.__grade = grade

    def get_grade(self):
        return self.__grade
```
### 1.2 Inheritance
- Inheritance allows a child class to acquire attributes and methods from a parent class.
- It promotes code reusability and establishes relationships between classes.

### Example:
```python
class Animal:
    def speak(self):
        print("Animal speaks")

class Dog(Animal):
    def speak(self):            # Overriding
        print("Dog barks")

d = Dog()
d.speak()
```
### 1.3 Polymorphism
- Polymorphism means the same method name can behave differently depending on the object.
- It allows one interface to be used for different implementations.

### Example:
```python
class Cat:
    def sound(self):
        return "Meow"

class Dog:
    def sound(self):
        return "Bark"

for obj in (Cat(), Dog()):
    print(obj.sound())
```
### 1.4 Abstraction
- Abstraction hides complex implementation details and exposes only essential features.
- Achieved in Python using abstract classes and abstract methods.

### Example:
```python
from abc import ABC, abstractmethod

class Vehicle(ABC):
    @abstractmethod
    def start(self):
        pass

class Car(Vehicle):
    def start(self):
        print("Car started")

c = Car()
c.start()
```
# References 
#### Python Official Documentation
- https://docs.python.org/3/tutorial/classes.html
- https://docs.python.org/3/library/abc.html
#### W3Schools Reference
- https://www.w3schools.com/python/python_classes.asp
- https://www.w3schools.com/python/python_inheritance.asp
#### Programiz Reference
- https://www.programiz.com/python-programming/object-oriented-programming
#### Jenny’s Lectures (OOP in Python)
- https://www.youtube.com/watch?v=Ic7ZBKqkS1E&list=PLdo5W4Nhv31bZSiqiOL5ta39vSnBxpOPT&index=88
#### Telusko – OOPs Concepts in Python
- https://www.youtube.com/watch?v=qiSCMNBIP2g

# 2 SOLID Principles in Python

SOLID is a set of five design principles used in Object-Oriented Programming to create clean, maintainable, and scalable software systems.

The five principles are:

1. **S — Single Responsibility Principle (SRP)**
2. **O — Open/Closed Principle (OCP)**
3. **L — Liskov Substitution Principle (LSP)**
4. **I — Interface Segregation Principle (ISP)**
5. **D — Dependency Inversion Principle (DIP)**

---

## 2.1 Single Responsibility Principle (SRP)

A class should have **only one reason to change** — it should do only one job.

### Wrong: One class doing multiple jobs
```python
class Report:
    def get_data(self):
        return "report data"

    def print_report(self, data):
        print("Printing:", data)

    def save_to_file(self, data):
        open("report.txt", "w").write(data)
```
### correct: One class doing only one jobs
```python
class Report:
    def get_data(self):
        return "report data"

class ReportPrinter:
    def print_report(self, data):
        print("Printing:", data)

class ReportSaver:
    def save_to_file(self, data):
        open("report.txt", "w").write(data)
```
## 2.2 Open/Closed Principle (OCP)
- Classes should be **open for extension** but **closed for modification**.
- You should extend a class by creating new subclasses instead of editing existing code.

```python
class Discount:
    def get_discount(self):
        return 10

class StudentDiscount(Discount):   # Extended behavior
    def get_discount(self):
        return 20

```
## 2.3 Liskov Substitution Principle (LSP)
- Subclasses should be able to **replace** their parent classes **without breaking the program**.
- A derived class must behave consistently with the expectations of the base class.

```python
class Bird:
    def move(self):
        return "Moving"

class Sparrow(Bird):
    def move(self):
        return "Flying"

class Ostrich(Bird):
    def move(self):
        return "Running"
```
## 2.4 Interface Segregation Principle (ISP)
- No class should be forced to implement methods it does not use.
- Prefer **multiple small interfaces** instead of one large interface.

```python
class Workable:
    def work(self):
        pass

class Eatable:
    def eat(self):
        pass

class Human(Workable, Eatable):
    def work(self):
        print("Human working")
    def eat(self):
        print("Human eating")

class Robot(Workable):
    def work(self):
        print("Robot working")
```
## 2.5  Dependency Inversion Principle (DIP)
- High-level modules should depend on **abstractions**, not concrete classes.
- Depend on interfaces, not implementations.

```python
class Database:
    def connect(self):
        pass

class MySQL(Database):
    def connect(self):
        print("MySQL connected")

class PostgreSQL(Database):
    def connect(self):
        print("PostgreSQL connected")

class Application:
    def __init__(self, db: Database):
        self.db = db

app = Application(MySQL())
app.db.connect()
```
# References for SOLID Principles
#### Official Documentation & Articles
- https://docs.python.org/3/tutorial/classes.html  
- https://www.geeksforgeeks.org/solid-principle-in-programming-understanding-the-basics/   
#### Telusko – SOLID Principles
- https://www.youtube.com/watch?v=UQqY3_6Epbg  










