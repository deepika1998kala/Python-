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

# 🧱 Python Data Structures: Complete Notes

Python provides several built-in data structures that are essential for organizing and managing data efficiently. These include lists, tuples, sets, and dictionaries.

---

## 📦 1. List

A **list** is an ordered, mutable (changeable) collection of items. It allows duplicate elements.

### ➤ Syntax
```python
my_list = [1, 2, 3, 4, 5]
```

### ➤ Common Methods
- `append(x)` – Adds an item to the end
- `insert(i, x)` – Inserts at a specific index
- `remove(x)` – Removes first occurrence of x
- `pop(i)` – Removes and returns element at index i
- `sort()` – Sorts the list
- `reverse()` – Reverses the list

### ➤ Example
```python
fruits = ["apple", "banana", "cherry"]
fruits.append("mango")
print(fruits)  # ['apple', 'banana', 'cherry', 'mango']
```

---

## 📦 2. Tuple

A **tuple** is an ordered, immutable collection. Tuples are faster and use less memory.

### ➤ Syntax
```python
my_tuple = (1, 2, 3)
```

### ➤ Key Features
- Cannot modify after creation
- Can be used as dictionary keys (if they contain only immutable elements)

### ➤ Example
```python
coordinates = (10.0, 20.0)
print(coordinates[0])  # 10.0
```

---

## 📦 3. Set

A **set** is an unordered collection of unique elements.

### ➤ Syntax
```python
my_set = {1, 2, 3}
```

### ➤ Common Operations
- `add(x)` – Adds an element
- `remove(x)` – Removes an element
- `union(set)` – Returns the union
- `intersection(set)` – Returns common elements

### ➤ Example
```python
s1 = {1, 2, 3}
s2 = {3, 4, 5}
print(s1.union(s2))         # {1, 2, 3, 4, 5}
print(s1.intersection(s2))  # {3}
```

---

## 📦 4. Dictionary

A **dictionary** is an unordered collection of key-value pairs. Keys must be unique and immutable.

### ➤ Syntax
```python
my_dict = {"name": "Ali", "age": 25}
```

### ➤ Common Methods
- `get(key)` – Returns the value for key
- `keys()` – Returns all keys
- `values()` – Returns all values
- `items()` – Returns key-value pairs
- `update()` – Updates dictionary with elements from another

### ➤ Example
```python
student = {"name": "Ali", "age": 25}
print(student["name"])  # Ali
student["grade"] = "A"
print(student)  # {'name': 'Ali', 'age': 25, 'grade': 'A'}
```

---

## 🔁 Choosing the Right Data Structure

| Use Case                        | Data Structure |
|--------------------------------|----------------|
| Need ordered & changeable data | List           |
| Fixed and ordered data         | Tuple          |
| Unique unordered items         | Set            |
| Key-value mapping              | Dictionary     |

---

Let me know if you want advanced data structure examples like `defaultdict`, `deque`, or custom classes!



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
Great question! Let's break it down with **clear definitions** and explanations directly from your code:

---

### 🔷 **What is a Class?**

> A **class** is a blueprint or template for creating objects. It defines attributes (variables) and behaviors (methods/functions) that the objects created from the class will have.

#### 👉 In Your Code:
```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model
    
    def display_info(self):
        print(f"Car Make: {self.make}, Model: {self.model}")
```

✅ `class Car:` → This defines a class named `Car`.

- `__init__()` → Special method called **constructor**, used to initialize objects.
- `self.make` and `self.model` → Instance variables (unique to each object).
- `display_info()` → A method that prints the car's details.

---

### 🔷 **What is an Object?**

> An **object** is an instance of a class. It is a real, usable thing that is created using the class blueprint.

#### 👉 In Your Code:
```python
car1 = Car("Toyota", "Corolla")
car2 = Car("Honda", "Civic")
```

✅ `car1` and `car2` are **objects** of the `Car` class.

- `car1` has:
  - `make = "Toyota"`
  - `model = "Corolla"`

- `car2` has:
  - `make = "Honda"`
  - `model = "Civic"`

These objects use the `display_info()` method to print their data:

```python
car1.display_info()  # Output: Car Make: Toyota, Model: Corolla
car2.display_info()  # Output: Car Make: Honda, Model: Civic
```

---

### ✅ **In Simple Terms**:

| Concept | Explanation |
|--------|-------------|
| **Class** | A design/plan — like the idea of a "Car" in general. |
| **Object** | A specific item made from the plan — like your actual Toyota or Honda car. |

Would you like me to show a diagram or analogy for better clarity too?
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
Here are the **types of inheritance** in Object-Oriented Programming (OOP), along with definitions and examples:

---

Certainly! Here are diagrams illustrating each type of inheritance in Object-Oriented Programming (OOP):

---

### 1. **Single Inheritance**

**Definition**: A subclass inherits from a single superclass.

**Diagram**:


```plaintext
    Animal
      |
      v
     Dog
```


---

### 2. **Multiple Inheritance**

**Definition**: A subclass inherits from more than one superclass.

**Diagram**:


```plaintext
  Father   Mother
     \\     /
      \\   /
       \\ /
       Child
```


---

### 3. **Multilevel Inheritance**

**Definition**: A subclass inherits from a superclass, and another subclass inherits from that subclass, forming a chain.

**Diagram**:


```plaintext
  Grandparent
       |
       v
     Parent
       |
       v
     Child
```


---

### 4. **Hierarchical Inheritance**

**Definition**: Multiple subclasses inherit from a single superclass.

**Diagram**:


```plaintext
    Animal
     /   \\
    /     \\
  Dog     Cat
```


---

### 5. **Hybrid Inheritance**

**Definition**: A combination of two or more types of inheritance.

**Diagram**:


```plaintext
    A
   / \\
  B   C
   \\ /
    D
```


---

These diagrams represent the various inheritance structures in OOP. Let me know if you'd like these diagrams added to your notes or if you need further clarification on any of these concepts. 

---

These inheritance types help in organizing code, promoting reusability, and establishing relationships between classes in object-oriented programming. 

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
Sure! Here's a concise yet informative explanation of **List Comprehensions**, **Decorators**, and **Generators** in Python, with definitions, use cases, and examples:

---

## ✅ **List Comprehensions**

### 📘 **Definition**:
A *List Comprehension* is a concise way to create lists in Python using a single line of code.

### 🔧 **Syntax**:
```python
[expression for item in iterable if condition]
```

### 🧪 **Example**:
```python
# Create a list of squares for even numbers from 0 to 9
squares = [x**2 for x in range(10) if x % 2 == 0]
print(squares)  # Output: [0, 4, 16, 36, 64]
```

### 🎯 **Use Cases**:
- Filtering lists
- Transforming data
- Quick operations on sequences

---

## ✅ **Decorators**

### 📘 **Definition**:
A *Decorator* is a function that takes another function as input and extends its behavior without modifying it directly.

### 🔧 **Syntax**:
```python
def decorator(func):
    def wrapper():
        print("Before function call")
        func()
        print("After function call")
    return wrapper

@decorator
def say_hello():
    print("Hello!")

say_hello()
```

### 🧪 **Output**:
```
Before function call
Hello!
After function call
```

### 🎯 **Use Cases**:
- Logging
- Authorization
- Caching
- Performance monitoring

---

## ✅ **Generators**

### 📘 **Definition**:
A *Generator* is a special type of iterator that yields one value at a time using the `yield` keyword, which saves memory.

### 🔧 **Syntax**:
```python
def count_up_to(n):
    i = 1
    while i <= n:
        yield i
        i += 1

for number in count_up_to(5):
    print(number)
```

### 🧪 **Output**:
```
1
2
3
4
5
```

### 🎯 **Use Cases**:
- Large data handling
- Streaming data
- Lazy evaluation

---
Absolutely! Let’s add **Lambda Functions** to the mix along with the others, explained in a clear and brief way:

---

## ✅ **Lambda Functions**

### 📘 **Definition**:
A **lambda function** is a small anonymous function defined using the `lambda` keyword. It's typically used when a short function is needed for a short period and is usually passed as an argument to higher-order functions.

### 🔧 **Syntax**:
```python
lambda arguments: expression
```

### 🧪 **Example**:
```python
# Lambda to add two numbers
add = lambda x, y: x + y
print(add(3, 5))  # Output: 8
```

### ✅ **With built-in functions**:
```python
# Using lambda with sorted()
points = [(2, 3), (4, 1), (1, 5)]
points_sorted = sorted(points, key=lambda x: x[1])
print(points_sorted)  # Output: [(4, 1), (2, 3), (1, 5)]
```

### 🎯 **Use Cases**:
- Used with functions like `map()`, `filter()`, `reduce()`, and `sorted()`
- Quick, inline function creation without defining a full `def` block

---

## ✅ Summary Table

| Concept           | Definition                                                                 | Use Case                                       | Syntax Example                     |
|-------------------|-----------------------------------------------------------------------------|------------------------------------------------|------------------------------------|
| List Comprehension | Short syntax to create lists                                               | Filtering, transforming lists                  | `[x for x in range(5) if x%2==0]`  |
| Decorator         | Enhances behavior of a function without changing it                         | Logging, authorization                         | `@decorator_name`                  |
| Generator         | Function that yields one value at a time                                    | Memory-efficient iteration                     | `yield` inside a function          |
| Lambda Function   | Anonymous function used for short, simple operations                        | Inline usage in map, filter, sorted, etc.      | `lambda x: x*x`                    |

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

