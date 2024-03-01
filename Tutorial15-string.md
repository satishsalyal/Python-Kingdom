# Python String


- [Create a String](#create-a-string)
- [Access String Characters](#access-string-characters)
- [Negative Indexing](#negative-indexing)
- [Slicing of a String](#slicing-of-a-string) 
- [Change and Delete String Characters](#change-and-delete-string-characters)
- [Python String Operations](#python-string-operations)
- [Iterating through a String](#iterating-through-a-string)
- [Python String Methods](#python-string-methods)
- [**Task**: Guess the Output](#programming-task)
---

### Create a String
A string is a sequence of characters or textual data. In Python, we create strings by enclosing characters inside quotations like:

```python
# single quote
text = 'Hello there'
print(text)

# double quotes
text = "Hello there"
print(text)

# triple quotes for multiline strings
text = """Hello there.
How are you doing"""
print(text)
```

**Output**
```
Hello there
Hello there
Hello there.
How are you doing
```

However, we can't use mismatching quotations like:

```python
# mismatching strings
text = 'Hello there"
print(text)
```

**Output**

```
File "<string>", line 2
    text = 'Hello there"
                       ^
SyntaxError: EOL while scanning string literal
```


Suppose we want to create a string:
```
He said, "What's there?"
```

It contains both single quotes and double quotes, so using either of those would give error:

```python
text =  "He said, "What's there?""
print(text)
```

**Output**
```
File "<string>", line 1
    text =  "He said, "What's there?""
                       ^
SyntaxError: invalid syntax
```

To fix this, we can escape characters like quotations by using a backslash `\` before it.

```python
text =  "He said, \"What\'s there?\""
print(text)
```

**Output**
```
He said, "What's there?"
```
---

## Access String Characters

A string is a sequence of characters, and these characters are in order. So, we can access individual characters of a string using indices just like with lists and tuples. 

```python
text = "Python"
print(text)
```

**Output**

```
Python
```

Here, every elements in the list maintain an order.

We can access individual characters of string by using its index. Index starts from `0`.
So the index of the first character is 0, the second character is 1 and so on.

|Character|Index|
|---|---|
|'P'|0|
|'y'|1|
|'t'|2|
|'h'|3|
|...|...|

We can use indices in the following way:

```python
text = "Python"

# first character
print(text[0])

# fourth character
print(text[3])
```

**Output**
```
P
h
```

If the specified index does not exist in the string, Python throws an `IndexError`
exception.

```python
text = "Python"
print(text[10])
```

**Output**

```
Traceback (most recent call last):
  File "<string>", line 2, in <module>
IndexError: string index out of range
```
---

### Negative Indexing

In Python, we can also use negative indexing for sequences like string.
Using a negative index gives us characters from the last.

|Character|Index|
|---|---|
|'P'|-6|
|'y'|-5|
|'t'|-4|
|'h'|-3|
|'o'|-2|
|'n'|-1|

Negative index can be used like normal index:

```python
text = "Python"

# last character
print(text[-1])

# third to last character
print(text[-3])
```

**Output**

```
n
h
```

---

### Slicing of a String

It is also possible to access multiple characters from the string, not just a single character.

For example,

```python
text = "Python"

# 2nd, 3rd and 4th characters
print(text[1:4])
```

**Output**

```
yth
```

While using slicing, the starting index is inclusive but the ending index is exclusive.

>**Notes**:
>- If we use the empty start index, the slicing starts from the beginning of the string.
>- If we use the empty end index, the slicing ends at the last string character.

```python
text = "Python"

# first to fourth characters
print(text[:4])

# from third to last character
print(text[2:])
```

**Output**

```
Pyth
thon
```

---

### Change and Delete String Characters

Strings in Python are immutable, and we cannot add or change characters of a string. Let's see what happens when we try to change characters of a string:

```python
text = "Python"
text[0] = "p"
print(text)
```

**Output**

```
Traceback (most recent call last):
  File "<string>", line 2, in <module>
TypeError: 'str' object does not support item assignment
```

---

### Python String Operations

#### Concatenation
It denotes the joining of two strings into one. To join two strings, we can use the plus `+` operator.

```python
text1 = "Python"
text2 = "Programming"

result = text1 + " " + text2
print(result)
```

**Output**
```
Python Programming
```

#### Repeating strings
We use the asterisk `*` operator to repeat a string a certain number of times:

```python
text = "Python"
new_text = text * 3

print(new_text)
```

**Output**
```
PythonPythonPython
```
---

### Iterating through a String

If we want to get individual characters of a string one by one, we can use a `for` loop.

```python
text = "Python"

for character in text:
    print(character) 
```

**Output**

```
P
y
t
h
o
n
```

In each iteration, the value of `character` is each individual character from the `text` string.

We can use `len()` to find length of a string:

```python
text = "Python"
print(len(text))
```

**Output**
```
6
```

We can also use the `in` operator to find out if a substring is present in a given string:

```python
text = "Python"
print("P" in text)

print("yth" in text)

print("ont" in text)
```

**Output**
```
True
True
False
```

---

### Python String Methods

Strings are probably the most frequently used data type. To make working with strings easier, Python has numerous string methods readily available for us to use.

#### `lower()` and `upper()` method

To make all the characters lowercase, we can use the `lower()` method.

```python
text = "I like Python 3"
result = text.lower()

print(result)
```

**Output**
```
i like python 3
```

Similarly, if we want all uppercase characters, we can use the `upper()` method.

```python
text = "I like Python 3"
result = text.upper()

print(result)
```

**Output**
```
I LIKE PYTHON 3
```

---

#### `find()` method

To find the index of the Python substring, we can use the `find()` method.

```python
text = "I like Python 3"
result = text.find("Python")

print(result)
```

**Output**
```
7
```

---

#### `replace()` method

To replace a substring with another, we can use the `replace()` method.

```python
text = "I like Python 3"
result = text.replace("Python 3", "Java")

print(result)
```

**Output**
```
I like Java
```

---

## Programming Task

**Can you guess the output of this program?**

```python
quote = "Talk is cheap. Show me the code."

print("1.", quote[3])
print("2.", quote[-3])
print("3.", quote.replace("code", "program"))
```

**Output**
```
1. k
2. d
3. Talk is cheap. Show me the program.
```
## String Operators in Python
```
Following are the common string operations that can be performed in Python:

Concatenation of two or more strings.
Extracting or slicing partial strings from string values.
Adding or removing spaces.
Converting to lower or upper case.
Formatting strings using string formatters.
Finding and/or replacing a text in the given string with another text.
```

```
Assignment operator: “=”
Concatenate operator: “+”
String repetition operator: “*”
String slicing operator: “[]”
String comparison operator: “==” & “!=”
Membership operator: “in” & “not in”
Escape sequence operator: “\”
String formatting operator: “%” & “{}”
```
```
Examples of String Operators in Python
In the following article, with examples, we will learn how to perform operations on a string in Python.

Example #1 – Assignment Operator “=”
Python string can be assigned to any variable with an assignment operator “= “. Python string can be defined with either single quotes [”], double quotes[“”], or triple quotes[‘””‘]. var_name = “string” assigns “string” to variable var_name.
```
Code:

string1 = "hello"
string2 = 'hello'
string3 = '''hello'''
print(string1)
print(string2)
print(string3)
Output:

String Operators in Python 1-1
Example #2 – Concatenate Operator “+”
Two strings can be concatenated or joined using the “+” operator in Python, as explained in the below example code:

Code:

string1 = "hello"
string2 = "world "
string_combined = string1+string2
print(string_combined)
Output:

hello world
Example #3 – String Repetition Operator “*”
The same string can be repeated in Python by n times using string*n, as explained in the below example.

Code:
```python
string1 = "helloworld "
print(string1*2)
print(string1*3)
print(string1*4)
print(string1*5)
```
```
Output:

Repetition
Example #4 – String slicing operator “[]”
Characters from a specific string index can be accessed with the string[index] operator. The index is interpreted as a positive index starting from 0 from the left side and a negative index starting from -1 from the right side.

String	H	E	L	L	O	W	O	R	L	D
Positive index	0	1	2	3	4	5	6	7	8	9
Negative index	-10	-9	-8	-7	-6	-5	-4	-3	-2	-1
string[a]: Returns a character from a positive index a of the string from the left side, as displayed in the index graph above.
string[-a]: Returns a character from a negative index a of the string from the right side, as displayed in the index graph above.
string[a:b]: Returns characters from positive index a to positive index b as displayed in the index graph above.
string[a:-b]: Returns characters from positive index a to the negative index b of the string as displayed in the index graph above.
string[a:]: Returns characters from positive index a to the end of the string.
string[:b] Returns characters from the start of the string to the positive index b.
string[-a:]: Returns characters from negative index a to the end of the string.
string[:-b]: Returns characters from the start of the string to the negative index b.
string[::-1]: Returns a string with reverse order.
```
Code:
```python
string1 = "helloworld"
print(string1[1])
print(string1[-3])
print(string1[1:5])
print(string1[1:-3])
print(string1[2:])
print(string1[:5])
print(string1[:-2])
print(string1[-2:])
print(string1[::-1])
```
```
Output:

String Operators in Python 1-4
Example #5 – String Comparison Operator “==” & “!=”
The string comparison operator in Python is used to compare two strings.

The “==” operator returns Boolean True if two strings are the same and Boolean False if two strings are different.
The “!=” operator returns Boolean True if two strings are not the same and returns Boolean False if two strings are the same.
These operators are mainly used along with the if condition to compare two strings where the decision will be taken based on string comparison.
```
Code:
```python
string1 = "hello"
string2 = "hello, world"
string3 = "hello, world"
string4 = "world"
print(string1==string4)
print(string2==string3)
print(string1!=string4)
print(string2!=string3)
```
```
Output:

Comparison 
Example #6 – Membership Operator “in” & “not in”
The membership operator searches whether the specific character is part/member of a given input Python string.

“a” in the string: Returns boolean True if “a” is in the string and returns False if “a” is not in the string.
“a” not in the string: Returns boolean True if “a” is not in the string and returns False if “a” is in the string.
A membership operator is also useful to find whether a specific substring is part of a given string.
```
```python
Code:

string1 = "helloworld"
print("w" in string1)
print("W" in string1)
print("t" in string1)
print("t" not in string1)
print("hello" in string1)
print("Hello" in string1)
print("hello" not in string1)
```
```
Example #7 – Escape Sequence Operator “\”
An escape character is used to insert a non-allowed character in the given input string. An escape character is a “\” or “backslash” operator followed by a non-allowed character. An example of a non-allowed character in a Python string is inserting double quotes in the string surrounded by double quotes.

1. Example of non-allowed double quotes in Python string:

Code:

string = "Hello world I am from "India""
print(string)
Output:

String Operators in Python 1-7
2. Example of non-allowed double quotes with escape sequence operator:

Code:

string = "Hello world I am from \"India\""
print(string)
Output:

String Operators in Python 1-8
Example #8 – String Formatting Operator “%”
The string formatting operator is used to format a string as per requirement. To insert another type of variable along with string, the “%” operator is used along with Python string. “%” is prefixed to another character, indicating the type of value we want to insert along with the Python string. Please refer to the table below for some of the commonly used different string formatting specifiers:

Operator	Description
%d	Signed decimal integer
%u	unsigned decimal integer
%c	Character
%s	String
%f	Floating-point real number
```
Code:
```python
name = "india"
age = 19
marks = 20.56
string1 = 'Hey %s' % (name)
print(string1)
string2 = 'my age is %d' % (age)
print(string2)
string3= 'Hey %s, my age is %d' % (name, age)
print(string3)
string3= 'Hey %s, my subject mark is %f' % (name, marks)
print(string3)
python
Output:
```
String Operators in Python 1-9
```
Example #9
Code:
```python
# String formatting using f-strings
print("Enter your name")
name = input()
print(f"Hey !! {name}, welcome to the party...")
print('\n')
print("Enter first number")
a = int(input())
print("Enter second number")
b = int(input())
print(f"sum of {a} and {b} is {a+b}")
# String formatting using format() method
str1 = "{} {} {}".format("Travelling", 'is', 'life')
print("String will be printed in default order:")
print(str1)
str2 = "{1} {2} {0}".format("love", "Travelling", "is")
print(str2)
str3 = "{T} {i} {l}".format(T='Travelling', l='love', i='is')
print(str3)
# String formatting using % operator
print('\n')
print("Enter number of items")
item = int(input())
print("%s is carrying %d items"%(name, item))
```
```
Explanation:

1. f-string: The letter “f” is placed before the beginning of the string, and the variables mentioned in curly braces will refer to the variables declared above. For example, {name} refers to the name variable defined above. Similarly, {a} and {b} refers to variable a and b, respectively.

2. format() method: format() method is called on a string object. We use curly braces {} that will refer to the format() method arguments inside the string. The number of {} should match the number of arguments inside format()

In default formatting, {} will refer to the format() arguments in the order in which they are placed.
In positional formatting, order is indicated inside {}. The above example “{1} {2} {0}” .format(“love”, “Travelling”, “is”) states that the argument positioned at index 1 (“travelling”) inside format() will come first, argument position at 2 index(“is”) will come second, and argument positioned at index 0(“love”) will come last.
In keyword formatting, specific keywords are used inside {}, which will be mapped to corresponding format() arguments.
3. % operator: The “%” operator will be replaced by variables defined in parenthesis/in tuple. %s means a string variable will come to this place, %d is an integer, and %f is a floating-point value.
```
Example #10
Code:
```python
string = "Various string methods"
string2 = "Investment in learning "
print("lower()")
print(string.lower())
print("\nupper()")
print(string.upper())
print("\nislower()")
print(string.islower())
print("\nisupper()")
print(string.isupper())
print("\nstartswith")
print(string.startswith("Var"))
print("\nendswith()")
print(string.endswith("el"))
print("join()")
print('-->'.join(['various', 'strings', 'methods']))
print("\nsplit()")
print(string.split())
print("\nljust()")
print("hello".ljust(15, '*'))
print("\nrjust(*)")
print("hello".rjust(15, '*'))
print("\ncenter()")
print("welcome".center(20, '*'))
print("\nstrip()>")
print(string2.strip())
print("\nlstrip()")
print(string2.lstrip())
print("\nrstrip()")
print(string2.rstrip())
```
