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


