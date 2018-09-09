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

### Getting to Know Python

- print function can use both apostrophes (‘) and quotation marks (“) to denote strings
  - If you use both (‘) and (“) in a print function such as in the following example:
    print(‘The pet shop owner said “No no, ‘e’s uh,… he’s resting” ’)
  - You can add backslash (\) in front of the marks you opened the string with (in this case apostrophes) to allow the function to interpret the mark as a string
  - e.g. \’e\’s will cause the interpreter to recognize the apostrophes as part of the string

- Highlighting code and pressing **Ctrl + / will** convert code to comment

