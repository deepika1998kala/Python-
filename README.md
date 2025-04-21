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

