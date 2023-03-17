## Regular expressions

A __Regular Expression__ (RegEx) is a sequence of characters that defines a search pattern. For example,
Python has a module named re to work with RegEx. Here's an example:
```python
^a...s$
```

Python has a module named re to work with RegEx. Here's an example:

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

### Examples
the whole words colour and color case insensitive with \b[Cc]olou?r\b|\bCOLOU?R\b or /colou?r/i

Date formats like dd-MM-yyyy with \b\d{2}-\d{2}-\d{4}\b

dd-MM-yyyy or dd-MM-yy at the beginning of a line with ^\d{2}-\d{2}-\d{2,4}
