# Object Oriented Programming I

## Objectives

- Define Object Oriented Programming
- Understand encapsulation and abstraction
- Create classes and instances and attach methods and properties to each

---

## General

- Objected Oriented Programming
  - Definition:  A programming paradigm which attempts to model some process or thing as a **class** or **object/instance**.
  - **class**:  A blueprint for objects.  Classes can contain methods (functions) and attributes.
    - Defines everything needed for creating an object.
    - e.g.  A user class has attributes (e.g. profile picture, username, password, e-mail).
    - e.g.  A user class has methods (e.g. change profile picture, log-out, check-out).
  - **object/instance**:  Objects that are constructed from a **class** blueprint which contains the class methods and properties.
  - Uses
    - OOP is an approach for *encapsulating* code into logical, hierarchical groupings using classes.
    - Allows for using logic at higher levels.

- **Encapsulation**
  - Definition:  The grouping of public and private attributes and methods into a programmatic class.
    - Doing so makes **abstraction** possible.
  - There is no true distinction between public and private informaton.  It is up to the developer.
    - The convention for private information is to lead an attribute or method name with an underscore.
    - e.g.  _cardsLeft is private a list attribute because the name leads with an underscore.
  - e.g.  Modeling a game of poker
    - Entities that could be modeled as object classes:
      - Game
      - Player
      - Card
      - Deck
      - Hand
      - Chip
      - Bet
    - For the deck class, cards can be made as a private attribute
    - The length of the cards can be accessed by a public method called count()

- **Abstraction**
  - Definition:  An approach to design which emphasizes on only revealing the relevant data in a class interface and hiding private information from users.

---

## Creating Classes and Instances

- Conventions
  - New class names start with an uppercase letter.
  - The first parameter for the **__init__()** method is named *self*.
  - Class attributes are defined near the beginning, before the **__init__()** method.
  - Class methods do not have a convention.  The first parameter is named *cls*  Just be consistent.

- **__init__()**:  A method that defines the initial attributes of a class and how they store data.
  - Syntax:  __init__(self, parameter1, ... parameterN)
    - The self parameter refers only to the current instance of the class.
    - The *self* parameter is never input as an argument by the user.  The first argument is parameter1.
    - Each parameter is an input for an attribute for the class.  Attributes and parameters are like key-value pairs.
  - Use
    - When a new classis created, this must be the first method to be defined.
    - When a new instance of a class is created, the **__init__()** method is automatically called.
    - This method is necessary to store data for a class.  For a class that only stores methods and does not store data, this method is unnecessary (rare).
  - e.g.
  ```python
  class User:
    def __init__(self, first, last = 'Solo'):
      self.firstName = first
      self.lastName = last
      self.age = age
  
  # The attribute firstName corresponds to the parameter *first* and so on.
  
  user1 = User('Han')
  print(user1.first) # This prints 'Han'
  print(user1.last) # This prints 'Solo' as the default argument
  ```

- Instance Methods
  - Definition:  Methods that affect a single instance of a class.
  - e.g.
  ```python
  class User:
    def __init__(self, first, last, age):
        self.first = first
        self.last = last
        self.age = age

    def full_name(self):
        return f'{self.first} {self.last}'

    def initials(self):
        return f'{self.first[0]}    {self.last[0]}'
  
  user1 = User('Joe', 'Smith', 68)
  print(user1.full_name()) # Returns 'Joe' 'Smith'
  print(user1.initials()) # Returns 'JS'
  ```

- Class Attributes
  - Definition:  An attribute that is shared by all instances of a class.
    - Must be scoped directly under the class definition (i.e. outside specific methods).
  - Defining an attribute as part of the class allows for easier manipulation if it's used by multiple methods.
    - Changing a class attribute for a specific instance will create a new attribute for that instance and not affect the class attribute.
  - e.g.
  ```python
  class User:

    active_users = 0

    def __init__(self, first, last, age):
        self.first = first
        self.last = last
        self.age = age
        User.active_users += 1
  
  # Every time a new instance of User is created, active_users is increased by 1.
  ```

- Class Methods
  - Definition:  A method that only affects the class and not instances.
  - Syntax:
  ```python
  class NewClass():
    #...
    
    @classmethod
    def newMethod(cls, *params):
      returm cls(*params)
  ```
    - @classmethod must always be directly above a class method definition.
    - Instead of referring to self, class methods refer to cls
  - e.g.
  ```python
  @classmethod
    def from_string(cls, str):
        first, last, age = str.split(',')
        return cls(first, last, int(age))
  
  tom = User.from_string('Tom,Jones,89')
  print(tom.full_name()) # 'Tom Jones'
  ```

---

## Miscellaneous

- Underscores
  - Single underscores are used to designate to the developer that a specific attribute/method is private.
  - **Dunder Method** (double underscores):  A method that overrides an inherent method.
    - Syntax:  __method__()
    - There is no technical difference between names that start with a letter or a single underscore.
  - **Name Mangling** (double underscore in front):  An automatic procedure in which a name leading with a double underscore is preceded by the encapsulating class.
    - Syntax:  __method -> _class__method()
    - This allows a name for an attribute or a method to be tied to the specific class if the name is also used in other classes.
    - e.g.
    ```python
    def class1(input):
      __method = action(input)
      
    def class2(class1):
      __method = action(input)
      
    # Class2 is dependent on class1 and __method is used for both definitions
    # Python automatically prefaces each method name with its respective class to avoid confusion
    # The method becomes _class1__method() and _class2__method()
    ```

- String Representation
  - Definition:  A dunder that allows for the representation of an instance as a string.
  - Syntax:  __repr__(self)
  - e.g.
  ```python
  def __repr__(self):
    return f'{self.first} is {self.age}.'
  ```
