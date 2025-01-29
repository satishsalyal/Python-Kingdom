# **Installing Python, Program Structure, Interactive Shell, Executable or Script Files, User Interface or IDE. Variables**

## **1. Installing Python**

Python is an open-source programming language that can be installed on Windows, macOS, and Linux.

### **Installation Steps:**
1. **Download Python:**
   - Visit the official Python website: [https://www.python.org/downloads/](https://www.python.org/downloads/)
   - Choose the latest stable version for your operating system.
2. **Run the Installer:**
   - Check the box **"Add Python to PATH"** before installing.
   - Click **Install Now**.
3. **Verify Installation:**
   - Open the terminal (Command Prompt or Terminal).
   - Type:
     ```sh
     python --version
     ```
   - This should display the installed Python version (e.g., `Python 3.10.4`).

---

## **2. Program Structure in Python**

Python programs follow a simple structure:
- **Statements:** Instructions written as code.
- **Indentation:** Used to define blocks of code.
- **Comments:** Used for documentation (`#` for single-line, `'''` or `"""` for multi-line).
- **Functions and Classes:** Modular code structures.

### **Example:**
```python
# This is a single-line comment
"""This is a multi-line comment"""

def greet(name):
    print("Hello,", name)  # Indented block

greet("Alice")
```

---

## **3. Interactive Shell (Python REPL)**

The Python **interactive shell (REPL - Read, Evaluate, Print, Loop)** allows users to execute Python commands interactively.

### **Accessing the Python Shell:**
- Open the terminal and type:
  ```sh
  python
  ```
- You should see a prompt like:
  ```
  >>>
  ```

### **Using the Python Shell:**
```python
>>> print("Hello, World!")
Hello, World!
>>> 5 + 3
8
>>> name = "Python"
>>> name.upper()
'PYTHON'
```

---

## **4. Executable or Script Files**

Python scripts can be saved as `.py` files and executed.

### **Creating a Python Script:**
1. Open a text editor (Notepad++, VS Code, PyCharm, etc.).
2. Write a Python script:
   ```python
   print("Hello, this is a Python script!")
   ```
3. Save the file as `script.py`.

### **Running a Python Script:**
- Open the terminal and navigate to the script's directory.
- Run:
  ```sh
  python script.py
  ```
- Output:
  ```
  Hello, this is a Python script!
  ```

---

## **5. User Interface or IDE**

An **Integrated Development Environment (IDE)** provides tools to write, test, and debug Python programs.

### **Popular Python IDEs:**
- **IDLE** (comes with Python installation)
- **PyCharm** (feature-rich, best for large projects)
- **VS Code** (lightweight and extensible)
- **Jupyter Notebook** (best for data science & machine learning)

### **Using IDLE (Python's Built-in IDE):**
1. Open **IDLE** from the Start menu or by typing `idle` in the terminal.
2. Click **File > New File** to create a new script.
3. Write Python code and save it as a `.py` file.
4. Run the script by clicking **Run > Run Module (F5)**.

---

## **6. Variables in Python**

A **variable** in Python is used to store data. Python is dynamically typed, so variable types are inferred automatically.

### **Declaring Variables:**
```python
name = "Alice"  # String
age = 25        # Integer
height = 5.7    # Float
is_student = True  # Boolean
```

### **Printing Variables:**
```python
print("Name:", name)
print("Age:", age)
print("Height:", height)
print("Student Status:", is_student)
```
**Output:**
```
Name: Alice
Age: 25
Height: 5.7
Student Status: True
```

### **Variable Naming Rules:**
- Must start with a **letter** or an **underscore (`_`)**.
- Can contain letters, numbers, and underscores.
- Cannot use Python **keywords** (e.g., `if`, `else`, `while`).
- Variable names are **case-sensitive** (`name` and `Name` are different).

### **Type Checking:**
```python
print(type(name))  # Output: <class 'str'>
print(type(age))   # Output: <class 'int'>
print(type(height))  # Output: <class 'float'>
```

### **Multiple Variable Assignment:**
```python
x, y, z = 10, 20, 30
print(x, y, z)

# Assigning the same value to multiple variables
a = b = c = "Python"
print(a, b, c)
```
**Output:**
```
10 20 30
Python Python Python
```

---

## **📌 Summary**
| Topic | Key Points |
|--------|------------|
| **Installing Python** | Download from Python.org, install, and verify using `python --version` |
| **Program Structure** | Uses indentation, statements, functions, and comments for clarity |
| **Interactive Shell** | REPL allows quick testing and debugging |
| **Executable Scripts** | Python files saved as `.py`, executed with `python filename.py` |
| **User Interface (IDE)** | Tools like IDLE, PyCharm, VS Code improve coding experience |
| **Variables** | Used to store data, dynamically typed, follow naming rules |



