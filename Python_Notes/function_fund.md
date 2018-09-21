# Function Fundamentals

### General

- Definition:  A process for executing a task
    - Accepts an input and returns an output
    - Useful for executing similar tasks repeatedly and organizing code

- Function Structure
  - Syntax:
  ```python
  def functionName(input):
    # code here
    return output
  ```
    - The input can be blank
    - The return function outputs the proceeding statement and terminates the function
    
  - e.g.
  ```python
  def saySomething(input):
    return input
  
  saySomething('Hi!')
  # Returns 'Hi!'
  ```
  
  - Input
    - **parameter:** a variable in a method definition
      - Default parameters can be set up by setting a parameter equal to the intended value
      - e.g.
      ```python
      def exp(num, power = 2):
        return num ** power
      
      exp(2, 3) # Returns 8
      exp(3, 2) # Returns 9
      exp(4) # Uses the default power parameter of 2 and returns 16
      ```
      
    - **argument:** the input that is passed into a function when the function is called
      - Keyword arguments allow the user to specify the order of the arguments
      - e.g.
      ```python
      def exp(num, power = 2):
        return num ** power
      
      exp(power = 5, num = 2)
      # Takes 2 to the power of 5 and returns 32
      ```

- Scope:  The level at which something exists
  - The scope of an object exists at the outermost shell it is contained within.
  - Scope Levels
    - **global:**  The outermost scope
    - **nonlocal:**  A scope outside the local scope but not in the outermost scope 
    - For any object that is defined at a global or nonlocal scope, the scope must precede the object to call the object.
    - e.g.
    ```python
    numbers = [1, 2, 3, 4, 5]
    
    def exp(num, power):
        num = global numbers # numbers exists outside the function so its scope must be specified
        output = num ** power
        return output
    ```
  - For functions, anything contained within a function only has a scope within the function
    - e.g.
    ```python
    def exp(num, power = 2):
        output = num ** power
        return output
    
    print(output) # This will return an error.
    ```
    - In the above example, the variable output only exist within the function.  It cannot be called directly outside the function.
    - If a variable with the same is created outside the function, it will not affect the variable with the same name inside the function.

- Documenting Functions
    - Documentation is a way of describing a function.  A function's documentation can be called.
    - Syntax: """Explanation"""
        - The documentation must be on the first line inside the function.
    - Calling a function followed by .__doc__ (double underscores) will print the documentation line
    - e.g.
    ```python
    def exp(num, power = 2):
        """A function that calculates the number raised to the power."""
        output = num ** power
        return output
    
    exp.__doc__ # This will print the documentation line.
    ```
    - Can be used on native python functions to explain them.

---

### Star Operators

- **Star Arguments (*args)**
  - Definition:  A special operator used to pass functions by gathering all proceeding arguments as a tuple.
    - There is no set amount of arguments required.
    - Useful for functions where the number of arguments can be variable.
  - Syntax:  def function(*parameter)
    - The parameter is usually named args.
    - The star operator is only applied for all proceeding arguments.  Any parameters/arguments preceding it are unaffected.
    - This allows a function to have both a number of required arguments and a variable number of arguments.
  - e.g.
    ```python
    def sum_all_nums(num1, num2, num3):
      return num1 + num2 + num3
    
    # If the user wants to input more than 3 arguments, this function would not work.
    # Using the star operator allows us to define a function that takes a variable number of arguments.
    
    def sum_all_nums(*args):
      total = 0
      for num in args:
        total += num
      return num
    ```

- **Star Keyword Arguments (**kwargs)**
  - Definition:  A special operator used to pass functions by gathering all proceeding arguments as a dictionary.
  - Syntax:  def function(**parameter):
    - The user input must specify a key word argument by setting the key equal to a value.
    - The keyword parameter will be converted to a string.  It must be called as a string in the function.
  - e.g.
  ```python
  def fav_colors(**kwargs):
    for person, color in kwargs.items():
      print(f"{person}'s favorite color is {color}")
  
  fav_colors(Colt = 'purple', Ruby = 'red', Ethel = 'teal')
  ```

- Parameter Ordering
  - Parameters in a function definition must be ordered as follows:
    - Parameters
    - *args
    - Default Parameters
    - **kwargs
  - e.g.
  ```python
  def display_info(a, b, *args, instructor = 'Colt', **kwargs):
    return [a, b, args, instructor, kwargs]
  ```

- Tuple Unpacking
  - * operators can be passed in a function argument to unpack list and tuple arguments.
    - The star operator must precede the list or tuple argument.
  - e.g.
  ```python
  def total_sum(*args):
    total = 0
    for num in args:
      total += num
    return total
  
  nums = [1, 2, 3, 4, 5]
  # Because nums is a list, it cannot be added to the integer 0 from total.
  # The list must be iterated over or unpacked.
  
  total_sums(*nums)
  # Returns 15
  ```
  
- Dictionary Unpacking
  - ** operators can be passed in a function argument to unpack dictionary arguments (e.g. key = value)
  - e.g.
  ```python
  def display_name(first, second):
    return f'{first} says hello to {second}'
  
  names = {'first': 'Colt', 'second': 'Rusty'}
  # Since names is a dictionary, the dictionary must either be converted to an iterable form or unpacked.
  
  display_name(**names)
  # Returns 'Colt says hello to Rusty'
  ```

  
