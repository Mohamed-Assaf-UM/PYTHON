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
