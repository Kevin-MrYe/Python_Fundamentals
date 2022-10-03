# Python_Fundamentals
## Definitions of terms

1. **Natural language** :Natural language such as English is the language, which is spoken and written for communication.

2. **Programming language** :Programming languages are used for developing computer programs, which enable a computer to perform some operations.

3. **Source code** : A program written in a high-level programming language.

4. **Source file** : The file containing the source code.

There are two different ways of transforming a program from a high-level programming language into machine language:

5. **Compilation** : The source program is translated once by getting a file containing the machine code, execution will be faster.

6. **Interpretation** : The source program is translated each time it has to be run.

6. **Positional arguments** : The arguments whose meaning is dictated by their position.

6. **Keyword arguments** : The arguments whose meaning is not dictated by their location, but by a special word (keyword) used to identify them.

## Print ( )
```python
print(*objects, sep=' ', end='\n')
```
The sep parameter specifies the separator between the outputted arguments.

The end parameter specifies what to print at the end of the print statement.



## Input ( )

## Literals
A literal is data whose values are determined by the literal itself.

1. **String** : "I am a literal."

  Escape Character: \
  
  ```python
  'I\'m happy' = "I'm happy"
  ```
  Two ways to encode apostrophe or quote:
  * Using Escape character \
  * Open and close the string using an opposite set of symbols(e.g., "I'm happy.",  'He loves "Python" very much' )

2. **Integers** : They are numbers written without a fractional component, e.g., 256, or -1 (negative integers).

    You can write this number either like this: 11111111, or like that: 11_111_111.

    Note:Python 3.6 has introduced underscores in numeric literals, allowing for placing single underscores between digits and after base specifiers for improved readability.

3. **Float** : They are numbers that contain (or are able to contain) a fractional component, e.g., 1.27.

    Scientific notation: 3E8 = 3*pow(10,8)

    **Note**:
    The exponent (the value after the E) has to be an integer;
    The base (the value in front of the E) may be an integer.

4. **Boolean** : The two constant objects True and False used to represent truth values.

5. **Octal and Hexadecimal**:

    Octal: An integer number is preceded by an 0O or 0o prefix (zero-o), it will be treated as an octal value.(e.g. 0o123 = 83)
    
    Hexadecimal: An integer number is preceded by an 0x or 0X prefix (zero-x), it will be treated as an hexadecimal value.(e.g. 0x123 = 291)

6. **None**: It is used to represent the absence of a value.

## Operators
**Unary operator** vs **binary operator**:
```
* A unary operator is an operator with only one operand, e.g., -1, or +3.
* A binary operator is an operator with two operands, e.g., 4 + 5, or 12 % 5.
```

**Integer** vs **float** Rules:
```
* When both ** arguments are integers, the result is an integer, too;
* When at least one ** argument is a float, the result is a float, too.
* But there is an exception: The result produced by the division operator is always a float.
```
1. Addition ("+")
```python
print(-4 + 4) #output is 0
print(-4. + 8) #output is 4.0
```
2. Substraction ("-")
```python
print(-4 - 4) #output is -8
print(4. - 8) #output is -4.0
print(-1.1) #output is -1.1
```
3. Multiplication ("*")
```python
print(2 * 3) #output is 6
print(2 * 3.) #output is 6.0
print(2. * 3) #output is 6.0
print(2. * 3.) #output is 6.0
```

4. Division ("/")
```python
print(6 / 3) #output is 2.0
print(6 / 3.) #output is 2.0
print(6. / 3) #output is 2.0
print(6. / 3.) #output is 2.0
```
5. Integer division ("//")
6. Modulo ("%")
7. Exponentiation (**)
```python
print(2 ** 3) #output is 8
print(2 ** 3.) #output is 8.0
print(2. ** 3) #output is 8.0
print(2. ** 3.) #output is 8.0
```

    
