# Dictionaries

### General

- Dictionary Basics
  - Definition:  A data structure which consists of key-value pairs.
    - Keys are used to describe data while values are used to represent the data
    - Keys are usually numbers and strings while values can be any element (e.g. numbers, strings, lists, dictionaries, etc.)
  - Syntax:  {key1: value1, key2: value2, key3: value3}
  - e.g.
  ```python
  instructor = {
    'name': 'Colt',
    'owns_dog': True
    'num_courses': 4
    'favorite_lang': 'Python'
    'is_hilarious': False
    44: 'my favorite number!'
  }
  ```
  - To access an entry, the dictionary must be called with the specific key
    ```python
    instructor[name] # This will output 'Colt'
    ```
  
- Dict Function
  - A function that creates a dictonary
  - Syntax:  dict(key = 'value')
    - If the key contains letters, it will be converted into a string.
    - If the key contains numbers, it will remain a number.
  - e.g.
  ```python
  another_dictionary = dict(key = 'value')
  ```

- Dictionary Iteration
  - **.values()** is a method that can create an iterable form of the preceding dictionary and return all the stored values
    ```python
    for value in instructor.values():
      print(value)
      
    # This will output all the values in the instructor dictionary
    ```
  - **.keys()** is a method that can create an iterable form of the preceding dictionary and return all the stored keys
  - **.items()** is a method that can create an iterable form of the preceding dictionary and return both the keys and the values
    - Calling a specific item will yield a list containing both the key and its respective value
    ```python
    for item in instructor.items():
      print item
    
    # OR
    
    for key, value in instructor.items():
      print item
    
    # This will yield all the items in the instructor dictionary
    
    dict_items([('name', 'Colt'), ('owns_dog', True), ('num_courses', 4) ...])
    ```

- Testing for Specific Elements
  - Presence of a key can be tested with a normal in statement
  - Presence of a value must be tested using the **.values()** method
  ```python
  'Colt' in instructor.values() # True
  ```

---

### Dictionary Methods

- **.clear()** is a method that deletes all the contents of the preceding dictionary

- **.copy()** is a method that copies all the contents of the preceding dictionary.  Must be stored to a variable.

- **.fromkeys()** is a method that creates key-valued pairs from elements separated by commas and stores them in the preceding, empty dictionary
  - syntax:  {}.fromkeys(iterable_element, value)
    - The key must be an iterable element such as a string or a list
    - The value can be anything
  - e.g.
  ```python
  {}.fromkeys('a', 'b') # {'a': 'b'}
  {}.fromkeys(['email'], 'unknown') # {'email': 'unknown'}
  {}.fromkeys('a', [1, 2, 3, 4, 5]) # {'a': [1, 2, 3, 4, 5]}
  {}.fromkeys('string', 1) # {'s': 1, 't': 1, 'r': 1, 'i': 1, 'n': 1, 'g': 1}
  ```
    - In this example, the last statement shows the key string being iterated over each letter.

- **.get()** is a method that retrieves a key in an object and returns None if the key does not exist
  - e.g.
  ```python
  instructor.get('Cool')
  # This returns None because 'Cool' key doesn't exist.
  ```

- **.pop()** is a method that takes a single argument corresponding to a key and removes the key-value pair from the dictionary.  The key-value pair is returned.
  - e.g.
  ```python
  d = dict(a = 1, b = 2, c = 3)
  d.pop() # This will return an error because an argument is required.
  d.pop('a') # Removes and returns 1
  d # {'c': 3, 'b': 2}
  d.pop('e') # This will return cause an error as e is not a key
  ```
- **.popitem()** is a method that removes a random key-value in a dictionary and returns it.
  - e.g.
  ```python
  d = dict(a = 1, b = 2, c = 3)
  d.popitem(a) # This willreturn an error as this method takes no arguments
  d.popitem() # This will remove a random item and reutrn it (e.g. a = 1)
  ```

- **.update()** is a method that updates keys and values in a dictionary with another set of key-value pairs.
  - Only useful for appending dictionaries

---

### Dictionary Comprehension

- Dictionary comprehension is a way to generate dictionaries with specified parameters
  - Syntax:  {_:_for_in_}
    - Iterates over keys by default
    - Can iterate over keys and values with **.items()** method
  - e.g.
  ```python
  numbers = dict(first = 1, second = 2, third = 3)
  squared_numbers = {key: value ** 2 for key, value in numbers.items()}
  print(squared_numbers) # {'first': 1, 'second': 4, 'third': 9}
  ```
  ```python
  str1 = "ABC"
  str2 = "123"
  combo = {str1[i]: str2[i] for i in range(0, len(str1))}
  print(combo) # {'A': 1, 'B': 2, 'C': 3}
  ```

- Dictionary comprehension with conditional logic
  - e.g.
  ```python
  num_list = [1, 2, 3, 4]
  {num: ('even' if num % 2 == 0 else 'odd') for num in num_list}
  # {1: 'odd', 2: 'even', 3: 'odd', 4: 'even'}
  ```
