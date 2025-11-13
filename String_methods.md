#  Strings
 - A **string** in Python is an immutable sequence of Unicode characters used to store and manipulate textual data. Strings can be created with single quotes (`'...'`), double quotes (`"..."`), or triple quotes (`'''...'''` / `"""..."""`) for multi-line text.


## String Methods
| **Method**     | **Description**                                                | **Example**                                         |
| -------------- | -------------------------------------------------------------- | --------------------------------------------------- |
| `capitalize()` | Converts the first character to uppercase                      | `"hello".capitalize()` → `Hello`                    |
| `casefold()`   | Converts string to lowercase (more aggressive than `lower()`)  | `"HELLO".casefold()` → `hello`                      |
| `count(sub)`   | Counts occurrences of substring                                | `"banana".count("a")`                               |
| `endswith()`   | Returns True if the string ends with the specified substring   | `"notes.pdf".endswith(".pdf")` → `True`             |
| `find()`       | Returns the index of the first occurrence, or -1 if not found  | `"hello".find("l")` → `2`                           |
| `isalnum()`    | True if all characters are alphanumeric                        | `"abc123".isalnum()` → `True`                       |
| `isalpha()`    | True if all characters are alphabets                           | `"Hima".isalpha()` → `True`                         |
| `isdigit()`    | True if all characters are digits                              | `"12345".isdigit()` → `True`                        |
| `join()`       | Joins elements of an iterable with the string as a separator   | `"-".join(["2025","11","13"])` → `"2025-11-13"`     |
| `lower()`      | Converts all characters to lowercase                           | `"HELLO".lower()` → `hello`                         |
| `upper()`      | Converts all characters to uppercase                           | `"hello".upper()` → `HELLO`                         |
| `title()`      | Capitalizes each word                                          | `"python programming".title()`                      |
| `replace()`    | Replaces a substring with another                              | `"hi Hima".replace("hi", "hello")` → `"hello Hima"` |
| `split()`      | Splits the string into a list                                  | `"a,b,c".split(",")` → `['a','b','c']`              |
| `startswith()` | Returns True if the string starts with the specified substring | `"Python".startswith("Py")` → `True`                |
| `strip()`      | Removes whitespace from both ends                              | `"  hello  ".strip()` → `"hello"`                   |
| `zip()`        | Pairs characters from two or more strings into tuples          | `list(zip("abc", "123"))` → `[('a','1'), ('b','2'), ('c','3')]`                |
| `swapcase()`   | Converts uppercase letters to lowercase and lowercase letters to uppercase | `"HeLLo".swapcase()` → `"hEllO"`        |

  
## Key Points
 ### 1.Strings are immutable
  - Once created, individual characters cannot be changed.
  ```python
  s = "hello"
  # s[0] = "H"  # This will raise an error
  ```
 ### 2. Strings support indexing and slicing
 - You can access characters and extract substrings using index ranges.
 ### 3. Strings allow concatenation and repetition
 - Use `+` to join strings and `*` to repeat them.
 ### 4. Strings come with powerful built-in methods
 - Methods like `upper()`, `lower()`, `find()`, `replace()`, and `split()` make text processing easier.

# References

#### Python Official Documentation
- https://docs.python.org/3/tutorial/datastructures.html
#### W3Schools References
- https://www.w3schools.com/python/python_strings.asp
- https://www.w3schools.com/python/python_strings_methods.asp
#### GeeksforGeeks References
- https://www.geeksforgeeks.org/python-strings/


