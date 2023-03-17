## Regular expressions

- A __Regular Expression__ (RegEx) is a sequence of characters that defines a search pattern. 
-  Regular Expression is beneficial for extracting information from text such as code, files, logs, spreadsheets, or even documents. 
- In simple words, RegEx is a combination of letters, symbols, and numbers you can use to search for things within a longer text. 
### For example,
Python has a module named re to work with RegEx. Here's an example:
```python
^a...s$
```

Python has a module named **_re_** to work with RegEx. Here's an example:

```python
import re

pattern = '^f.r$'
test_string = 'information'
result = re.match(pattern, test_string)

if result:
  print("Search successful.")
else:
  print("Search unsuccessful.")	
  
```
### Metacharacters are characters that are interpreted in a special way by a RegEx engine. Here's a list of metacharacters:

[] . ^ $ * + ? {} () \ |

### Common regex metacharacters
Square brackets define a list or range of characters to be found:

- [abc] matches a, b or c
- [a-z] matches any lower case letter
- [A-Za-z] matches any letter
- [A-Za-z0-9] matches any letter or any digit

### Useful special characters:

- . matches any single character

- * matches the preceding element zero or more times, e.g. colou*r matches color, colour, colouur, etc.

- ? matches when the preceding character appears zero or one time, e.g. colou?r matches color and colour

- + matches the preceding element one or more times, e.g. .+ matches ., .., ... etc.

- {N} matches the preceding character N times

- {N,} matches the preceding character N or more times

{N,M} matches the preceding character at least N times, but not more than M times

- \ used to escape the following character when that character is a special character e.g. to find .org you have to use the regular expression \.org because . is the special character that matches any character

^ asserts the position at the start of the line

- $ asserts the position at the end of the line

- | means or

## And then there are:

- \d matches any single digit

- \w matches any part of word character and is equivalent to [A-Za-z0-9]

- \s matches any space, tab, or newline

- \b asserts that the pattern must match at a word boundary

- /i renders an expression case-insensitive equivalent to [A-Za-z]

### Examples: Re modile functions
The RegEx mechanism comes with the module named re, and it provides many functions.

### re.match() Function

The re.match() function of the re module in Python searches for the regular expression pattern and returns the first occurrence. 

```python
import re

pattern = "C"

sequence1 = "IceCream"

sequence2 = "Catch"

print("Sequence 1: ", re.match(pattern, sequence1))

print("Sequence 2: ", re.match(pattern,sequence2).group())
```

#### re.search() Function

The re.search() function searches for the regular expression pattern and returns the first occurrence in a string.

```python
import re

patterns = ["Software testing", "Dan"]

my_string = "Software testing is a tough job"

for pattern in patterns:

    print("Looking for '%s' in '%s' " % (pattern, my_string), end='')

    if re.search(pattern,my_string):

        print("Here is a match case")

    else:

        print("Not a match")
```

### re.findall() Function

The re.findall() method returns a list of strings containing all the matching cases from the input text upon provided pattern.
```python
import re

my_string1 = "Hello 10 Dan 20. Howdy? 30"

my_string2 = "Hello Dan Howdy?"

pattern = '\d+'

result1 = re.findall(pattern, my_string1)

result2 = re.findall(pattern, my_string2)

print(result1)

print(result2)
```
