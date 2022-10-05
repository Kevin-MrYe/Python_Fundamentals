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
- pop (index=-1)
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

**Note:**

- if remove() an element which is not in list, an exception is raised.
- a.pop() simply removes the last item in the list:
- pop() returns a value: the item that was removed.

**6. Sorting a list**
- sort()
- sorted()
- reverse()
```python
# sort() sort the list in-place
lst1 = [5, 3, 1, 2, 4]
lst1.sort()
print(lst1)  # outputs: [1, 2, 3, 4, 5]

# sorted() did not change list, not in-place
lst2 = [5, 3, 1, 2, 4]
print(sorted(lst2)) # outputs: [1, 2, 3, 4, 5]
print(lst2)         # outputs: [5, 3, 1, 2, 4]

# reverse() reverse the list in-place
lst3 = [5, 3, 1, 2, 4]
lst3.reverse()
print(lst3) # outputs: [4, 2, 1, 3, 5]
```

**In and not in Operator**

Test if some items exist in a list or not using the keywords in and not in.
```python
my_list = ["A", "B", 1, 2]

print("A" in my_list)  # outputs: True
print("C" not in my_list)  # outputs: True
print(2 not in my_list)  # outputs: False
```


## Slice

Slice makes a brand new copy of a list, or parts of a list.
```
my_list[start:end:stepsize]
```
- start is the index of the first element included in the slice, default is 0.
- end is the index of the first element not included in the slice, default  is length(list).
- stepsize is the different between two adjacent elements in the slice, default is 1.

```python
lst1 = [1,2,3,4,5,6,7,8]

# with stepsize
lst2 = lst1[1:5:2]
print(lst2) # output: [2, 4]

# negative indice
lst3 = lst1[1:-1]
print(lst3) # output: [2, 3, 4, 5, 6, 7]

# omit star, star from 0
lst4 = lst1[:3]
print(lst4) #output: [1, 2, 3]

# omit end, end at len(my_list)
lst5 = lst1[5:] 
print(lst5) #output: [6, 7, 8]

# omit star&end, makes a copy of the whole list
lst6 = lst1[:]
print(lst6) #output: [1, 2, 3, 4, 5, 6, 7, 8]

# start is further than end, slice will be empty list
lst7 = lst1[-1:2]
print(lst7) #output:[]
```



## Tuple
**Tuple Feature:**
- Tuple is ordered
- Tuple is immutable
- Tuple can be nested
- The values contained in the tuple don’t need to be the same type.

A tuple is an immutable sequence type. It can behave like a list, but it mustn't be modified in situ. You can not append tuples, or modify, or remove tuple elements.



**1. Create**
- using parenthesis
- using commas
```python
# using parenthesis
tuple_1 = (1, 2, 4, 8)
# using commas
tuple_2 = 1., .5, .25, .125

print(tuple_1) #output: (1, 2, 4, 8)
print(tuple_2) #output: (1.0, 0.5, 0.25, 0.125)
```

  **Note:**
  If creating a one-element tuple, having one element within parentheses is not enough. We will need a trailing comma to indicate that it is a tuple.
  ```python
  # define one-element with commas
  one_element_tuple_1 = (1, )
  one_element_tuple_2 = 1.,

  # define one-element without commas
  one_element_tuple_3 = (1)

  print(one_element_tuple_1) #output: (1,)
  print(one_element_tuple_2) #output: (1.0,)
  print(one_element_tuple_3) #output: 1
  ```

**2. Read**
- index
- slice
```python
my_tuple = (1, 10, 100, 1000)

# using index
print(my_tuple[0]) #output: 1

# using negative index
print(my_tuple[-1]) #output: 100

# using slicing
print(my_tuple[1:]) #output: (10, 100, 1000)
print(my_tuple[:-2]) #output:(1, 10)

```
**3. Delete**
Due to the immutability of tuple, we can not change the elements in the tuple. That means can not delete the element, but it is possible to delete the whole tuple.
```python
my_tuple = 1, 2, 3, 
del my_tuple
print(my_tuple)    # NameError: name 'my_tuple' is not defined
```


**4. Unpacking**
```python
my_tuple = (1, 10, 100, 1000)

a,b,c,d = my_tuple
print(a) #output: 1
print(b) #output: 10
print(c) #output: 100
print(d) #output: 1000
```
When unpacking, the number of variables on the left must match the number of values in the tuple

**5. Tuple methods**
- count()
- index()
```python
my_tuple = ('a', 'p', 'p', 'l', 'e',)

print(my_tuple.count('p'))  # Output: 2
print(my_tuple.index('l'))  # Output: 3
```

## Dictionary
**Dictionary Features:**
- Dictionary is mutable.
- Dictionary is dynamic. It can grow and shrink as needed.
- Dictionary can be nested
- The values contained in the dictionary don’t need to be the same type.

In Python 3.6x dictionaries have become ordered collections by default. Your results may vary depending on what Python version you're using.

**1. Creating**
- curly braces {}
- dict()
```python
# dictionary with curly braces
my_dict = {1: 'apple', 2: 'banana'}

# using dict()
my_dict = dict({1:'apple', 2:'banana'})
```

**2. Add and Update**

If the key is already present, then the existing value gets updated. 

If the key is not present, a new (key: value) pair is added to the dictionary.
```
my_dict = {'name': 'Mike','age': 26}

# update value
my_dict['age'] = 27
print(my_dict) #Output: {'name': 'Mike', 'age': 27}

# add item
my_dict['address'] = 'Downtown'
print(my_dict) # Output: {'name': 'Mike', 'age': 27, 'address': 'Downtown'}
```

**3. Read**
- dict[key]
- get[]
```
# [] vs get for retrieving elements
my_dict = {'name': 'Jack', 'age': 26}

print(my_dict['name']) # Output: Jack
print(my_dict.get('age')) # Output: 26

# Trying to access keys which doesn't exist throws error
print(my_dict.get('address')) # Output None
print(my_dict['address']) # KeyError
```

**4. Delete**



## String
