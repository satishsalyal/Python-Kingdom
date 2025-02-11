# **Python Variables**  

## **📌 Introduction**  
Variables are essential in Python as they store data values. Python is a dynamically-typed language, meaning you do not need to specify the variable type explicitly.

---

## **🔹 What is a Variable?**  
A variable is a **named memory location** used to store data.

### **✅ Example:**
```python
name = "Alice"  # String variable
age = 25         # Integer variable
height = 5.9     # Float variable
is_student = True # Boolean variable
```

---

## **🔹 Rules for Naming Variables**
1. Must start with a **letter (A-Z, a-z) or an underscore (_)**.
2. Can contain letters, numbers, and underscores.
3. Cannot be a Python **keyword** (e.g., `class`, `def`, `import`).
4. Case-sensitive (`Name` and `name` are different).

### **🚫 Invalid Variable Names:**
```python
2name = "John"   # ❌ Cannot start with a number
my-name = "Bob"  # ❌ Hyphens are not allowed
class = 10       # ❌ 'class' is a reserved keyword
```

---

## **🔹 Variable Assignment & Dynamic Typing**
Python allows reassigning different data types to the same variable.

### **✅ Example:**
```python
x = 10      # Integer
x = "Hello" # Now a String
x = 3.14    # Now a Float
```

> **📝 Note:** Python automatically assigns the type based on the value.

---

## **🔹 Data Types in Python**
Python supports various built-in data types:

| Data Type  | Example      | Description |
|------------|-------------|-------------|
| `int`      | `42`        | Integer numbers |
| `float`    | `3.14`      | Decimal numbers |
| `str`      | `"Hello"`   | Text (strings) |
| `bool`     | `True`      | Boolean values |
| `list`     | `[1, 2, 3]` | Ordered collection |
| `tuple`    | `(1, 2, 3)` | Immutable ordered collection |
| `dict`     | `{ "a": 1 }` | Key-value pairs |
| `set`      | `{1, 2, 3}` | Unordered collection |

### **✅ Example: Checking Data Types**
```python
x = 100
print(type(x))  # Output: <class 'int'>

y = "Python"
print(type(y))  # Output: <class 'str'>
```

---

## **🔹 Multiple Variable Assignment**
Python allows assigning multiple variables in one line.

### **✅ Example:**
```python
a, b, c = 5, "Hello", 3.14
print(a)  # Output: 5
print(b)  # Output: Hello
print(c)  # Output: 3.14
```

---

## **🔹 Constants in Python**
In Python, constants are usually written in **UPPER_CASE** by convention.

### **✅ Example:**
```python
PI = 3.14159
GRAVITY = 9.8
```
> **📝 Note:** Python does not enforce constants, but developers follow this convention.

---

## **🔹 Variable Type Conversion (Type Casting)**
Python allows explicit type conversion using built-in functions: `int()`, `float()`, `str()`, etc.

### **✅ Example:**
```python
num = "10"  # String
to_int = int(num)  # Convert to integer
print(to_int, type(to_int))  # Output: 10 <class 'int'>
```

---

## **🔹 Global vs Local Variables**
- **Local variables**: Declared inside a function and accessible only within that function.
- **Global variables**: Declared outside a function and accessible throughout the program.

### **✅ Example:**
```python
global_var = "I am global"

def my_function():
    local_var = "I am local"
    print(local_var)  # Accessible here
    print(global_var) # Accessible here

my_function()
print(global_var)  # Accessible outside
#print(local_var)  # ❌ Error: Not accessible outside function
```

---

## **🔹 Deleting Variables**
Python allows deleting a variable using `del` keyword.

### **✅ Example:**
```python
x = 100
del x
#print(x)  # ❌ Error: x is deleted
```

---

## **📌 Summary**
✔ Variables store data and are dynamically typed.  
✔ Naming rules must be followed to avoid errors.  
✔ Python supports multiple data types and type conversions.  
✔ Variables can be local or global.  
✔ Constants are named using uppercase letters by convention.  
✔ `del` keyword can remove a variable.

🚀 **Happy Coding!** 🎯

