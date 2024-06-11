# List

## Creating List : 

* Empty List 
```python
    list_one = []

    list_two = list() # useful when you need to convert another iterable to a list
```
* List with default values
```python
    list_one = ["Yash" , 23, "GEHU"]

    tuple_two = ("Iron Man" , 2013 , "Thor")    
    list_two = list( tuple_two)
```

## Mutability of List

* append() -> adding single element/object element at end list
```python

    list_one = ["yash" , 23 , "Naruto" , "Iron Man"]
    list_one.append("Thor")
    print(list_one) # ["yash" , 23 , "Naruto" , "Iron Man", "Thor"]

    list_one.append(["America" , "India", France])
    print(list_one) # ['yash', 23, 'Naruto', 'Iron Man', 'Thor', ['America', 'India', 2020]]
 
```

* extend() -> adding multiple elements at end of list
```python
    
    list_a = ["Yash" , 23 , True]
    print(list_a)

    list_a.extend(("Iron Man", "Thor", 2020)) # Covnert Ittrable to list components
    print(list_a)

```

* insert(int pos, int ele) -> adding element at given position in list
```python
    list_a = ["Yash" , 23 , True]
    print(list_a)

    list_a.insert(1,"GEHU")
    print(list_a)

    list_a.insert(5,"Iron Man") # insert at end of list by default
    print(list_a)
```

* remove(int ele) -> remove element from the list
    - if element is not present on list Error occurs

``` python
    list_a = ['Yash', 'GEHU', 23, True, 'Hulk', 'Iron Man']
    list_a.remove(True)
    print(list_a) # ['Yash', 'GEHU', 23, 'Hulk', 'Iron Man']
```

* pop(int index) ->  remove and return an element from the list, but by default it removes only the last element of the list

``` python

    list_a = ['Yash', 'GEHU', 23, True, 'Hulk', 'Iron Man']
    removed_element = list_a.pop()
    print("removed_element : {} , -> new list {}".format(removed_element, list_a)) # By default remove last element

    remover_element = list_a.pop(1) # remove element at index 1
    print(list_a)   
    
```

## Some commom functions performed on List

* index(int element) -> find first occurrence index of element if exist else give error

```python
    list_a = ['Yash', 'GEHU', 23, True,'GEHU', 'Hulk', 'Iron Man']
    print(list_a.index("GEHU")) # 2
    print(list_a.index(1)) # 3 -> 1 in python is Equivalent to True therefore output is 3

```

* count(int element) -> returns frequency of element in list

```python

    list_a = [1 , 2, 3, 4, 4, 2, 2, 7, 9]
    print(list_a.count(2)) # 3
    print(list_a.count(12)) # 0
```

*  copy() -> returns shallow copy of list 
```python
    
    list_a = ['Yash',23, True,'GEHU', 'Hulk', 'Iron Man']

    list_b = list_a.copy()
    print(list_b) #  ['Yash',23, True,'GEHU', 'Hulk', 'Iron Man']


    list_b[1] = 10
    print(list_a) #  ['Yash',23, True,'GEHU', 'Hulk', 'Iron Man']
    print(list_b) # #  ['Yash',10, True,'GEHU', 'Hulk', 'Iron Man']


    list_a = [1, 2, 3, 4, 5, 6 ,[ 7, 8, 9]]
    list_b = list_a.copy()

    list_b[6][1] = 18
    print(list_a) # [1, 2, 3, 4, 5, 6 ,[ 7, 8, 9]]
    print(list_b) # [1, 2, 3, 4, 5, 6 ,[ 7, 8, 9]]

```
>[!Note]
>- copy() creates shallow copy i.e in case of nested objects it copy reference of object
>- deepcopy() is used to created when we need to ensure complete independence between original and copy in case of nested list
```python
    import copy
    list_a = [1, 2, 3, 4, 5, 6 ,[ 7, 8, 9]]
    list_b = copy.deepcopy(list_a)

    list_b[6][1] = 18
    print(list_a)
    print(list_b)
```

