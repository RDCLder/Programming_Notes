# Debugging

### Objectives

- Understand common errors and how they occur in Python
- Use pdb to set breakpoints and step through code
- Use try and except blocks to handle errors

---

### Common Errors

- **SyntaxError**:  An error which occurs when incorrect syntax is encountered.

- **NameError**:  An error which occurs when a variable is not defined/assigned.

- **TypeError**:  An error which occurs when an operation/function/method is applied to the wrong data type.
  - Common causes:
    - Using multiple data types that are not compatible.
  - e.g.
  ```python
  len(5) # Integer objects do not have a length property.
  
  'awesome' + [] # Cannot concatenate 'str' and 'list' objects.
  ```

- **Index Error**:  An error which occurs when trying to access in a list using an invalid index.
  - Common causes:
    - Forgetting that Python starts counting at 0
    - Miscalculating ranges
    - Misusing negative numbers or negative steps.
  - e.g.
  ```python
  list = [1, 2, 3]
  list[3] # Returns an error because list only has indices 0, 1, and 2.
  ```

- **ValueError**:  An error which occurs when a built-in operation/function receives an argument with the right type but an inappropriate value.
  - Common causes:
    - **int()** function which only accepts certain values for string-type objects.
  - e.g.
  ```python
  int('5') # Returns 5
  int('five') # This returns an error because only strings that exclusively contain numbers are accepted.
  ```

- **KeyError**:  A dictionary error which occurs when calling a key that does not exist.

- **AttributeError**:  An error which occurs when a variable does not have a specified attribute.
  - Common causes:
    - Calling an attribute that is inappropriate for an object or does not exist.
  - e.g.
  ```python
  'awesome'.foo # The string does not have a 'foo' attribute.
  ```

- Creating Custom Errors
  - Custom errors can be created using the **raise** keyword.
  - Syntax:  raise ErrorType('Error message')
    - ErrorType can be anything (see above error types)
  - e.g.
  ```python
  def colorize(text, color)
    if type(text) is not str:
      raise TypeError('text must be instance of str')
    return f'Printed {text} in {color}
  
  colorize('Hello', 'red') # 'Hello in red'
  colorize(24, 'red') # Returns error because text is a number
  ```

---

### Debugging & Error Handling

- Error Handling
  - In Python, it is strongly encouraged to use **try/except** blocks to catch potential exceptions if possible.
  - **try** is a command that will attempt to run the encompassed statement.
    - If the statement cannot be run, the next line is run.
  - **except** is a coammand that will run the encompassed statement if the try statement does not work.
  - e.g.
  ```python
  try:
    unnamed_function = input()
  except:
    if unnamed_function == False:
      print('try instance undefined')
  ```

- 
