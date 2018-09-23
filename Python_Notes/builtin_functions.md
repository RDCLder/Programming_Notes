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
  - Syntax:  any(iterable)
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

---

### Miscellaneous

  - Definition:  A lambda is a function without a name definition.
    - Also called anonymous functions
    - Can be saved to a variable
  - Used for cases in which a function needs to be passed into another function as a parameter
