# Lists

### General

- List Basics
  - Defintion:  An arrayed data structure that can store elements
  - Syntax:  [element1, element2, element3]
  - e.g.
  ```python
  list = ['One', 2, [3, 4, 5]]
  ```

- List Properties
  - Lists are mutable
    - Being mutable means non-static and changeable
    - Lists can be appended in multiple ways
  - Lists can store different elements, including other lists

- Nested Lists
  - Lists inside of other lists
  - List comprehension can be performed inside lists

---

### List Manipulations

- **Slicing**:  Making a new list from "slices" of existing lists
  - Syntax:  list[start:stop:step]
  ```python
  list = [1, 2, 3, 4, 5]
    
  list[0:]
  # This will print 1, 2, 3, 4, 5
    
  list[2:4]
  # This will print 3, 4, 5
  ```
  - The start, stop, and step can be negative
  ```python
  list = [1, 2, 3, 4, 5]
    
  list[-1:1:-1]
  # This will print 5, 4, 3, 2
  list[-4:]
  # This will print 2, 3, 4, 5
  ```
    
- **swap** is a way of mixing the elements of a list
    ```python
    list = ['First', 'Second']
    list[0], list[1] = list[1], list[0]
    
    # The position of the strings will be reversed
    # list = ['Second', 'First']
    ```
    - Useful for shuffling and sorting algorithms

- List Comprehension:  A method for generating a new list 
  - Syntax: [item + action for item in list]
    - For each item in the list, a certain action is performed to the item.  All items are then stored in a new list.
  - e.g.
  ```python
  numbers = [1, 2, 3]
  
  doubled = [num * 2 for num in numbers]
  ```
    - This will generate a new list containing [2, 4, 6].
  
  ```python
  name = 'bob'
  
  upperName = [char.upper() for char in name]
  ```
    - This will produce a new list containing the uppercase version of each letter: ['B', 'O', 'B']
  
  - Lists comprehension can include conditional logic
    - Syntax:  [item + action for item in list if condition]
      ```python
      numbers = [1, 2, 3, 4, 5, 6]
      evens = [num for num in numbers if num % 2 == 0] # [2, 4, 6]
      odds = [num for num in numbers if num % 2 != 0] # [1, 3, 5]
      
      double_half = [num * 2 if num % 2 == 0 else num / 2 for num in numbers]
      # [0.5, 4, 1.5, 8, 2.5, 12]
      ```
  
---

### List Methods

- List Addition
  - **.append()** is a method that adds a single enclosed element to the preceding element

  - **.extend([])** is a method that adds multiple enclosed elements to the preceding element
    - Note that the method only takes one argument so all elements must be enclosed in brackets []

  - **.insert(position, element)** is a method that adds the enclosed element to a specified position in the preceding element
    ```python
    list = [1, 2, 3, 4]
    list.insert(2, 'Hi')
    list.insert(-1, 'Second to Last')
    print(list) == [1, 2, 'Hi, 3, 'Second to Last', 4]
    ```
    - In the above example, the string 'Hi' will be inserted at position 2 between 2 and 3
    - Using a negative number for the position will cause the insertion to go backwards from the end of the list

- List Removal
  - **.clear()** is a method that will erase all the stored contents of the preceding elements

  - **.pop()** is a method that removes an element at a specified position and returns it
    - If no position is specified, the last element will be removed

  - **.remove()** is a method that will remove the first element from a list that matches the enclosed element
    ```python
    list = [1, 2, 3, 4]
    list.remove(2)
    print(list) == [1, 3, 4]
    ```
- Miscellaneous
  - **.index()** is a method that returns the index of the enclosed element in the preceding element
  
  - **.count()** is a method that returns the number of instances the enclosed element occurs in the preceding element
  
  - **.reverse()** is a method that reverses the preceding element
  
  - **.sort()** is a method that sorts the enclosed elements alphanumerically
    - Numbers cannot be mixed with strings
    - For strings, numbers come before letters and uppercase comes before lowercase
    - This method cannot be stored in a variable, it can only be applied to an existing variable
  
  - **.join()** is a string method that takes the preceding string and combines it with each element from the enclosed, iterable argument
    ```python
    words = ['Coding', 'is', 'fun']
    ' '.join(words)
    # This will yield the following string: 'Coding is fun'
    ```
    - The join method is commonly used to convert lists to strings.
