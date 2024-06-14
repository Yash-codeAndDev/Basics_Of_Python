# Dictionary

## Creating Dictionary

* creating empty dictionary
```python
    user_a = {}
    print(user_a) # {}

    user_b = dict()
    print(user_b) # {}
```

* creating dictionary with initial values using {}
```python

    user_a = {
        'name' : 'Yash Khati',
        'Roll No' : 2018899,
        'University' : "GEHU",
        3 : 8,  # can have number as key
        (1,2) : "tuple Key", # can have tuple as key
        True : "Yes", 
        None : "None Value",
    }
    print(user_a) # {'name': 'Yash Khati', 'University': 'GEHU', 3: 8, (1, 2): 'tuple Key', True: 'Yes', None: 'None Value'}


```
>[!Note] 
> * dictionary keys must be immutable and hashable e.g(Integer, Float, String, Tuples, Boolean, None , custom Objects)

* creating dictionary with initial values using dict()

```python
    
user_b = dict(name = 'Yash',University = "GEHU" )

user_b[3] = 8
user_b[(1, 2)] = "tuple Key"
user_b[True] = "Yes"

print(user_b) # {'name': 'Yash', 'University': 'GEHU', 3: 8, (1, 2): 'tuple Key', True: 'Yes'}


user_c = dict([
    ('Name', 'Yash'),
    (3, 8),
    (True, "Yes"),
    (None, "Nothing"),
    ((1, 2), "tuple key")
])

print(user_c) # {'Name': 'Yash', 3: 8, True: 'Yes', None: 'Nothing', (1, 2): 'tuple key'}

```
>[!Note]
> -  When using the dict() function to create a dictionary, the keys must be strings that are valid Python identifiers
> -  If we want to use non-string keys, keys with spaces, or other types such as tuples, integers, or booleans, you cannot directly pass them as arguments to the dict() function.We need to add those keys separately


## Mutablity Of Dictionary



* Updation of Key-Value Pair

    - user[key] = value -> if key exist value is updated and if it does not exist a new key-value pair is created

    ```python
        user_a = {
        'name' : 'Yash Khati',
        'university' : "GEHU",
        'Roll_No' : 2018877,
        (1,2) : "tuple Key",
        True : "Yes",
        }
        user_a['Roll_No'] = 2018821 
        print(user_a) # {'name': 'Yash Khati', 'university': 'GEHU', 'Roll_No': 2018821, (1, 2): 'tuple Key', True: 'Yes'}
    ```
    - update( pairs ) -> Updates multiple key-value pairs in the dictionary from another dictionary or iterable of key-value pairs.

    ```python
        user_a = {
            'name' : 'Yash Khati',
            'university' : "GEHU",
            'Roll_No' : 2018877,
            (1,2) : "tuple Key",
            True : "Yes",
        }

        user_a.update( {True : "No", 'name' : "Ayush Rawat"} )
        print(user_a) # {'name': 'Ayush Rawat', 'university': 'GEHU', 'Roll_No': 2018877, (1, 2): 'tuple Key', True: 'No'}



        # updation using another dictionary
        
        user_b = {
            "name" : "Yash",
            "university" : "GEHU",
            "Semester" : 8,
        }

        user_a.update(user_b)
        print(user_a) # {'name': 'Yash', 'university': 'GEHU', 'Roll_No': 2018877, (1, 2): 'tuple Key', True: 'No', 'Semester' : 8}
    ```

* dict.get(key, default=None) -> Returns the value for the specified key if the key is in the dictionary. If not, returns the default value.

    ```python
        user_a = {
            'name' : 'Yash Khati',
            'university' : "GEHU",
            'Roll_No' : 2018877,
            (1,2) : "tuple Key",
            True : "Yes",
        }

        print(user_a.get('name'))

        print(user_a.get('Section' , 'N/A'))
    ```

* get all keys, values and entries

```python
    user_a = {
    'name' : 'Yash Khati',
    'university' : "GEHU",
    'Roll_No' : 2018877,
    (1,2) : "tuple Key",
    True : "Yes",
    }

    # get all keys : 
    print(user_a.keys()) # dict_keys(['name', 'university', 'Roll_No', (1, 2), True])

    # get all values : 
    print(user_a.values()) # dict_values(['Yash Khati', 'GEHU', 2018877, 'tuple Key', 'Yes'])

    # get all items : 
    print(user_a.items())
    # dict_items([('name', 'Yash Khati'), ('university', 'GEHU'), ('Roll_No', 2018877), ((1, 2), 'tuple Key'), (True, 'Yes')])
```
* dict.pop(key, default) -> Removes the specified key and returns the corresponding value. If the key is not found, returns the default value if provided; otherwise, raises a KeyError
    ```python
        user_a = {
            'name' : 'Yash Khati',
            'university' : "GEHU",
            'Roll_No' : 2018877,
            False : "No",
        }

        print( user_a.pop("name")) # Yash Khati

        print(user_a.pop('Section', "No Available Value")) # No Available Value
    ```

* dict.popitem() -> Removes and returns a random (key, value) pair as a tuple. Raises a KeyError if the dictionary is empty.
    ```python      
        user_a = {
            'name' : 'Yash Khati',
            'university' : "GEHU",
            'Roll_No' : 2018877,
            False : "No",
        }

        print( user_a.popitem()) 
    ```

* dict.setdefault(key, default=None) -> Returns the value of the specified key. If the key does not exist, inserts the key with the specified default value.

    ```python
        user_a = {
            'name' : 'Yash Khati',
            'university' : "GEHU",
            'Roll_No' : 2018877,
            False : "No",
        }
        print(user_a.setdefault("name", "Ayush")) # Yash Khati
        print(user_a.setdefault("Section", "C")) # C
        print(user_a) # {'name': 'Yash Khati', 'university': 'GEHU', 'Roll_No': 2018877, False: 'No', 'Section': 'C'}

    ```