
# **Understanding Variables in Python**

In Python, a **variable** is a name used to store data. Variables act as containers for values, allowing you to use and manipulate them later in your code.

---

## **🌟 Declaring Variables**
To create a variable in Python:
1. Choose a variable name.
2. Assign a value to it using the **`=`** operator.

### **Example:**

```python
# Declaring variables
name = "Alice"       # A string
age = 25             # An integer
height = 5.6         # A floating-point number
is_student = True    # A boolean

# Printing the variables
print(name)
print(age)
print(height)
print(is_student)
```

**Output:**

```
Alice
25
5.6
True
```

---

## **🔤 Variable Naming Rules**
- Variable names must start with a **letter** or an **underscore** (e.g., `_my_var`).
- The name can contain letters, numbers, and underscores, but **no spaces**.
- Variable names are **case-sensitive** (e.g., `name` and `Name` are different).
- Avoid using **Python keywords** (e.g., `if`, `else`, `True`) as variable names.

---

## **💡 Dynamic Typing in Python**
Python is a **dynamically typed language**, meaning you don’t need to specify the type of the variable. Python automatically determines the type based on the value you assign.

### **Example:**

```python
# Dynamic typing
x = 10      # Initially an integer
print(x)

x = "Hello" # Reassigned as a string
print(x)
```

**Output:**

```
10
Hello
```

---

## **⚡ Multiple Variable Assignment**
Python allows assigning values to multiple variables in a single line.

### **Example:**

```python
# Assigning multiple values
a, b, c = 1, 2, 3

# Assigning the same value to multiple variables
x = y = z = 0

print(a, b, c)
print(x, y, z)
```

**Output:**

```
1 2 3
0 0 0
```

---

## **🔍 Type Checking**
To check the type of a variable, use the **`type()`** function.

### **Example:**

```python
age = 25
name = "Alice"

print(type(age))  # Output: <class 'int'>
print(type(name)) # Output: <class 'str'>
```

**Output:**

```
<class 'int'>
<class 'str'>
```

---

## **📋 Variable Best Practices**
- Use **descriptive names** that explain the purpose of the variable (e.g., `total_price` instead of `tp`).
- Follow the **snake_case** naming convention (e.g., `user_name`).
- Avoid using **special characters** in variable names (except `_`).

---

