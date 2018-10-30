# Fundamentals

## Numbers and Operators

- Numbers can be represented by different data types
  - **Integers** are real, whole numbers
  - **Floats** are real numbers that include decimals
  - **Complex numbers** are numbers that include both real and imaginary components

- Operators are basic commands that let numbers (and certain data types) interact with each other.
  - Operators include basic mathematical operators and a few special operators
    - \\ gives the integer value of the quotient and discard any decimals
    - % gives the remainder (e.g. 5 % 2 = 1)
    - ** denotes exponent
    
  - Python uses order of operations to compute operations
  - Multiplying and dividing will always create floats
    - functions can be used to determine decimal accuracy
    - int function will take any number data type and return the integer and discard any decimals

- Not all data types can interact with each other
  - Integers and floats are different data types and can't interact through operators.

---

## Strings and Variables

- Strings are a data type that can consist of any characters enclosed by ' or "
  - A backslash (\) will cause the interpreter to interpret the proceeding character as a part of the string
  
- String Manipulation
  - Strings can be concatenated to other strings or multiplied by an integer
  - String operators
    - \n will start the proceeding string on a new line
    - \t will indent the proceeding string
    - Triple ' or " will interpret any enclosed character as a string and allow the string to be written over different lines
    
- String Formatting
  - Strings can include replacement fields designated by {} that can be replaced by data types and variables
    - Replacement fields can be formatted with the **.format()** function
    
    ```python
    '2 + 2 is equal to {}'.format('4')
    ```
    
    - Replacement fields formatted with **format** function can be numbered to be replaced with the corresponding element in the format function.  Otherwise, they will be replaced sequentially.
    
    - Replacement fields can be formatted directly with the **f** function
    
    ```python
    answer = 2 + 2
    f'2 + 2 is equal to {answer}'
    ```

- Variables are a placeholder for an element
  - Syntax: var = element
  - Variables must be defined before they can be used
    - Defintions can include null elements like 0 or None
  - Variables can hold any element
  - Variables can be reset if a new definition is given
 
 - Variable Naming
  - The start of a variable must be an underscore or a letter
  - The rest of the variable can include any character
  - Variables are case-sensitive

---

## Relevant Functions and Tips

- **str** will convert the enclosed elements into a printable string if applicable
  - Numbers can be converted to strings
  - Certain arrayed data structures like lists can be converted while others like tuples and dictionaries cannot be converted

- **int** will convert a string or a number type into an integer if applicable
  - Numbers converted will lose any decimals
  - Strings can only be converted if they include a single, whole numbers and no other characters (besides spaces and tabs)
  
- **print()** will output the enclosed element(s)
  - The enclosed elements can be any data type and can undergo any operation or manipulation
 
- **.join()** will join the preceding string with the proceeding element with the enclosed element
  - Used for concatenating strings in a list

- Highlighting code and pressing **Ctrl + /** will convert code to comment and vice versa
