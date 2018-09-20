# Tuples and Sets

### Tuples

- General
  - Definition:  An immutable, ordered collection or grouping of items.
    - Unlike lists and dictionaries, tuples are immutable (cannot be changed).
  - Syntax:  (item1, item2, item3)
    - Unlike dictionaries and lists, parentheses are used.
  - e.g.
  ```python
  x = (1, 2, 3)
  3 in x # True
  x[0] = 'change me!' This will return an error.
  
  # Tuple contents cannot be re-assigned.  Tuple variables, however, can be.
  ```

- **tuple()** is a function that takes an arrayed argument and returns a tuple of the argument

- Tuple Usage
  - Tuples are faster than lists because tuples support less built-in functions/methods
  - Tuples can be safer for data that will never be changed.
  - Tuples can be used as keys in dictionaries.

- Looping over a tuple is the same as looping over a list

- **.count()** is a method that takes an argument and returns the number of times it appears in the tuple

- **.index()** is a method that takes an argument and returns its index in the tuple

---

### Sets

- General
  - Defintiion:  An unordered collection of data without duplicate values
    - Sets can contain any element
    - Any duplicates passed to a set will be automatically removed.  Useful for reducing data to unique items.
    - As sets are unordered, items in a set are not indexed.
  - Syntax:  {item1, item2, item3}
    - Uses curly brackets like a dictionary every element is discrete and unpaired
  - e.g.
  ```python
  s1 = {1, 2, 3}
  ```
  - To create an empty set, the **set()** function must be used
    - e.g.
    ```python
    s2 = set({1, 2, 3, 4, 4, 5})
    # Duplicates will be removed.  s2 = {1, 2, 3, 4, 5}
    ```
- Set Comprehension
  - Syntax:  {x for x in object if x condition}
  - e.g.
  ```python
  even = {num for num in [1, 2, 3, 4, 5] if num % 2 == 0}
  print(even) # {2, 4}
  ```

- **.add()** is a method that takes an argument and adds it to the set
  - e.g.
  ```python
  even = {2, 4}
  even.add(6)
  print(even) # {2, 4, 6}
  ```
  
- **.remove()** is a method that takes an argument and removes it from the set
  - If the argument is not in the set, it will return an error.
  - e.g.
  ```python
  even = {2, 4, 6}
  even.remove(4)
  print(even) # (2, 6)
  even.remove{8} # This will return an error as 8 is not in the set.
  ```

- **.discard()** is a method that takes an argument and removes it from the set
  - If the argment is not in the set, no error will be returned.

- **.copy()** is a method that will copy the preceding set
  - The method must be set to a variable
  - e.g.
  ```python
  set1 = {1, 2, 3}
  set2 = set1.copy()
  print(set2) # {1, 2, 3}
  ```
  
- **.clear()** is a method that removes all the contents of the preceding set

- **Set Math** contains operators that can be used to interact with sets.
  - **|**:  Union operator.  Joins two sets.
    ```python
    s = {1, 2, 3} | {4, 5, 6}
    # {1, 2, 3, 4, 5, 6}
    ```
  - **&**:  Intersection.  Takes two sets and returns items present in both sets.
    ```python
    s = {1, 2, 3, 4, 5} & {2, 4, 6, 8, 10}
    # {2, 4}
    ```
