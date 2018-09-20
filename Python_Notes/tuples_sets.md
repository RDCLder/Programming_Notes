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
  x[0] = 'change me!' # This will return an error as tuple contents cannot be re-assigned.  Tuple variables, however, can be re-assigned.
  ```
