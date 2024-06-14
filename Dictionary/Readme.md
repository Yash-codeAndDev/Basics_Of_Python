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