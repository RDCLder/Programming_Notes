# Built-In Functions

### Common Built-In Functions

- **lambda**:  A lambda is a function without a name definition.
  - Syntax:  lambda value: value + action
    - Also called anonymous functions
    - Can be saved to a variable
  - Used for cases in which a function needs to be passed into another function as a parameter
  - e.g.
  ```python
  nums = [1, 2, 3]
  square = lambda n: n ** 2
  square(nums) # [1, 4, 9]
  ```

- **map()**:  A function that accepts two or more arguments, a function and an iterable item, and returns the iterable applied to the function.
  - Syntax: map(function, iterable)
    - The function parameter can be a lambda.
    - The returned data needs to be converted to an iterable form (e.g. list, tuple, etc.).
  - e.g.
  ```pyton
  nums = [1, 3, 5, 7, 9]
  double = map(lambda n: n * 2, nums)
  # At this point, double contains data but not in an iterable form.
  list(double)
  # This will convert the data to a list [2, 6, 10, 14, 18]
  ```

- **filter()**:  A function that accepts two or more arguments, a function and an iterable item, and returns iterable items that are True for the function.
  - Syntax: filter(function, iterable)
    - The function parameter can be lambda.
    - The return data needs to be converted to an iterable form (e.g. list, tuple, etc.).
  - Unlike a map, the function only tests for True or False conditions.
    - No transformations can be applied to the data.  
    - Only data that return True are stored.
  - e.g.
  ```python
  nums = [1, 2, 3, 4]
  evens = list(filter(lambda n: n % 2 == 0, nums))
  # Returns [2, 4]
  ```

- **all()**:  A function that tests for whether all items of an iterable are True.
  - Syntax:  all(iterable)
    - If any single iterable item is False, the function returns False.
    - If the iterable is empty, the function returns True.
  - e.g.
  ```python
  all([0, 1, 2, 3]) # False because 0 is False
  all([char for char in 'eio' if char in 'aeiou']) # True
  all([num for num in [4, 2, 10, 6, 8] if num % 2 == 0]) # True because all numbers are even
  
  people = ['Charlie', 'Casey', 'Cody', 'Kristen']
  [name[0] == C for name in people]
  # Returns [True, True, True, False]
  
  all([name[0] == C for name in people])
  # Because Kristen doesn't start with a C, one item is False and the function returns False
  ```
  
- **any()**:  A function that tests for whether any item of an iterable is True.
  - If the iterable is empty, the function returns False.

- **sorted()**:  A function that takes an iterable and returns a sorted list.
  - Syntax:  sorted(iterable, key = None, reverse = False)
    - Sorts alphanumerically (numbers before letters, uppercase before lowercase)
    - The key and reverse parameters are optional.
    - Key is used to specify which attribute to sort by (e.g. length, alphabetically, etc.).
  - e.g
  ```python
  users = [
	{"username": "samuel", "tweets": ["I love cake", "I love pie", "hello world!"]},
	{"username": "katie", "tweets": ["I love my cat"]},
	{"username": "jeff", "tweets": [], "color": "purple"},
	{"username": "bob123", "tweets": [], "num": 10, "color": "teal"},
	{"username": "doggo_luvr", "tweets": ["dogs are the best", "I'm hungry"]},
	{"username": "guitar_gal", "tweets": []}]

  # To sort users by their username
  sorted(users,key=lambda user: user['username'])

  # Finding our most active users...
  # Sort users by number of tweets, descending
  sorted(users,key=lambda user: len(user["tweets"]), reverse=True)
  ```
  
- **max/min()**:  A function which returns the largest/smallest item in an iterable or multiple arguments.
  - Syntax:  max/min(iterable, key = attribute) or max/min(arg1, arg2, arg3, key = attribute)
    - The key parameter is optional.  It specifies the attribute by which max/min is calculated.
    - An iterable argument must be by itself.  It cannot be input with other arguments.
  - e.g.
  ```python
  max(1, 2, 3, 4, 5)
  # Returns 5
  
  min('hello world')
  # Returns ' ' (space in the middle)
  
  names = ['Arya', 'Samson', 'Dora', 'Tim', 'Ollivander']
  max(names, key = lambda name: len(name))
  # Returns 'Ollivander'
  ```

- **reversed()**:  A function which returns a reverse iterator.
  - Unlike **.reverse()**, the **reversed** function works on all iterable items.

- **len()**:  A function which returns the length of an object.
  - The object can be a sequence (e.g. string, list, tuple, range) or collection (dictionary, set).
  - All characters and objects have a length property that can be called by .__len__()
    - It is possible to create custom objects with custom defined properties (see OOP section).

- **abs()**:  A function which retuns the absolute value of a number.

- **sum()**:  A function which returns the sum of a numeric iterable.
  - Syntax:  sum(iterable, start = 0)
    - start specifies the starting point.  The default is 0

- **round()**:  Returns a number rounded to the nearest ndigits precision after the decimal point.
  - If ndigits is omitted or equals None, the function returns the nearest integer to the input.

---

### Miscellaneous
