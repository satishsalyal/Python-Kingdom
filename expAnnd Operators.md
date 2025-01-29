# **Expressions and Statements: Values and Types, Variables, Variable Names and Keywords, Operators and Operands**

## **1. Expressions and Statements**
Python programs consist of expressions and statements. Understanding their differences is fundamental to writing efficient code.

### **Expressions**
An **expression** is a combination of values, variables, and operators that produces a value. It is evaluated by Python and returns a result.

#### **Examples of expressions**
```python
x = 10 + 5  # 10 + 5 is an expression that evaluates to 15
y = x * 2   # x * 2 is an expression that evaluates to 30
```
Here, `10 + 5` and `x * 2` are expressions because they produce a value.

### **Statements**
A **statement** is an instruction that Python executes. Statements do not necessarily return values.

#### **Examples of statements**
```python
x = 20         # Assignment statement
print(x)       # Function call statement
if x > 10:     # Conditional statement
    print("x is greater than 10")
```
Here, `x = 20` is an assignment statement, `print(x)` is a function call statement, and the `if` condition is a control statement.

> **Key Difference:** Expressions produce a value, while statements perform an action.

---

## **2. Values and Types**
In Python, everything is a value, and every value has a type.

### **Basic Types in Python**
| Data Type  | Example      | Description |
|------------|-------------|-------------|
| `int`      | `42`        | Integer numbers |
| `float`    | `3.14`      | Decimal numbers |
| `str`      | `"Hello"`   | Text (strings) |
| `bool`     | `True`      | Boolean (True/False) |
| `list`     | `[1, 2, 3]` | Ordered collection of items |
| `tuple`    | `(1, 2, 3)` | Immutable ordered collection |
| `dict`     | `{"a": 1}`  | Key-value pairs |

#### **Example of checking types**
```python
print(type(42))        # Output: <class 'int'>
print(type(3.14))      # Output: <class 'float'>
print(type("Hello"))   # Output: <class 'str'>
print(type(True))      # Output: <class 'bool'>
```

> **Note:** Python is dynamically typed, meaning variables can change types.

---

## **3. Variables**
A **variable** is a name assigned to a value, which allows us to store and manipulate data.

### **Variable Assignment**
```python
age = 25  # Assigning an integer value
name = "Alice"  # Assigning a string
pi = 3.14  # Assigning a float
```

### **Dynamic Typing Example**
```python
x = 10    # Initially an integer
x = "Hi"  # Now a string
print(x)  # Output: Hi
```
Here, `x` initially stores an integer but later stores a string, demonstrating Python's dynamic typing.

---

## **4. Variable Names and Keywords**
### **Variable Naming Rules**
1. Must start with a letter (A-Z or a-z) or an underscore `_`
2. Can contain letters, digits (0-9), and underscores
3. Cannot be a Python keyword (reserved word)

#### **Valid Variable Names**
```python
name = "John"
_age = 30
total_score = 95
```

#### **Invalid Variable Names**
```python
2name = "Alice"   # Cannot start with a number
my-name = "Bob"   # Hyphens are not allowed
class = 10        # "class" is a reserved keyword
```

### **Python Keywords (Reserved Words)**
Keywords are special words in Python that cannot be used as variable names.

#### **List of Keywords**
```python
import keyword
print(keyword.kwlist)
```
**Example Output:**
```python
['False', 'None', 'True', 'and', 'as', 'assert', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```

---

## **5. Operators and Operands**
Operators are symbols used to perform operations on values or variables.

### **Types of Operators in Python**
| Operator Type | Example | Description |
|--------------|---------|-------------|
| Arithmetic  | `+`, `-`, `*`, `/`, `%`, `**`, `//` | Basic math operations |
| Comparison  | `==`, `!=`, `<`, `>`, `<=`, `>=` | Compare values |
| Logical     | `and`, `or`, `not` | Boolean logic |
| Assignment  | `=`, `+=`, `-=`, `*=`, `/=` | Assign values |
| Bitwise     | `&`, `|`, `^`, `~`, `<<`, `>>` | Binary operations |

#### **Example of Operators**
```python
a = 10
b = 3
print(a + b)  # Addition: 13
print(a / b)  # Division: 3.3333
print(a // b) # Floor division: 3
print(a ** b) # Exponentiation: 1000
```

---

## **6. Interactive Mode and Script Mode**
Python can be run in two modes:

### **1. Interactive Mode**
- Runs in the Python shell (REPL).
- Executes one line at a time.
- Used for quick testing.

#### **Example**
```python
>>> 2 + 3
5
>>> print("Hello")
Hello
```

### **2. Script Mode**
- Runs Python code from a file (`.py`).
- Used for larger programs.

#### **Example: Running a script**
Create a file `script.py`:
```python
x = 10
y = 20
print(x + y)
```
Run it using:
```sh
python script.py
```

---

## **7. Order of Operations**
When multiple operators are used in an expression, Python follows the **PEMDAS** rule:

### **PEMDAS Rule**
1. **P** - Parentheses `()`
2. **E** - Exponents `**`
3. **M/D** - Multiplication `*` and Division `/`
4. **A/S** - Addition `+` and Subtraction `-`

#### **Example**
```python
result = 5 + 2 * 3  # Multiplication first, then addition
print(result)  # Output: 11
```
```python
result = (5 + 2) * 3  # Parentheses first
print(result)  # Output: 21
```

> **Tip:** Use parentheses to make expressions clearer.

---

## **Conclusion**
- **Expressions** produce a value, while **statements** perform an action.
- Python has different **data types** and allows **dynamic typing**.
- **Variable names** must follow naming rules and should not be **keywords**.
- **Operators** perform calculations, comparisons, and logic.
- **Order of operations** follows **PEMDAS**.

Let me know if you have any questions! 🚀

