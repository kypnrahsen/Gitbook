# Tuples



## What is a tuple?

In Python, a tuple is an immutable data structure. This means that once created, its content cannot be changed. A tuple consists of comma-separated elements within parentheses (). For example:

```
my_tuple = (1, 2, 3)
```

However, you can also create tuples without using parentheses by separating the elements with commas:

```
another_tuple = 4, 5, 6
```

Tuples differ from lists because tuples are immutable and therefore their content cannot be changed once they are created. Tuples are often used to return multiple values ​​from functions or to store data that you do not want to be modified.

Properties of tuples:

* **Immutable:** Once created, you cannot change the elements within the tuple. This can be useful to ensure the security of data.
* **Heterogenous:** A tuple may contain elements of different data types(e.g integers, strings, boelean values)
* **Ordered:** Elements within tuples are ordered can be accessed by indexing.
* **Hashable:** Tuples can be used as keys in hash table-based data structures such as dictionaries.



## How to create a tuple?

You can use parentheses () to create tuples in Python. You define the elements inside the tuple by separating them with commas. Here are the tuple creation methods:

1. **Creating a Tuple Using Parentheses:**

```
my_tuple = (1, 2, 3, 4, 5)
```

2. **Creating a Tuple Without Parentheses:**

```
another_tuple = 4, 5, 6
```

3. **Converting a Variable to Tuple:**

```
my_list = [10, 20, 30]
converted_tuple = tuple(my_list)
```

It is very important to use commas when creating tuples. If you want to create a tuple with only one element, you must put a comma at the end of the element. Otherwise, Python treats this element as an object.

```
single_element_tuple = (10,)  # Bir elemanlı tuple
single_element_tuple_without_comma = (10)  # It is just an integer, not tuple.
```

Since tuples are immutable, you cannot change the elements inside them after you create them. If you need to use a data structure whose content needs to be changed, it is better to use a list.



## Some examples of using tuples in Python:

1. **Personal Information Tuple:**

```
person = ("Alice", 28, "Engineer")
print(person[0])  # Output: "Alice"
print(person[1])  # Output: 28
```

2. **Returning More Than One Value of a Function**:

```
def divide_and_remainder(a, b):
    quotient = a // b
    remainder = a % b
    return quotient, remainder

result = divide_and_remainder(10, 3)
print(result)  # Output: (3, 1)
```

3. **Tuple Containing Various Data Types:**

```
mixed_tuple = ("apple", 42, True, 3.14)
```

4. **Nested Tuple:**

```
nested_tuple = ((1, 2, 3), ("a", "b", "c"), (True, False))
```

5. **Merging Tuples with Lists:**

```
tuple1 = (1, 2, 3)
tuple2 = (4, 5, 6)
combined_tuple = tuple1 + tuple2  # (1, 2, 3, 4, 5, 6)
```

6. **Unpacking Tuples:**

```
coordinates = (10, 20)
x, y = coordinates
print(x)  # Output: 10
print(y)  # Output: 20
```

7. **Using Tuples as Dictionary Keys**:

```
location = (40.7128, -74.0060)
locations = {
    "New York": location,
    "Los Angeles": (34.0522, -118.2437)
}
```

8. **Tuples and Looping:**

```
fruits = ("apple", "banana", "orange")
for fruit in fruits:
    print(fruit)
# Output:
# apple
# banana
# orange
```

### How can I access the elements in the tuple?

You can access the tuple's elements using index or by tuple unpacking method.

1. **Reaching Elements Using Index:** You can access the tuple's elements by index number. Indexes start from 0.

```
my_tuple = (10, 20, 30, 40, 50)
first_element = my_tuple[0]  # First element (10)
third_element = my_tuple[2]  # Third element (30)
```

2. **Reaching Elements with Tuple Unpacking:** Tuple unpacking allows accessing the elements in the tuple by assigning them to separate variables.

```
my_tuple = (10, 20, 30)
x, y, z = my_tuple
print(x)  # 10
print(y)  # 20
print(z)  # 30
```

3. **Reaching Elements with Negative Indexes:** You can index backwards from the end of the tuple by using negative indexes.

```
my_tuple = (10, 20, 30, 40, 50)
last_element = my_tuple[-1]  # Output: (50)
second_last_element = my_tuple[-2]  # Output:(40)
```

4. Reaching Elements in a Specific Range with Slicing:&#x20;

```
my_tuple = (10, 20, 30, 40, 50)
sub_tuple = my_tuple[1:4]  # Elements from first index to third index.
# sub_tuple: (20, 30, 40)
```

### Can we change the tuple and the elements within the tuple?

Tuples are immutable data structures in Python, so once created, you cannot change their contents. If you need to use a data structure whose content needs to be changed, it would be more appropriate to use a lists.

If you need to change the contents of the tuple, you will need to create a new tuple using the tuple's elements. For example:

```
my_tuple = (1, 2, 3)
new_tuple = my_tuple + (4,)  #A new tuple is created to add the element 4
# new_tuple: (1, 2, 3, 4)
```

Or you can create a new tuple with a specific slicing from an existing tuple:

```
my_tuple = (1, 2, 3, 4, 5)
new_tuple = my_tuple[:3] + (10, 20) + my_tuple[4:]  
# Up to the 3rd element, then 10 and 20 are added, then the remaining elements are added
# new_tuple: (1, 2, 3, 10, 20, 4, 5)
```

However, remember that with these methods you essentially create a new tuple, the content of the existing tuple does not change.

If the elements in a tuple have mutable data types, you can change these elements. But the tuple itself will still be immutable.

That is, if the elements in the tuple are a mutable data type, such as a list, you can change the content of these elements. However, operations such as completely changing the elements of the tuple or adding elements will still not be possible.

For example:

```
my_tuple = ([1, 2, 3], [4, 5, 6])
my_tuple[0][1] = 10  # Changes the second element of the first element to 10
print(my_tuple)  # Çıktı: ([1, 10, 3], [4, 5, 6])
```

In the above example, since the elements inside **my\_tuple** are lists, we can change the elements inside it. However, you cannot completely replace **my\_tuple**.

Tuples are immutable data structures in Python, so once created, you cannot change their contents. If you need to use a data structure whose content needs to be changed, it would be more appropriate to use a list.



\






