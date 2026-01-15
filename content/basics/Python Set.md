---
title: Python Set
date: 2026-01-15
author: Your Name
cell_count: 33
score: 30
---

Creating a Set


```python
A = set()
print(A)
```

    set()
    


```python
B = {1, 2, 3, 4}
print(B)
```

    {1, 2, 3, 4}
    


```python
set = {1, "Python", 3.5, True}
print(set)
```

    {1, 3.5, 'Python'}
    

Automatic Removal of Duplicates


```python
num = {1, 2, 2, 3, 3, 4, 6, 7, 7, 8 , 8}
print(num) 
```

    {1, 2, 3, 4, 6, 7, 8}
    


```python
f = {"apple", "banana"}
f.add("orange")
print(f)
```

    {'banana', 'orange', 'apple'}
    

Adding Multiple Elements with update()


```python
c = {"red", "green"}
c.update(["blue", "yellow"])

print(c)
```

    {'green', 'blue', 'red', 'yellow'}
    

Removing Elements from a Set


```python
num = {10, 20, 30, 40, 50}
num.remove(20)
print(num)
```

    {50, 40, 10, 30}
    


```python
num = {10, 20, 30, 40, 50}
num.discard(50)
print(num)
```

    {20, 40, 10, 30}
    


```python
num = {10, 20, 30, 40, 50}
num.discard(10)
print(num)
```

    {50, 20, 40, 30}
    


```python
num = {10, 20, 30, 40, 50}
num.discard(30)
print(num)
```

    {50, 20, 40, 10}
    

 Set Length and Membership


```python
data = {5, 10, 15}
print(len(data))  
```

    3
    


```python
data = {5, 10, 15, 78, 56,43}
print(len(data))  
```

    6
    


```python
print(10 in data) 
```

    True
    


```python
print(100 not in data)

```

    True
    


```python
print(10 not in data)
```

    False
    

 Iterating Through a Set


```python
language = {"Python", "Java", "Go"}
for lang in language:
    print(lang)
```

    Java
    Go
    Python
    

Mathematical Set Operations


```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}
print(A | B)
```

    {1, 2, 3, 4, 5, 6}
    


```python
print(A & B)  
```

    {3, 4}
    


```python
print(A - B)
```

    {1, 2}
    


```python
print(A ^ B)
```

    {1, 2, 5, 6}
    


```python
A = {1, 2, 3}
B = {1, 2}

print(B.issubset(A)) 
```

    True
    


```python
print(A.issuperset(B))
```

    True
    


```python
print(A.issubset(B)) 
```

    False
    

Converting Sets to Other Types


```python
set = {1, 2, 3}
listv = list(set)
print(listv) 
```

    [1, 2, 3]
    


```python
tuplev = tuple(set)
print(tuplev)
```

    (1, 2, 3)
    


---
**Score: 30**