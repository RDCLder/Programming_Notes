# Data Structures

### Lists

- Defintion:  An arrayed data structure that can store elements

- Syntax:

```python
  list = [item1, item2, item3]
  ```

- List Properties
  - Lists are mutable
    - Being mutable means non-static and changeable
    - Lists can be appended in multiple ways
  - Lists can store different elements, including other lists

- Nested Lists

- Relevant Methods/Functions
  - **.append()** is a method that adds a single enclosed element to the preceding element
  - **.extend([])** is a method that adds multiple enclosed elements to the preceding element
    - Note that the method only takes one argument so all elements must be enclosed in brackets []
  - **.insert()** is a method that adds the enclosed element to a specified position in the preceding element
    ```python
    list1 = [1, 2, 3, 4]
    list1.insert(2, 'Hi')
    list1.insert(-1, 'Second to Last')
    print(list1) == [1, 2, 'Hi, 3, 'Second to Last', 4]
    ```
    - In the above example, the string 'Hi' will be inserted at position 2 between 2 and 3
    - Using a negative number for the position will cause the insertion to go backwards from the end of the list

---

### Dictionaries

---

### Tuples and Sets
