---
title: Python Tuple
date: 2026-01-13
author: Your Name
cell_count: 32
score: 30
---

Creating a Tuple


```python
empty = ()
print(empty)
```

    ()
    


```python
single= (10)
print(single)
```

    10
    


```python
num = (1, 2, 3, 4)
print(num)
```

    (1, 2, 3, 4)
    


```python
mixed = (10, "Python", True)
print(mixed)
```

    (10, 'Python', True)
    

Accessing Tuple Elements


```python
colors = ("red", "green", "blue")
print(colors[0])
```

    red
    


```python
print(colors[-1])
```

    blue
    


```python
print(colors[-2])
```

    green
    


```python
print(colors[1])
```

    green
    

Slicing Tuples


```python
values = (0, 1, 2, 3, 4)
print(values[1:4])
```

    (1, 2, 3)
    


```python
values = (0, 1, 2, 3, 4)

print(values[0:3])
```

    (0, 1, 2)
    

Tuple Packing and Unpacking


```python
person = ("Swathiii", 21, "Engineer")
name, age, profession = person
```


```python
print(name) 
```

    Swathiii
    


```python
print(age) 
```

    21
    


```python
print(profession)
```

    Engineer
    

Nested Tuples


```python
data = ((1, 2), (3, 4), (5, 6))
print(data[1])
```

    (3, 4)
    


```python
print(data[2])
```

    (5, 6)
    


```python
print(data[1][0])
```

    3
    


```python
print(data[2][1])
```

    6
    

Tuple Length and Membership


```python
num = (10, 20, 30)
print(len(num))
```

    3
    


```python
numbers = (10, 20, 30, 78, 90)

print(len(numbers))
```

    5
    


```python
print(20 in numbers) 
```

    True
    


```python
print(60 in numbers) 
```

    False
    

Iterating Through a Tuple


```python
languages = ("Python", "Java", "Go")
for lang in languages:
    print(lang)
```

    Python
    Java
    Go
    

Converting Between Tuples and Lists


```python
values = (1, 2, 3)

list1 = list(values)
tuple1 = tuple(list1)

print(list1)   
print(tuple1) 
```

    [1, 2, 3]
    (1, 2, 3)
    


---
**Score: 30**