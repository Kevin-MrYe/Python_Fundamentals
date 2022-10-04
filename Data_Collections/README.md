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

## Dictionary

## String
