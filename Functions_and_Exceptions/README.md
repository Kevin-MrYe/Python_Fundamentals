# Functions and Exceptions

**Positional arguments VS Keyword arguments VS Default Parameters :** 

Positional arguments are the ones whose meaning is dictated by their position, 

Keyword arguments are the ones whose meaning is not dictated by their location, but by a special word (keyword) used to identify them.

Default parameters allow some arguments to be omitted when the function is called.


**Function VS Methods**

A function doesn't belong to any data - it gets data, it may create new data and it (generally) produces a result.In general, a typical function invocation may look like this:
```
result = function(arg)
```

A method is owned by the class it works for, while a function is owned by the whole code. A typical method invocation usually looks like this:
```
result = data.method(arg)
```

## Function
**1. When need a function:**

- if a particular fragment of the code begins to appear in more than one place
- if a piece of code becomes so large that reading and understating it may cause a problem

**2. Four basic types of functions:**
- Built-in functions
- Functions come from pre-installed modules
- User-defined functions
- Lambda functions


**3. Function definition and call:**
```
def function_name(parameter):
    function_body
function_name(arguments)
```

**Note:**

- The function definition should always be present before the function call. Otherwise, we will get an error.
- The parameters exist only inside functions in which they have been defined.
- The arguments exist outside functions, and are carriers of values passed to corresponding parameters.

**4. shadowing**

It's legal, and possible, to have a variable named the same as a function's parameter. A situation like this activates a mechanism called **shadowing**:
```python
def message(number):
    print("Enter a number:", number) #output: 1

number = 1234
message(1)
print(number) #output: 1234
```

**Note:**

- Parameter number shadows any variable of the same name, but only inside the function.

**5. Arguments passing**

- Positional argument passing
- Keyword (named) argument passing
- Mix of positional and keyword argument passing
```python
# Positional argument passing
def subtra(a, b):
    print(a - b)

subtra(5, 2)    # outputs: 3
subtra(2, 5)    # outputs: -3

# Keyword (named) argument passing
def subtra(a, b):
    print(a - b)

subtra(a=5, b=2)    # outputs: 3
subtra(b=2, a=5)    # outputs: 3

# Mix of positional and keyword argument passing
def subtra(a, b):
    print(a - b)

subtra(5, b=2)    # outputs: 3
subtra(a=5, 2)    # outputs: SyntaxError: positional argument follows keyword argument
```

**Note:**

- Positional arguments mustn put before follow keyword arguments, otherwise syntaxerror will be raised.

**6. Default parameters**
```python
def name(first_name, last_name="Smith"):
    print(first_name, last_name)

name("Andy")    # outputs: Andy Smith
name("Betty", "Johnson")    # outputs: Betty Johnson (the keyword argument replaced by "Johnson")

def name(first_name='Smith', last_name):
    print(first_name, last_name) #outputs: non-default argument follows default argument
```

**Note:**

- All default parameters must follow non-default parameters.

**7. Return statements**

- return without an expression
- return with an expression
- No return statement

```python
# return with an expression
def multiply(a, b):
    return a * b

print(multiply(3, 4))    # outputs: 12

# return without an expression
def multiply(a, b):
    return

print(multiply(3, 4))    # outputs: None

# No return statement,but it will be executed implicitly at the end of the function.
def multiply(a, b):
    pass

print(multiply(3, 4))    # outputs: None
```

**Note:**

-  if a function doesn't return a certain value using a return expression clause, it is assumed that it implicitly returns None.

**8. Variable Scope**

- A variable that exists outside a function has a scope inside the function body unless the function defines a variable of the same name
```python
var = 2

def mult_by_var(x):
    return x * var

print(mult_by_var(7))    # outputs: 14

# function defines a variable of the same name
# the function variable will shadow the variable outside the function
def mult(x):
    var = 7
    return x * var

var = 3
print(mult(7))    # outputs: 49
```
- A variable that exists inside a function has a scope inside the function body, it is inaccessiable outside the function.
```python
def adding(x):
    var = 7
    return x + var

print(adding(4))    # outputs: 11
print(var)    # NameError
```

- Use the global keyword followed by a variable name to make the variable's scope global.
```python
var = 2
print(var)    # outputs: 2

def return_var():
    global var
    var = 5
    return var

print(return_var())    # outputs: 5
print(var)    # outputs: 5

```

## Exceptions

**1. Types of errors**

- Syntax errors(parsing errors)

Syntax errors occur when the parser comes across a statement that is incorrect.
```python
print("Hello, World!) #output: SyntaxError: EOL while scanning string literal
```
- Exceptions

Exceptions occur even when a statement/expression is syntactically correct; these are the errors that are detected during execution.
```python
# ZeroDivisionError
# perform any operation which provokes division in which the divider is zero
print(1/0) #ZeroDivisionError

# ValueError
# when a function receives an argument of a proper type, but its value is unacceptable.
print(int('hello'))

# TypeError
# Apply a data whose type cannot be accepted in the current context.
short_list = [1]
one_value = short_list[0.5] # TypeError

# AttributeError
# Activate a method which doesn't exist in an item you're dealing with.
short_list = [1]
short_list.append(2)
short_list.depend(3) # AttributeError
```

