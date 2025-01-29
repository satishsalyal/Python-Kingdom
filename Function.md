

# **Python Functions: A Comprehensive Guide**

Functions are a fundamental part of Python programming, allowing code reuse, modularity, and readability. This guide covers function-related topics in detail with examples.

---

## **1. Function Calls**
A **function call** is an instruction that tells Python to execute a function. Python has built-in functions like `print()`, `len()`, and `type()`, and you can define custom functions.

### **Example of Function Calls**
```python
print("Hello, World!")  # Calls the built-in print function
length = len("Python")  # Calls len() to get the length of the string
print(length)  # Output: 6
```

---

## **2. Type Conversion Functions**
Python provides built-in functions to convert data types.

| Function  | Description                  | Example |
|-----------|------------------------------|---------|
| `int()`   | Converts to integer          | `int("10") → 10` |
| `float()` | Converts to float            | `float("3.14") → 3.14` |
| `str()`   | Converts to string           | `str(10) → "10"` |
| `bool()`  | Converts to boolean          | `bool(0) → False` |
| `list()`  | Converts to list             | `list("abc") → ['a', 'b', 'c']` |

### **Example**
```python
num = "42"
converted_num = int(num)  # Convert string to integer
print(type(converted_num))  # Output: <class 'int'>
```

---

## **3. Math Functions**
Python provides built-in math functions and the `math` module for advanced calculations.

### **Common Built-in Math Functions**
| Function | Description | Example |
|----------|------------|---------|
| `abs(x)` | Absolute value | `abs(-10) → 10` |
| `round(x, n)` | Rounds to `n` decimals | `round(3.1415, 2) → 3.14` |
| `max(a, b, c, ...)` | Returns the largest value | `max(3, 7, 1) → 7` |
| `min(a, b, c, ...)` | Returns the smallest value | `min(3, 7, 1) → 1` |
| `pow(x, y)` | Power (x^y) | `pow(2, 3) → 8` |

### **Using the `math` Module**
```python
import math
print(math.sqrt(16))  # Square root: 4.0
print(math.pi)  # Pi value: 3.141592653589793
print(math.sin(math.radians(30)))  # Sine of 30 degrees
```

---

## **4. Composition of Functions**
Functions can be **nested** inside each other.

### **Example**
```python
result = round(math.sqrt(25))  # sqrt(25) → 5.0, then round(5.0) → 5
print(result)  # Output: 5
```
Here, `math.sqrt()` computes the square root first, then `round()` rounds it.

---

## **5. Adding New Functions**
You can define your own functions using the `def` keyword.

### **Syntax**
```python
def function_name(parameters):
    # Function body
    return value  # Optional return statement
```

### **Example: Defining a Function**
```python
def greet(name):
    return "Hello, " + name + "!"

print(greet("Alice"))  # Output: Hello, Alice!
```

---

## **6. Definitions and Uses**
A **function definition** specifies what the function does, and a **function call** executes it.

### **Example**
```python
def add(a, b):  # Function definition
    return a + b

result = add(5, 3)  # Function call
print(result)  # Output: 8
```

---

## **7. Flow of Execution**
The flow of execution follows **top-to-bottom** order but jumps when calling a function.

### **Example**
```python
def first():
    print("First function")

def second():
    print("Second function")
    first()  # Calls first()

second()  # Output: Second function → First function
```
**Execution Order:**
1. `second()` is called.
2. It prints "Second function".
3. Calls `first()`, which prints "First function".

---

## **8. Parameters and Arguments**
- **Parameters**: Variables inside function definitions.
- **Arguments**: Actual values passed when calling a function.

### **Example**
```python
def multiply(x, y):  # x and y are parameters
    return x * y

result = multiply(4, 5)  # 4 and 5 are arguments
print(result)  # Output: 20
```

---

## **9. Stack Diagrams**
A **stack diagram** shows function calls in a hierarchical structure. Each function call creates a new **stack frame**.

### **Example**
```python
def square(n):
    return n * n

def sum_of_squares(a, b):
    return square(a) + square(b)

print(sum_of_squares(3, 4))
```
### **Stack Diagram Representation**
```
main() → calls sum_of_squares()
    sum_of_squares() → calls square(3) → returns 9
                     → calls square(4) → returns 16
                     → returns 9 + 16 = 25
```

---

## **Summary Table**
| Topic | Key Points |
|-------|-----------|
| **Function Calls** | Call functions using `function_name()` |
| **Type Conversion** | Use `int()`, `float()`, `str()` to convert data types |
| **Math Functions** | Use built-in math functions or `math` module |
| **Composition** | Nest functions within each other |
| **Adding New Functions** | Define using `def function_name():` |
| **Flow of Execution** | Functions are executed in a stack order |
| **Parameters & Arguments** | Parameters define function inputs, arguments provide actual values |
| **Stack Diagrams** | Represent function calls visually |

---

### **Conclusion**
Functions make Python programs efficient, modular, and reusable. Understanding function calls, parameters, flow of execution, and stack diagrams is crucial for writing clear, maintainable code.

Would you like me to expand on any section? 🚀
