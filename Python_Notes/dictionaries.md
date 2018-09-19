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

- **.copy()** is a method that copies all the contents of the contained dictionary into the preceding dictionary

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

- **.pop()** is a method that 
