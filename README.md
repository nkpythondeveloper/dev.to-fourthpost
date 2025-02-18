# Python Fundamentals – Data Types, Control Flow, and Loops

Before diving into advanced Python topics, it’s essential to have a solid understanding of basic data types, control flow, and loops. These fundamental building blocks are what make Python such a flexible and powerful language.

In this post, we’ll cover:

✅ Python's core data types and how they work
✅ Control flow statements like if-else, match-case, and try-except
✅ Loops in Python (for, while, and iterators)

Let’s get started! 🚀

**1️⃣ Python’s Built-in Data Types**

Python provides several built-in data types, categorized as follows:

| Category | Data Type |  Example |
|----------|-----------|----------|
| Numbers |	int, float, complex | 	42, 3.14, 1+2j |
| Text |	str	 | "Hello, Python!" |
| Boolean | 	bool | 	True, False |
| Sequences | 	list, tuple, range	 | [1, 2, 3], (1, 2, 3), range(5) |
| Mapping | 	dict | 	{"name": "Alice", "age": 25} |
| Sets | 	set, frozenset | 	{1, 2, 3}, frozenset({1, 2, 3}) |
| Binary | 	bytes, bytearray, memoryview | 	b'hello', bytearray(5), memoryview(bytes(5)) |
| NoneType | 	None	| None |

**🔍 Examples of Basic Data Types in Python**

# Numbers
```python
x = 10        # Integer
y = 3.14      # Float
z = 1 + 2j    # Complex Number
```

# Strings
```python
name = "Python"
```

# Booleans
```python
is_python_easy = True
```

# Lists
```python
fruits = ["apple", "banana", "cherry"]
```

# Tuples
```python
coordinates = (10, 20)
```

# Dictionaries
```python
person = {"name": "Alice", "age": 25}
```

# Sets
```python
unique_numbers = {1, 2, 3, 4, 5}
```

**🔥 Key Takeaways:**

✅ Python dynamically assigns types – you don’t need to declare them explicitly.
✅ list and tuple are ordered, while set is unordered and unique.
✅ dict stores key-value pairs.


**2️⃣ Control Flow: Making Decisions in Python**

Python provides several control flow statements that help us direct program execution based on conditions.

**🔹 1. if-elif-else Statements**

Python executes blocks of code based on conditions.
```python
age = 18

if age < 18:
    print("You're a minor.")
elif age == 18:
    print("You're exactly 18!")
else:
    print("You're an adult.")
```

**🔹 2. match-case (Python 3.10+)**


Python 3.10 introduced match-case, which works like a switch statement.
```python
def check_number(num):
    match num:
        case 1:
            print("One")
        case 2:
            print("Two")
        case _:
            print("Something else")

check_number(2)  # Output: Two
```

**🔹 3. Exception Handling with try-except-finally**

Python uses try-except blocks to handle errors gracefully.
```python
try:
    result = 10 / 0  # This will cause an error
except ZeroDivisionError as e:
    print(f"Error: {e}")
finally:
    print("This block runs no matter what.")  # Always executes
```

**3️⃣ Loops: Iterating Over Data**

Loops allow us to repeat actions efficiently.

**🔹 1. for Loop: Iterating Over a Sequence**

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

**🔹 Looping with range()**

```python
for i in range(5):  # Prints 0 to 4
    print(i)
```

**🔹 2. while Loop: Repeating Until a Condition is False**

```python
counter = 3
while counter > 0:
    print(counter)
    counter -= 1
```

**🔹 Using break and continue**

```python
for i in range(5):
    if i == 3:
        break  # Stops the loop when i == 3
    if i == 1:
        continue  # Skips the iteration when i == 1
    print(i)
```

**4️⃣ Iterators and Generators in Python**

**🔹 1. What is an Iterator?**

An iterator is an object that can be iterated over using next().

```python
my_list = [1, 2, 3]
iterator = iter(my_list)

print(next(iterator))  # 1
print(next(iterator))  # 2
print(next(iterator))  # 3
```

**🔹 Using Custom Iterators**

```python
class Counter:
    def __init__(self, max):
        self.max = max
        self.current = 0

    def __iter__(self):
        return self

    def __next__(self):
        if self.current >= self.max:
            raise StopIteration
        self.current += 1
        return self.current

counter = Counter(3)
for num in counter:
    print(num)
```

**🔹 2. Generators: Efficient Iteration**

A generator is a special function that yields values one at a time, saving memory.

```python
def count_up_to(max):
    num = 1
    while num <= max:
        yield num  # Yield instead of return
        num += 1

counter = count_up_to(3)
print(next(counter))  # 1
print(next(counter))  # 2
print(next(counter))  # 3
```

**🔹 Conclusion**

✅ Data Types form the foundation of Python programming.
✅ Control Flow Statements (if-else, match-case, try-except) allow for decision-making.
✅ Loops (for, while, iterators, generators`) allow efficient iteration over data.

Understanding these basics will help you write more efficient, structured Python code. 🚀

***What’s Next?***

In the next post, we’ll explore Functions and Object-Oriented Programming (OOP) in Python. Stay tuned! 🔥

**💬 What Do You Think?**

What’s your favorite Python feature? Do you use match-case in your projects? Let’s discuss in the comments! 💡
