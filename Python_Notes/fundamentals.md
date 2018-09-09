# Fundamentals

### PowerShell Fundamentals

-	The PowerShell is the command prompt for windows OS
  - An OS is structured like a tree in which a root directory can then branch off into subdirectories (e.g. folders, files, etc.)
    - Root directory is C:
    - Levels of the hierarchy are separated by \
    - Home directory is designated by ~ and is usually C:\Users\Username

  - The command prompt has greater functionality than a GUI like Windows Explorer
    - e.g.  Instead of manually dragging a file from directory to directory, PowerShell can perform that function with a line of code

-	PowerShell has several basic functions that can be used to manipulate files
  - Basic directory functions
    - cd  addresses the current directory
    - ..	goes back one level to parent directory (e.g. cd ..)
    - ls	lists all the contents of current directory
    - wpd	lists the exact path from root directory to current directory
    - ~	accesses the home directory

  - Other functions
    - clear	clears current PowerShell text

- Creating Directories
  - mkdir command can make new directories
    - syntax:  mkdir folder
    - This will create a new folder called “folder” in the current directory

### Numbers and Operators

- Numbers can be represented by different data types
  - **Integers** are real, whole numbers
  - **Floats** are real numbers that include decimals
  - **Complex numbers** are numbers that include both real and imaginary components

- Operators are basic functions that let numbers (and some different data types) interact with each other.
  - Operators include basic mathematical operators and a few special operators
    - \\ gives the integer value of the quotient and discard any decimals
    - % gives the remainder (e.g. 5 % 2 = 1)
    - ** denotes exponent
    
  - Python uses order of operations to compute operations
  - Multiplying and dividing will always create floats
    - functions can be used to determine decimal accuracy
    - int function will take any number data type and return the integer and discard any decimals

- Integers and floats are different data types and can't interact through operators.

### Strings and Print Function

- print function can use both apostrophes (') and quotation marks (") to denote strings
  - If you use both (') and (") in a print function such as in the following example:
    print('The pet shop owner said "No no, 'e's uh,… he's resting" ')
  - A backslash (\) will cause the interpreter to interpret the proceeding character as a string
  - e.g. \’e\’s will cause the interpreter to recognize the apostrophes as part of the string

- Highlighting code and pressing **Ctrl + / will** convert code to comment

```python
def longest_palindrome(s):
    length = 0

    for char in s:
        if s.count(char) > 1:
            for i in range(len(s)):
                for j in range(len(s) - 1, i, -1):
                    if s[i] == s[j]:
                        for k in range(round((j - i) / 2)):
                            check = 0
                            if s[i + k] == s[j - k]:
                                check += 1
                                if check == round((j - i) / 2):
                                    length = j - i + 1

    return print(length)
```
