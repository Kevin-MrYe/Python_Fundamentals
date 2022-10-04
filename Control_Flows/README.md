# Control Flows

## Conditional statements
**1. if**
```python
x = 10

if x == 10: # condition
    print("x is equal to 10")  # Executed if the condition is True.
```

**2. if-else**
```python
x = 10

if x < 10:  # Condition
    print("x is less than 10")  # Executed if the condition is True.

else:
    print("x is greater than or equal to 10")  # Executed if the condition is False.
```

**3. if-elif-else**
```python
x = 10

if x == 10:  # True
    print("x == 10")

if x > 15:  # False
    print("x > 15")

elif x > 10:  # False
    print("x > 10")

elif x > 5:  # True
    print("x > 5")

else:
    print("else will not be executed")

```

**4. Nest conditional statements**
```python
x = 10

if x > 5:  # True
    if x == 6:  # False
        print("nested: x == 6")
    elif x == 10:  # True
        print("nested: x == 10")
    else:
        print("nested: else")
else:
    print("else")
```

Note:
* you mustn't use else without a preceding if;
* else is always the last branch of the cascade, regardless of whether you've used elif or not;
* else is an optional part of the cascade, and may be omitted;
* if there is an else branch in the cascade, only one of all the branches is executed;
* if there is no else branch, it's possible that none of the available branches is executed.

## While loop
While loop executes a statement or a set of statements as long as a specified boolean condition is true.
```python
counter = 5
while counter > 2:
    print(counter)
    counter -= 1 #output is 5 4 3
```

## For Loop
For loop executes a set of statements many times; it's used to iterate over a sequence.
```python
# Example 1
word = "Python"
for letter in word:
    print(letter, end="*") #output is P*y*t*h*o*n*

# Example 2
for i in range(1, 10):
    if i % 2 == 0:
        print(i) #output is 2 4 6 8
```

## Break and Continue
**Break:**

Use break to exit a loop
```python
text = "Hello Python"
for letter in text:
    if letter == "P":
        break
    print(letter, end="") ## output is Hello
```

**Continue:**

Use continue to skip the current iteration, and continue with the next iteration,
```python
text = "pyxpyxpyx"
for letter in text:
    if letter == "x":
        continue
    print(letter, end="") #output is pypypy
```

## While-else and For-else

The while and for loops can also have an else clause in Python.

The else clause executes after the loop finishes its execution as long as it has not been terminated by break.
```python
n = 0

while n != 3:
    print(n)
    n += 1
else:
    print(n, "else") #output is 0 1 2 3 else

print()

for i in range(0, 3):
    print(i)
else:
    print(i, "else") #output is 0 1 2 2 else
```

## Range()

The range() function generates a sequence of numbers. It accepts integers and returns range objects. 

The syntax of range() looks as follows: **range(start, stop, step)**
* start is an optional parameter specifying the starting number of the sequence (0 by default)
* stop is an optional parameter specifying the end of the sequence generated (it is not included),
* step is an optional parameter specifying the difference between the numbers in the sequence (1 by default.)

```python
for i in range(3):
    print(i, end=" ")  # Outputs: 0 1 2

for i in range(6, 1, -2):
    print(i, end=" ")  # Outputs: 6, 4, 2
```




