# Function Fundamentals

### General

Function Basics
  - Definition:  A process for executing a task
    - Accepts an input and returns an output
    - Useful for executing similar tasks repeatedly and organizing code

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
    - For functions, their scope is the script that contains them, which is the outermost scope.
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
