#  Dictionaries
 - Dictionaries are used to store data values in key:value pairs.
 - A dictionary is a collection which is ordered*, changeable and do not allow duplicates.
 - Python dictionary is a data structure that stores the value in key: value pairs. Values in a dictionary can be of any data type and can be duplicated, whereas keys can't be repeated and must be immutable.
     - Keys are case sensitive which means same name but different cases of Key will be treated distinctly.
     - Keys must be immutable which means keys can be strings, numbers or tuples but not lists.
     - Duplicate keys are not allowed and any duplicate key will overwrite the previous value.
 - Internally uses hashing. Hence, operations like search, insert, delete can be performed in Constant Time.
 - From Python 3.7 Version onward, Python dictionary are Ordered, but you cannot index like lists.In Python 3.6 and earlier, dictionaries are unordered.

## Dictionary Methods
| **Method**     | **Description**                                                                                      | **Example**                                                       |
| -------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------|
| `clear()`      | Removes all items from the dictionary                                                                | `d = {"a":1, "b":2}; d.clear();  # d = {}`                        |
| `copy()`       | Returns a shallow copy of the dictionary                                                             | `d1 = {"x":10}; d2 = d1.copy();  # d2 = {"x":10}`                 |
| `fromkeys()`   | Creates a new dictionary with specified keys and a single value                                      | `keys = ["a","b"]; d = dict.fromkeys(keys, 0);  # {"a":0, "b":0}` |
| `get()`        | Returns the value of the specified key (or `None`/default if key not found)                          | `d = {"name":"Hima"}; d.get("name");  # "Hima"`                   |
| `items()`      | Returns view object of key-value pairs (tuples)                                                      | `d = {"a":1,"b":2}; list(d.items());  # [("a",1),("b",2)]`        |
| `keys()`       | Returns view object of all keys in the dictionary                                                    | `d = {"a":1,"b":2}; list(d.keys());  # ["a","b"]`                 |
| `pop()`        | Removes the item with the specified key and returns its value                                        | `d = {"a":1,"b":2}; val = d.pop("a");  # val=1, d={"b":2}`        |
| `popitem()`    | Removes the last inserted key-value pair and returns it (Python 3.7+)                                | `d = {"a":1,"b":2}; item = d.popitem();  # item=("b",2)`          |
| `setdefault()` | Returns value of specified key; if key not present, inserts it with specified default value          | `d = {"a":1}; v = d.setdefault("b",2);  # v=2, d={"a":1,"b":2}`   |
| `update()`     | Updates dictionary with key-value pairs from another dict or iterable; existing keys get overwritten | `d={"a":1}; d.update({"a":10,"b":2});  # d={"a":10,"b":2}`        |
| `values()`     | Returns view object of all values in the dictionary                                                  | `d = {"a":1,"b":2}; list(d.values());  # [1,2]`                   |

## Key Points
### 1. Dictionaries are mutable
- You can add, update, or remove key–value pairs anytime.
### 2. Keys must be unique and immutable
- Keys can be strings, numbers, tuples—but **not lists or other dictionaries**.
### 3. `get()` is safer than direct access
- It avoids errors when a key doesn’t exist and allows default values.
### 4. Can store complex and nested data
- Values can be lists, other dictionaries, or even objects.
### 5. Built-in methods make modification easier
- Methods like `update()`, `pop()`, `keys()`, and `values()` simplify operations.

# References

### Python Official Documentation
- https://docs.python.org/3/tutorial/datastructures.html
### W3Schools References
- https://www.w3schools.com/python/python_dictionaries.asp
- https://www.w3schools.com/python/python_dictionaries_methods.asp
### GeeksforGeeks References
- https://www.geeksforgeeks.org/python-strings/
- https://www.geeksforgeeks.org/python-list/
- https://www.geeksforgeeks.org/python-dictionary/
### Programiz References
- https://www.programiz.com/python-programming/dictionary

