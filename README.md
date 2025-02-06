# Python Programming - Complete Guide

This notebook contains a detailed explanation of the Python language including primitive and non-primitive data types, control flow, functions, OOP concepts, and other essential topics.

## 1. Basic Syntax

**Definition**: The basic syntax in Python refers to the rules and structure that Python code follows for it to be valid and executable. It includes how to write statements, use indentation, declare variables, etc.

### Hello World Program

```python

print("Hello, World!")

```

Explanation: This is the simplest Python program that prints the string "Hello, World!" to the console.

### Comments

Comments in Python are used to add descriptions or explanations in the code that are not executed. They help improve code readability.

- **Single-line comment**:

```python

# This is a single-line comment

```

- **Multi-line comment**:

```python

""" 

This is a 

multi-line comment 

""" 

```

## 2. Variables and Data Types

### Primitive Data Types

These represent basic data types, such as integers and floating-point numbers, that hold simple values.

- **Integer (`int`)**: Represents whole numbers.

```python

x = 10  # integer

```

- **Float (`float`)**: Represents decimal or floating-point numbers.

```python

y = 3.14  # float

```

- **String (`str`)**: Represents sequences of characters, typically used for text.

```python

name = "Alice"  # string

```

- **Boolean (`bool`)**: Represents a value that is either True or False.

```python

is_active = True  # boolean

```

### Non-Primitive Data Types

Non-primitive data types, also called **complex types**, can hold more than one value and are generally more complex.

- **List**: An ordered, mutable collection of elements, which can be of mixed data types.

```python

my_list = [1, 2, 3, "apple"]  # list

```

- **Tuple**: An ordered, immutable collection of elements, which can be of mixed data types.

```python

my_tuple = (1, 2, 3, "apple")  # tuple

```

- **Set**: An unordered collection of unique elements (no duplicates).

```python

my_set = {1, 2, 3, 4}  # set

```

- **Dictionary**: An unordered collection of key-value pairs.

```python

my_dict = {"name": "Alice", "age": 25}  # dictionary

```

- **NoneType**: Represents the absence of a value, commonly used for default values or as a placeholder.

```python

my_variable = None  # NoneType

```

## 3. Control Flow

**Definition**: Control flow statements are used to control the order of execution of the code, based on conditions or repetitions.

### If-Else Statements

```python

x = 10

if x > 0:

    print("Positive")

else:

    print("Non-positive")

```

Explanation: The `if-else` statement is used to execute different code based on a condition.

### Elif Statement

```python

x = 5

if x > 0:

    print("Positive")

elif x == 0:

    print("Zero")

else:

    print("Negative")

```

Explanation: The `elif` (else if) statement allows you to check multiple conditions after the `if`.

### For Loop

```python

for i in range(5):

    print(i)  # prints 0 to 4

```

Explanation: A `for` loop is used for iterating over a sequence (like a list or range).

### While Loop

```python

x = 0

while x < 5:

    print(x)  # prints 0 to 4

    x += 1

```

Explanation: The `while` loop runs as long as the given condition is `True`.

### Break and Continue

```python

for i in range(10):

    if i == 5:

        break  # Exits the loop

    if i % 2 == 0:

        continue  # Skips the current iteration

    print(i)

```

Explanation: The `break` statement exits the loop immediately, and the `continue` statement skips the current iteration.

## 4. Functions

**Definition**: Functions are reusable blocks of code that can be called with arguments and can return values.

### Function Definition

```python

def greet(name):

    print(f"Hello, {name}!")

greet("Alice")

```

Explanation: A function is defined with the `def` keyword. It takes an argument `name` and prints a greeting message.

### Return Statement

```python

def add(a, b):

    return a + b

result = add(3, 4)

print(result)  # prints 7

```

Explanation: A function can return a value using the `return` keyword.

### Lambda Function

```python

multiply = lambda x, y: x * y

print(multiply(2, 3))  # prints 6

```

Explanation: A lambda function is a small anonymous function defined with the `lambda` keyword.

## 5. List Comprehension

**Definition**: List comprehension is a concise way to create lists using a single line of code.

```python

squares = [x**2 for x in range(5)]

print(squares)  # prints [0, 1, 4, 9, 16]

```

Explanation: The list comprehension `[x**2 for x in range(5)]` generates a list of squared values.

## 6. Exception Handling

**Definition**: Exception handling allows you to handle runtime errors gracefully using `try`, `except`, and `finally`.

### Try-Except Block

```python

try:

    x = 10 / 0

except ZeroDivisionError:

    print("Cannot divide by zero")

finally:

    print("This will always execute")

```

Explanation: The `try` block contains code that may raise an exception. The `except` block catches specific exceptions, and `finally` executes after the `try-except` block, regardless of success or failure.


# 7. Object-Oriented Programming (OOP) in Python

This notebook contains a detailed explanation of the Object-Oriented Programming (OOP) concepts in Python, including class definition, objects, inheritance, polymorphism, and more.

## 1. Classes and Objects

**Definition**: Classes are blueprints for creating objects. Objects are instances of a class, which encapsulate data and functionality.

### Class Definition

A class is defined using the `class` keyword.

```python

class Person:

    def __init__(self, name, age):

        self.name = name

        self.age = age

    def greet(self):

        print(f"Hello, my name is {self.name} and I am {self.age} years old.")

# Creating an object of Person

person1 = Person("Alice", 25)

person1.greet()  # Output: Hello, my name is Alice and I am 25 years old.

```

Explanation: A class is defined using the `class` keyword. The `__init__` method is the constructor that initializes the object's attributes. We can create an object of the class by calling it like a function.

### Objects

An object is an instance of a class. Objects hold the data and methods defined in the class.

```python

# Creating another object

person2 = Person("Bob", 30)

person2.greet()  # Output: Hello, my name is Bob and I am 30 years old.

```

## 2. Inheritance

**Definition**: Inheritance allows a class to inherit attributes and methods from another class, promoting code reusability.

### Inheriting from a Base Class

```python

class Student(Person):

    def __init__(self, name, age, grade):

        super().__init__(name, age)

        self.grade = grade

    def greet(self):

        super().greet()  # Call the greet method of the base class

        print(f"I am in grade {self.grade}")

# Creating an object of Student

student1 = Student("Charlie", 18, 12)

student1.greet()  # Output: Hello, my name is Charlie and I am 18 years old. I am in grade 12

```

Explanation: The `Student` class inherits from the `Person` class, using the `super()` function to call the constructor of the base class.

### Overriding Methods

The `Student` class overrides the `greet` method of the `Person` class to add additional functionality.

## 3. Polymorphism

**Definition**: Polymorphism allows objects of different classes to be treated as instances of the same class through inheritance, enabling method overriding.

### Method Overriding

```python

class Dog:

    def speak(self):

        print("Woof!")

class Cat:

    def speak(self):

        print("Meow!")

animals = [Dog(), Cat()]

for animal in animals:

    animal.speak()

```

Explanation: Both `Dog` and `Cat` classes have the `speak` method, but each class implements it differently. This is an example of method overriding, where different classes can have the same method name but with different behaviors.

Output: Woof! Meow!

## 4. Encapsulation

**Definition**: Encapsulation is the practice of restricting access to certain attributes or methods and bundling them within a class.

### Private Attributes and Methods

You can make attributes or methods private by prefixing them with double underscores (`__`). This restricts access to them from outside the class.

```python

class BankAccount:

    def __init__(self, owner, balance):

        self.owner = owner

        self.__balance = balance  # Private attribute

    def deposit(self, amount):

        if amount > 0:

            self.__balance += amount

        else:

            print("Invalid amount")

    def get_balance(self):

        return self.__balance

# Creating an object of BankAccount

account = BankAccount("Alice", 1000)

account.deposit(500)

print(account.get_balance())  # Output: 1500

# Direct access to __balance is not allowed

# print(account.__balance)  # This will raise an AttributeError

```

Explanation: The `__balance` attribute is private and cannot be accessed directly from outside the class. Accessing it directly would result in an `AttributeError`.

## 5. Abstraction

**Definition**: Abstraction is the concept of hiding the complex implementation details and exposing only the essential features.

### Abstract Base Class (ABC)

Python provides the `abc` module to define abstract base classes that cannot be instantiated directly. It allows you to define methods that must be implemented by subclasses.

```python

from abc import ABC, abstractmethod

class Animal(ABC):

    @abstractmethod

    def speak(self):

        pass

class Dog(Animal):

    def speak(self):

        print("Woof!")

dog = Dog()

dog.speak()  # Output: Woof!

# The following will raise an error because Animal is abstract and cannot be instantiated

# animal = Animal()  # TypeError: Can't instantiate abstract class Animal with abstract methods speak

```

Explanation: The `Animal` class is abstract and cannot be instantiated. The `speak` method is abstract and must be implemented in the `Dog` subclass.
This notebook contains all the commonly used data structures in Python for **Data Structures and Algorithms (DSA)**, along with their methods. Each data structure is explained with methods that are commonly used in competitive programming and problem-solving.

## 1. Lists (Arrays in Python)

- Lists are dynamic and can store mixed data types.

- Used for sorting, searching, dynamic programming, etc.

### Methods:

- `append(x)` → Add an element at the end.

- `insert(i, x)` → Insert element `x` at index `i`.

- `remove(x)` → Remove the first occurrence of element `x`.

- `pop(i)` → Remove and return element at index `i`.

- `clear()` → Remove all elements.

- `extend(iterable)` → Append all items from an iterable (list, tuple, etc.).

- `index(x)` → Return the index of the first occurrence of `x`.

- `count(x)` → Count occurrences of `x`.

- `sort()` → Sort the list in ascending order.

- `reverse()` → Reverse the list in place.

- `copy()` → Return a shallow copy of the list.

- `len()` → Returns the number of elements.

- `del` → Used for deleting an element or slice (`del arr[2]`).

```python

arr = [1, 2, 3, 4, 5]

arr.append(6)  # Adds 6 to the end

arr.pop()  # Removes and returns 6

arr.sort()  # Sorts the list in ascending order

```

## 2. Strings

- Strings are immutable sequences of characters.

- Used for pattern matching, substring problems, and hashing.

### Methods:

- `upper()` → Convert string to uppercase.

- `lower()` → Convert string to lowercase.

- `title()` → Convert to title case.

- `strip()` → Remove leading/trailing whitespace.

- `split(sep)` → Split the string by separator `sep`.

- `join(iterable)` → Join the iterable using the string as a separator.

- `replace(old, new)` → Replace occurrences of `old` with `new`.

- `find(sub)` → Return the lowest index of substring `sub`.

- `count(sub)` → Count the number of occurrences of `sub`.

- `startswith(prefix)` → Check if the string starts with `prefix`.

- `endswith(suffix)` → Check if the string ends with `suffix`.

- `splitlines()` → Split string into a list by line breaks.

- `len()` → Get the length of the string.

```python

s = 'hello world'

print(s.upper())  # Output: 'HELLO WORLD'

print(s.find('world'))  # Output: 6

```

## 3. Hashing (Dictionaries and Sets)

- **Dictionaries (`dict`)** are key-value stores.

- **Sets (`set`)** are unordered collections of unique elements.

### Dictionaries Methods (`dict`):

- `dict[key]` → Access value by key.

- `dict.get(key)` → Return value for `key`, or `None` if not found.

- `dict.update(d)` → Update dictionary with items from `d`.

- `dict.keys()` → Return a view object of all keys.

- `dict.values()` → Return a view object of all values.

- `dict.items()` → Return a view object of key-value pairs.

- `dict.pop(key)` → Remove and return value for `key`.

- `dict.popitem()` → Remove and return an arbitrary (key, value) pair.

- `dict.clear()` → Remove all items from the dictionary.

### Sets Methods (`set`):

- `set.add(x)` → Add element `x` to the set.

- `set.remove(x)` → Remove element `x` from the set.

- `set.discard(x)` → Remove `x` from the set if it exists (doesn't raise error).

- `set.pop()` → Remove and return an arbitrary element.

- `set.clear()` → Remove all elements from the set.

- `set.update(iterable)` → Add all items from iterable to the set.

- `set.intersection(other_set)` → Return the intersection of two sets.

- `set.union(other_set)` → Return the union of two sets.

- `set.difference(other_set)` → Return elements present in the set but not in the other set.

- `set.symmetric_difference(other_set)` → Return elements that are in either set, but not both.

```python

d = {'a': 1, 'b': 2}

d.get('a')  # Output: 1

d.keys()  # Output: dict_keys(['a', 'b'])

s = {1, 2, 3}

s.add(4)  # Adds 4 to the set

```

## 4. Stacks (Using Lists or `deque`)

- **LIFO (Last In, First Out)**

- Used in DFS, backtracking, and expression evaluation.

### Using List (LIFO):

- `append(x)` → Push `x` onto the stack.

- `pop()` → Pop the last element from the stack.

### Using `collections.deque` (Optimized):

- `append(x)` → Add element `x` to the right end.

- `appendleft(x)` → Add element `x` to the left end.

- `pop()` → Remove and return element from the right end.

- `popleft()` → Remove and return element from the left end.

- `clear()` → Remove all elements.

- `extend(iterable)` → Add all items from iterable to the right.

- `extendleft(iterable)` → Add all items from iterable to the left.

```python

from collections import deque

stack = deque()

stack.append(1)

stack.pop()  # Removes and returns 1

```

## 5. Queues (`deque` or `queue.Queue`)

- **FIFO (First In, First Out)**

- Used in BFS, task scheduling.

### Using `collections.deque`:

- `append(x)` → Add element to the right end.

- `appendleft(x)` → Add element to the left end.

- `pop()` → Remove and return element from the right end.

- `popleft()` → Remove and return element from the left end.

### Using `queue.Queue` (Thread-Safe):

- `put(x)` → Add `x` to the queue.

- `get()` → Remove and return an element from the queue.

- `queue.empty()` → Check if the queue is empty.

- `queue.full()` → Check if the queue is full.

```python

from collections import deque

queue = deque()

queue.append(1)

queue.popleft()  # Removes and returns 1

```