# 🐍 Python Full Notes: Beginner to Advanced

---

## 📌 Introduction to Python
Python is a high-level, interpreted, general-purpose programming language. It emphasizes readability, simplicity, and flexibility. It is dynamically typed and supports multiple programming paradigms, including procedural, object-oriented, and functional programming.

- **Created by**: Guido van Rossum
- **First released**: 1991
- **Current version**: Python 3.x (as of April 2025)
- **Why Python?**:
  - Easy to learn and read
  - Vast standard library and ecosystem
  - Great for scripting, automation, data science, machine learning, web development, etc.

---

## 🧱 Basic Syntax and Variables

### ➤ Variables
Variables are containers for storing data values.
```python
x = 10       # int
y = 3.14     # float
name = "Ali" # str
flag = True  # bool
```

### ➤ Naming Rules
- Can contain letters, digits, and underscores
- Must start with a letter or underscore
- Case-sensitive (`name` and `Name` are different)

---

## 🧮 Data Types and Memory Sizes

| Type   | Description                         | Example          | Typical Size (in bytes) |
|--------|-------------------------------------|------------------|--------------------------|
| int    | Integer numbers                     | `x = 10`         | 28 (varies with value)   |
| float  | Decimal numbers                     | `pi = 3.14`      | 24                       |
| str    | String of characters                | `name = "Ali"`   | 49 + 1 per char approx   |
| bool   | Boolean value (True or False)       | `flag = True`    | 28                       |
| list   | Ordered collection (mutable)        | `[1, 2, 3]`      | 64 + 8 per element       |
| tuple  | Ordered collection (immutable)      | `(1, 2)`         | 48 + 8 per element       |
| set    | Unordered collection of unique items| `{1, 2, 3}`      | 224 (approx)             |
| dict   | Key-value pairs                     | `{"a": 1}`       | 240 (approx)             |

---

## 🔄 Type Conversion

### ➤ Implicit Conversion
```python
x = 5
y = 2.0
result = x + y  # float: 7.0
```

### ➤ Explicit Conversion (Casting)
```python
int("10")        # 10
float("3.14")    # 3.14
str(100)         # "100"
bool(0)          # False
```

---

## 🧰 Operators

### ➤ Arithmetic
`+`, `-`, `*`, `/`, `//`, `%`, `**`

### ➤ Comparison
`==`, `!=`, `>`, `<`, `>=`, `<=`

### ➤ Logical
`and`, `or`, `not`

### ➤ Bitwise
`&`, `|`, `^`, `~`, `<<`, `>>`

### ➤ Assignment
`=`, `+=`, `-=`, `*=`, `/=`, etc.

---

## 🔁 Conditional Statements
```python
x = 5
if x > 0:
    print("Positive")
elif x == 0:
    print("Zero")
else:
    print("Negative")
```

---

## 🔄 Loops

### ➤ While Loop
```python
n = 5
while n > 0:
    print(n)
    n -= 1
```

### ➤ For Loop
```python
for i in range(5):
    print(i)
```

### ➤ Break & Continue
```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

---

## 🧱 Functions
```python
def greet(name):
    return f"Hello, {name}!"

print(greet("Deepika"))
```

### ➤ Default & Keyword Arguments
```python
def greet(name="Guest"):
    print("Hello", name)

greet()
```

---

## 🗃️ Data Structures

### ➤ List
```python
fruits = ["apple", "banana"]
fruits.append("cherry")
```

### ➤ Tuple
```python
point = (10, 20)
```

### ➤ Set
```python
unique_items = {1, 2, 3}
```

### ➤ Dictionary
```python
student = {"name": "Ali", "age": 21}
```

---

## 📦 Modules and Packages
```python
import math
print(math.sqrt(25))
```

```python
from datetime import datetime
print(datetime.now())
```

---

## 🧪 Exception Handling
```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
finally:
    print("Done")
```

---

## 🧱 Object-Oriented Programming (OOP)
```python
class Person:
    def __init__(self, name):
        self.name = name

    def greet(self):
        print("Hello, my name is", self.name)

p = Person("Deepika")
p.greet()
```
I have created a comprehensive OOPs (Object-Oriented Programming) canvas, from beginner to advanced level. Here is a detailed structure with explanations and examples:

---

# 🧰 **Object-Oriented Programming (OOP) in Python: From Beginner to Advanced**

OOP is a programming paradigm that organizes software design around data, or objects, rather than functions and logic. It emphasizes **encapsulation**, **inheritance**, **polymorphism**, and **abstraction**.

---

## 📌 **1. Classes and Objects**

### **Definition**:
- **Class**: A blueprint for creating objects, defining attributes and behaviors.
- **Object**: An instance of a class.

### **Example**:

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model
    
    def display_info(self):
        print(f"Car Make: {self.make}, Model: {self.model}")

# Creating objects
car1 = Car("Toyota", "Corolla")
car2 = Car("Honda", "Civic")

# Accessing methods and attributes
car1.display_info()  # Car Make: Toyota, Model: Corolla
car2.display_info()  # Car Make: Honda, Model: Civic
```

---

## 📌 **2. Constructors (`__init__`)**

### **Definition**:
The `__init__` method is a special method in Python that is automatically called when an object is created. It initializes the object’s state.

### **Example**:

```python
class Employee:
    def __init__(self, name, salary):
        self.name = name
        self.salary = salary
    
    def display(self):
        print(f"Employee Name: {self.name}, Salary: {self.salary}")

emp = Employee("John", 50000)
emp.display()  # Employee Name: John, Salary: 50000
```

---

## 📌 **3. Instance Variables**

### **Definition**:
Instance variables are attributes tied to an instance of a class. They are used to store the state of an object.

### **Example**:

```python
class Person:
    def __init__(self, name, age):
        self.name = name  # Instance variable
        self.age = age    # Instance variable

person1 = Person("Alice", 30)
person2 = Person("Bob", 25)

print(person1.name)  # Alice
print(person2.age)   # 25
```

---

## 📌 **4. Class Variables**

### **Definition**:
Class variables are shared across all instances of the class. They are defined inside the class but outside any method.

### **Example**:

```python
class Student:
    school_name = "ABC High School"  # Class variable
    
    def __init__(self, name, grade):
        self.name = name
        self.grade = grade

student1 = Student("Alice", "A")
student2 = Student("Bob", "B")

print(student1.school_name)  # ABC High School
print(student2.school_name)  # ABC High School
```

---

## 📌 **5. Inheritance**

### **Definition**:
Inheritance allows a class (child class) to inherit attributes and methods from another class (parent class).

### **Example**:

```python
class Animal:
    def sound(self):
        print("Animal makes a sound")

class Dog(Animal):  # Inherits from Animal class
    def sound(self):
        print("Dog barks")

# Creating object
dog = Dog()
dog.sound()  # Dog barks
```

---

## 📌 **6. Method Overriding**

### **Definition**:
Method overriding occurs when a subclass provides a specific implementation for a method that is already defined in the parent class.

### **Example**:

```python
class Animal:
    def sound(self):
        print("Animal makes a sound")

class Dog(Animal):
    def sound(self):  # Overriding method
        print("Dog barks")

# Creating object
dog = Dog()
dog.sound()  # Dog barks
```

---

## 📌 **7. Polymorphism**

### **Definition**:
Polymorphism allows methods to be used interchangeably with different data types or objects. Methods with the same name can behave differently depending on the object.

### **Example**:

```python
class Cat:
    def sound(self):
        print("Meow")

class Dog:
    def sound(self):
        print("Bark")

# Polymorphism in action
def animal_sound(animal):
    animal.sound()

cat = Cat()
dog = Dog()

animal_sound(cat)  # Meow
animal_sound(dog)  # Bark
```

---

## 📌 **8. Encapsulation**

### **Definition**:
Encapsulation refers to the bundling of data (attributes) and methods (functions) that operate on the data into a single unit (class), while restricting direct access to some of the object's components.

### **Example**:

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private variable
    
    def deposit(self, amount):
        self.__balance += amount
    
    def get_balance(self):
        return self.__balance

account = BankAccount(1000)
account.deposit(500)
print(account.get_balance())  # 1500
```

---

## 📌 **9. Abstraction**

### **Definition**:
Abstraction is the process of hiding the complex implementation details and showing only the essential features. This is typically done by using abstract classes.

### **Example**:

```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    
    def area(self):
        return 3.14 * self.radius * self.radius

circle = Circle(5)
print(circle.area())  # 78.5
```

---

## 📌 **10. Static Methods (`@staticmethod`)**

### **Definition**:
Static methods do not require access to instance-specific data. They belong to the class and are typically used for utility functions.

### **Example**:

```python
class Math:
    @staticmethod
    def add(x, y):
        return x + y

print(Math.add(10, 20))  # 30
```

---

## 📌 **11. Class Methods (`@classmethod`)**

### **Definition**:
Class methods are bound to the class rather than an instance. They can modify class-level variables.

### **Example**:

```python
class Person:
    count = 0

    @classmethod
    def increment_count(cls):
        cls.count += 1

    def __init__(self, name):
        self.name = name
        Person.increment_count()

person1 = Person("Alice")
person2 = Person("Bob")
print(Person.count)  # 2
```

---

## 📌 **12. Real-World Example Using OOP Concepts**

### **Problem**:
You are building a **Library Management System**. The system involves managing Books, Users, and Transactions.

- **Classes**: `Book`, `User`, `Admin`
- **Inheritance**: Admin inherits from User, but has additional capabilities.
- **Polymorphism**: Borrowing books with different behaviors for users and admins.
- **Encapsulation**: Book status is hidden and only accessed via methods.

### **Solution**:

```python
class Book:
    def __init__(self, title, author, book_id):
        self.title = title
        self.author = author
        self.book_id = book_id
        self.__availability = True  # Private variable
    
    def borrow_book(self):
        if self.__availability:
            self.__availability = False
            print(f"Book {self.title} borrowed successfully!")
        else:
            print(f"Book {self.title} is currently unavailable.")
    
    def return_book(self):
        self.__availability = True
        print(f"Book {self.title} returned successfully.")
    
    def get_availability(self):
        return "Available" if self.__availability else "Not Available"

class User:
    def __init__(self, username):
        self.username = username
    
    def borrow(self, book):
        print(f"User {self.username} trying to borrow: {book.title}")
        book.borrow_book()

class Admin(User):
    def __init__(self, username):
        super().__init__(username)
    
    def borrow(self, book):
        print(f"Admin {self.username} has special access to borrow: {book.title}")
        book.borrow_book()

book1 = Book("Python Programming", "John Doe", 1)
user1 = User("Alice")
admin1 = Admin("Bob")

user1.borrow(book1)  # User tries to borrow
admin1.borrow(book1)  # Admin tries to borrow
```

---

## 📌 **13. Conclusion**

Object-Oriented Programming allows for better organization of code and can make your programs more modular and reusable. It encourages the creation of code that is easier to maintain, scale, and test.

---

## 🧪 File Handling
```python
with open("file.txt", "r") as f:
    print(f.read())

with open("file.txt", "w") as f:
    f.write("Hello")
```

---

## 🧠 Advanced Topics

### ➤ Lambda Functions
```python
square = lambda x: x*x
print(square(5))
```

### ➤ List Comprehensions
```python
even = [x for x in range(10) if x%2==0]
```

### ➤ Decorators
```python
def decorator(func):
    def wrapper():
        print("Before")
        func()
        print("After")
    return wrapper

@decorator
def say_hi():
    print("Hi!")

say_hi()
```

### ➤ Generators
```python
def count_up_to(n):
    i = 1
    while i <= n:
        yield i
        i += 1

for num in count_up_to(5):
    print(num)
```

---

## 🧪 Virtual Environment & Package Management
```bash
python -m venv env
source env/bin/activate   # macOS/Linux
env\Scripts\activate      # Windows

pip install requests
pip freeze > requirements.txt
```

---

## 🔧 Popular Libraries
- NumPy, Pandas – Data Science
- Flask, Django – Web Development
- Tkinter – GUI Apps
- TensorFlow, PyTorch – Deep Learning
- Matplotlib, Seaborn – Data Visualization

---

Let me know if you’d like quizzes, project ideas, interview questions, or deep dives into any topic!

