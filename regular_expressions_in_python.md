
# 📘 Regular Expressions in Python

**Regular Expressions (regex or regexp)** are sequences of characters that define a search pattern, mainly used for string matching and manipulation. Python provides a built-in module called `re` to work with regular expressions.

---

## 🔹 Importing the `re` Module

To start using regular expressions in Python:

```python
import re
```

---

## 🔹 Basic Functions in `re` Module

| Function        | Description                                      |
|-----------------|--------------------------------------------------|
| `re.match()`    | Checks for a match only at the beginning of the string |
| `re.search()`   | Searches for a match anywhere in the string      |
| `re.findall()`  | Returns a list of all matches                    |
| `re.finditer()` | Returns an iterator yielding match objects       |
| `re.sub()`      | Replaces occurrences of a pattern with a replacement |
| `re.split()`    | Splits a string by the occurrences of a pattern  |
| `re.compile()`  | Compiles a regex pattern into a regex object for reuse |

---

## 🔹 Special Characters and Metacharacters

| Metacharacter | Meaning                          |
|---------------|----------------------------------|
| `.`           | Matches any character (except newline) |
| `^`           | Matches the start of the string  |
| `$`           | Matches the end of the string    |
| `*`           | Matches 0 or more repetitions    |
| `+`           | Matches 1 or more repetitions    |
| `?`           | Matches 0 or 1 repetition        |
| `{m,n}`       | Matches from m to n repetitions  |
| `[]`          | Matches any one character in brackets |
| `|`           | Acts like an OR                  |
| `\`          | Escapes special characters or signals a special sequence |

---

## 🔹 Special Sequences

| Sequence | Meaning                        |
|----------|--------------------------------|
| `\d`    | Matches any digit, same as `[0-9]` |
| `\D`    | Matches any non-digit          |
| `\s`    | Matches whitespace (space, tab, newline) |
| `\S`    | Matches any non-whitespace     |
| `\w`    | Matches word characters (alphanumeric + underscore) |
| `\W`    | Matches non-word characters    |
| `\b`    | Matches word boundary          |
| `\B`    | Matches non-word boundary      |

---

## 🔹 Examples and Usage

### ✅ `re.match()`

```python
import re
result = re.match(r'Hello', 'Hello world!')
print(result.group())  # Output: Hello
```

### ✅ `re.search()`

```python
match = re.search(r'world', 'Hello world!')
print(match.group())  # Output: world
```

### ✅ `re.findall()`

```python
numbers = re.findall(r'\d+', 'There are 12 apples and 20 oranges')
print(numbers)  # Output: ['12', '20']
```

### ✅ `re.sub()`

```python
cleaned = re.sub(r'\s+', '-', 'Python     Regex    Tutorial')
print(cleaned)  # Output: Python-Regex-Tutorial
```

### ✅ `re.split()`

```python
parts = re.split(r'[,;]', 'apple,orange;banana')
print(parts)  # Output: ['apple', 'orange', 'banana']
```

---

## 🔹 Raw Strings (`r''`) in Regex

In Python, regex patterns are often written as raw strings (`r''`) to avoid confusion with escape characters.

```python
pattern = r"\d{3}"
```

---

## 🔹 Regex with Groups

Grouping allows parts of patterns to be extracted separately:

```python
text = "Name: Alice, Age: 30"
match = re.search(r'Name: (\w+), Age: (\d+)', text)
print(match.group(1))  # Output: Alice
print(match.group(2))  # Output: 30
```

---

## 🔹 Compiling Patterns

For repeated use of the same regex pattern:

```python
pattern = re.compile(r'\d+')
matches = pattern.findall("Numbers: 12 45 78")
print(matches)  # Output: ['12', '45', '78']
```

---

## 🔹 Greedy vs Non-Greedy Matching

- Greedy (`.*`) matches as much as possible.
- Non-Greedy (`.*?`) matches as little as possible.

```python
text = "<tag>content</tag><tag>more</tag>"
greedy = re.findall(r'<tag>.*</tag>', text)
non_greedy = re.findall(r'<tag>.*?</tag>', text)
print(greedy)       # Output: ['<tag>content</tag><tag>more</tag>']
print(non_greedy)   # Output: ['<tag>content</tag>', '<tag>more</tag>']
```

---

## 🔹 Real-Life Examples

### 1. Validate Email Address

```python
email = "test@example.com"
if re.match(r'^\w+@\w+\.\w+$', email):
    print("Valid email")
```

### 2. Extract All Hashtags

```python
tweet = "Loving #Python and #AI"
hashtags = re.findall(r'#\w+', tweet)
print(hashtags)  # Output: ['#Python', '#AI']
```

---

## 🔹 Summary

Regular expressions are a powerful tool for:
- String validation
- Data extraction
- Cleaning and transforming text
- Searching and replacing patterns

Although initially tricky, they are indispensable for text processing once mastered.
