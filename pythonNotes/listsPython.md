createdAt: "2019-08-20T17:56:14.142Z"
updatedAt: "2021-06-01T20:25:13.862Z"
type: "MARKDOWN_NOTE"
folder: "68038d270558e5b040df"
title: "Python Lists"
tags: [
  "python"
  "list"
  "in"
  "not_in"
  "membership_operator"
]
content: '''
  # Python Lists
  
  - list is compound data type
  - list is an ordered sequence
  - lists are mutable (unlike tuples)

  ## Creating lists
  
  ```python
  lst = [0] * 3
  # [0, 0, 0]
  
  my_list = [1, 'foo', 3.14, [11, 12], ('bar', 3)]
  ```
  - lists ca- n be indexed
  ```python
  print(my_list[0])
  # 1
  print(my_list[3][1])
  # 12
  print(my_list[-1])
  # ('bar', 3)
  ```
  
  ### list comprehension
  ```python
  
  ```
  
  ## Slicing lists
  - lists can be sliced
  ```python
  my_list[1:3]
  # ['foo', 3.14]
  ```
  
  - list can be reversed by slicing
  ```python
  a = 'alma'
  b = a[::-1]
  # 'amla'
  
  my_list = [1, 2, 3]
  reversed = my_list[::-1]
  # [3, 2, 1]
  ```
  - lists can be concatenated
  ```python
  long_list = [1, 2, 3] + [1, 1]
  # [1, 2, 3, 1, 1]
  ```
  
  ### Modifying lists

  #### Adding elements with `append()` vs `extend()`
  
  - use `extend()` to concatenate new elements to list
  ```python
  lst = [1, 2, 3]
  lst.extend([4, 5])
  print(lst)
  # [1, 2, 3, 4, 5]
  ```
  - use `append()` to add one new element to list
  ```python
  lst = [1, 2, 3]
  lst.append([4, 5])
  print(lst)
  # [1, 2, 3, [4, 5]]
  ```

  ### Add element with `insert()`
  - use `insert()` to insert an item at a specified index
  ```python
  my_list = [1, 2, 3]
  my_list.insert(1, 'bob')
  ````


  ### Change element based on index
  ```python
  lst = [1, 2, 3]
  lst[1] = 1
  print(lst)
  # [1, 1, 3]
  ```

  ### Delete element

  - use `del()` to delete a specific element
  ```python
  lst = [1, 2, 3]
  del(lst[2])
  print(lst)
  # [1, 2]
  ``` 
  
  - use `pop(index)` to delete and return element at index
  - if index is not specified it deletes and returns the last element
  ```python
  lst = [1, 2, 3]
  last_element = lst.pop()
  print(lst)
  # [1, 2]
  ``` 
  
  ### Converting strings to lists
  
  - use `split()` to separate string to list elements
  default separation character is space
  ```python
  my_str = 'one,two three'
  lst1 = my_str.split();
  print(lst1)
  # ['one, two', 'three']
  lst2 = my_str.split(',')
  print(lst2)
  # ['one', 'two three']
  ```
  ### Converting lists to string
  ```python
  lst = ['h', 'e', 'l', 'l', 'o']
  str = ''.join(lst)
  # 'hello'
  ``````
  
  ### Aliasing & Copying by Value
  When we set variable B equal to the list variable A both are referencing the same list in memory
  ```python
  A = [1, 2, 3]
  B = A
  B[1] = 5
  print(A)
  # [1, 5, 3]
  ```
  
  To assign a copy of list A to list B:
  ```python
  A = [1, 2, 3]
  B = A[:]]
  B[1] = 5
  print(A)
  # [1, 2, 3]
  ```
  
  ## Useful Built In Functions
  
  ```python
  my_list = [3, 2, 5]
  
  max(my_list)  # returns 5
  
  min(my_list)  # returns 2
  
  # returns a copy of the list sorted
  # leaves original list unchanged
  sorted_list = sorted(my_list, reverse=True)
  ```
  
  
  ## Membership Operators
  `in` and `not in`
  ```python
  seasons = ['spring', 'summer', 'fall', 'winter']
  
  print('spring' in seasons)
  # True
  
  print('Monday' not in seasons)
  # True
  
  ```
  
  ## List Manipulation
  
  ```python
  str_of_numbers = '-1 8 5'
  str_arr = str_of_numbers.split(' ')
  # -> ['-1', '8', '5']
  num_array = list(map(lambda x: int(x), str_arr))
  # -> [-1, 8, 5]
  ```
  
  
'''
linesHighlighted: []
isStarred: false
isTrashed: false
