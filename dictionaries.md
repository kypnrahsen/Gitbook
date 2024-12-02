# Dictionaries



## What is dictionary in Python?

In Python, a **dictionary** is a collection data type that is used to store data in **key-value pairs**. It is one of Python's built-in data structures and is highly versatile.

### Key Features of Dictionaries

1. **Key-Value Pairs**:
   * Data is stored in the format `{key: value}`.
   * Keys are unique and immutable (e.g., strings, numbers, or tuples).
   * Values can be of any data type and can even be mutable objects.
2. **Unordered**: Dictionaries are unordered until Python 3.6, but starting from Python 3.7+, dictionaries maintain the insertion order of keys.&#x20;
3. **Mutable**: You can add, remove, or modify key-value pairs after the dictionary is created.
4. **Fast Access**: Dictionary lookups are optimized using hash tables, making them efficient for retrieving values by keys.

### Syntax

**Creating a Dictionary:**

```
# Empty dictionary
my_dict = {}

# Dictionary with data
my_dict = {
    "name": "Alice",
    "age": 25,
    "city": "New York"
}
print(my_dict)  # Output: {'name': 'Alice', 'age': 25, 'city': 'New York'}

```

In Python, you can create a dictionary using the **`dict()`** constructor. This method provides several flexible ways to define key-value pairs.

```
my_dict = dict()
print(my_dict)  # Output: {}
```

```
my_dict = dict(name="Alice", age=25, city="New York")
print(my_dict)  # Output: {'name': 'Alice', 'age': 25, 'city': 'New York'}
```

You can use `dict()` with an iterable (like a list or tuple) containing key-value pairs as 2-item tuples:

```
# Using a list of tuples
key_value_pairs = [("name", "Bob"), ("age", 30), ("city", "London")]
my_dict = dict(key_value_pairs)
print(my_dict)  # Output: {'name': 'Bob', 'age': 30, 'city': 'London'}

# Using a tuple of tuples
key_value_pairs = (("name", "Carol"), ("age", 35))
my_dict = dict(key_value_pairs)
print(my_dict)  # Output: {'name': 'Carol', 'age': 35}

```

Similar to tuples, you can use a list of lists where each list has exactly two elements (key, value):

```
key_value_pairs = [["name", "Dan"], ["age", 40], ["city", "Berlin"]]
my_dict = dict(key_value_pairs)
print(my_dict)  # Output: {'name': 'Dan', 'age': 40, 'city': 'Berlin'}

```

If you have a set of 2-item tuples, you can use `dict()` to convert it into a dictionary:

```
key_value_pairs = {("name", "Eve"), ("age", 28)}
my_dict = dict(key_value_pairs)
print(my_dict)  # Output: {'name': 'Eve', 'age': 28}

```

You can use `dict()` to create a new dictionary from an existing dictionary:

```
original_dict = {"name": "Frank", "age": 32}
new_dict = dict(original_dict)
print(new_dict)  # Output: {'name': 'Frank', 'age': 32}
```

While not directly using `dict()`, dictionary comprehensions can be combined with it:

```
# Generating key-value pairs dynamically
squares = dict((x, x**2) for x in range(5))
print(squares)  # Output: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

You can convert a string of characters into a dictionary, using `dict()` along with `zip()`:

```
keys = "abc"
values = [1, 2, 3]
my_dict = dict(zip(keys, values))
print(my_dict)  # Output: {'a': 1, 'b': 2, 'c': 3}

```

You can create a dictionary from `enumerate()`:

```
my_dict = dict(enumerate(["Python", "Java", "C++"]))
print(my_dict)  # Output: {0: 'Python', 1: 'Java', 2: 'C++'}
```

In Python, you can create a dictionary using the **`dict()`** constructor. This method provides several flexible ways to define key-value pairs.

***

#### **1. Creating an Empty Dictionary**

You can create an empty dictionary by calling `dict()` without any arguments:

```python
my_dict = dict()
print(my_dict)  # Output: {}
```

***

#### **2. Creating a Dictionary with Key-Value Pairs**

You can pass key-value pairs as **keyword arguments** to `dict()`:

```python
my_dict = dict(name="Alice", age=25, city="New York")
print(my_dict)  # Output: {'name': 'Alice', 'age': 25, 'city': 'New York'}
```

***

#### **3. Creating a Dictionary from an Iterable of Tuples**

You can use `dict()` with an iterable (like a list or tuple) containing key-value pairs as 2-item tuples:

```python
# Using a list of tuples
key_value_pairs = [("name", "Bob"), ("age", 30), ("city", "London")]
my_dict = dict(key_value_pairs)
print(my_dict)  # Output: {'name': 'Bob', 'age': 30, 'city': 'London'}

# Using a tuple of tuples
key_value_pairs = (("name", "Carol"), ("age", 35))
my_dict = dict(key_value_pairs)
print(my_dict)  # Output: {'name': 'Carol', 'age': 35}
```

***

#### **4. Creating a Dictionary from a List of Lists**

Similar to tuples, you can use a list of lists where each list has exactly two elements (key, value):

```python
key_value_pairs = [["name", "Dan"], ["age", 40], ["city", "Berlin"]]
my_dict = dict(key_value_pairs)
print(my_dict)  # Output: {'name': 'Dan', 'age': 40, 'city': 'Berlin'}
```

***

#### **5. Creating a Dictionary from a Set of Tuples**

If you have a set of 2-item tuples, you can use `dict()` to convert it into a dictionary:

```python
key_value_pairs = {("name", "Eve"), ("age", 28)}
my_dict = dict(key_value_pairs)
print(my_dict)  # Output: {'name': 'Eve', 'age': 28}
```

***

#### **6. Creating a Dictionary from Another Dictionary**

You can use `dict()` to create a new dictionary from an existing dictionary:

```python
original_dict = {"name": "Frank", "age": 32}
new_dict = dict(original_dict)
print(new_dict)  # Output: {'name': 'Frank', 'age': 32}
```

***

#### **7. Using Dictionary Comprehensions**

While not directly using `dict()`, dictionary comprehensions can be combined with it:

```python
# Generating key-value pairs dynamically
squares = dict((x, x**2) for x in range(5))
print(squares)  # Output: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

***

#### **8. Converting Other Data Structures**

**From a String:**

You can convert a string of characters into a dictionary, using `dict()` along with `zip()`:

```python
keys = "abc"
values = [1, 2, 3]
my_dict = dict(zip(keys, values))
print(my_dict)  # Output: {'a': 1, 'b': 2, 'c': 3}
```

**From Enumerate:**

You can create a dictionary from `enumerate()`:

```python
my_dict = dict(enumerate(["Python", "Java", "C++"]))
print(my_dict)  # Output: {0: 'Python', 1: 'Java', 2: 'C++'}
```

***

#### Summary Table of `dict()` Usage

| **Input Type**     | **Example**                        | **Output**                 |
| ------------------ | ---------------------------------- | -------------------------- |
| Empty              | `dict()`                           | `{}`                       |
| Keyword Arguments  | `dict(a=1, b=2)`                   | `{'a': 1, 'b': 2}`         |
| Iterable of Tuples | `dict([("a", 1), ("b", 2)])`       | `{'a': 1, 'b': 2}`         |
| List of Lists      | `dict([["a", 1], ["b", 2]])`       | `{'a': 1, 'b': 2}`         |
| Set of Tuples      | `dict({("a", 1), ("b", 2)})`       | `{'a': 1, 'b': 2}`         |
| Another Dictionary | `dict({"a": 1, "b": 2})`           | `{'a': 1, 'b': 2}`         |
| From `zip`         | `dict(zip("ab", [1, 2]))`          | `{'a': 1, 'b': 2}`         |
| From Enumerate     | `dict(enumerate(["x", "y", "z"]))` | `{0: 'x', 1: 'y', 2: 'z'}` |

The `dict()` constructor is versatile and works well in different scenarios for creating dictionaries!



The **`fromkeys()`** method in Python is used to create a new dictionary with specified keys and a common default value.

```
keys = ["a", "b", "c"]
default_value = 0

my_dict = dict.fromkeys(keys, default_value)
print(my_dict)  # Output: {'a': 0, 'b': 0, 'c': 0}
```

```
keys = ["x", "y", "z"]

my_dict = dict.fromkeys(keys)
print(my_dict)  # Output: {'x': None, 'y': None, 'z': None}
```

```
keys = "abc"
my_dict = dict.fromkeys(keys, 1)
print(my_dict)  # Output: {'a': 1, 'b': 1, 'c': 1}

```

```
keys = ["a", "b", "c"]
my_dict = dict.fromkeys(keys, [])

# Modifying one key affects all keys
my_dict["a"].append(1)
print(my_dict)  # Output: {'a': [1], 'b': [1], 'c': [1]}

```

If you want independent mutable values for each key, use a dictionary comprehension instead:

```
keys = ["a", "b", "c"]
my_dict = {key: [] for key in keys}
my_dict["a"].append(1)
print(my_dict)  # Output: {'a': [1], 'b': [], 'c': []}
```



### How can I access the elements in the Dictionary?

You can access elements in a dictionary in Python by using the **keys** to retrieve the associated values. Here are the primary ways to access dictionary elements:

1. **Using Square Brackets (`[]`):**&#x59;ou can directly access a value by its key using square brackets.

* If the key exists, it returns the corresponding value.
* If the key does **not exist**, it raises a `KeyError`.

```
my_dict = {"name": "Alice", "age": 25, "city": "New York"}
print(my_dict["name"])  # Output: Alice
print(my_dict["age"])   # Output: 25
```

2. **Using the `get()` Method:**&#x54;he `get()` method retrieves a value for a given key, but it avoids raising an error if the key does not exist.

```
my_dict = {"name": "Alice", "age": 25, "city": "New York"}
print(my_dict.get("name"))  # Output: Alice
print(my_dict.get("country"))  # Output: None
```

You can provide a default value to return if the key is missing:

```
print(my_dict.get("country", "Not Found"))  # Output: Not Found
```

3. **Accessing All Keys:**&#x54;o get a list of all keys in the dictionary, use the `keys()` method.

```
my_dict = {"name": "Alice", "age": 25, "city": "New York"}
keys = my_dict.keys()
print(keys)  # Output: dict_keys(['name', 'age', 'city'])
```

You can convert the `dict_keys` object to a list:

```
keys_list = list(my_dict.keys())
print(keys_list)  # Output: ['name', 'age', 'city']
```

4. **Accessing All Values:**&#x54;o get all the values in the dictionary, use the `values()` method.

```
my_dict = {"name": "Alice", "age": 25, "city": "New York"}
values = my_dict.values()
print(values)  # Output: dict_values(['Alice', 25, 'New York'])
```

Convert values to a list:

```
values_list = list(my_dict.values())
print(values_list)  # Output: ['Alice', 25, 'New York']
```

5. **Accessing All Key-Value Pairs:**&#x54;o access all key-value pairs, use the `items()` method. This returns a view of key-value tuples.

```
my_dict = {"name": "Alice", "age": 25, "city": "New York"}
items = my_dict.items()
print(items)  # Output: dict_items([('name', 'Alice'), ('age', 25), ('city', 'New York')])

```

* You can iterate through key-value pairs:

```
for key, value in my_dict.items():
    print(f"{key}: {value}")
# Output:
# name: Alice
# age: 25
# city: New York
```

6. &#x20;**Checking if a Key Exists:**

Use the `in` keyword to check if a key exists in the dictionary.

```
my_dict = {"name": "Alice", "age": 25, "city": "New York"}
print("name" in my_dict)  # Output: True
print("country" in my_dict)  # Output: False
```

7. **Accessing Elements in a Nested Dictionary:**

If the dictionary contains other dictionaries as values, use multiple keys to access the nested data.

```
nested_dict = {
    "person": {
        "name": "Alice",
        "age": 25,
        "city": "New York"
    },
    "job": "Engineer"
}

print(nested_dict["person"]["name"])  # Output: Alice
print(nested_dict["person"]["city"])  # Output: New York

```

8. **Handling Missing Keys:**

If you're unsure whether a key exists, use `get()` or check for the key using `in` to avoid errors:

```
my_dict = {"name": "Alice", "age": 25}

# Using get()
print(my_dict.get("city", "Not Available"))  # Output: Not Available

# Checking key existence
if "city" in my_dict:
    print(my_dict["city"])
else:
    print("City not found!")
```

## How to add or update an element in dictionary?

### Adding a New Element:

You can add a new element to a dictionary by specifying a new key and assigning it a value.

```
my_dict = {"name": "Alice", "age": 25}
my_dict["city"] = "New York"  # Adding a new key-value pair
print(my_dict)  # Output: {'name': 'Alice', 'age': 25, 'city': 'New York'}
```

### Updating an Existing Element:

If the key already exists, assigning a value to that key will update the existing value.

```
my_dict = {"name": "Alice", "age": 25}
my_dict["age"] = 26  # Updating the value for the key 'age'
print(my_dict)  # Output: {'name': 'Alice', 'age': 26}
```

### Using the `update()` Method:

The `update()` method allows you to add multiple key-value pairs or update existing ones in a single call.

```
my_dict = {"name": "Alice", "age": 25}

# Adding or updating elements
my_dict.update({"city": "New York", "age": 26})
print(my_dict)  # Output: {'name': 'Alice', 'age': 26, 'city': 'New York'}
```

### Adding or Updating with Variable Keys:

You can dynamically add or update dictionary elements using variables as keys.

```
my_dict = {"name": "Alice"}
key = "age"
value = 25
my_dict[key] = value  # Adding an element dynamically
print(my_dict)  # Output: {'name': 'Alice', 'age': 25}
```

### Adding or Updating Nested Dictionary Elements:

For nested dictionaries, you can add or update elements within the nested structure by referencing the nested key.

```
nested_dict = {
    "person": {
        "name": "Alice",
        "age": 25
    }
}

# Updating an existing nested value
nested_dict["person"]["age"] = 26

# Adding a new key-value pair in the nested dictionary
nested_dict["person"]["city"] = "New York"

print(nested_dict)
# Output:
# {'person': {'name': 'Alice', 'age': 26, 'city': 'New York'}}

```

### Adding Multiple Elements Dynamically:

You can add multiple elements dynamically using a loop.

```
my_dict = {}
new_entries = [("name", "Alice"), ("age", 25), ("city", "New York")]

for key, value in new_entries:
    my_dict[key] = value

print(my_dict)
# Output: {'name': 'Alice', 'age': 25, 'city': 'New York'}

```



## Other Dictionary Methods:

Python provides a variety of dictionary methods for managing and manipulating dictionaries. Here’s a comprehensive list with explanations and examples:

1. **clear():**&#x52;emoves all items from the dictionary, leaving it empty.

```
my_dict = {"name": "Alice", "age": 25}
my_dict.clear()
print(my_dict)  # Output: {}
```

2. **copy():** Returns a shallow copy of the dictionary.

```
original = {"name": "Alice", "age": 25}
copy_dict = original.copy()
print(copy_dict)  # Output: {'name': 'Alice', 'age': 25}
```

3. **fromkeys(keys, value):**&#x43;reates a new dictionary with the specified keys and a shared value. The default value is `None`.

```
keys = ["name", "age", "city"]
new_dict = dict.fromkeys(keys, "unknown")
print(new_dict)  # Output: {'name': 'unknown', 'age': 'unknown', 'city': 'unknown'}

```

4. **`get(key, default):`**&#x52;eturns the value for the specified key. If the key is not found, it returns the default value (or `None` if no default is provided).

```
my_dict = {"name": "Alice", "age": 25}
print(my_dict.get("name"))  # Output: Alice
print(my_dict.get("country", "Not Found"))  # Output: Not Found
```

5. **items():**&#x52;eturns a view object that displays a list of dictionary’s key-value pairs as tuples.

```
my_dict = {"name": "Alice", "age": 25}
print(my_dict.items())  # Output: dict_items([('name', 'Alice'), ('age', 25)])
```

6. **keys():**&#x52;eturns a view object containing all the keys in the dictionary.

```
my_dict = {"name": "Alice", "age": 25}
print(my_dict.keys())  # Output: dict_keys(['name', 'age'])
```

7. **pop(key, default):**&#x52;emoves the specified key and returns its value. If the key is not found, it returns the default value (or raises a `KeyError` if no default is provided).

```
my_dict = {"name": "Alice", "age": 25}
age = my_dict.pop("age")
print(age)       # Output: 25
print(my_dict)   # Output: {'name': 'Alice'}

```

8. **popitem():**&#x52;emoves and returns the last inserted key-value pair as a tuple (in Python 3.7+). Raises a `KeyError` if the dictionary is empty.

```
my_dict = {"name": "Alice", "age": 25}
last_item = my_dict.popitem()
print(last_item)  # Output: ('age', 25)
print(my_dict)    # Output: {'name': 'Alice'}
```

9. **setdefault(key, default):**&#x52;eturns the value of the specified key. If the key does not exist, inserts the key with the specified default value.

```
my_dict = {"name": "Alice"}
city = my_dict.setdefault("city", "New York")
print(city)      # Output: New York
print(my_dict)   # Output: {'name': 'Alice', 'city': 'New York'}
```

10. **update(\[other]):**&#x55;pdates the dictionary with key-value pairs from another dictionary or iterable of key-value pairs. Existing keys will be overwritten.

```
my_dict = {"name": "Alice", "age": 25}
my_dict.update({"age": 26, "city": "New York"})
print(my_dict)  # Output: {'name': 'Alice', 'age': 26, 'city': 'New York'}
```

11. **values():**&#x52;eturns a view object containing all the values in the dictionary.

```
my_dict = {"name": "Alice", "age": 25}
print(my_dict.values())  # Output: dict_values(['Alice', 25])
```

12. **len():** (Not a method, but a built-in function) Returns the number of items (key-value pairs) in the dictionary.

```
my_dict = {"name": "Alice", "age": 25}
print(len(my_dict))  # Output: 2
```

13. **`in` (Membership Test):**(Not a method, but a built-in operator) Checks if a key exists in the dictionary.

```
my_dict = {"name": "Alice", "age": 25}
print("name" in my_dict)  # Output: True
print("city" in my_dict)  # Output: False
```



Python provides a variety of dictionary methods for managing and manipulating dictionaries. Here’s a comprehensive list with explanations and examples:

***

#### **1. `clear()`**

Removes all items from the dictionary, leaving it empty.

```python
my_dict = {"name": "Alice", "age": 25}
my_dict.clear()
print(my_dict)  # Output: {}
```

***

#### **2. `copy()`**

Returns a shallow copy of the dictionary.

```python
original = {"name": "Alice", "age": 25}
copy_dict = original.copy()
print(copy_dict)  # Output: {'name': 'Alice', 'age': 25}
```

***

#### **3. `fromkeys(keys, value)`**

Creates a new dictionary with the specified keys and a shared value. The default value is `None`.

```python
keys = ["name", "age", "city"]
new_dict = dict.fromkeys(keys, "unknown")
print(new_dict)  # Output: {'name': 'unknown', 'age': 'unknown', 'city': 'unknown'}
```

***

#### **4. `get(key, default)`**

Returns the value for the specified key. If the key is not found, it returns the default value (or `None` if no default is provided).

```python
my_dict = {"name": "Alice", "age": 25}
print(my_dict.get("name"))  # Output: Alice
print(my_dict.get("country", "Not Found"))  # Output: Not Found
```

***

#### **5. `items()`**

Returns a view object that displays a list of dictionary’s key-value pairs as tuples.

```python
my_dict = {"name": "Alice", "age": 25}
print(my_dict.items())  # Output: dict_items([('name', 'Alice'), ('age', 25)])
```

***

#### **6. `keys()`**

Returns a view object containing all the keys in the dictionary.

```python
my_dict = {"name": "Alice", "age": 25}
print(my_dict.keys())  # Output: dict_keys(['name', 'age'])
```

***

#### **7. `pop(key, default)`**

Removes the specified key and returns its value. If the key is not found, it returns the default value (or raises a `KeyError` if no default is provided).

```python
my_dict = {"name": "Alice", "age": 25}
age = my_dict.pop("age")
print(age)       # Output: 25
print(my_dict)   # Output: {'name': 'Alice'}
```

***

#### **8. `popitem()`**

Removes and returns the last inserted key-value pair as a tuple (in Python 3.7+). Raises a `KeyError` if the dictionary is empty.

```python
my_dict = {"name": "Alice", "age": 25}
last_item = my_dict.popitem()
print(last_item)  # Output: ('age', 25)
print(my_dict)    # Output: {'name': 'Alice'}
```

***

#### **9. `setdefault(key, default)`**

Returns the value of the specified key. If the key does not exist, inserts the key with the specified default value.

```python
my_dict = {"name": "Alice"}
city = my_dict.setdefault("city", "New York")
print(city)      # Output: New York
print(my_dict)   # Output: {'name': 'Alice', 'city': 'New York'}
```

***

#### **10. `update([other])`**

Updates the dictionary with key-value pairs from another dictionary or iterable of key-value pairs. Existing keys will be overwritten.

```python
my_dict = {"name": "Alice", "age": 25}
my_dict.update({"age": 26, "city": "New York"})
print(my_dict)  # Output: {'name': 'Alice', 'age': 26, 'city': 'New York'}
```

***

#### **11. `values()`**

Returns a view object containing all the values in the dictionary.

```python
my_dict = {"name": "Alice", "age": 25}
print(my_dict.values())  # Output: dict_values(['Alice', 25])
```

***

#### **12. `len()`**

(Not a method, but a built-in function) Returns the number of items (key-value pairs) in the dictionary.

```python
my_dict = {"name": "Alice", "age": 25}
print(len(my_dict))  # Output: 2
```

***

#### **13. `in` (Membership Test)**

(Not a method, but a built-in operator) Checks if a key exists in the dictionary.

```python
my_dict = {"name": "Alice", "age": 25}
print("name" in my_dict)  # Output: True
print("city" in my_dict)  # Output: False
```

***

#### **Summary Table of Dictionary Methods**

| **Method**     | **Description**                                                                |
| -------------- | ------------------------------------------------------------------------------ |
| `clear()`      | Removes all elements from the dictionary.                                      |
| `copy()`       | Returns a shallow copy of the dictionary.                                      |
| `fromkeys()`   | Creates a new dictionary with specified keys and a default value.              |
| `get()`        | Returns the value of a key; returns default if key not found.                  |
| `items()`      | Returns a view of key-value pairs.                                             |
| `keys()`       | Returns a view of dictionary keys.                                             |
| `pop()`        | Removes the specified key and returns its value.                               |
| `popitem()`    | Removes and returns the last key-value pair.                                   |
| `setdefault()` | Returns the value of a key, or inserts it with a default value if not present. |
| `update()`     | Updates the dictionary with another dictionary or iterable.                    |
| `values()`     | Returns a view of dictionary values.                                           |

These methods give you powerful tools to work with dictionaries effectively!

### What is Dictionary Comprehension in Python?

Dictionary comprehensions provide a concise and elegant way to create dictionaries in Python. Using a single line of code, you can construct a dictionary from an iterable or other source, optionally applying conditions or transformations.

#### Syntax of Dictionary Comprehension

```
{key_expression: value_expression for item in iterable if condition}
```

* **`key_expression`**: Determines the keys of the dictionary.
* **`value_expression`**: Determines the values of the dictionary.
* **`iterable`**: An iterable (like a list, tuple, or range) that provides items for the dictionary.
* **`if condition`** _(optional)_: Filters which items are included in the dictionary.

Creating a Simple Dictionary:

```
squares = {x: x**2 for x in range(1, 6)}
print(squares)  # Output: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

### How to iterate through elements in a Dictionary using a loop?

You can use a for loop in Python to loop through a dictionary. There are two common methods you can use to access the keys or values ​​of the dictionary. Here are examples of both methods:

1. **Loop through keys:**

```
my_dict = {"key1": "value1", key2": "value2", "key3": "value3"}

for key in my_dict:
    deger = my_dict[anahtar]
    print(f"Anahtar: {anahtar}, Değer: {deger}")
```

2. **Loop through values:**

```
my_dict = {"key": "value1", "key2": "value2", "key3": "value3"}

for value in my_dict.values():
    print(f"Value: {value}")
```

3. **Loop through keys and value:**

```
my_dict = {"key1": "value1", "key2": "value2", "key3": "value3"}

for key, value in my_dict.items():
    print(f"Key: {key}, Value: {value}")
```

### What is a Nested Dictionary in Python?

A **nested dictionary** is a dictionary where the values themselves are dictionaries. This allows you to create complex data structures, such as hierarchical relationships or multi-level mappings.

In a nested dictionary, you can have dictionaries inside dictionaries, and this can go as deep as needed.&#x20;

### Examples of Nested Dictionaries:

1. **Simple Nested Dictionary:**

A nested dictionary representing an employee with information about their name, age, and department.

```
employee = {
    "employee1": {
        "name": "Alice",
        "age": 30,
        "department": "HR"
    },
    "employee2": {
        "name": "Bob",
        "age": 25,
        "department": "Engineering"
    }
}

print(employee)
# Output: {
#     'employee1': {'name': 'Alice', 'age': 30, 'department': 'HR'},
#     'employee2': {'name': 'Bob', 'age': 25, 'department': 'Engineering'}
# }

```

2. **Accessing Elements in a Nested Dictionary:**

You can access elements by chaining the keys.

```
employee = {
    "employee1": {
        "name": "Alice",
        "age": 30,
        "department": "HR"
    },
    "employee2": {
        "name": "Bob",
        "age": 25,
        "department": "Engineering"
    }
}

print(employee["employee1"]["name"])  # Output: Alice
print(employee["employee2"]["age"])   # Output: 25
```

3. **Modifying Elements in a Nested Dictionary:**

```
employee = {
    "employee1": {
        "name": "Alice",
        "age": 30,
        "department": "HR"
    }
}

# Update the age of employee1
employee["employee1"]["age"] = 31

# Add a new key-value pair for employee1
employee["employee1"]["salary"] = 50000

print(employee)
# Output: {
#     'employee1': {'name': 'Alice', 'age': 31, 'department': 'HR', 'salary': 50000}
# }

```

4. **Adding a New Dictionary Inside a Nested Dictionary**:

```
company = {
    "employee1": {
        "name": "Alice",
        "department": "HR"
    }
}

# Add a new employee with a nested dictionary
company["employee2"] = {
    "name": "Bob",
    "department": "Engineering",
    "salary": 60000
}

print(company)
# Output: {
#     'employee1': {'name': 'Alice', 'department': 'HR'},
#     'employee2': {'name': 'Bob', 'department': 'Engineering', 'salary': 60000}
# }

```

5. **Nested Dictionary with Multiple Levels:**

```
company = {
    "employee1": {
        "name": "Alice",
        "details": {
            "age": 30,
            "address": "123 Main St"
        }
    },
    "employee2": {
        "name": "Bob",
        "details": {
            "age": 25,
            "address": "456 Oak St"
        }
    }
}

print(company["employee1"]["details"]["address"])  # Output: 123 Main St

```

6. **Iterating Over a Nested Dictionary:**&#x59;ou can iterate over a nested dictionary using loops.

```
company = {
    "employee1": {
        "name": "Alice",
        "department": "HR"
    },
    "employee2": {
        "name": "Bob",
        "department": "Engineering"
    }
}

for employee, details in company.items():
    print(f"{employee}: {details['name']} works in {details['department']}")

```
