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

