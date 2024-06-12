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

print(user_b)
```
>[!Note]
> - When using the dict() function to create a dictionary, the keys must be strings that are valid Python identifiers
> -  If we want to use non-string keys, keys with spaces, or other types such as tuples, integers, or booleans, you cannot directly pass them as arguments to the dict() function.We need to add those keys separately