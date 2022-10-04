# Data Collection

## List
**List Feature:**
- Lists are ordered.
- Lists can contain any arbitrary objects.
- List elements can be accessed by index.
- Lists can be nested to arbitrary depth.
- Lists are mutable.
- Lists are dynamic.



**1. Create**

List starts with an open square bracket and ends with a closed square bracket:
```python
list1 = [10, "hi", 7.5, True]
print(list1) #output is [10, "hi", 7.5, True]

list2 = []
print(list2) #output is []
```
The elements inside a list may have different types. Some of them may be integers, others floats, and yet others may be lists.

**2. Add**


- append (value)

  It takes its argument's value and puts it at the end of the list.
  ```python
  a = ['a','b']
  a.append(123)
  print(a) #output is ['a','b','123']
  ```

- insert (location, value)

  It can add a new element at any place in the list, not only at the end.
  ```python
  a = ['a','b']
  a.insert(1,123)
  print(a) #output is ['a',123,'b']
  ```

- extend (list)

It can extend a list to another list.
```python
a = ['a','b']
b = [1,2]
a.extend(b)
print(a) #output is ['a', 'b', 1, 2]
```


**3. Read**

- index

The value inside the brackets which selects one element of the list is called an index.

While the operation of selecting an element from the list is known as indexing.
```python
a = ['num1','num2','num3']
print(a[1]) #output is num2
print(a[-1]) #output is num3
```
**Note**: 
- The elements in a list are always numbered starting from zero
- Negative indices are legal, an element with an index equal to -1 is the last one in the list.



**4. Update**
```python
a = ['num1','num2','num3']
a[1] = 123
print(a) #output is ['num1', 123, 'num3']
```

**5. Delete**
- del
- remove (value)
- pop (index)
- clear
```python
# del an element or the entire list
a = ['num1','num2','num3']
del a[0]
print(a) #output is ['num2','num3']
del a 
print() #output is empty

# remove a specific value from list
b = ['num1','num2','num3']
b.remove('num2')
print(b) #output is ['num1', 'num3']

# pop the element fron list
c = ['num1','num2','num3']
c.pop(2)
print(c) #output is ['num1', 'num2']

# clear all elements in the list
d = ['num1','num2','num3']
d.clear()
print(d) #output is []

```



## Tuple

## Dictionary

## String
