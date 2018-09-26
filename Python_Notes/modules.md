# Modules

### Objectives

- Define a module
- Import code from built-in modules
- Import code from other files
- Import code from external modules using pip
- Describe common module patterns
- Describe the request/response cycle in HTTP
- Use the requests module to make requests to web apps

### General

- Basics
  - Definition:  A module is a file that contains code.
  - Uses
    - Allocating segments of code to specific files keeps file sizes small.
    - Allows code that perform specific functions to be grouped together and used multiple times.
  - Python has built-in modules and allows for the creation of custom modules.

- Importing Modules
  - Modules must be imported either as the entire module or as part of the module to be used.
    - Modules and parts of modules that are imported can be renamed
    - e.g. import random as rand
  - Importing an entire module 
    - Syntax:  import module_name
    - e.g.
    ```python
    import random
    choice = random.choice([1, 2, 3, 4, 5])
    ```
    
  - Importing a specific part of a module
    - Syntax:  from module_name import function/method
    - It is unnecessary to import an entire module when only a specific part is necessary
    - e.g.
    ```python
    from random import choice
    outcome = choice([1, 2, 3, 4, 5])
    # Notice that random.choice() is now just choice()
    ```

- External Modules:  Modules stored in external systems (e.g. online).
  - **pip**:  Python's package management system.
    - Used to download external modules.
    - Command line:  python -m pip install NAME_OF_PACKAGE

### Useful Packages/Modules

- **autopep8**
  - A tool that automatically formats Python code to conform to the PEP 8 style guide.

- 
