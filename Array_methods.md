# 1 Arrays
  - Python does not have built-in support for Arrays, but Python Lists can be used instead.
  - Lists are used to store multiple values in one single variable
  - List items are ordered, changeable, and allow duplicate values.
  - List items are indexed, the first item has index [0], the second item has index [1] etc.
  - A List is an ordered data structure with elements seperated by a comma and enclosed within square brackets.
  - List can store all type of data (String,Integer,Boolean,Float)
    ```
    Ex :["ABC",34,True,4.55,]
    ```
## List Methods
| **Method**  | **Description**                                                          | **Example**                                          |
| ----------- | ------------------------------------------------------------------------ | ---------------------------------------------------- |
| `append()`  | Adds an element at the end of the list                                   | `nums = [1, 2]; nums.append(3)  # [1, 2, 3]`         |
| `clear()`   | Removes all elements from the list (list becomes empty but still exists) | `nums = [1, 2]; nums.clear()  # []`                  |
| `copy()`    | Returns a shallow copy of the list                                       | `a = [1, 2]; b = a.copy()  # b = [1, 2]`             |
| `count()`   | Returns the number of times a value appears                              | `nums = [1, 2, 2]; nums.count(2)  # 2`               |
| `extend()`  | Adds elements of another iterable to the end                             | `nums = [1, 2]; nums.extend([3, 4])  # [1, 2, 3, 4]` |
| `index()`   | Returns the index of the first occurrence of a value                     | `nums = [10, 20, 30]; nums.index(20)  # 1`           |
| `insert()`  | Inserts an element at a specific position                                | `nums = [1, 3]; nums.insert(1, 2)  # [1, 2, 3]`      |
| `pop()`     | Removes and returns element at a given position (default last)           | `nums = [1, 2, 3]; nums.pop(1)  # returns 2`         |
| `remove()`  | Removes the first occurrence of the specified value                      | `nums = [1, 2, 2]; nums.remove(2)  # [1, 2]`         |
| `reverse()` | Reverses the list order                                                  | `nums = [1, 2, 3]; nums.reverse()  # [3, 2, 1]`      |
| `sort()`    | Sorts the list in ascending order                                        | `nums = [3, 1, 2]; nums.sort()  # [1, 2, 3]`         |


## Key points
 ### 1.append() adds one item only
  - It always adds the element as a single item at the end.
  - If you append a list, it becomes a nested list.
  ```
    EX : a.append([3,4]) → [1,2,[3,4]]
  ````
### 2.extend() adds multiple items
  - Use it when adding elements from another list or iterable.
  - It does not create nested lists.
 ```
    Ex : a.extend([3,4]) → [1,2,3,4]
 ```
### 3.remove() deletes the first matching value
  - Removes only the first occurrence of the specified item.
  - Gives ValueError if the item does not exist.
 ```
    EX: a.remove(2) → removes first 2
 ```
### 4.sort() sorts the list in-place
 - It modifies the original list (cannot be undone).
 - Use sorted() if you want a new sorted list without changing the original.
 ```
    EX: a.sort() → [1,2,3,4]
 ```
# 2 Strings
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
- https://docs.python.org/3/tutorial/datastructures.html
- https://www.w3schools.com/python/python_strings_methods.asp
- https://www.geeksforgeeks.org/python-strings/
- https://www.geeksforgeeks.org/python-list/





  
