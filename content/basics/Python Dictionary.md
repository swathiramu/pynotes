---
title: Python Dictionary
date: 2026-01-14
author: Your Name
cell_count: 27
score: 25
---

 Creating a Dictionary


```python
dict = {}
print(dict)
```

    {}
    


```python
student = {"name": "Alice", "age": 22, "grade": "A"}
print(student)
```

    {'name': 'Alice', 'age': 22, 'grade': 'A'}
    

Accessing Dictionary Values


```python
emp = {"id": 186, "name": "Swathi", "role": "Developer"}
print(emp)
```

    {'id': 186, 'name': 'Swathi', 'role': 'Developer'}
    


```python
emp = {"id": 186, "name": "Swathi", "role": "Developer"}
print(emp["name"])
```

    Swathi
    


```python
emp = {"id": 186, "name": "Swathi", "role": "Developer"}
print(emp.get("role"))
```

    Developer
    

Adding and Updating Dictionary Entries


```python
prof = {"username": "admin"}
prof["email"] = "swathiramu28@gmail.com"
prof["username"] = "admin"
print(prof)
```

    {'username': 'admin', 'email': 'swathiramu28@gmail.com'}
    

Removing Items from a Dictionary


```python
data = {"a": 1, "b": 2, "c": 3}
removed = data.pop("b")
del data["a"]
print(data)    
```

    {'c': 3}
    


```python
print(removed)
```

    2
    

Dictionary Length and Membership


```python
set = {"theme": "dark", "version": 1.0}
print(len(set))  
```

    2
    


```python
print("theme" in set) 
```

    True
    

Iterating Through Dictionaries


```python
user = {"name": "Swathi", "age": 21, "city": "London"}

for key in user:
    print(key, ":", user[key])

for key, value in user.items():
    print(key, "=>", value)
```

    name : Swathi
    age : 21
    city : London
    name => Swathi
    age => 21
    city => London
    

Dictionary Methods


```python
data = {"x": 10, "y": 20}
print(data.keys()) 
```

    dict_keys(['x', 'y'])
    


```python
print(data.values())
```

    dict_values([10, 20])
    


```python
print(data.items()) 
```

    dict_items([('x', 10), ('y', 20)])
    

Merging Dictionaries


```python
dict1 = {"a": 1, "b": 2}
dict2 = {"c": 3, "d": 4}
merged = dict1 | dict2
print(merged)
```

    {'a': 1, 'b': 2, 'c': 3, 'd': 4}
    

Nested Dictionaries


```python
employee = {"id": 101,"personal": {"name": "John","email": "john@example.com"}}
print(employee["personal"]["name"])
```

    John
    

 Dictionary Comprehension


```python
squa = {x: x**2 for x in range(5)}
print(squa) 
```

    {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
    


---
**Score: 25**