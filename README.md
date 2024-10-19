# PYTHON


### **Python Syntax and Semantics**

---

### **1. Comments in Python**

- **Single-line Comments**: Begin with a `#` symbol. These comments are ignored by Python and are used to explain your code.
  ```python
  # This is a single-line comment
  print("Hello World")
  ```

- **Multiline Comments**: Python doesn’t have a special syntax for multiline comments, but you can use triple quotes (`'''` or `"""`) to create block comments or docstrings.
  ```python
  """
  This is a multiline comment.
  """
  print("Multiline comment example")
  ```

### **2. Definition of Syntax and Semantics**

- **Syntax**: Rules that define the structure of a program. Syntax errors occur when these rules are broken, such as missing colons or incorrect indentation.
- **Semantics**: Refers to the meaning of the code. A program might have correct syntax but still behave unexpectedly due to semantic errors.

### **3. Basic Syntax Rules in Python**

- **Case Sensitivity**: Python is case-sensitive, meaning `Name` and `name` are two different variables.
  ```python
  name = "Mohamed"
  Name = "Assaf"

  print(name)  # Output: Mohamed
  print(Name)  # Output: Assaf
  ```

- **Indentation**: Python uses indentation (commonly 4 spaces) to define blocks of code. It is mandatory, and incorrect indentation will result in an `IndentationError`.
  ```python
  age = 21
  if age > 18:
      print("Adult")
  ```

- **Line Continuation**: Use a backslash (`\`) to continue a statement onto the next line.
  ```python
  total = 1 + 2 + 3 + 4 + \
          5 + 6 + 7
  print(total)  # Output: 28
  ```

- **Multiple Statements on a Single Line**: You can use semicolons (`;`) to write multiple statements on a single line, although this is not recommended for readability.
  ```python
  x = 5; y = 10; z = x + y
  print(z)  # Output: 15
  ```

### **4. Understanding Semantics in Python**

- **Variable Assignment**: Python is dynamically typed, meaning you do not have to declare variable types explicitly.
  ```python
  age = 21  # Integer
  name = "Mohamed Assaf"  # String

  print(type(age))  # Output: <class 'int'>
  print(type(name))  # Output: <class 'str'>
  ```

- **Type Inference**: Variables can change their type during execution.
  ```python
  variable = 10
  print(type(variable))  # Output: <class 'int'>

  variable = "Mohamed Assaf"
  print(type(variable))  # Output: <class 'str'>
  ```

### **5. Common Syntax Errors and How to Avoid Them**

- **NameError**: Occurs when you try to use a variable that hasn’t been defined.
  ```python
  a = b  # This will raise a NameError because 'b' is not defined.
  ```

- **IndentationError**: Happens when there is incorrect indentation.
  ```python
  if True:
  print("Incorrect indentation")  # IndentationError
  ```

- **SyntaxError**: Commonly occurs when the syntax rules are violated, like missing colons (`:`) or parentheses.
  ```python
  if True
      print("Syntax error")  # Missing colon will raise SyntaxError.
  ```

### **6. Practical Code Examples**

- **Correct and Incorrect Indentation**:
  ```python
  if True:
      print("Correct indentation")
      if False:
          print("This won't print")
      print("This will print")
  print("Outside the if block")
  ```

- **Type Checking and Type Conversion**:
  ```python
  age = 21
  print(type(age))  # Output: <class 'int'>

  age_str = str(age)
  print(type(age_str))  # Output: <class 'str'>
  ```

  Converting incompatible types will raise an error:
  ```python
  name = "Mohamed Assaf"
  int(name)  # ValueError: invalid literal for int() with base 10: 'Mohamed Assaf'
  ```

### **7. Variables in Python**

- **Variable Declaration and Assignment**: Python variables do not need explicit declaration, and memory is allocated automatically.
  ```python
  age = 21
  height = 6.1
  name = "Mohamed Assaf"
  is_student = True

  print("Age:", age)
  print("Height:", height)
  print("Name:", name)
  ```

- **Naming Conventions**: Variables should be descriptive, start with a letter or underscore (`_`), and can include numbers. Variable names are case-sensitive.
  ```python
  first_name = "Mohamed"
  last_name = "Assaf"
  ```

  Invalid variable names:
  ```python
  # 2age = 30  # Cannot start with a number
  # first-name = "Mohamed"  # Hyphen not allowed in variable names
  ```

- **Dynamic Typing**: Variables in Python can change their type at runtime.
  ```python
  var = 10
  print(var, type(var))  # Output: 10 <class 'int'>

  var = "Hello"
  print(var, type(var))  # Output: Hello <class 'str'>

  var = 3.14
  print(var, type(var))  # Output: 3.14 <class 'float'>
  ```

### **8. Input and Basic Programs**

- **Taking Input from Users**:
  ```python
  age = int(input("Enter your age: "))
  print("Your age is:", age)
  ```

- **Simple Calculator**:
  ```python
  num1 = float(input("Enter first number: "))
  num2 = float(input("Enter second number: "))

  sum = num1 + num2
  difference = num1 - num2
  product = num1 * num2
  quotient = num1 / num2

  print("Sum:", sum)
  print("Difference:", difference)
  print("Product:", product)
  print("Quotient:", quotient)
  ```

---

### **Missed Points to Add**:

- **String Formatting**: Use f-strings for better formatting.
  ```python
  name = "Mohamed Assaf"
  age = 21
  print(f"My name is {name} and I am {age} years old.")
  ```

- **Exception Handling**: Use `try`, `except`, and `finally` for error handling.
  ```python
  try:
      result = 10 / 0
  except ZeroDivisionError:
      print("Cannot divide by zero.")
  finally:
      print("This will always run.")
  ```

- **Docstrings for Functions**: Used for documenting code.
  ```python
  def greet():
      """This function prints a greeting message."""
      print("Hello!")

  print(greet.__doc__)  # Output: This function prints a greeting message.
  ```
---

### **Data Types**

#### **1. Definition**:
Data types classify data to tell the interpreter how to handle the data. They determine operations that can be performed, the data values allowed, and how much memory is required.

#### **2. Importance of Data Types in Programming**:
- They ensure data is efficiently stored.
- They help in performing correct operations on data.
- Proper use prevents errors and bugs in programs.

---

### **Basic Data Types**

#### **1. Integers**
Integers represent whole numbers without a decimal point.

```python
age = 21  # Integer example
print(type(age))  # Output: <class 'int'>
```

#### **2. Floating-Point Numbers**
Floating-point numbers represent real numbers with decimal points.

```python
height = 5.11  # Floating-point example
print(height)  # Output: 5.11
print(type(height))  # Output: <class 'float'>
```

#### **3. Strings**
Strings represent sequences of characters, enclosed in quotes.

```python
name = "Mohamed Assaf"
print(name)  # Output: Mohamed Assaf
print(type(name))  # Output: <class 'str'>
```

#### **4. Booleans**
Booleans store `True` or `False` values.

```python
is_true = True
print(type(is_true))  # Output: <class 'bool'>

a = 10
b = 10
print(type(a == b))  # Output: <class 'bool'>, since comparison returns a boolean value
```

---

### **Common Errors**

#### **TypeError:**
A TypeError occurs when incompatible types are used together, such as adding a string and a number.

```python
# This will raise a TypeError because you can't add a string and an integer
result = "Hello" + 5
# Output: TypeError: can only concatenate str (not "int") to str

# Correct approach: Convert the integer to a string
result = "Hello" + str(5)
print(result)  # Output: Hello5
```

---

### **Deep Dive into Operators**

#### **Arithmetic Operators**

Arithmetic operators perform mathematical operations such as addition, subtraction, multiplication, and division.

```python
a = 10
b = 5

add_result = a + b  # Addition
sub_result = a - b  # Subtraction
mult_result = a * b  # Multiplication
div_result = a / b  # Division
floor_div_result = a // b  # Floor Division
modulus_result = a % b  # Modulus (remainder)
exponent_result = a ** b  # Exponentiation (power)

print(add_result)  # Output: 15
print(sub_result)  # Output: 5
print(mult_result)  # Output: 50
print(div_result)  # Output: 2.0
print(floor_div_result)  # Output: 2
print(modulus_result)  # Output: 0
print(exponent_result)  # Output: 100000
```

- **Floor Division** truncates the decimal part, while **regular division** keeps the decimal.

```python
print(21 / 5)  # Output: 4.2
print(21 // 5)  # Output: 4
```

---

### **Comparison Operators**

Comparison operators compare two values and return `True` or `False`.

```python
a = 10
b = 10

# Equal to
print(a == b)  # Output: True

# Not equal to
str1 = "Mohamed"
str2 = "Mohamed"
print(str1 != str2)  # Output: False

str3 = "Mohamed"
str4 = "mohamed"
print(str3 != str4)  # Output: True

# Greater than and Less than
num1 = 45
num2 = 55
print(num1 > num2)  # Output: False
print(num1 < num2)  # Output: True

# Greater than or equal to
number1 = 45
number2 = 45
print(number1 >= number2)  # Output: True

# Less than or equal to
number1 = 44
number2 = 45
print(number1 <= number2)  # Output: True
```

---

### **Logical Operators**

Logical operators combine multiple conditions.

- **AND**: Returns `True` if both conditions are true.
- **OR**: Returns `True` if at least one condition is true.
- **NOT**: Inverts the condition (True becomes False, and vice versa).

```python
X = True
Y = True

# AND
result = X and Y
print(result)  # Output: True

X = False
result = X and Y
print(result)  # Output: False

# OR
X = False
Y = False
result = X or Y
print(result)  # Output: False

# NOT
X = False
print(not X)  # Output: True
```

---

### **Simple Calculator Example**

This program performs basic arithmetic operations using input from the user.

```python
# Simple calculator
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

# Performing arithmetic operations
addition = num1 + num2
subtraction = num1 - num2
multiplication = num1 * num2
division = num1 / num2
floor_division = num1 // num2
modulus = num1 % num2
exponentiation = num1 ** num2

# Displaying results
print("Addition:", addition)
print("Subtraction:", subtraction)
print("Multiplication:", multiplication)
print("Division:", division)
print("Floor Division:", floor_division)
print("Modulus:", modulus)
print("Exponentiation:", exponentiation)
```

**Sample Output**:
```
Addition: 16.0
Subtraction: 8.0
Multiplication: 48.0
Division: 3.0
Floor Division: 3.0
Modulus: 0.0
Exponentiation: 20736.0
```

---
---

## **Conditional Statements (if, elif, else)**

### **Video Outline**:
1. Introduction to Conditional Statements
2. if Statement
3. else Statement
4. elif Statement
5. Nested Conditional Statements
6. Practical Examples
7. Common Errors and Best Practices

---

### **1. if Statement**

The `if` statement checks a condition, and if it's `True`, it executes the indented block of code. 

Example:

```python
age = 20

if age >= 18:
    print("You are allowed to vote in the elections")
```

**Output**:
```
You are allowed to vote in the elections
```

**Explanation**: Since `age >= 18` is `True`, the code inside the `if` block gets executed.

---

### **2. else Statement**

The `else` statement executes a block of code if the condition in the `if` statement is `False`.

Example:

```python
age = 16

if age >= 18:
    print("You are eligible for voting")
else:
    print("You are a minor")
```

**Output**:
```
You are a minor
```

---

### **3. elif Statement**

The `elif` statement allows you to check multiple conditions. It stands for "else if."

Example:

```python
age = 17

if age < 13:
    print("You are a child")
elif age < 18:
    print("You are a teenager")
else:
    print("You are an adult")
```

**Output**:
```
You are a teenager
```

---

### **4. Nested Conditional Statements**

You can place one or more `if`, `elif`, or `else` statements inside another to create nested conditions.

Example:

```python
num = int(input("Enter the number: "))

if num > 0:
    print("The number is positive")
    if num % 2 == 0:
        print("The number is even")
    else:
        print("The number is odd")
else:
    print("The number is zero or negative")
```

---

### **5. Practical Examples**

#### **Example 1: Leap Year Check**

```python
year = int(input("Enter the year: "))

if year % 4 == 0:
    if year % 100 == 0:
        if year % 400 == 0:
            print(year, "is a leap year")
        else:
            print(year, "is not a leap year")
    else:
        print(year, "is a leap year")
else:
    print(year, "is not a leap year")
```

---

#### **Example 2: Simple Calculator**

```python
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))
operation = input("Enter operation (+, -, *, /): ")

if operation == '+':
    result = num1 + num2
elif operation == '-':
    result = num1 - num2
elif operation == '*':
    result = num1 * num2
elif operation == '/':
    if num2 != 0:
        result = num1 / num2
    else:
        result = "Error! Division by zero."
else:
    result = "Invalid operation."

print("Result:", result)
```

---

#### **Example 3: Ticket Price Based on Age and Student Status**

```python
age = int(input("Enter your age: "))
is_student = input("Are you a student? (yes/no): ").lower()

if age < 5:
    price = "Free"
elif age <= 12:
    price = "$10"
elif age <= 17:
    if is_student == 'yes':
        price = "$12"
    else:
        price = "$15"
elif age <= 64:
    if is_student == 'yes':
        price = "$18"
    else:
        price = "$25"
else:
    price = "$20"

print("Ticket Price:", price)
```

---

#### **Example 4: Employee Bonus Calculation**

```python
years_of_service = int(input("Enter years of service: "))
performance_rating = float(input("Enter performance rating (1.0 to 5.0): "))

if performance_rating >= 4.5:
    if years_of_service > 10:
        bonus_percentage = 20
    elif years_of_service > 5:
        bonus_percentage = 15
    else:
        bonus_percentage = 10
elif performance_rating >= 3.5:
    if years_of_service > 10:
        bonus_percentage = 15
    elif years_of_service > 5:
        bonus_percentage = 10
    else:
        bonus_percentage = 5
else:
    bonus_percentage = 0

salary = float(input("Enter current salary: "))
bonus_amount = salary * bonus_percentage / 100

print("Bonus Amount: ${:.2f}".format(bonus_amount))
```

---

#### **Example 5: User Login System**

```python
stored_username = "admin"
stored_password = "password123"

username = input("Enter username: ")
password = input("Enter password: ")

if username == stored_username:
    if password == stored_password:
        print("Login successful!")
    else:
        print("Incorrect password.")
else:
    print("Username not found.")
```

---
---

## **Loops**

Loops allow you to execute a block of code multiple times. There are two main types of loops in Python: `for` loops and `while` loops.

---

### **1. for Loop**

The `for` loop is used to iterate over a sequence (like a list, tuple, string, or range) and execute a block of code for each item in the sequence.

#### **Example 1: Iterating over a range**

```python
for i in range(5):
    print(i)
```

**Output**:
```
0
1
2
3
4
```

#### **Example 2: Iterating over a string**

```python
name = "Mohamed Assaf"

for char in name:
    print(char)
```

**Output**:
```
M
o
h
a
m
e
d

A
s
s
a
f
```

#### **Example 3: Iterating with a step value**

```python
for i in range(1, 10, 2):
    print(i)
```

**Output**:
```
1
3
5
7
9
```

---

### **2. while Loop**

The `while` loop continues to execute the block of code as long as the given condition is `True`.

#### **Example 1: Basic while loop**

```python
count = 0

while count < 5:
    print(count)
    count += 1
```

**Output**:
```
0
1
2
3
4
```

---

### **3. Loop Control Statements**

Loop control statements change the execution flow of loops.

#### **1. break Statement**

The `break` statement is used to exit the loop prematurely when a certain condition is met.

#### **Example**:

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

**Output**:
```
0
1
2
3
4
```

---

#### **2. continue Statement**

The `continue` statement skips the current iteration of the loop and moves to the next iteration.

#### **Example**:

```python
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)
```

**Output**:
```
1
3
5
7
9
```

---

#### **3. pass Statement**

The `pass` statement is a null operation. It is used as a placeholder when no action is required for certain conditions.

#### **Example**:

```python
for i in range(5):
    if i == 3:
        pass
    print(i)
```

**Output**:
```
0
1
2
3
4
```

---

### **4. Nested Loops**

A nested loop is a loop inside another loop. The inner loop executes completely each time the outer loop runs one iteration.

#### **Example**:

```python
for i in range(3):
    for j in range(2):
        print(f"i:{i}, j:{j}")
```

**Output**:
```
i:0, j:0
i:0, j:1
i:1, j:0
i:1, j:1
i:2, j:0
i:2, j:1
```

---

### **5. Practical Examples of Loops**

#### **Example 1: Sum of First N Natural Numbers (Using `for` loop)**

```python
n = 10
sum = 0

for i in range(1, n+1):
    sum += i

print("Sum of first", n, "natural numbers:", sum)
```

**Output**:
```
Sum of first 10 natural numbers: 55
```

#### **Example 2: Prime Numbers between 1 and 100** 
### Key Points:
- The `else` block runs if the `for` loop **iterates over all items**.
- If the loop is **terminated early** by a `break` statement, the `else` block is **skipped**.
```python
for num in range(1, 101):
    if num > 1:
        for i in range(2, num):
            if num % i == 0:
                break
        else:
            print(num)
```

**Output**:
```
2
3
5
7
11
13
17
19
23
29
31
37
41
43
47
53
59
61
67
71
73
79
83
89
97
```

---
---

### Introduction to Lists
- **Lists** in Python are ordered, mutable collections of items that can contain items of different data types such as integers, strings, floats, or even other lists.
- Lists are represented using square brackets `[]`.

### Creating Lists
- You can create an empty list or a list with values.
  
```python
lst = []  # Empty list
print(type(lst))  # Output: <class 'list'>

names = ["Assaf", "Aysha", "Sumaya", 1, 2, 3]  # List with mixed data types
print(names)
```

**Output**:
```plaintext
['Assaf', 'Aysha', 'Sumaya', 1, 2, 3]
```

### Accessing List Elements
- List elements are indexed starting from `0`.
- You can access items using positive or negative indices.

```python
fruits = ["apple", "banana", "cherry", "kiwi", "guava"]
print(fruits[0])    # Output: apple
print(fruits[2])    # Output: cherry
print(fruits[-1])   # Output: guava (negative index for last item)
```

### Modifying List Elements
- Lists are mutable, meaning you can change their elements.

```python
fruits[1] = "watermelon"
print(fruits)  # Output: ['apple', 'watermelon', 'cherry', 'kiwi', 'guava']
```

### List Methods
- Python provides several built-in methods to modify and interact with lists.

1. **`append()`**: Adds an item to the end.
2. **`insert()`**: Inserts an item at a specific index.
3. **`remove()`**: Removes the first occurrence of an item.
4. **`pop()`**: Removes and returns the last element (or by index).
5. **`index()`**: Returns the index of the first occurrence of an item.
6. **`count()`**: Counts the occurrences of an item in the list.
7. **`sort()`**: Sorts the list in ascending order.
8. **`reverse()`**: Reverses the order of the list.
9. **`clear()`**: Removes all items from the list.

**Examples**:

```python
fruits.append("orange")
print(fruits)  # Output: ['apple', 'watermelon', 'cherry', 'kiwi', 'guava', 'orange']

fruits.insert(1, "banana")
print(fruits)  # Output: ['apple', 'banana', 'watermelon', 'cherry', 'kiwi', 'guava', 'orange']

fruits.remove("banana")
print(fruits)  # Output: ['apple', 'watermelon', 'cherry', 'kiwi', 'guava', 'orange']

last_fruit = fruits.pop()
print(last_fruit)  # Output: orange
print(fruits)      # Output: ['apple', 'watermelon', 'cherry', 'kiwi', 'guava']
```

### Slicing Lists
- You can access parts of a list using **slicing**.

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(numbers[2:5])  # Output: [3, 4, 5] (index 2 to 4)
print(numbers[:5])   # Output: [1, 2, 3, 4, 5] (first 5 elements)
print(numbers[5:])   # Output: [6, 7, 8, 9, 10] (from index 5 onward)
print(numbers[::2])  # Output: [1, 3, 5, 7, 9] (step of 2)
print(numbers[::-1]) # Output: [10, 9, 8, 7, 6, 5, 4, 3, 2, 1] (reversed)
```

### Iterating Over Lists
- You can loop through a list using a `for` loop.

```python
for number in numbers:
    print(number)
```

- To get both the **index** and **value**, use `enumerate()`:

```python
for index, number in enumerate(numbers):
    print(f"Index: {index}, Value: {number}")
```

---

### List Comprehension
A list comprehension is just a shorter way to create a new list based on an existing list (or any iterable). The basic structure looks like this:

### Basic Structure
```python
[expression for item in iterable]
```

- `expression`: What you want to do with each `item`.
- `item`: The element you are iterating over (from a list, range, etc.).
- `iterable`: The collection you are going through (like a list or range).

### Example 1: Simple List Comprehension

Without list comprehension:
```python
squares = []
for num in range(5):
    squares.append(num**2)

print(squares)  # Output: [0, 1, 4, 9, 16]
```

With list comprehension:
```python
squares = [num**2 for num in range(5)]
print(squares)  # Output: [0, 1, 4, 9, 16]
```
Explanation: 
- `num**2`: For each number in `range(5)`, square it.
- The result is a list of squared numbers.

### Example 2: List Comprehension with Condition

Without list comprehension:
```python
evens = []
for num in range(10):
    if num % 2 == 0:
        evens.append(num)

print(evens)  # Output: [0, 2, 4, 6, 8]
```

With list comprehension:
```python
evens = [num for num in range(10) if num % 2 == 0]
print(evens)  # Output: [0, 2, 4, 6, 8]
```
Explanation: 
- `num % 2 == 0`: This checks if `num` is even.
- Only even numbers get added to the list.

### Example 3: Nested Loops in List Comprehension

Without list comprehension:
```python
pairs = []
for i in [1, 2, 3]:
    for j in ['a', 'b', 'c']:
        pairs.append((i, j))

print(pairs)
# Output: [(1, 'a'), (1, 'b'), (1, 'c'), (2, 'a'), (2, 'b'), (2, 'c'), (3, 'a'), (3, 'b'), (3, 'c')]
```

With list comprehension:
```python
pairs = [(i, j) for i in [1, 2, 3] for j in ['a', 'b', 'c']]
print(pairs)
# Output: [(1, 'a'), (1, 'b'), (1, 'c'), (2, 'a'), (2, 'b'), (2, 'c'), (3, 'a'), (3, 'b'), (3, 'c')]
```
Explanation:
- We're creating pairs by iterating over two lists.
- For each `i` in `[1, 2, 3]`, we combine it with each `j` in `['a', 'b', 'c']`.

### Try this: Create a list of numbers from 1 to 10, but only include numbers greater than 5:
```python
numbers = [num for num in range(1, 11) if num > 5]
print(numbers)  # Output: [6, 7, 8, 9, 10]
```
---
### Practical Examples and Common Errors

1. **Managing a To-Do List**:
```python
to_do_list = ["Buy groceries", "Pay bills", "Clean house"]
to_do_list.append("Go for a run")
to_do_list.remove("Clean house")

for task in to_do_list:
    print(f"- {task}")
```

2. **Student Grades**:
```python
grades = [85, 92, 78, 90]
grades.append(95)

average = sum(grades) / len(grades)
print(f"Average Grade: {average:.2f}")  # Output: Average Grade: 88.00
```

3. **Common Errors**:
- **IndexError**: Trying to access an element at an index that doesn't exist:
  
```python
print(fruits[10])  # Error: IndexError: list index out of range
```

- **TypeError**: Performing unsupported operations on incompatible types.

```python
print(fruits + 3)  # Error: TypeError: can only concatenate list (not "int") to list
```
---
### **Example 1: Managing a To-Do List**
A to-do list helps you keep track of tasks to complete. In this case:

```python
to_do_list = ["Buy Groceries", "Clean the house", "Pay bills"]

# Adding tasks
to_do_list.append("Schedule meeting")
to_do_list.append("Go For a Run")

# Removing a completed task
to_do_list.remove("Clean the house")

# Checking if a task exists
if "Pay bills" in to_do_list:
    print("Don't forget to pay the utility bills")

# Displaying remaining tasks
print("To Do List remaining:")
for task in to_do_list:
    print(f"- {task}")
```
**Key Operations:**
- **Adding tasks** using `append()`
- **Removing tasks** with `remove()`
- **Checking if a task exists** using `if ... in list`

---

### **Example 2: Organizing Student Grades**
Storing and calculating the average grade, highest, and lowest grade for students:

```python
grades = [85, 92, 78, 90, 88]

# Adding a new grade
grades.append(95)

# Calculating average
average_grade = sum(grades) / len(grades)
print(f"Average Grade: {average_grade:.2f}")

# Finding highest and lowest grades
highest_grade = max(grades)
lowest_grade = min(grades)
print(f"Highest Grade: {highest_grade}")
print(f"Lowest Grade: {lowest_grade}")
```
**Key Operations:**
- **Calculating average** using `sum()` and `len()`
- **Finding maximum and minimum values** with `max()` and `min()`

---

### **Example 3: Managing an Inventory**
This example manages inventory items in a store:

```python
inventory = ["apples", "bananas", "oranges", "grapes"]

# Adding a new item
inventory.append("strawberries")

# Removing an out-of-stock item
inventory.remove("bananas")

# Checking if an item is in stock
item = "oranges"
if item in inventory:
    print(f"{item} are in stock.")
else:
    print(f"{item} are out of stock.")

# Printing the inventory
print("Inventory List:")
for item in inventory:
    print(f"- {item}")
```
**Key Operations:**
- **Managing stock** with `append()` and `remove()`
- **Checking stock availability** with `if ... in list`

---

### **Example 4: Collecting User Feedback**
Gather and analyze feedback from users:

```python
feedback = ["Great service!", "Very satisfied", "Could be better", "Excellent experience"]

# Adding new feedback
feedback.append("Not happy with the service")

# Counting positive feedback
positive_feedback_count = sum(1 for comment in feedback if "great" in comment.lower() or "excellent" in comment.lower())
print(f"Positive Feedback Count: {positive_feedback_count}")

# Printing all feedback
print("User Feedback:")
for comment in feedback:
    print(f"- {comment}")
```
**Key Operations:**
- **Filtering positive feedback** with `if "word" in comment`
- **Counting occurrences** using `sum()`

---

Let's break down the line step by step:

```python
positive_feedback_count = sum(1 for comment in feedback if "great" in comment.lower() or "excellent" in comment.lower())
```

### What it does:
1. **Loop through each comment**: It checks each item in the `feedback` list (like "Great service!", "Excellent experience").
   
2. **Convert comment to lowercase**: `comment.lower()` converts the entire comment to lowercase so that it doesn't matter if the word "great" or "excellent" appears in upper or lowercase.

3. **Check if the comment contains "great" or "excellent"**: The line checks if either of these words is present in the comment.

4. **Count positive feedback**: For every comment that contains "great" or "excellent," it adds `1` to the count (via `sum(1 for ...)`). The `sum` function adds up all the `1`s for comments that meet this condition, giving you the total count of positive feedback.

### Example for better understanding:

Imagine you have the following feedback:

```python
feedback = ["Great service!", "Could be better", "Excellent experience", "Not happy"]
```

The line of code checks each comment:
- "Great service!" → contains "great" → count `1`
- "Could be better" → doesn't contain "great" or "excellent" → count `0`
- "Excellent experience" → contains "excellent" → count `1`
- "Not happy" → doesn't contain "great" or "excellent" → count `0`

So, the total `positive_feedback_count` will be `2`.

### More Examples:

#### Example 1: Counting Words with "happy"
```python
comments = ["I'm happy!", "Not happy with the service", "Could be better"]
happy_count = sum(1 for comment in comments if "happy" in comment.lower())
print(happy_count)
```
- Checks each comment to see if it contains "happy".
- Result: `2` because "I'm happy!" and "Not happy with the service" contain the word "happy".

#### Example 2: Counting Comments with "bad"
```python
comments = ["Bad experience", "Not bad!", "Good service"]
bad_count = sum(1 for comment in comments if "bad" in comment.lower())
print(bad_count)
```
- This will count the comments that contain "bad".
- Result: `2` because "Bad experience" and "Not bad!" contain "bad".

#### Example 3: Counting Comments with Multiple Keywords
```python
comments = ["Amazing service", "Very good", "Excellent work!", "Not impressed"]
positive_count = sum(1 for comment in comments if "amazing" in comment.lower() or "excellent" in comment.lower())
print(positive_count)
```
- This counts comments that contain either "amazing" or "excellent".
- Result: `2` because "Amazing service" and "Excellent work!" meet the condition.

### Summary:
The line `sum(1 for ...)` counts how many times a condition is true (like finding certain words). The condition checks each comment and, if it meets the requirement (contains "great" or "excellent"), it adds `1` to the total count.
To get input from a user to create a list, you can use the `input()` function in Python. Here are a few methods to gather a list from user input:

### Method 1: Input a List of Items as a Single Line
You can prompt the user to input items separated by spaces, commas, or another delimiter, and then split the input to create a list.

```python
# Ask the user to input items separated by spaces
user_input = input("Enter items separated by spaces: ")

# Split the input string into a list
user_list = user_input.split()  # By default, split() splits by spaces

print("Your list:", user_list)
```

#### Example Output:
```
Enter items separated by spaces: apple banana orange
Your list: ['apple', 'banana', 'orange']
```

### Method 2: Input a List of Numbers
If you are expecting a list of numbers from the user, you can convert each item to an integer or float.

```python
# Input a list of numbers
user_input = input("Enter numbers separated by spaces: ")

# Convert input string into a list of integers (or floats)
number_list = [int(num) for num in user_input.split()]  # Use float() if you want decimal numbers

print("Your list of numbers:", number_list)
```

#### Example Output:
```
Enter numbers separated by spaces: 10 20 30 40
Your list of numbers: [10, 20, 30, 40]
```

### Method 3: Input Items One by One
You can also ask the user to input list items one at a time using a loop.

```python
# Ask the user how many items they want to add to the list
n = int(input("How many items do you want to add? "))

user_list = []

# Loop to get each item
for i in range(n):
    item = input(f"Enter item {i+1}: ")
    user_list.append(item)

print("Your list:", user_list)
```

#### Example Output:
```
How many items do you want to add? 3
Enter item 1: apple
Enter item 2: banana
Enter item 3: cherry
Your list: ['apple', 'banana', 'cherry']
```

### Method 4: Input Items Until the User Says 'Stop'
You can also keep accepting inputs from the user until they enter a special keyword like "stop."

```python
user_list = []

while True:
    item = input("Enter an item (or type 'stop' to finish): ")
    if item.lower() == 'stop':
        break
    user_list.append(item)

print("Your list:", user_list)
```

#### Example Output:
```
Enter an item (or type 'stop' to finish): apple
Enter an item (or type 'stop' to finish): banana
Enter an item (or type 'stop' to finish): stop
Your list: ['apple', 'banana']
```

---
### Introduction to Tuples

Tuples in Python are **ordered** collections of items that are **immutable**, meaning once a tuple is created, its elements cannot be changed, unlike lists. Tuples are useful when you want to ensure that the data remains constant throughout your program.

---

### Differences between Lists and Tuples:
- **Mutability**: Lists are mutable (you can change elements), while tuples are immutable (once created, elements can't be changed).
- **Syntax**: Lists use square brackets `[ ]`, while tuples use parentheses `( )`.
- **Performance**: Tuples can be more efficient in terms of memory and speed since they are immutable.

---

### Example of Creating a Tuple

```python
# Empty tuple
empty_tuple = ()
print(empty_tuple)  # Output: ()

# Tuple with multiple elements
mixed_tuple = (1, "Hello", 3.14, True)
print(mixed_tuple)  # Output: (1, 'Hello', 3.14, True)

# Tuple from a list
numbers = tuple([1, 2, 3, 4, 5, 6])
print(numbers)  # Output: (1, 2, 3, 4, 5, 6)
```

---

### Accessing Tuple Elements
You can access tuple elements just like lists using indices.

```python
numbers = (1, 2, 3, 4, 5, 6)
print(numbers[2])    # Output: 3
print(numbers[-1])   # Output: 6
print(numbers[0:4])  # Output: (1, 2, 3, 4)
```

---

### Tuple Operations

1. **Concatenation**: Combine tuples using `+`.
   ```python
   new_tuple = numbers + mixed_tuple
   print(new_tuple)
   # Output: (1, 2, 3, 4, 5, 6, 1, 'Hello', 3.14, True)
   ```

2. **Repetition**: Repeat a tuple using `*`.
   ```python
   repeated_tuple = mixed_tuple * 2
   print(repeated_tuple)
   # Output: (1, 'Hello', 3.14, True, 1, 'Hello', 3.14, True)
   ```

---

### Immutability of Tuples

Once a tuple is created, you cannot modify its elements. This is what makes tuples different from lists.

```python
numbers = (1, 2, 3, 4, 5, 6)
numbers[1] = "Assaf"  # This will throw an error
# TypeError: 'tuple' object does not support item assignment
```

---

### Tuple Methods

1. **count()**: Returns the number of times an element appears in a tuple.
   ```python
   print(numbers.count(1))  # Output: 1
   ```

2. **index()**: Returns the index of the first occurrence of an element.
   ```python
   print(numbers.index(3))  # Output: 2
   ```

---

### Packing and Unpacking Tuples

- **Packing**: You can pack multiple values into a tuple.
  ```python
  packed_tuple = 1, "Hello", 3.14
  print(packed_tuple)  # Output: (1, 'Hello', 3.14)
  ```

- **Unpacking**: You can assign values of a tuple to variables.
  ```python
  a, b, c = packed_tuple
  print(a)  # Output: 1
  print(b)  # Output: Hello
  print(c)  # Output: 3.14
  ```

- **Unpacking with `*` (rest)**: You can unpack parts of a tuple while keeping the remaining elements in a list.
  ```python
  first, *middle, last = numbers
  print(first)   # Output: 1
  print(middle)  # Output: [2, 3, 4, 5]
  print(last)    # Output: 6
  ```

---

### Nested Tuples

Tuples can contain other tuples or even lists inside them.

```python
nested_tuple = ((1, 2, 3), ("a", "b", "c"), (True, False))

# Accessing elements in nested tuples
print(nested_tuple[0])       # Output: (1, 2, 3)
print(nested_tuple[1][2])    # Output: 'c'

# Iterating over nested tuples
for sub_tuple in nested_tuple:
    for item in sub_tuple:
        print(item, end=" ")
    print()
# Output:
# 1 2 3 
# a b c 
# True False 
```

---

### Missing Topics:

1. **Why Use Tuples?**
   - Immutability ensures data integrity.
   - Used for fixed collections of items like coordinates, days of the week, etc.

2. **Tuples as Dictionary Keys**:
   Tuples, being immutable, can be used as keys in dictionaries (unlike lists).

3. **Tuples in Functions**:
   You can return multiple values from a function using tuples.

---
Python **does not have tuple comprehensions** in the same way it has list comprehensions. However, you can create a tuple using a generator expression and then convert it to a tuple, but this won't directly generate a tuple. Here's how it works:

### Example: Simulating Tuple Comprehension with a Generator Expression

You can use a generator expression inside the `tuple()` constructor to create a tuple:

```python
# Generator expression inside tuple()
numbers_tuple = tuple(x**2 for x in range(5))
print(numbers_tuple)  # Output: (0, 1, 4, 9, 16)
```

This looks similar to list comprehensions, but instead of creating a tuple directly, you create a generator expression, which is then passed to `tuple()` to convert the result into a tuple.

### Key Difference:
- **List Comprehension** creates a list directly:
  ```python
  squares = [x**2 for x in range(5)]
  print(squares)  # Output: [0, 1, 4, 9, 16]
  ```

- **Tuple Comprehension** doesn't exist directly, but you can use a generator expression with `tuple()` to achieve a similar result.

```python
numbers_tuple = tuple(x**2 for x in range(5))  # Uses generator expression
```
This is how you can create a tuple in a similar way to how you'd create a list comprehension, though tuple comprehension isn't a built-in syntax.
No, there is no direct concept of **list packing** like there is with tuples in Python. However, you can achieve a similar effect by creating a list using square brackets or by explicitly passing multiple values to a list.

### Example: List Creation (Packing-like behavior)

To create a list with multiple elements, you simply enclose the values in square brackets:

```python
# Creating a list (like packing values into a list)
my_list = [1, "Hello", 3.14]
print(my_list)  # Output: [1, 'Hello', 3.14]
```

While this creates a list, it doesn't automatically happen like tuple packing. You have to explicitly use square brackets (`[]`) or the `list()` constructor.

### Example: List Creation Using `list()`

You can also use the `list()` function to convert values into a list:

```python
my_list = list((1, "Hello", 3.14))  # Convert tuple to list
print(my_list)  # Output: [1, 'Hello', 3.14]
```

### Collecting Multiple Values into a List Using `*`

While there's no direct list packing, if you use `*` with lists, you can **collect** multiple values into a list when unpacking, similar to how tuple unpacking works with `*`.

### Example: List with `*` for Packing-Like Behavior

```python
def pack_into_list(first, *rest):
    print(f"First value: {first}")
    print(f"Remaining values packed into a list: {list(rest)}")

pack_into_list(1, 2, 3, 4, 5)
```

**Output:**
```
First value: 1
Remaining values packed into a list: [2, 3, 4, 5]
```

In this example, `*rest` collects all remaining values and "packs" them into a list, but this only happens when using the `*` in function parameters or unpacking.

So, while there's no automatic list packing, you can explicitly create or collect values into lists using these methods.

---
## Tuple as Input from the User
To take a tuple as input from the user, you can ask the user to provide comma-separated values, then convert that input into a tuple.

Here's a simple way to do that:

### Example: Taking Tuple Input from User

```python
# Asking for user input (comma-separated values)
user_input = input("Enter comma-separated values for a tuple: ")

# Converting the input string to a tuple
user_tuple = tuple(user_input.split(','))

print("Your tuple:", user_tuple)
```

### Explanation:

1. **`input()`**: Takes user input as a string.
2. **`split(',')`**: Splits the string by commas into a list.
3. **`tuple()`**: Converts the list into a tuple.

### Example Run:

```
Enter comma-separated values for a tuple: 1,hello,3.14,True
Your tuple: ('1', 'hello', '3.14', 'True')
```

### Note:

- The elements of the tuple will be strings by default. If you want to convert them to specific types (like integers, floats, etc.), you need to handle that manually.

### Handling Different Data Types in a Tuple

If you want to take input for a tuple containing different data types (e.g., integers, strings, etc.), you can modify the code like this:

```python
# Input a tuple with different types
user_input = input("Enter comma-separated values (e.g., 1,hello,3.14): ")

# Convert input into a list and process elements
user_tuple = tuple(eval(i) for i in user_input.split(','))

print("Your tuple with converted data types:", user_tuple)
```

### Example Run:

```
Enter comma-separated values (e.g., 1,hello,3.14): 1,hello,3.14,True
Your tuple with converted data types: (1, 'hello', 3.14, True)
```

In this case, `eval(i)` automatically converts numeric strings to `int` or `float`, and recognizes `True`/`False` as boolean values. However, be cautious with `eval()` since it executes the input directly, which might not be safe for arbitrary inputs.

## Introduction to Sets

Sets are a built-in data type in Python that allow you to store collections of **unique** items. Unlike lists and tuples, sets do not maintain any specific order, and they automatically eliminate duplicates. Sets are particularly useful for operations that involve unique items, such as membership tests and mathematical set operations like union, intersection, and difference.

#### Key Characteristics of Sets:
- **Unordered**: The elements do not have a specific order.
- **Unique**: No duplicate elements are allowed.
- **Mutable**: You can add or remove items from a set.

### Creating Sets

You can create sets in a few different ways:

1. **Using Curly Braces**:
   ```python
   my_set = {1, 2, 3, 4, 5}
   ```

2. **Using the `set()` Constructor**:
   ```python
   my_empty_set = set()  # Creates an empty set
   my_set = set([1, 2, 3, 4, 5, 6])  # Converts a list to a set
   ```

3. **Eliminating Duplicates**:
   ```python
   my_set = set([1, 2, 3, 6, 5, 4, 5, 6])  # Duplicates are removed
   ```

### Basic Set Operations

1. **Adding and Removing Elements**:
   - **Add an Element**:
     ```python
     my_set.add(7)  # Adds 7 to the set
     ```
   - **Remove an Element**:
     ```python
     my_set.remove(3)  # Removes 3 from the set
     # If the element is not found, it raises a KeyError
     ```
   - **Using `discard()`**:
     ```python
     my_set.discard(10)  # Does nothing if 10 is not found
     ```
   - **Pop an Element**:
     ```python
     removed_element = my_set.pop()  # Removes and returns an arbitrary element
     ```
   - **Clear All Elements**:
     ```python
     my_set.clear()  # Removes all elements from the set
     ```

2. **Membership Test**:
   ```python
   print(3 in my_set)  # Returns True if 3 is in the set
   print(10 in my_set)  # Returns False if 10 is not in the set
   ```

### Mathematical Operations on Sets

1. **Union**:
   Combines all unique elements from both sets.
   ```python
   union_set = set1.union(set2)  # or set1 | set2
   ```

2. **Intersection**:
   Returns elements that are common to both sets.
   ```python
   intersection_set = set1.intersection(set2)  # or set1 & set2
   ```

3. **Difference**:
   Returns elements in the first set that are not in the second set.
   ```python
   difference_set = set1.difference(set2)  # or set1 - set2
   ```

4. **Symmetric Difference**:
   Returns elements in either set but not in both.
   ```python
   symmetric_difference_set = set1.symmetric_difference(set2)  # or set1 ^ set2
   ```

### Set Methods

- **Subset**: Checks if all elements of one set are in another.
  ```python
  print(set1.issubset(set2))
  ```

- **Superset**: Checks if one set contains all elements of another.
  ```python
  print(set1.issuperset(set2))
  ```

### Example: Counting Unique Words in a Text

You can use sets to eliminate duplicates from a list of words:
```python
text = "In this tutorial we are discussing about sets"
words = text.split()  # Splits the text into words
unique_words = set(words)  # Converts the list of words to a set
print(unique_words)
print(len(unique_words))  # Counts the number of unique words
```

### Differences Between Sets and Other Data Types

- **Lists**: Ordered, can contain duplicates, and elements can be accessed by index.
- **Tuples**: Ordered, can contain duplicates, immutable (cannot be changed after creation).
- **Sets**: Unordered, cannot contain duplicates, and are mutable.

Sets are particularly useful when you need to ensure all elements are unique and do not care about the order of those elements. They provide efficient methods for performing mathematical operations, making them a versatile data structure in Python.

---
---

## Introduction to Dictionaries

Dictionaries are unordered collections of items that store data in key-value pairs. In a dictionary, keys must be unique and immutable (like strings, numbers, or tuples), while values can be of any type.

### Creating Dictionaries

```python
# Creating an empty dictionary
empty_dict = {}
print(type(empty_dict))  # Output: <class 'dict'>

# Creating a dictionary with student information
student = {"name": "Assaf", "age": 21, "grade": "A"}
print(student)  # Output: {'name': 'Assaf', 'age': 21, 'grade': 'A'}
print(type(student))  # Output: <class 'dict'>

# Note: Keys must be unique; if you repeat a key, the last value will be used.
student = {"name": "Assaf", "age": 21, "name": "A+"}
print(student)  # Output: {'name': 'A+', 'age': 21}
```

### Accessing Dictionary Elements

```python
# Accessing dictionary elements using keys
print(student["name"])  # Output: Assaf
print(student["age"])  # Output: 21

# Using the get() method
print(student.get("grade"))  # Output: A
print(student.get("last_name"))  # Output: None
print(student.get("last_name", "Not Available"))  # Output: Not Available
```

### Modifying Dictionary Elements

Dictionaries are mutable, meaning you can add, update, or delete elements.

```python
print(student)  # Output: {'name': 'Assaf', 'age': 21, 'grade': 'A'}

# Updating a value
student["age"] = 22
print(student)  # Output: {'name': 'Assaf', 'age': 22, 'grade': 'A'}

# Adding a new key-value pair
student["address"] = "India"
print(student)  # Output: {'name': 'Assaf', 'age': 22, 'grade': 'A', 'address': 'India'}

# Deleting a key-value pair
del student["grade"]
print(student)  # Output: {'name': 'Assaf', 'age': 22, 'address': 'India'}
```

### Dictionary Methods

```python
# Getting all keys
keys = student.keys()
print(keys)  # Output: dict_keys(['name', 'age', 'address'])

# Getting all values
values = student.values()
print(values)  # Output: dict_values(['Assaf', 22, 'India'])

# Getting all key-value pairs
items = student.items()
print(items)  # Output: dict_items([('name', 'Assaf'), ('age', 22), ('address', 'India')])
```

### Shallow Copy

```python
# Creating a shallow copy of the dictionary
student_copy = student.copy()
print(student_copy)  # Output: {'name': 'Assaf', 'age': 22, 'address': 'India'}

# Modifying the original dictionary
student["name"] = "Assaf Updated"
print(student)  # Output: {'name': 'Assaf Updated', 'age': 22, 'address': 'India'}
print(student_copy)  # Output: {'name': 'Assaf', 'age': 22, 'address': 'India'}
```

### Iterating Over Dictionaries

```python
# Iterating over keys
for key in student.keys():
    print(key)

# Iterating over values
for value in student.values():
    print(value)

# Iterating over key-value pairs
for key, value in student.items():
    print(f"{key}: {value}")
```

### Nested Dictionaries

```python
# Creating nested dictionaries
students = {
    "student1": {"name": "Assaf", "age": 21},
    "student2": {"name": "Peter", "age": 35}
}

# Accessing nested dictionary elements
print(students["student1"]["name"])  # Output: Assaf
print(students["student2"]["age"])  # Output: 35
```

### Dictionary Comprehension

```python
# Creating a dictionary using comprehension
squares = {x: x ** 2 for x in range(5)}
print(squares)  # Output: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}

# Conditional dictionary comprehension
evens = {x: x ** 2 for x in range(10) if x % 2 == 0}
print(evens)  # Output: {0: 0, 2: 4, 4: 16, 6: 36, 8: 64}
```

### Practical Examples

#### Counting Frequency of Elements in a List

```python
numbers = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]
frequency = {}

for number in numbers:
    if number in frequency:
        frequency[number] += 1
    else:
        frequency[number] = 1
print(frequency)  # Output: {1: 1, 2: 2, 3: 3, 4: 4}
```

#### Merging Two Dictionaries

```python
dict1 = {"a": 1, "b": 2}
dict2 = {"b": 3, "c": 4}
merged_dict = {**dict1, **dict2}
print(merged_dict)  # Output: {'a': 1, 'b': 3, 'c': 4}
```

---
***The curly braces `{}`*** are used to create both sets and dictionaries in Python, but there are important distinctions between them:

1. **Dictionaries**: 
   - Defined using key-value pairs.
   - Example: 
     ```python
     my_dict = {"name": "Assaf", "age": 21}
     ```

2. **Sets**: 
   - Contain only unique elements and do not have key-value pairs.
   - Example: 
     ```python
     my_set = {1, 2, 3, 4, 5}
     ```

### Key Differences:
- **Data Structure**: 
  - Sets are collections of unique items without any associated values.
  - Dictionaries are collections of key-value pairs, where each key must be unique.

- **Accessing Elements**:
  - In a set, you can only access items based on their value.
  - In a dictionary, you can access values using their corresponding keys.

### Creating an Empty Set and Dictionary:
- To create an empty set, you must use the `set()` function:
  ```python
  empty_set = set()  # Creates an empty set
  ```
  
- To create an empty dictionary, you can use either `{}` or `dict()`:
  ```python
  empty_dict = {}    # Creates an empty dictionary
  empty_dict2 = dict()  # Also creates an empty dictionary
  ```

### Example:
```python
# Dictionary
my_dict = {"name": "Assaf", "age": 21}
print(my_dict)  # Output: {'name': 'Assaf', 'age': 21}

# Set
my_set = {1, 2, 3, 4, 5}
print(my_set)  # Output: {1, 2, 3, 4, 5}
```
while the curly braces look the same, they represent different data types in Python!

---

## FUCTIONS:

### Introduction to Functions

**Definition**:  
A function is a reusable block of code that performs a specific task. It helps organize code, avoid repetition, and makes it easier to understand and maintain.

### Syntax of a Function:
```python
def function_name(parameters):
    """Docstring"""
    # Function body
    return expression
```

- `def`: This keyword is used to define a function.
- `function_name`: The name of the function.
- `parameters`: Optional inputs the function can take.
- `"""Docstring"""`: An optional string to describe what the function does.
- `return`: This is used to send a result back after the function finishes.

### Why Functions?

Imagine you have the following code:
```python
num = 24
if num % 2 == 0:
    print("the number is even")
else:
    print("the number is odd")
```
This code works but isn't reusable for checking other numbers. To solve this, you can put it inside a function:

```python
def even_or_odd(num):
    """This function finds whether a number is even or odd."""
    if num % 2 == 0:
        print("the number is even")
    else:
        print("the number is odd")
```

You can now call this function multiple times with different inputs:
```python
even_or_odd(24)
even_or_odd(13)
```

### Function with Multiple Parameters:

You can also define functions that take multiple inputs:
```python
def add(a, b):
    return a + b

result = add(2, 4)
print(result)  # Output: 6
```

- The function `add(a, b)` takes two parameters `a` and `b` and returns their sum.

### Default Parameters:

If you want to give a default value to a parameter, you can use default parameters:

```python
def greet(name="Guest"):
    print(f"Hello {name}, Welcome to the paradise")
    
greet()         # Output: Hello Guest, Welcome to the paradise
greet("Mohamed Assaf")  # Output: Hello Mohamed Assaf, Welcome to the paradise
```

- If no argument is provided, the function will use the default value `"Guest"`.

### Variable-Length Arguments:

Sometimes you don't know how many arguments will be passed to a function. Python allows functions to handle this with `*args` for positional arguments and `**kwargs` for keyword arguments.

#### Positional Arguments (`*args`):

You can pass a variable number of arguments, and they will be received as a tuple:

```python
def print_numbers(*args):
    for number in args:
        print(number)

print_numbers(1, 2, 3, 4, 5)
```
- `*args` collects all the arguments passed to the function.

#### Keyword Arguments (`**kwargs`):

For keyword arguments, you use `**kwargs`, which collects them as a dictionary:

```python
def print_details(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_details(name="Mohamed Assaf", age="21", country="India")
```
- `**kwargs` captures keyword arguments in the form of key-value pairs.

### Using Both `*args` and `**kwargs` Together:

You can combine both types of arguments in one function:
```python
def print_details(*args, **kwargs):
    for val in args:
        print(f"Positional argument: {val}")
    
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_details(1, 2, "Mohamed Assaf", name="Mohamed Assaf", age="21", country="India")
```
- Here, `1, 2, "Mohamed Assaf"` are positional arguments (`*args`), and the rest are keyword arguments (`**kwargs`).

### Return Statements:

A function can return a result using `return`:
```python
def multiply(a, b):
    return a * b

result = multiply(2, 3)
print(result)  # Output: 6
```

### Returning Multiple Values:

Functions can return more than one value by separating them with commas:
```python
def multiply(a, b):
    return a * b, a

result = multiply(2, 3)
print(result)  # Output: (6, 2)
```
- The function returns a tuple with both values.

This version should now fully reflect your details! Let me know if you need any further changes.

---
### `*args` in Python

`*args` is used in functions to allow for a variable number of positional arguments. It collects all the arguments into a tuple.

#### Example:
```python
def print_numbers(*args):
    for number in args:
        print(number)

print_numbers(1, 2, 3, 4, 5)
```

In this example:
- When you call `print_numbers(1, 2, 3, 4, 5)`, Python packs these arguments into a tuple `(1, 2, 3, 4, 5)`.
- Inside the function, `args` refers to this tuple.

---

### Passing a List to `*args`

1. **Passing a List Directly:**
   - If you pass a list directly to a function with `*args`, the entire list is treated as a single element inside the tuple.

   ```python
   def print_numbers(*args):
       for number in args:
           print(number)

   my_list = [1, 2, 3, 4, 5]
   print_numbers(my_list)
   ```

   **Output:**
   ```
   [1, 2, 3, 4, 5]
   ```

   - In this case, `args` will be `([1, 2, 3, 4, 5],)`, meaning the list is treated as one element inside the tuple.

2. **Unpacking the List:**
   - To treat each element of the list as a separate argument, you can use the unpacking operator `*` when calling the function.

   ```python
   def print_numbers(*args):
       for number in args:
           print(number)

   my_list = [1, 2, 3, 4, 5]
   print_numbers(*my_list)  # Unpacks the list into individual arguments
   ```

   **Output:**
   ```
   1
   2
   3
   4
   5
   ```

   - Here, using `*my_list` unpacks the list into its individual elements, so the function receives `1, 2, 3, 4, 5` as separate positional arguments. 
   - Inside the function, `args` becomes `(1, 2, 3, 4, 5)`.

---

### Functions Examples Explained

Functions are reusable pieces of code that perform specific tasks. Below are examples of various functions, with explanations to make each concept easy to understand.

### Example 1: **Temperature Conversion**
This function converts temperatures between Celsius and Fahrenheit based on the unit provided.

```python
def convert_temperature(temp, unit):
    """This function converts temperature between Celsius and Fahrenheit."""
    if unit == 'C':
        return temp * 9/5 + 32  # Celsius to Fahrenheit
    elif unit == "F":
        return (temp - 32) * 5/9  # Fahrenheit to Celsius
    else:
        return None

print(convert_temperature(25, 'C'))  # Output: 77.0
print(convert_temperature(77, 'F'))  # Output: 25.0
```

- **Explanation**: 
  - If the unit is `'C'`, it converts Celsius to Fahrenheit.
  - If the unit is `'F'`, it converts Fahrenheit to Celsius.
  - If the unit is not recognized, it returns `None`.

---

### Example 2: **Password Strength Checker**
This function checks if a password is strong by following certain rules like length, digits, and special characters.

```python
def is_strong_password(password):
    """This function checks if the password is strong or not."""
    if len(password) < 8:
        return False
    if not any(char.isdigit() for char in password):
        return False
    if not any(char.islower() for char in password):
        return False
    if not any(char.isupper() for char in password):
        return False
    if not any(char in '!@#$%^&*()_+' for char in password):
        return False
    return True

print(is_strong_password("WeakPwd"))      # Output: False
print(is_strong_password("Str0ngPwd!"))   # Output: True
```

- **Explanation**:
  - Checks if the password has at least 8 characters.
  - Ensures it contains at least one digit, one lowercase letter, one uppercase letter, and one special character.

---

### Example 3: **Calculate the Total Cost of Items in a Shopping Cart**
This function calculates the total cost of items based on their price and quantity in a shopping cart.

```python
def calculate_total_cost(cart):
    total_cost = 0
    for item in cart:
        total_cost += item['price'] * item['quantity']
    return total_cost

# Example cart data
cart = [
    {'name': 'Apple', 'price': 0.5, 'quantity': 4},
    {'name': 'Banana', 'price': 0.3, 'quantity': 6},
    {'name': 'Orange', 'price': 0.7, 'quantity': 3}
]

total_cost = calculate_total_cost(cart)
print(total_cost)  # Output: 5.9
```

- **Explanation**: 
  - Loops through each item in the cart and multiplies the price by the quantity to get the total cost.

---

### Example 4: **Check if a String Is a Palindrome**
This function checks if a string is a palindrome (a word or sentence that reads the same forward and backward).

```python
def is_palindrome(s):
    s = s.lower().replace(" ", "")  # Converts to lowercase and removes spaces
    return s == s[::-1]  # Checks if the string is the same when reversed

print(is_palindrome("A man a plan a canal Panama"))  # Output: True
print(is_palindrome("Hello"))                         # Output: False
```

- **Explanation**: 
  - Converts the string to lowercase, removes spaces, and checks if the string is equal to its reverse.

---

### Example 5: **Calculate Factorials Using Recursion**
This function calculates the factorial of a number using recursion (a function calling itself).

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(6))  # Output: 720
```

- **Explanation**: 
  - The base case is `n == 0`, which returns 1.
  - Otherwise, it multiplies `n` by `factorial(n-1)`.

---

### Example 6: **Count Word Frequency in a File**
This function reads a file and counts the frequency of each word in the file.

```python
def count_word_frequency(file_path):
    word_count = {}
    with open(file_path, 'r') as file:
        for line in file:
            words = line.split()
            for word in words:
                word = word.lower().strip('.,!?;:"\'')  # Removes punctuation
                word_count[word] = word_count.get(word, 0) + 1
    return word_count

filepath = 'sample.txt'
word_frequency = count_word_frequency(filepath)
print(word_frequency)
```

- **Explanation**: 
  - Reads the file line by line, splits each line into words, and counts how many times each word appears.

---

### Example 7: **Validate Email Address**
This function checks if an email is valid using regular expressions.

```python
import re

def is_valid_email(email):
    """This function checks if the email is valid."""
    pattern = r'^[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+$'
    return re.match(pattern, email) is not None

print(is_valid_email("test@example.com"))  # Output: True
print(is_valid_email("invalid-email"))     # Output: False
```

- **Explanation**: 
  - Uses a regular expression pattern to match a valid email format.
  - `re.match()` returns `None` if no match is found, so the function checks if it returns a match to verify the email.

---
Sure! Here’s a combined explanation of the `is_valid_email` function along with the details about `if not`, `elif`, and `any()`:

---

### **Understanding Functions and Email Validation in Python**

#### **1. Functions Overview**
- A **function** is a block of code that performs a specific task. Functions help in organizing code, reusing code, and improving readability.

#### **Basic Structure of a Function:**
```python
def function_name(parameters):
    """Docstring explaining the function."""
    # Function body
    return expression
```

### **Example: Email Validation Function**
Here's a function that checks if an email address is valid:

```python
import re

def is_valid_email(email):
    """This function checks if the email is valid."""
    pattern = r'^[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+$'
    return re.match(pattern, email) is not None

# Test the function
print(is_valid_email("test@example.com"))  # Output: True
print(is_valid_email("invalid-email"))     # Output: False
```

#### **Step-by-Step Explanation:**

1. **Importing the `re` Module:**
   - The `re` module supports regular expressions (regex), which allows searching for patterns in text.

2. **Defining the `is_valid_email` Function:**
   - The function takes an `email` as input and checks if it follows the correct format.

3. **Pattern Explanation:**
   - The `pattern` is a regex that defines the rules for a valid email:
     - **`^`**: Starts at the beginning of the string.
     - **`[a-zA-Z0-9_.+-]+`**: Matches username characters.
     - **`@`**: The separator between username and domain.
     - **`[a-zA-Z0-9-]+`**: Matches the domain name.
     - **`\.`**: Matches the dot before the extension.
     - **`[a-zA-Z0-9-.]+`**: Matches the domain extension.
     - **`$`**: Ends at the end of the string.

4. **Matching the Email with the Pattern:**
   - The function uses `re.match(pattern, email)` to check if the email fits the pattern.
   - If it matches, it returns a match object; if not, it returns `None`.

5. **Returning the Result:**
   - The expression `re.match(pattern, email) is not None` checks if there's a match.
   - Returns `True` for a valid email, `False` for an invalid one.

#### **Examples of Function Use:**
- **Valid Email:**
  ```python
  print(is_valid_email("test@example.com"))  # Output: True
  ```
- **Invalid Email:**
  ```python
  print(is_valid_email("invalid-email"))     # Output: False
  ```

#### Focus on the Section: `@[a-zA-Z0-9-]+`
- **`[a-zA-Z0-9-]`**: This character class allows the following characters:
  - **`a-z`**: Lowercase letters from **a** to **z**.
  - **`A-Z`**: Uppercase letters from **A** to **Z**.
  - **`0-9`**: Digits from **0** to **9**.
  - **`-`**: The hyphen character (`-`).

### **Why Include the Hyphen `-`?**
- The hyphen (`-`) is commonly used in domain names. For example:
  - `example-domain.com`
  - `my-site.org`
- Therefore, including `-` in the pattern allows the function to match valid domain names that contain hyphens.
---
### **2. Control Structures in Python**

#### **`if not` vs. `elif`:**
- **`if not`:** Used to negate a condition. Checks if a condition is **False**.
  ```python
  if not x > 20:
      print("x is not greater than 20")
  ```

- **`elif`:** Allows checking multiple conditions in sequence. Used in decision-making chains.
  ```python
  if x > 20:
      print("x is greater than 20")
  elif x == 10:
      print("x is equal to 10")
  ```

#### **Key Difference:**
- `if not` negates a condition; `elif` adds more conditions in a chain.

---

### **3. The `any()` Function**
- **`any()`** checks if **any** element in an iterable is **True**. Returns **True** if at least one element is **True**; otherwise, returns **False**.

#### Example:
```python
my_list = [0, 0, 1, 0]
print(any(my_list))  # Output: True
```
- Here, `any(my_list)` returns `True` because `1` is a **True** value.

### Summary
- The `is_valid_email` function uses regex to validate email formats, returning `True` for valid emails and `False` for invalid ones.
- `if not` is for checking negated conditions, while `elif` allows checking multiple conditions.
- `any()` helps to verify if any elements in a collection are **True**.

--- 

### **1. Lambda Functions Overview**

- **Lambda functions** are small, anonymous functions defined using the `lambda` keyword.
- They can take any number of arguments, but they are limited to **only one expression**.
- Lambda functions are often used for short operations or passed as arguments to other functions.

#### **Syntax:**
```python
lambda arguments: expression
```

### **2. Example: Regular Function vs Lambda Function**

#### **Regular Function:**
```python
def addition(a, b):
    return a + b

print(addition(2, 3))  # Output: 5
```
- A regular function `addition` takes two arguments and returns their sum.

#### **Lambda Function:**
```python
addition = lambda a, b: a + b
print(addition(5, 6))  # Output: 11
```
- The same function using **lambda**: `lambda a, b: a + b` performs the same addition but in a more concise way.
- **Type:** Lambda functions are still function objects, just written differently.

---

### **3. Lambda for Even Number Check**

#### **Regular Function:**
```python
def even(num):
    if num % 2 == 0:
        return True

print(even(24))  # Output: True
```
- This function checks if a number is even by returning `True` if it is divisible by 2.

#### **Lambda Equivalent:**
```python
even1 = lambda num: num % 2 == 0
print(even1(12))  # Output: True
```
- Using `lambda`, we achieve the same result in a single line.

---

### **4. Lambda for Multiple Arguments**

#### **Regular Function:**
```python
def addition(x, y, z):
    return x + y + z

print(addition(12, 13, 14))  # Output: 39
```
- A function that adds three numbers.

#### **Lambda Equivalent:**
```python
addition1 = lambda x, y, z: x + y + z
print(addition1(12, 13, 14))  # Output: 39
```
- The lambda version achieves the same with fewer lines of code.

---

### **5. Using `map()` with Lambda Functions**

- **`map()`** applies a function to each item in a list (or any iterable).

#### **Example with Regular Function:**
```python
def square(number):
    return number ** 2

numbers = [1, 2, 3, 4, 5, 6]
squared_numbers = list(map(square, numbers))
print(squared_numbers)  # Output: [1, 4, 9, 16, 25, 36]
```
- The `square` function squares each number in the list.

#### **Example with Lambda Function:**
```python
numbers = [1, 2, 3, 4, 5, 6]
squared_numbers = list(map(lambda x: x ** 2, numbers))
print(squared_numbers)  # Output: [1, 4, 9, 16, 25, 36]
```
- With `lambda`, we define the square operation directly within `map()`.

---
Lambda functions are often used in Python when you need a **short, simple function** for a **one-time use** or for passing to other functions. Here's where and why they are commonly used:

### **1. Using Lambda with `map()`**

- **Why:** To apply a function to every item in a list without having to define a separate function.
- **How:** You can use a lambda function directly inside `map()`.

#### Example:
```python
numbers = [1, 2, 3, 4]
squared_numbers = list(map(lambda x: x ** 2, numbers))
print(squared_numbers)  # Output: [1, 4, 9, 16]
```
- **Explanation:** We used `lambda` to square each number in the list without creating a separate function.

---

### **2. Using Lambda with `filter()`**

- **Why:** To filter out items in a list that meet a certain condition.
- **How:** `filter()` takes a function and a list, returning only the items that satisfy the condition.

#### Example:
```python
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers)  # Output: [2, 4, 6]
```
- **Explanation:** The `lambda` function filters the list, returning only even numbers.

---

### **3. Using Lambda with `sorted()` and `key` Parameter**

- **Why:** To sort complex data like tuples, dictionaries, or lists based on a custom key.
- **How:** You can pass a lambda function to the `key` parameter to define custom sorting behavior.

#### Example:
```python
students = [("Mohamed", 21), ("Assaf", 20), ("Krishna", 22)]
students_sorted = sorted(students, key=lambda x: x[1])
print(students_sorted)  # Output: [('Assaf', 20), ('Mohamed', 21), ('Krishna', 22)]
```
- **Explanation:** We sorted the list of students by their age using `lambda x: x[1]` to specify that sorting should be based on the second item (age) in each tuple.

---

### **4. Using Lambda with `reduce()` (from `functools`)**

- **Why:** To apply a rolling calculation to the elements of a list, like finding the sum or product.
- **How:** `reduce()` combines elements of a list into a single result based on a function.

#### Example:
```python
from functools import reduce

numbers = [1, 2, 3, 4]
product = reduce(lambda x, y: x * y, numbers)
print(product)  # Output: 24
```
- **Explanation:** The `lambda` function multiplies elements in the list, producing the product.

---

### **5. Using Lambda in Data Structures (like dictionaries)**

- **Why:** When you need to store small, quick functions in a data structure like a dictionary.
- **How:** Lambda functions can be used as values in dictionaries to create dynamic behavior.

#### Example:
```python
operations = {
    "add": lambda a, b: a + b,
    "subtract": lambda a, b: a - b
}

print(operations["add"](5, 3))        # Output: 8
print(operations["subtract"](5, 3))   # Output: 2
```
- **Explanation:** We used lambda functions in a dictionary to perform different operations based on the keys.

---

### **Why Use Lambda Functions?**
- **Conciseness:** Lambda functions allow you to write quick, small functions in a single line.
- **Anonymous:** They don’t require a name, making them perfect for **one-time use**.
- **Functional Programming:** They work well with functions like `map()`, `filter()`, and `reduce()`, which are common in functional programming.

### **Summary:**
- **Lambda functions** provide a shorter syntax for defining simple functions.
- They are useful when you need a function for a quick operation or to pass as an argument to other functions like `map()`.
- You can use lambda functions in place of regular functions when the task is simple and doesn’t require multiple lines of code.
### `map()` Function in Python - Simplified Explanation

The `map()` function is used to apply a function to each item in a list (or any iterable) and return the result as a new list (or an iterator). It is useful when you want to apply the same operation to all elements in a collection without writing a loop.

---

### **Basic Example**
```python
def square(x):
    return x * x

numbers = [1, 2, 3, 4, 5, 6, 7, 8]
squared_numbers = list(map(square, numbers))
print(squared_numbers)
```
**Output:**  
`[1, 4, 9, 16, 25, 36, 49, 64]`

- **Explanation:**  
  The `map()` function applies the `square()` function to every item in the `numbers` list. Each number is squared, and the result is returned in a new list.

---

### **Using `lambda` with `map()`**
You can replace the `square()` function with a **lambda function** to make the code more concise.

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8]
squared_numbers = list(map(lambda x: x * x, numbers))
print(squared_numbers)
```
**Output:**  
`[1, 4, 9, 16, 25, 36, 49, 64]`

- **Explanation:**  
  The lambda function (`lambda x: x * x`) does the same thing as the `square()` function but in a shorter form.

---

### **`map()` with Multiple Iterables**
You can pass more than one iterable (like lists) to `map()` if the function takes multiple arguments.

```python
numbers1 = [1, 2, 3]
numbers2 = [4, 5, 6]

added_numbers = list(map(lambda x, y: x + y, numbers1, numbers2))
print(added_numbers)
```
**Output:**  
`[5, 7, 9]`

- **Explanation:**  
  The lambda function adds the corresponding elements from `numbers1` and `numbers2`. So, `1 + 4 = 5`, `2 + 5 = 7`, and so on.

---

### **Converting Data Types with `map()`**
You can use `map()` to transform data types in a list, such as converting a list of strings to integers.

```python
str_numbers = ['1', '2', '3', '4', '5']
int_numbers = list(map(int, str_numbers))
print(int_numbers)
```
**Output:**  
`[1, 2, 3, 4, 5]`

- **Explanation:**  
  Here, `map(int, str_numbers)` converts each string in the list to an integer.

---

### **Changing Case of Strings Using `map()`**
You can use `map()` to apply string methods like `.upper()` to all elements in a list of strings.

```python
words = ['apple', 'banana', 'cherry']
upper_words = list(map(str.upper, words))
print(upper_words)
```
**Output:**  
`['APPLE', 'BANANA', 'CHERRY']`

- **Explanation:**  
  The `str.upper` method is applied to each word, converting them to uppercase.

---

### **Extracting Data from Lists of Dictionaries**
You can use `map()` to extract specific values from a list of dictionaries.

```python
def get_name(person):
    return person['name']

people = [
    {'name': 'Assaf', 'age': 21},
    {'name': 'Aysha', 'age': 19}
]

names = list(map(get_name, people))
print(names)
```
**Output:**  
`['Assaf', 'Aysha']`

- **Explanation:**  
  The `get_name()` function is applied to each dictionary, extracting the `'name'` field.

---

### **Conclusion**
The `map()` function is a powerful tool for applying a function to all items in an iterable. It is often used for:
- **Transforming** data (like squaring numbers or converting case).
- **Combining** multiple iterables (like adding two lists element-wise).
- **Converting** data types (like turning strings into integers).

It's a cleaner and more efficient way to apply operations to collections compared to using loops.

---
### The `filter()` Function in Python - Simplified Explanation

The `filter()` function is used to filter out items from a list (or any other iterable) based on a condition. It creates a new list containing only those elements that return **True** when passed through a filtering function.

---

### **Basic Example of `filter()`**
```python
def even(num):
    if num % 2 == 0:
        return True

lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]
filtered_lst = list(filter(even, lst))
print(filtered_lst)
```
**Output:**  
`[2, 4, 6, 8, 10, 12]`

- **Explanation:**  
  The `even()` function checks if a number is even. The `filter()` function applies this check to each number in `lst`, and only the even numbers are included in the final result.

---

### **Using `filter()` with a Lambda Function**
You can use a **lambda function** to write the filtering condition more concisely.

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
greater_than_five = list(filter(lambda x: x > 5, numbers))
print(greater_than_five)
```
**Output:**  
`[6, 7, 8, 9]`

- **Explanation:**  
  The lambda function (`lambda x: x > 5`) checks if the number is greater than 5. The `filter()` function keeps only those numbers that satisfy this condition.

---

### **Filter with Multiple Conditions**
You can combine multiple conditions in the lambda function for more complex filtering.

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
even_and_greater_than_five = list(filter(lambda x: x > 5 and x % 2 == 0, numbers))
print(even_and_greater_than_five)
```
**Output:**  
`[6, 8]`

- **Explanation:**  
  The lambda function checks two conditions: the number should be greater than 5 **and** even (`x % 2 == 0`). Only numbers that satisfy both conditions are included in the result.

---

### **Filter with Dictionaries**
You can use `filter()` to filter elements in a list of dictionaries. For example, checking if the age is greater than 25 in a list of people.

```python
people = [
    {'name': 'Nisha', 'age': 43}, 
    {'name': 'Ibrahim', 'age': 55}, 
    {'name': 'Assaf', 'age': 21}
]

def age_greater_than_25(person):
    return person['age'] > 25

filtered_people = list(filter(age_greater_than_25, people))
print(filtered_people)
```
**Output:**  
`[{'name': 'Nisha', 'age': 43}, {'name': 'Ibrahim', 'age': 55}]`

- **Explanation:**  
  The `age_greater_than_25()` function checks if a person's age is more than 25. The `filter()` function keeps only those people whose age is greater than 25.

---

### **Conclusion**
- The `filter()` function allows you to filter out items from a list (or any iterable) based on a **condition**.
- You can use **regular functions** or **lambda functions** as the filtering criteria.
- It is useful for selecting specific elements from a collection based on certain conditions.
---
## Modules in Python

**Modules** and **packages** in Python help organize code into separate files and folders, making it easier to reuse and manage. When you import a module or a package, you bring in pre-written code to use in your program.

---

### **What is a Module?**
A **module** is simply a Python file that contains definitions (like functions, classes, or variables) that you can use in other Python programs.

### **What is a Package?**
A **package** is a collection of modules organized in directories. Packages make it easy to manage large projects.

---

### **1. Basic Import**

```python
import math
print(math.sqrt(16))  # Output: 4.0
```

- **Explanation:**  
  The `math` module is imported, and you can now use its functions like `sqrt()` to find the square root.

---

### **2. Importing Specific Functions**

```python
from math import sqrt, pi
print(sqrt(16))  # Output: 4.0
print(sqrt(25))  # Output: 5.0
print(pi)        # Output: 3.141592653589793
```

- **Explanation:**  
  This imports only the `sqrt` function and `pi` constant from the `math` module. You don't need to write `math.sqrt()`, just `sqrt()`.

---

### **3. Importing External Libraries (like `numpy`)**

```python
import numpy as np
arr = np.array([1, 2, 3, 4])
print(arr)  # Output: [1 2 3 4]
```

- **Explanation:**  
  External libraries like **NumPy** can be imported to work with specialized functions. `np` is an alias to make calling the library shorter.

---

### **4. Importing All Functions**

```python
from math import *
print(sqrt(16))  # Output: 4.0
print(pi)        # Output: 3.141592653589793
```

- **Explanation:**  
  `from math import *` imports all the functions and constants from the `math` module, allowing you to use them directly without prefixing them with `math.`.

---

### **5. Importing from a Package**

If you have custom modules in a package (a folder), you can import functions from them like this:

```python
from package.maths import addition
print(addition(2, 3))  # Output: 5
```

OR

```python
from package import maths
print(maths.addition(2, 3))  # Output: 5
```

- **Explanation:**  
  In the first example, you import just the `addition` function from the `maths` module inside the `package`.  
  In the second example, you import the entire `maths` module from the `package` and then call the function.

---

### **Adding More Topics:**

#### **6. Using Aliases for Modules**
You can give a module a short alias to make it easier to call:

```python
import math as m
print(m.sqrt(16))  # Output: 4.0
```

- **Explanation:**  
  This renames the `math` module as `m`, so you can use `m.sqrt()` instead of `math.sqrt()`.

---

#### **7. Importing Custom Modules**
You can create your own Python file (e.g., `my_module.py`) and import it into another file.

```python
# my_module.py
def greet(name):
    return f"Hello, {name}!"

# main.py
import my_module
print(my_module.greet("Assaf"))  # Output: Hello, Assaf!
```

---

#### **8. Relative Imports**
When working within a package, you can use **relative imports** to import modules that are in the same package or sub-packages.

```python
from .module import function_name
```

- **Explanation:**  
  `.` represents the current directory, and `..` represents the parent directory. This is useful when your project has many subfolders.

---

### **Conclusion:**
- **Modules** and **packages** in Python help you **organize and reuse code** effectively.
- You can import an entire module, specific functions, or everything using `import`, `from ... import`, or `from ... import *`.
- Using modules allows you to keep your code clean, structured, and easy to maintain.
---
### **Python's Standard Library Overview – Simplified**

The **Python Standard Library** is a huge collection of pre-built modules and packages that provide a wide range of functionalities without requiring external libraries. These modules allow you to perform tasks like file handling, math operations, random number generation, and more, straight out of the box.

---

### **1. `array` Module**
The `array` module provides a way to create an array (similar to lists but with fixed types, like all integers or all floats).

```python
import array
arr = array.array('i', [1, 2, 3, 4])
print(arr)
# Output: array('i', [1, 2, 3, 4])
```

- **Explanation:**  
  This creates an array of integers (`'i'` stands for integers) and prints it.

---

### **2. `math` Module**
The `math` module contains mathematical functions like square root, constants like `pi`, etc.

```python
import math
print(math.sqrt(16))  # Output: 4.0
print(math.pi)        # Output: 3.141592653589793
```

- **Explanation:**  
  `sqrt(16)` gives the square root of 16, and `pi` returns the value of Pi.

---

### **3. `random` Module**
The `random` module is used for generating random numbers and making random selections.

```python
import random
print(random.randint(1, 10))                      # Output: Random integer between 1 and 10
print(random.choice(['apple', 'banana', 'cherry']))  # Output: Randomly selects one from the list
```

- **Explanation:**  
  `randint(1, 10)` gives a random integer between 1 and 10, and `choice()` randomly picks one element from the given list.

---

### **4. File and Directory Access with `os` Module**
The `os` module provides functions to interact with the operating system, such as accessing directories.

```python
import os
print(os.getcwd())  # Output: Current working directory
os.mkdir('test_dir')  # Creates a new directory named 'test_dir'
```

- **Explanation:**  
  `os.getcwd()` gets the current directory, and `os.mkdir()` creates a new directory.

---

### **5. File Operations with `shutil` Module**
The `shutil` module allows for high-level file operations like copying files.

```python
import shutil
shutil.copyfile('source.txt', 'destination.txt')
# Output: 'destination.txt' is created as a copy of 'source.txt'
```

- **Explanation:**  
  This copies the content of `source.txt` into `destination.txt`.

---

### **6. Data Serialization with `json` Module**
The `json` module helps convert Python objects (like dictionaries) into JSON strings and vice versa.

```python
import json
data = {'name': 'Assaf', 'age': 21}

json_str = json.dumps(data)  # Convert to JSON string
print(json_str)              # Output: '{"name": "Assaf", "age": 21}'

parsed_data = json.loads(json_str)  # Convert back to Python dict
print(parsed_data)                  # Output: {'name': 'Assaf', 'age': 21}
```

- **Explanation:**  
  `json.dumps()` converts a dictionary to a JSON string, and `json.loads()` converts the JSON string back to a dictionary.

---

### **7. Working with CSV Files**
The `csv` module is used to read from and write to CSV (Comma Separated Values) files.

```python
import csv

# Writing to a CSV file
with open('example.csv', mode='w', newline='') as file:
    writer = csv.writer(file)
    writer.writerow(['name', 'age'])
    writer.writerow(['Assaf', 21])

# Reading from a CSV file
with open('example.csv', mode='r') as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
# Output: ['name', 'age'], ['Assaf', '21']
```

- **Explanation:**  
  This shows how to write rows to a CSV file and then read them back.

---

### **8. `datetime` Module**
The `datetime` module is used for manipulating dates and times.

```python
from datetime import datetime, timedelta

now = datetime.now()  # Get current date and time
print(now)

yesterday = now - timedelta(days=1)  # Subtract 1 day
print(yesterday)
```

- **Explanation:**  
  `datetime.now()` gives the current date and time, and `timedelta(days=1)` subtracts a day from the current date.

---

### **9. `time` Module**
The `time` module allows you to work with time-related functions, like pausing the program for a few seconds.

```python
import time
print(time.time())   # Output: Current time in seconds since epoch
time.sleep(2)        # Pauses for 2 seconds
print(time.time())
```

- **Explanation:**  
  `time.time()` returns the current time in seconds, and `time.sleep()` pauses the program for the specified number of seconds.

---

### **10. Regular Expressions with `re` Module**
The `re` module is used to work with regular expressions for pattern matching.

```python
import re

pattern = r'\d+'  # Regular expression to find digits
text = 'There are 123 apples 456'
match = re.search(pattern, text)
print(match.group())  # Output: 123
```

- **Explanation:**  
  The pattern `\d+` looks for one or more digits, and `re.search()` finds the first match in the text.
In the regular expression `\d+`, the `+` symbol is called a **quantifier**. It means "one or more" of the preceding element.

- `\d` represents any digit (0–9).
- `+` means "one or more of the preceding element."

So, together `\d+` means "one or more digits."

For example:
- In the text "There are 123 apples 456", `\d+` would match `123` and `456` because both are sequences of digits.

---

### **Conclusion**
Python's Standard Library contains a wide range of modules that make programming easier. Whether it's working with files, handling data formats like JSON and CSV, manipulating dates and times, or using advanced math and random functions, Python’s Standard Library has you covered! Understanding and using these modules helps you write efficient, clean, and powerful Python programs.

## File Operation:

### 1. **Read a Whole File**
```python
with open('example.txt', 'r') as file:
    content = file.read()
    print(content)
```
- Opens `example.txt` in read mode (`'r'`), reads all its content, and prints it.
- Output: 
  ```
  Hello How are you?
  I am good
  Krish is my name
  Welcome to the course
  ```

### 2. **Read a File Line by Line**
```python
with open('example.txt', 'r') as file:
    for line in file:
        print(line.strip())
```
- Opens the file and reads it line by line. 
- `.strip()` removes extra newline characters at the end of each line.
- Output (each line printed without extra spaces):
  ```
  Hello How are you?
  I am good
  Krish is my name
  Welcome to the course
  ```

### 3. **Writing to a File (Overwriting)**
```python
with open('example.txt', 'w') as file:
    file.write('Hello World!\n')
    file.write('This is a new line.')
```
- Opens `example.txt` in write mode (`'w'`), which overwrites the file.
- Writes two lines of text to the file: `Hello World!` and `This is a new line.`

### 4. **Appending to a File (Without Overwriting)**
```python
with open('example.txt', 'a') as file:
    file.write("Append operation taking place!\n")
```
- Opens the file in append mode (`'a'`) and adds `"Append operation taking place!\n"` to the end without overwriting existing content.

### 5. **Writing a List of Lines to a File**
```python
lines = ['First line \n', 'Second line \n', 'Third line\n']
with open('example.txt', 'a') as file:
    file.writelines(lines)
```
- Appends multiple lines to the file at once using `writelines()`.

### 6. **Binary Files**
- **Writing Binary Data:**
  ```python
  data = b'\x00\x01\x02\x03\x04'
  with open('example.bin', 'wb') as file:
      file.write(data)
  ```
  - Writes binary data (`b'\x00\x01\x02\x03\x04'`) to a file.
  
- **Reading Binary Data:**
  ```python
  with open('example.bin', 'rb') as file:
      content = file.read()
      print(content)
  ```
  - Reads the binary data from the file and prints it.
  - Output: `b'\x00\x01\x02\x03\x04'`

### 7. **Copying Content from One File to Another**
```python
with open('example.txt', 'r') as source_file:
    content = source_file.read()

with open('destination.txt', 'w') as destination_file:
    destination_file.write(content)
```
- Reads content from `example.txt` and writes it to `destination.txt`.

### 8. **Counting Lines, Words, and Characters in a Text File**
```python
def count_text_file(file_path):
    with open(file_path, 'r') as file:
        lines = file.readlines()
        line_count = len(lines)
        word_count = sum(len(line.split()) for line in lines)
        char_count = sum(len(line) for line in lines)
    return line_count, word_count, char_count

file_path = 'example.txt'
lines, words, characters = count_text_file(file_path)
print(f'Lines: {lines}, Words: {words}, Characters: {characters}')
```
- This function reads the file and counts the number of lines, words, and characters.
- Example output: `Lines: 4, Words: 11, Characters: 63`

### 9. **Writing and Reading a File Using `w+` Mode**
```python
with open('example.txt', 'w+') as file:
    file.write("Hello world\n")
    file.write("This is a new line \n")

    file.seek(0)  # Move cursor to the start of the file
    content = file.read()
    print(content)
```
- Opens the file for both writing and reading (`'w+'` mode), writes content, then moves the cursor to the beginning using `seek(0)` to read the content back.
- Output:
  ```
  Hello world
  This is a new line
  ```
  ---
### Working with File Paths

Handling file paths properly ensures your code is compatible across different operating systems. Python's `os` module helps you manage file paths effectively.

#### 1. **Getting the Current Working Directory**
```python
import os
cwd = os.getcwd()
print(f"Current working directory is {cwd}")
```
- **What It Does:** This retrieves the current working directory (the folder where your script is running) and prints it.

#### 2. **Creating a New Directory**
```python
new_directory = "package"
os.mkdir(new_directory)
print(f"Directory '{new_directory}' created")
```
- **What It Does:** This creates a new directory named "package" in the current working directory and confirms its creation.

#### 3. **Listing Files and Directories**
```python
items = os.listdir('.')
print(items)
```
- **What It Does:** This lists all files and directories in the current directory (`.`) and prints them.

#### 4. **Joining Paths**
```python
dir_name = "folder"
file_name = "file.txt"
full_path = os.path.join(dir_name, file_name)
print(full_path)
```
- **What It Does:** This combines `dir_name` and `file_name` into a complete file path (e.g., `folder\file.txt`).

```python
full_path = os.path.join(os.getcwd(), dir_name, file_name)
print(full_path)
```
- **What It Does:** This creates a full path by joining the current working directory with the `dir_name` and `file_name`, resulting in something like `e:\UDemy Final\python\6-File Handling\folder\file.txt`.

#### 5. **Checking if a Path Exists**
```python
path = 'example1.txt'
if os.path.exists(path):
    print(f"The path '{path}' exists")
else:
    print(f"The path '{path}' does not exist")
```
- **What It Does:** This checks whether the specified path (`example1.txt`) exists and prints the result.

#### 6. **Checking if a Path is a File or Directory**
```python
path = 'example.txt'
if os.path.isfile(path):
    print(f"The path '{path}' is a file.")
elif os.path.isdir(path):
    print(f"The path '{path}' is a directory.")
else:
    print(f"The path '{path}' is neither a file nor a directory.")
```
- **What It Does:** This checks if the given path is a file or a directory and prints the result.

#### 7. **Getting the Absolute Path**
```python
relative_path = 'example.txt'
absolute_path = os.path.abspath(relative_path)
print(absolute_path)
```
- **What It Does:** This converts a relative path (`example.txt`) to an absolute path and prints it, providing the full path from the root of the filesystem.

### Summary
Using the `os` module, you can effectively manage file paths by getting the current working directory, creating directories, listing files, checking path existence, and getting absolute paths. This ensures your code runs smoothly across different environments.

---
---
## Exception Handling:
### What Are Exceptions?
Exceptions are errors that occur during the execution of a program and disrupt its flow. Instead of the program crashing, Python provides a way to handle these exceptions gracefully.

### Try and Except Block
This block helps catch exceptions that occur in the `try` part of the code. If an exception happens, the `except` block is executed.

#### Example:
```python
try:
    a = b
except:
    print("The variable has not been assigned")
```
In this case, a `NameError` occurs because `b` is not defined. Without the `except` block, this would cause the program to crash, but with the block, the error is caught, and the message is printed.

#### Improved Version:
You can catch specific exceptions by naming them:
```python
try:
    a = b
except NameError as ex:
    print(ex)
```
This way, it specifically catches a `NameError` and prints the exact error message.

### Catching Multiple Exceptions
You can handle different types of exceptions with multiple `except` blocks.
```python
try:
    result = 1 / num
    a = b
except ZeroDivisionError as ex:
    print(ex)
    print("Please enter a denominator greater than 0")
except Exception as ex1:
    print(ex1)
    print("Main exception got caught here")
```
Here, if `num` is zero, the `ZeroDivisionError` is caught. If there's any other error (like `b` not being defined), it's caught by the general `Exception` block.

### Try, Except, and Else Block
The `else` block runs only if no exceptions are raised.
```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
except ValueError:
    print("That's not a valid number!")
except ZeroDivisionError:
    print("You can't divide by zero!")
else:
    print(f"The result is {result}")
```
If no exception occurs, the code in the `else` block runs, which prints the result.

### Finally Block
The `finally` block runs no matter what happens (whether an exception is raised or not). It’s typically used for cleanup actions, like closing a file or releasing resources.
```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
except ValueError:
    print("That's not a valid number!")
except ZeroDivisionError:
    print("You can't divide by zero!")
else:
    print(f"The result is {result}")
finally:
    print("Execution complete.")
```
Even if an error occurs, the message "Execution complete" is always printed.

### Exception Handling in File Operations
When dealing with files, exceptions like `FileNotFoundError` are common, and it's important to close the file whether an exception occurs or not.
```python
try:
    file = open('example1.txt', 'r')
    content = file.read()
    a = b  # This will raise an exception
    print(content)
except FileNotFoundError:
    print("The file does not exist")
except Exception as ex:
    print(ex)
finally:
    if 'file' in locals() or not file.closed:
        file.close()
        print('File closed')
```
The `finally` block ensures the file is closed even if an error occurs while reading the file or if some other error like `NameError` is raised.

### Missing Piece: Raising Exceptions
You can also manually raise exceptions in your code using the `raise` keyword. This can be helpful if you want to ensure certain conditions are met.
```python
def divide(a, b):
    if b == 0:
        raise ZeroDivisionError("b cannot be zero!")
    return a / b
```

This covers all the important parts of exception handling:
1. `try` and `except` blocks for catching exceptions.
2. Specific exceptions like `ZeroDivisionError`, `NameError`, etc.
3. `else` block for code to execute when no exception occurs.
4. `finally` block for cleanup, no matter what happens.
5. Raising exceptions manually.

This should give you a complete picture of how to handle exceptions in Python.
### raise :
 When you use `raise` to manually raise an exception, it stops the program and throws the error, just like a built-in exception would. This is because the purpose of `raise` is to signal that an exceptional condition has occurred and should be handled.

To handle this error without stopping the program, you need to wrap the call to `divide()` in a `try` block, and catch the `ZeroDivisionError` in an `except` block.

Here’s how you can do it:

```python
def divide(a, b):
    if b == 0:
        raise ZeroDivisionError("b cannot be zero!")
    return a / b

try:
    print(divide(5, 0))
except ZeroDivisionError as ex:
    print(ex)
```

### Output:
```
b cannot be zero!
```

Now, instead of the program crashing, the exception is caught, and the message `"b cannot be zero!"` is printed.

In summary:
- Without `try-except`, the program stops when an exception is raised.
- With `try-except`, you can handle the exception and continue running the program.
### Pass:
In Python, the `pass` statement is used as a placeholder in code where a statement is syntactically required, but no action needs to be taken. It allows you to define functions, loops, classes, or conditionals without adding any functionality at that moment.

### Why and When to Use `pass`:
1. **As a Placeholder for Incomplete Code**:
   When you're working on a project and want to structure your code without implementing all the details yet, you can use `pass` to avoid syntax errors. It helps you write the skeleton of your code while focusing on other parts.

   Example:
   ```python
   def my_function():
       pass  # Placeholder until you implement the function
   ```

2. **In Empty Classes**:
   If you want to define a class but don’t want to add attributes or methods at the moment, you can use `pass`.

   Example:
   ```python
   class Car:
       pass  # Placeholder for later implementation
   ```

3. **In Empty Loops**:
   If you’re creating a loop, but you don’t want it to do anything for now, you can use `pass` to avoid errors.

   Example:
   ```python
   for i in range(5):
       pass  # Do nothing for now
   ```

4. **In Conditionals**:
   If you're writing an `if` statement and don’t need to take any action when the condition is met (or not met), `pass` allows you to skip adding functionality without breaking the code.

   Example:
   ```python
   x = 10
   if x > 5:
       pass  # No action needed if x > 5
   else:
       print("x is less than or equal to 5")
   ```

### Why Not Just Leave It Blank?
In Python, leaving certain blocks (like class definitions or function bodies) empty will cause a syntax error. The `pass` statement tells Python, “Do nothing here, but this block is intentionally left empty,” preventing the error.

### Summary:
- **Purpose**: The `pass` statement is used when you need to define the structure of your code but haven't implemented it yet.
- **When to use**: In empty classes, functions, loops, conditionals, or any block where you plan to add functionality later.

---
## Class and Object:
## **Classes and Objects in Python**

Object-Oriented Programming (OOP) is a programming paradigm that uses classes and objects to design applications and represent real-world scenarios. In Python, a **class** is a blueprint for creating objects, and an **object** is an instance of that class.

### **1. What is a Class?**
A class defines the structure and behavior (data and methods) that its objects will have. Classes typically contain:
- **Attributes**: Variables that hold data related to the object (instance variables).
- **Methods**: Functions that define the behavior of the object.

Example:
```python
class Car:
    pass  # A class with no attributes or methods for now
```

In this example, `Car` is a class with no functionality yet (we use `pass` as a placeholder when we haven't implemented any logic).

### **2. What is `pass` in Python?**
`pass` is a special statement used in Python when a statement is syntactically required but no action is needed. It is useful when you're defining classes, functions, or loops but don't want to implement their logic just yet.

Example:
```python
class Car:
    pass  # Placeholder for future attributes and methods
```

### **3. Creating Objects from a Class**
Objects are instances of a class. You create an object by calling the class as if it were a function.

Example:
```python
audi = Car()  # Creating an object of class Car
bmw = Car()

print(type(audi))  # Output: <class '__main__.Car'>
```

Here, `audi` and `bmw` are two different objects (instances) of the `Car` class.

### **4. Instance Variables and Methods**
Instance variables are data unique to each object, and methods are functions that belong to the class. 

#### **4.1 Constructor and Instance Variables**
A **constructor** (`__init__`) is a special method that initializes the object with attributes. It is automatically called when an object is created.

Example:
```python
class Dog:
    def __init__(self, name, age):
        self.name = name  # Instance variable
        self.age = age    # Instance variable

# Creating objects
dog1 = Dog("Buddy", 3)
dog2 = Dog("Lucy", 4)

print(dog1.name)  # Output: Buddy
print(dog2.age)   # Output: 4
```

#### **4.2 What is `self`?**
`self` is a reference to the current instance of the class. It is used to access the instance variables and methods of the object. It must be the first parameter of instance methods, but it is not passed when the method is called — Python does this automatically.

Example:
```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def bark(self):
        print(f"{self.name} says woof!")  # Accessing instance variable using self

dog1 = Dog("Buddy", 3)
dog1.bark()  # Output: Buddy says woof!
```

Here, `self.name` refers to the specific instance (`dog1`), allowing the method to access the `name` attribute of that object. `self` enables each object to keep track of its own data.

### **5. Defining Instance Methods**
Instance methods operate on data contained within an object and typically have `self` as their first parameter.

Example:
```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def bark(self):
        print(f"{self.name} says woof!")

dog1 = Dog("Buddy", 3)
dog1.bark()  # Output: Buddy says woof!
```

### **6. Example: Modeling a Bank Account**

Here’s a practical example of how classes, objects, and methods can model real-world scenarios like a bank account:

```python
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.balance = balance

    def deposit(self, amount):
        self.balance += amount
        print(f"{amount} is deposited. New balance is {self.balance}")

    def withdraw(self, amount):
        if amount > self.balance:
            print("Insufficient funds!")
        else:
            self.balance -= amount
            print(f"{amount} is withdrawn. New Balance is {self.balance}")

    def get_balance(self):
        return self.balance
    
# Create an account object
account = BankAccount("Mohamed Assaf", 5000)
account.deposit(100)  # Output: 100 is deposited. New balance is 5100
account.withdraw(300)  # Output: 300 is withdrawn. New Balance is 4800
```

### **7. Error: Attribute Not Found**
When accessing instance variables, if you try to access an attribute that wasn’t assigned to an object, Python raises an `AttributeError`.

Example:
```python
tata = Car()
tata.doors = 4
print(tata.windows)  # This will raise an AttributeError since `windows` was never defined for `tata`.
```

### **Conclusion**
Object-Oriented Programming in Python allows you to model real-world entities using classes and objects. In this lesson, we covered:
- Creating classes and objects.
- Using `self` to refer to the current instance.
- Defining and using instance variables and methods.
- Handling real-world scenarios using OOP principles.

By understanding these concepts, you can write more organized, reusable, and maintainable Python code!

--- 
### **Inheritance in Python**

Inheritance is a key concept in Object-Oriented Programming (OOP) that allows a class to inherit attributes and methods from another class. This enables code reuse, modular design, and allows us to build complex systems based on simpler ones. In Python, there are two main types of inheritance:
1. **Single Inheritance**: One class inherits from one parent class.
2. **Multiple Inheritance**: A class can inherit from more than one base class.

This explanation will cover both **single inheritance** and **multiple inheritance**, using the code you provided and expanding on missing topics.

---

### **1. Single Inheritance**

In **single inheritance**, a child class (also called a derived class or subclass) inherits from a single parent class (also called a base class). This allows the child class to reuse the attributes and methods of the parent class.

#### **Example:**

```python
## Parent class
class Car:
    def __init__(self, windows, doors, enginetype):
        self.windows = windows
        self.doors = doors
        self.enginetype = enginetype
    
    def drive(self):
        print(f"The person will drive the {self.enginetype} car.")

# Creating an object of the parent class
car1 = Car(4, 5, "petrol")
car1.drive()  # Output: The person will drive the petrol car.
```

Here, the `Car` class is the parent class, which has attributes like `windows`, `doors`, and `enginetype`, and a method `drive()`.

#### **Child Class Inheriting from Parent Class:**

```python
class Tesla(Car):  # Tesla is the child class inheriting from Car
    def __init__(self, windows, doors, enginetype, is_selfdriving):
        super().__init__(windows, doors, enginetype)  # Inherit attributes from parent class
        self.is_selfdriving = is_selfdriving  # Add a new attribute specific to Tesla

    def selfdriving(self):
        print(f"Tesla supports self-driving: {self.is_selfdriving}")

# Creating an object of the child class
tesla1 = Tesla(4, 5, "electric", True)
tesla1.selfdriving()  # Output: Tesla supports self-driving: True
tesla1.drive()        # Output: The person will drive the electric car.
```

#### **Explanation:**
- **Parent Class (`Car`)**: This class contains common attributes and methods that all cars should have (like `windows`, `doors`, `enginetype`, and `drive()`).
- **Child Class (`Tesla`)**: This class inherits from `Car` using `super().__init__()` to reuse the `windows`, `doors`, and `enginetype` attributes. Additionally, `Tesla` adds a new attribute `is_selfdriving` and a method `selfdriving()` specific to Tesla cars.
- `super()` is used to call the parent class's constructor and initialize the inherited attributes.

### **2. Multiple Inheritance**

In **multiple inheritance**, a class can inherit attributes and methods from more than one parent class. This allows a child class to combine functionality from multiple sources.

#### **Example:**

```python
## Base class 1
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print("Subclass must implement this method")

## Base class 2
class Pet:
    def __init__(self, owner):
        self.owner = owner

## Derived class inheriting from both Animal and Pet
class Dog(Animal, Pet):
    def __init__(self, name, owner):
        Animal.__init__(self, name)  # Initialize the Animal class
        Pet.__init__(self, owner)    # Initialize the Pet class

    def speak(self):
        return f"{self.name} says woof!"

# Create an object of the derived class
dog = Dog("Buddy", "Krish")
print(dog.speak())          # Output: Buddy says woof!
print(f"Owner: {dog.owner}")  # Output: Owner: Krish
```

#### **Explanation:**
- **Parent Classes (`Animal`, `Pet`)**: `Animal` has the attribute `name`, and `Pet` has the attribute `owner`. Both classes can provide useful behaviors and attributes.
- **Child Class (`Dog`)**: This class inherits from both `Animal` and `Pet` using multiple inheritance. It combines the attributes from both parent classes (`name` and `owner`). In the `__init__` method, we explicitly call the constructors of both `Animal` and `Pet` using `Animal.__init__()` and `Pet.__init__()` to initialize their respective attributes.

### **Key Concepts in Inheritance:**

#### **1. Method Overriding:**
A subclass can **override** a method from its parent class if it needs to provide a specific implementation. This happens when the child class defines a method with the same name as one in the parent class.

Example:
```python
class Animal:
    def speak(self):
        return "Animal sound"

class Dog(Animal):
    def speak(self):  # Method overriding
        return "Woof!"

dog = Dog()
print(dog.speak())  # Output: Woof!
```
In this example, `Dog` overrides the `speak()` method of the `Animal` class to provide a more specific implementation for dogs.

#### **2. `super()` in Python:**
The `super()` function allows you to call methods from the parent class. It is typically used in the child class to access the parent class's methods and attributes.

Example:
```python
class Parent:
    def __init__(self):
        print("Parent class constructor")

class Child(Parent):
    def __init__(self):
        super().__init__()  # Call the parent class constructor
        print("Child class constructor")

child = Child()
# Output:
# Parent class constructor
# Child class constructor
```
`super()` is particularly useful when a child class needs to modify or extend the behavior of the parent class.

#### **3. The `isinstance()` and `issubclass()` Functions:**
- `isinstance(object, class)`: Checks if an object is an instance of a class or a subclass of it.
- `issubclass(class1, class2)`: Checks if `class1` is a subclass of `class2`.

Example:
```python
print(isinstance(dog, Dog))  # Output: True
print(issubclass(Dog, Animal))  # Output: True
```

### **Conclusion:**
Inheritance in Python allows for the creation of hierarchical class structures, promoting code reuse and reducing redundancy. It simplifies complex programs by enabling the reuse of shared logic, making them easier to maintain and extend.

- **Single Inheritance**: One class inherits from another.
- **Multiple Inheritance**: A class can inherit from multiple parent classes.
- **Method Overriding**: A child class can override methods from its parent.
- **`super()`**: Used to access parent class methods and attributes from a child class.

By using inheritance effectively, you can create well-organized, maintainable, and scalable programs.
### **Polymorphism in Python**

Polymorphism is an essential concept in Object-Oriented Programming (OOP) that allows objects of different classes to be treated as objects of a common superclass. This flexibility enables a single function or method to behave differently based on the type of object it is interacting with. Polymorphism can be achieved through:
- **Method Overriding**: When a subclass provides a specific implementation of a method that is already defined in its superclass.
- **Abstract Base Classes**: These enforce that derived classes implement specific methods, ensuring consistency across different implementations.

---

### **1. Polymorphism through Method Overriding**

Method overriding occurs when a child class provides a specific implementation of a method that already exists in its parent class. This allows each subclass to define its own behavior while keeping the same method name.

#### **Example:**

```python
## Base Class
class Animal:
    def speak(self):
        return "Sound of the animal"
    
## Derived Class 1
class Dog(Animal):
    def speak(self):
        return "Woof!"
    
## Derived Class 2
class Cat(Animal):
    def speak(self):
        return "Meow!"
    
## Function that demonstrates polymorphism
def animal_speak(animal):
    print(animal.speak())
    
# Create objects of Dog and Cat
dog = Dog()
cat = Cat()

# Call methods individually
print(dog.speak())  # Output: Woof!
print(cat.speak())  # Output: Meow!

# Use polymorphism in a function
animal_speak(dog)  # Output: Woof!
animal_speak(cat)  # Output: Meow!
```

#### **Explanation:**
- `Dog` and `Cat` classes both override the `speak()` method of the `Animal` class.
- Even though the `animal_speak()` function only knows about the `Animal` type, it can call the `speak()` method on both `Dog` and `Cat` objects, allowing each object to respond in its own way.

---

### **2. Polymorphism with Functions and Methods**

Polymorphism is not limited to just method overriding. It can also be demonstrated through functions and methods, where different classes implement their own versions of a method that performs a similar function.

#### **Example:**

```python
## Base class
class Shape:
    def area(self):
        return "The area of the figure"
    
## Derived class 1
class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height
    
## Derived class 2
class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius
    
## Function that demonstrates polymorphism
def print_area(shape):
    print(f"The area is {shape.area()}")

# Create objects of Rectangle and Circle
rectangle = Rectangle(4, 5)
circle = Circle(3)

# Use polymorphism to call the same method on different shapes
print_area(rectangle)  # Output: The area is 20
print_area(circle)     # Output: The area is 28.26
```

#### **Explanation:**
- Both `Rectangle` and `Circle` classes have their own implementation of the `area()` method.
- The `print_area()` function can take any shape (either `Rectangle` or `Circle`) and call the appropriate `area()` method based on the object passed.

---

### **3. Polymorphism with Abstract Base Classes**

Polymorphism can also be enforced using **Abstract Base Classes (ABCs)**. These are classes that define abstract methods that must be implemented by all derived classes. This ensures that each derived class implements the necessary methods in its own way, while still maintaining consistency.

#### **Example:**

```python
from abc import ABC, abstractmethod

## Define an abstract class
class Vehicle(ABC):
    @abstractmethod
    def start_engine(self):
        pass

## Derived class 1
class Car(Vehicle):
    def start_engine(self):
        return "Car engine started"
    
## Derived class 2
class Motorcycle(Vehicle):
    def start_engine(self):
        return "Motorcycle engine started"
    
# Function that demonstrates polymorphism
def start_vehicle(vehicle):
    print(vehicle.start_engine())

# Create objects of Car and Motorcycle
car = Car()
motorcycle = Motorcycle()

# Use polymorphism to call the same method on different vehicles
start_vehicle(car)        # Output: Car engine started
start_vehicle(motorcycle)  # Output: Motorcycle engine started
```

#### **Explanation:**
- `Vehicle` is an abstract class that defines the abstract method `start_engine()`. This method must be implemented by all subclasses (like `Car` and `Motorcycle`).
- Polymorphism allows the `start_vehicle()` function to call the `start_engine()` method on both `Car` and `Motorcycle` objects, even though they implement the method differently.

---

### **Key Concepts in Polymorphism:**

#### **1. Method Overriding:**
Method overriding allows subclasses to provide their own implementation of a method that is already defined in the parent class. This enables polymorphic behavior, where the same method call behaves differently based on the object that is invoking it.

#### **2. Abstract Base Classes (ABC):**
Abstract Base Classes are used to define common methods for a group of related classes. ABCs enforce that derived classes implement specific methods, ensuring a consistent interface across different subclasses.

#### **3. `isinstance()` in Polymorphism:**
The `isinstance()` function can be used to check whether an object is an instance of a specific class, which is helpful when working with polymorphic behavior.

Example:
```python
print(isinstance(dog, Animal))  # Output: True
print(isinstance(circle, Shape))  # Output: True
```

### **Conclusion:**
Polymorphism is a powerful feature of OOP that allows for flexibility and code reuse. It enables a single function to handle objects of different classes, each with its own implementation of a method. By using polymorphism, you can create more extensible and maintainable programs that adapt to new requirements without requiring significant changes to existing code.
In Python, **`ABC` (Abstract Base Class)** and **`abstractmethod`** are part of the `abc` module and are used to define abstract classes and methods. Abstract classes serve as blueprints for other classes. Here's a breakdown of why and when to use them:

### **Why Use `ABC` and `abstractmethod`?**

1. **Enforcing Structure**:
   - Abstract classes allow you to define a **common structure** for a group of related classes. You can specify that certain methods **must be implemented** in any class that inherits from the abstract class.
   - For example, if you have a `Vehicle` abstract class, you want every subclass (like `Car` or `Motorcycle`) to have a `start_engine()` method. Using `abstractmethod` ensures that every subclass provides its own implementation of this method.

2. **Preventing Instantiation of Abstract Classes**:
   - You cannot create an instance of an abstract class directly. This prevents incomplete or inappropriate use of a class meant to serve as a template for other classes.
   - For example, creating a `Vehicle` object doesn't make sense if it doesn't have a working `start_engine()` method. With `abstractmethod`, Python will raise an error if someone tries to instantiate an abstract class.

3. **Providing Consistent Interfaces**:
   - By defining abstract methods, you ensure that every subclass follows the same interface or "contract." This is particularly useful in large codebases where consistency and adherence to design patterns are important.

### **How `ABC` and `abstractmethod` Work**

- **`ABC`**: A class inherits from `ABC` when you want it to be treated as an abstract base class.
- **`abstractmethod`**: This decorator marks methods that **must** be implemented in any subclass.

### **Example:**

```python
from abc import ABC, abstractmethod

# Define an abstract base class
class Vehicle(ABC):
    @abstractmethod
    def start_engine(self):
        pass  # This is an abstract method, no implementation here

# Derived class 1: Car must implement start_engine
class Car(Vehicle):
    def start_engine(self):
        return "Car engine started"

# Derived class 2: Motorcycle must also implement start_engine
class Motorcycle(Vehicle):
    def start_engine(self):
        return "Motorcycle engine started"

# Function to demonstrate polymorphism
def start_vehicle(vehicle):
    print(vehicle.start_engine())

# Creating objects of Car and Motorcycle
car = Car()
motorcycle = Motorcycle()

start_vehicle(car)          # Output: Car engine started
start_vehicle(motorcycle)   # Output: Motorcycle engine started
```

#### **Explanation:**
1. `Vehicle(ABC)` is the abstract base class, meaning it defines a template for other vehicle types.
2. The `@abstractmethod` decorator on `start_engine()` ensures that any class that inherits from `Vehicle` **must implement this method**.
3. The `Car` and `Motorcycle` classes inherit from `Vehicle` and **must provide their own implementation** of `start_engine()` to become concrete classes.
4. If you try to instantiate `Vehicle` directly without defining `start_engine()`, Python will raise an error.

### **What Happens if You Don’t Implement the Abstract Method?**

If a subclass fails to implement the abstract method, Python will throw a `TypeError` when you try to create an instance of the subclass.

#### Example:

```python
class Truck(Vehicle):
    pass  # No start_engine method implemented

# This will raise a TypeError
truck = Truck()  # Error: Can't instantiate abstract class Truck with abstract method start_engine
```

### **Conclusion:**
- `ABC` and `abstractmethod` are used to **define abstract base classes** in Python.
- They allow you to create **blueprints** for other classes and ensure that all subclasses implement specific methods.
- This enforces a **consistent interface** across different types of classes, making your code more organized and maintainable.
Sure! Here's the explanation of Encapsulation and Abstraction, with your name and age updated accordingly:

---

### Encapsulation and Abstraction

**Encapsulation** and **Abstraction** are two fundamental principles of Object-Oriented Programming (OOP) that help in designing robust, maintainable, and reusable code. 

- **Encapsulation** involves bundling data and methods that operate on the data within a single unit (class). It restricts direct access to some of the object's components, preventing accidental interference and misuse of the data.

- **Abstraction** involves hiding complex implementation details and exposing only the necessary features of an object. This simplifies interactions with the object and reduces complexity.

### Encapsulation with Getter and Setter Methods

Encapsulation is implemented using access modifiers, which control the visibility of class members (attributes and methods). 

- **Public Variables**: Accessible from anywhere.
- **Protected Variables**: Indicated by a single underscore (`_`), meant for internal use and inherited classes.
- **Private Variables**: Indicated by double underscores (`__`), inaccessible from outside the class.

### Example of Encapsulation

#### Public Variables

```python
class Person:
    def __init__(self, name, age):
        self.name = name    # public variable
        self.age = age      # public variable

def get_name(person):
    return person.name

person = Person("Assaf", 21)
print(get_name(person))  # Output: Assaf
```

#### Private Variables

```python
class Person:
    def __init__(self, name, age, gender):
        self.__name = name    # private variable
        self.__age = age      # private variable
        self.gender = gender

def get_name(person):
    return person.__name  # This will cause an AttributeError

person = Person("Assaf", 21, "Male")
# print(get_name(person))  # Uncommenting this will raise an error
```

In the above example, trying to access `__name` outside the class will result in an `AttributeError` because it's private.

#### Protected Variables

```python
class Person:
    def __init__(self, name, age, gender):
        self._name = name    # protected variable
        self._age = age      # protected variable
        self.gender = gender

class Employee(Person):
    def __init__(self, name, age, gender):
        super().__init__(name, age, gender)

employee = Employee("Assaf", 21, "Male")
print(employee._name)  # Output: Assaf
```

### Encapsulation with Getter and Setter Methods

Encapsulation can also be achieved through getter and setter methods, which provide controlled access to private variables.

```python
class Person:
    def __init__(self, name, age):
        self.__name = name  # Private variable
        self.__age = age    # Private variable

    # Getter method for name
    def get_name(self):
        return self.__name
    
    # Setter method for name
    def set_name(self, name):
        self.__name = name

    # Getter method for age
    def get_age(self):
        return self.__age
    
    # Setter method for age
    def set_age(self, age):
        if age > 0:
            self.__age = age
        else:
            print("Age cannot be negative.")

person = Person("Assaf", 21)

# Access and modify private variables using getter and setter
print(person.get_name())  # Output: Assaf
print(person.get_age())   # Output: 21

person.set_age(22)
print(person.get_age())   # Output: 22

person.set_age(-5)        # Output: Age cannot be negative.
```

### Conclusion

Encapsulation and abstraction are essential for building robust applications. By restricting access to the inner workings of objects and exposing only necessary functionalities, you can create a clear interface and improve the maintainability of your code. Encapsulation ensures that the data is protected from unauthorized access and modification, while abstraction allows you to focus on what an object does rather than how it does it.

--- 

### Encapsulation and Abstraction

**Encapsulation** and **Abstraction** are two fundamental principles of Object-Oriented Programming (OOP) that help in designing robust, maintainable, and reusable code. 

- **Encapsulation** involves bundling data and methods that operate on the data within a single unit (class). It restricts direct access to some of the object's components, preventing accidental interference and misuse of the data.

- **Abstraction** involves hiding complex implementation details and exposing only the necessary features of an object. This simplifies interactions with the object and reduces complexity.

### Encapsulation with Getter and Setter Methods

Encapsulation is implemented using access modifiers, which control the visibility of class members (attributes and methods). 

- **Public Variables**: Accessible from anywhere.
- **Protected Variables**: Indicated by a single underscore (`_`), meant for internal use and inherited classes.
- **Private Variables**: Indicated by double underscores (`__`), inaccessible from outside the class.

### Example of Encapsulation

#### Public Variables

```python
class Person:
    def __init__(self, name, age):
        self.name = name    # public variable
        self.age = age      # public variable

def get_name(person):
    return person.name

person = Person("Assaf", 21)
print(get_name(person))  # Output: Assaf
```

#### Private Variables

```python
class Person:
    def __init__(self, name, age, gender):
        self.__name = name    # private variable
        self.__age = age      # private variable
        self.gender = gender

def get_name(person):
    return person.__name  # This will cause an AttributeError

person = Person("Assaf", 21, "Male")
# print(get_name(person))  # Uncommenting this will raise an error
```

In the above example, trying to access `__name` outside the class will result in an `AttributeError` because it's private.

#### Protected Variables

```python
class Person:
    def __init__(self, name, age, gender):
        self._name = name    # protected variable
        self._age = age      # protected variable
        self.gender = gender

class Employee(Person):
    def __init__(self, name, age, gender):
        super().__init__(name, age, gender)

employee = Employee("Assaf", 21, "Male")
print(employee._name)  # Output: Assaf
```

### Encapsulation with Getter and Setter Methods

Encapsulation can also be achieved through getter and setter methods, which provide controlled access to private variables.

```python
class Person:
    def __init__(self, name, age):
        self.__name = name  # Private variable
        self.__age = age    # Private variable

    # Getter method for name
    def get_name(self):
        return self.__name
    
    # Setter method for name
    def set_name(self, name):
        self.__name = name

    # Getter method for age
    def get_age(self):
        return self.__age
    
    # Setter method for age
    def set_age(self, age):
        if age > 0:
            self.__age = age
        else:
            print("Age cannot be negative.")

person = Person("Assaf", 21)

# Access and modify private variables using getter and setter
print(person.get_name())  # Output: Assaf
print(person.get_age())   # Output: 21

person.set_age(22)
print(person.get_age())   # Output: 22

person.set_age(-5)        # Output: Age cannot be negative.
```

### Conclusion

Encapsulation and abstraction are essential for building robust applications. By restricting access to the inner workings of objects and exposing only necessary functionalities, you can create a clear interface and improve the maintainability of your code. Encapsulation ensures that the data is protected from unauthorized access and modification, while abstraction allows you to focus on what an object does rather than how it does it.

--- 

## Abstraction

Abstraction is a fundamental concept in Object-Oriented Programming (OOP) that focuses on hiding the complex implementation details of a system and exposing only the necessary features to the user. This simplifies the interaction with complex systems by allowing users to use objects without needing to understand the underlying complexities.

### Benefits of Abstraction
- **Reduces Complexity**: Users can interact with objects without needing to know the internal workings.
- **Improves Code Maintainability**: Changes in implementation details do not affect the code that uses the abstracted objects.
- **Encourages Code Reusability**: Abstract classes can be extended to create specific implementations without rewriting common functionality.

### Implementing Abstraction in Python

In Python, abstraction can be achieved using **Abstract Base Classes (ABCs)**, which are defined in the `abc` module. An abstract class can contain both implemented methods (concrete methods) and methods that are declared but not implemented (abstract methods).

### Code Example

Let's break down the code you provided:

```python
from abc import ABC, abstractmethod

## Abstract base class
class Vehicle(ABC):
    def drive(self):
        print("The vehicle is used for driving")

    @abstractmethod
    def start_engine(self):
        pass

class Car(Vehicle):
    def start_engine(self):
        print("Car engine started")

def operate_vehicle(vehicle):
    vehicle.start_engine()
    vehicle.drive()

car = Car()
operate_vehicle(car)
```

#### Code Breakdown

1. **Importing the ABC Module**:
   ```python
   from abc import ABC, abstractmethod
   ```
   This imports the `ABC` class and the `abstractmethod` decorator, which are used to define abstract base classes.

2. **Defining an Abstract Base Class**:
   ```python
   class Vehicle(ABC):
   ```
   - `Vehicle` is defined as an abstract base class by inheriting from `ABC`.
   - It can contain regular methods (like `drive`) as well as abstract methods (like `start_engine`).

3. **Concrete Method**:
   ```python
   def drive(self):
       print("The vehicle is used for driving")
   ```
   - This method provides a concrete implementation that can be used by subclasses.

4. **Abstract Method**:
   ```python
   @abstractmethod
   def start_engine(self):
       pass
   ```
   - The `start_engine` method is decorated with `@abstractmethod`, indicating that any subclass must implement this method. If a subclass does not implement all abstract methods, it cannot be instantiated.

5. **Defining a Subclass**:
   ```python
   class Car(Vehicle):
       def start_engine(self):
           print("Car engine started")
   ```
   - The `Car` class inherits from the `Vehicle` class and provides an implementation for the `start_engine` method.

6. **Function to Operate a Vehicle**:
   ```python
   def operate_vehicle(vehicle):
       vehicle.start_engine()
       vehicle.drive()
   ```
   - This function takes a `vehicle` object (which can be any subclass of `Vehicle`) and calls its methods. This demonstrates polymorphism as `operate_vehicle` can accept any object derived from `Vehicle`.

7. **Creating an Object and Using the Function**:
   ```python
   car = Car()
   operate_vehicle(car)
   ```
   - Here, an instance of `Car` is created, and `operate_vehicle` is called with this instance. The output will be:
   ```
   Car engine started
   The vehicle is used for driving
   ```

### Conclusion

Abstraction allows developers to work with objects at a higher level without needing to understand the complex details of their implementation. By using abstract classes and methods, you can create a clean, understandable interface while hiding the complexities of the implementation. This promotes better software design and enhances code maintainability.

---
## Magic Methods:

**magic methods** in Python, also known as **dunder methods** (short for "double underscore methods"), with a detailed explanation and real-time examples.

### What are Magic Methods?

Magic methods are special methods in Python that allow you to define the behavior of your objects in specific situations. They are always defined with two underscores before and after their name, hence the name "dunder" methods. 

These methods enable you to customize how your objects behave with built-in Python operations like addition, string representation, and more.

### Common Magic Methods

Here are some common magic methods along with simple explanations and examples:

1. **`__init__`**: This is the constructor method that initializes a new object. It’s called automatically when a new object of a class is created.

   **Example:**
   ```python
   class Person:
       def __init__(self, name, age):
           self.name = name
           self.age = age

   person1 = Person("Assaf", 21)
   print(person1.name)  # Output: Assaf
   print(person1.age)   # Output: 21
   ```

   In this example, when you create `person1`, the `__init__` method initializes the `name` and `age` attributes.

2. **`__str__`**: This method returns a string representation of an object, which is user-friendly.

   **Example:**
   ```python
   class Person:
       def __init__(self, name, age):
           self.name = name
           self.age = age

       def __str__(self):
           return f"{self.name}, {self.age} years old"

   person1 = Person("Assaf", 21)
   print(person1)  # Output: Assaf, 21 years old
   ```

   Here, when you use `print(person1)`, Python automatically calls the `__str__` method to get the string representation.

3. **`__repr__`**: This method returns an "official" string representation of an object, often useful for debugging. It should ideally return a valid Python expression that could be used to recreate the object.

   **Example:**
   ```python
   class Person:
       def __init__(self, name, age):
           self.name = name
           self.age = age

       def __repr__(self):
           return f"Person(name={self.name}, age={self.age})"

   person1 = Person("Assaf", 21)
   print(repr(person1))  # Output: Person(name=Assaf, age=21)
   ```

   The `__repr__` method provides a more detailed string representation of the object, which is useful for developers.

4. **`__len__`**: This method returns the length of the object when you use the built-in `len()` function.

   **Example:**
   ```python
   class Group:
       def __init__(self, members):
           self.members = members

       def __len__(self):
           return len(self.members)

   group = Group(["Assaf", "Alice", "Bob"])
   print(len(group))  # Output: 3
   ```

   Here, the `__len__` method allows you to use `len(group)` to get the number of members in the group.

5. **`__getitem__`** and **`__setitem__`**: These methods allow you to access and set items using indexing.

   **Example:**
   ```python
   class ShoppingCart:
       def __init__(self):
           self.items = []

       def __getitem__(self, index):
           return self.items[index]

       def __setitem__(self, index, value):
           self.items.insert(index, value)

   cart = ShoppingCart()
   cart[0] = "Apples"  # Using __setitem__
   print(cart[0])      # Using __getitem__, Output: Apples
   ```

   In this case, the `__getitem__` and `__setitem__` methods enable index-based access to the `items` in the shopping cart.

### Real-Time Example: Customizing a Class with Magic Methods

Let's put it all together in a real-time example using a `Vector` class to represent mathematical vectors.

```python
class Vector:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __str__(self):
        return f"Vector({self.x}, {self.y})"

    def __add__(self, other):
        return Vector(self.x + other.x, self.y + other.y)

    def __len__(self):
        return int((self.x ** 2 + self.y ** 2) ** 0.5)

# Creating vector objects
v1 = Vector(2, 3)
v2 = Vector(5, 7)

# Using __str__ to print the vector
print(v1)  # Output: Vector(2, 3)

# Adding two vectors using __add__
v3 = v1 + v2
print(v3)  # Output: Vector(7, 10)

# Getting the length of the vector using __len__
print(len(v3))  # Output: 12 (length calculated using Pythagorean theorem)
```

### Summary

- **Magic methods** allow you to define the behavior of your objects for built-in operations.
- Common magic methods include `__init__`, `__str__`, `__repr__`, `__len__`, `__getitem__`, and `__setitem__`.
- They help you create more intuitive and user-friendly classes in Python, making your code cleaner and easier to understand.
---
### Operator Overloading in Python

**Operator overloading** allows you to redefine or customize the behavior of Python's built-in operators (`+`, `-`, `*`, `/`, etc.) for your custom objects. This is done by overriding specific magic methods in your class.

#### Key Magic Methods for Operator Overloading:

- `__add__(self, other)`: Defines the behavior of the `+` operator.
- `__sub__(self, other)`: Defines the behavior of the `-` operator.
- `__mul__(self, other)`: Defines the behavior of the `*` operator.
- `__truediv__(self, other)`: Defines the behavior of the `/` operator.
- `__eq__(self, other)`: Defines the behavior of the `==` operator.
- `__lt__(self, other)`: Defines the behavior of the `<` operator.
- `__gt__(self, other)`: Defines the behavior of the `>` operator.

### Example 1: Operator Overloading with Vectors

Let's overload operators to define how two vectors should be added, subtracted, and multiplied by a scalar.

```python
class Vector:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    # Overloading the + operator
    def __add__(self, other):
        return Vector(self.x + other.x, self.y + other.y)

    # Overloading the - operator
    def __sub__(self, other):
        return Vector(self.x - other.x, self.y - other.y)

    # Overloading the * operator (for scalar multiplication)
    def __mul__(self, scalar):
        return Vector(self.x * scalar, self.y * scalar)

    # Overloading the == operator to compare two vectors
    def __eq__(self, other):
        return self.x == other.x and self.y == other.y

    # String representation of the Vector object
    def __repr__(self):
        return f"Vector({self.x}, {self.y})"

# Create objects of the Vector class
v1 = Vector(2, 3)
v2 = Vector(4, 5)

# Use overloaded operators
print(v1 + v2)  # Output: Vector(6, 8)
print(v1 - v2)  # Output: Vector(-2, -2)
print(v1 * 3)   # Output: Vector(6, 9)
print(v1 == v2) # Output: False
```

#### Explanation:
- **`__add__`**: Adds two vectors by adding their `x` and `y` components.
- **`__sub__`**: Subtracts two vectors component-wise.
- **`__mul__`**: Multiplies the vector by a scalar value.
- **`__eq__`**: Compares two vectors for equality based on their `x` and `y` components.
- **`__repr__`**: Provides a string representation, which helps when printing the vector.

### Example 2: Operator Overloading with Complex Numbers

Here’s how you can overload operators to perform addition, subtraction, multiplication, and division on complex numbers.

```python
class ComplexNumber:
    def __init__(self, real, imag):
        self.real = real
        self.imag = imag

    # Overloading the + operator
    def __add__(self, other):
        return ComplexNumber(self.real + other.real, self.imag + other.imag)

    # Overloading the - operator
    def __sub__(self, other):
        return ComplexNumber(self.real - other.real, self.imag - other.imag)

    # Overloading the * operator
    def __mul__(self, other):
        real_part = self.real * other.real - self.imag * other.imag
        imag_part = self.real * other.imag + self.imag * other.real
        return ComplexNumber(real_part, imag_part)

    # Overloading the / operator
    def __truediv__(self, other):
        denominator = other.real ** 2 + other.imag ** 2
        real_part = (self.real * other.real + self.imag * other.imag) / denominator
        imag_part = (self.imag * other.real - self.real * other.imag) / denominator
        return ComplexNumber(real_part, imag_part)

    # Overloading the == operator
    def __eq__(self, other):
        return self.real == other.real and self.imag == other.imag

    # String representation of the complex number
    def __repr__(self):
        return f"{self.real} + {self.imag}i"

# Create objects of the ComplexNumber class
c1 = ComplexNumber(2, 3)
c2 = ComplexNumber(1, 4)

# Use overloaded operators
print(c1 + c2)  # Output: 3 + 7i
print(c1 - c2)  # Output: 1 - 1i
print(c1 * c2)  # Output: -10 + 11i
print(c1 / c2)  # Output: 0.8235294117647058 + -0.29411764705882354i
print(c1 == c2) # Output: False
```

![image](https://github.com/user-attachments/assets/a6d4da2f-6be6-4da9-86ce-2fe107befe97)

### Summary of Operator Overloading:
- **Operator overloading** allows you to use standard operators with custom objects.
- You do this by overriding the special magic methods like `__add__`, `__sub__`, `__mul__`, etc.
- The goal is to make objects behave in a way that is natural for mathematical or logical operations.

