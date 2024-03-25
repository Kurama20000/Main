# Main
11. Functions
=============

  I. Introduction
 II. Different Types of Functions (User-defined/Built-in)
III. Nested/Recursive/Decorator
 IV. Different types of Arguments
  V. Anonymous Function (Lambda Function)

***************************************************************************************************
I. Introduction:
----------------

    - Function is a block of organized, reusable code that performs a specific task. 
    - Functions help in modularizing code and make it more readable and maintainable.


        1. Code Organization : Functions help break down a program into smaller, manageable parts.
        2. Reusability       : Functions can be reused across the codebase, reducing redundancy.
        3. Readability       : Well-named functions enhance code readability and comprehension.
        4. Debugging         : Isolating functionality into functions aids in pinpointing and fixing issues.
 

        Functions vs Methods:
        ---------------------

        Functions:
        ----------
            - Defined using the def keyword.
            - Not associated with any object.
            - Can be standalone and called independently.

        Methods:
        --------
            - Associated with objects and classes.
            - Invoked on an object using the dot notation.
            - Dependent on the object they are called on.

        Params vs Args:
        ---------------
            - Parameters (params) : Variables listed in the function definition.
            - Arguments (args)    : Values passed to the function during a function call.

        Print vs Return:
        ----------------
            - Print  : Outputs information to the console but doesn't return a value.
            - Return : Sends a value back to the caller and terminates the function's execution.

***************************************************************************************************

II. Different Types of Functions (User-defined/Built-in):
---------------------------------------------------------

    User-defined Functions:
    ----------------------

    def add_numbers(x, y):
        return x + y


    Built-in Functions:
    -------------------

    result = len("Hello, World!")

***************************************************************************************************
III. Nested/Recursive/Decorator:
--------------------------------

    Nested Function:
    ----------------

    def outer_function(x):
        def inner_function(y):
            return x + y
        return inner_function

    result = outer_function(5)(3)


    Recursive Function:
    -------------------
    
    def factorial(n):
        if n == 0:
            return 1
        else:
            return n * factorial(n-1)

    Decorator Function:
    -------------------

    def decorator(func):
        def wrapper():
            print("Before function execution")
            func()
            print("After function execution")
        return wrapper

    @decorator
    def my_function():
        print("Executing my_function")

    my_function()

***************************************************************************************************
IV. Different types of Arguments:
----------------------------------------

    Positional Arguments:
    ---------------------

    def add(x, y):
        return x + y

    result = add(3, 5)


    Keyword Arguments:
    ------------------

    def greet(name, message):
        print(f"Hello, {name}! {message}")

    greet(message="Welcome", name="Python")

    Default arguments:
    ------------------
    - Feature that allows you to provide default values for parameters in a function. 
    - When a function is called, if a value for a parameter is not provided by the caller, 
      the default value specified in the function definition is used.

    def function_name(param1, param2=default_value):
    # logic implementation
    
    param1: Required parameter without a default value.
    param2: Optional parameter with a default value.

    *args **kwargs:
    ---------------
        - *args    : allows a function to accept any number of positional arguments.
        - **kwargs : allows a function to accept any number of keyword arguments.

        Example:
        --------

        def variable_args(*args, kwargs):
          """Prints positional and keyword arguments."""
          print("Positional arguments : ", args)
          print("Keyword arguments    : ", kwargs)

        variable_args(1, 2, 3, name='John', age=25)

***************************************************************************************************

V. Anonymous Function (Lambda Function):
----------------------------------------

    - A lambda function is an anonymous function created using the 'lambda' keyword. 
    - It is a way to define a small, one-time-use function without the need for a formal function definition using 'def'. 
    - Lambda functions are a powerful tool when you need a quick, disposable function for simple operations.

    Syntax:
    -------

    lambda arguments: expression

        - 'lambda'     : Keyword indicating the creation of a lambda function.
        - 'arguments'  : Comma-separated list of input parameters.
        - 'expression' : Single expression to be evaluated and returned.



Note:
-----
    - Typing Module
    - adding type hints to function parameters, return values, and variables.
    - isinstance --
    - what are identifiers in python
    - map, filter, reduce, zip --> with lambda
    
