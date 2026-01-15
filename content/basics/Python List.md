---
title: Python List
date: 2026-01-15
author: Your Name
cell_count: 32
score: 30
---

Creating a List


```python
empty = []
print(empty)
```

    []
    


```python
num = [1, 2, 3, 4, 5]
print(num)
```

    [1, 2, 3, 4, 5]
    


```python
mix = [60, "Swathi", True, 5.665]
print(mix)
```

    [60, 'Swathi', True, 5.665]
    

Accessing List Elements (Indexing)

f = ["apple", "banana", "orange"]
print(f[0])


```python
print(f[-1])
```

    orange
    


```python
print(f[-2])
```

    banana
    


```python
print(f[2])
```

    orange
    

Slicing Lists


```python
num = [0, 1, 2, 3, 4, 5]
print(num[1:4])
```

    [1, 2, 3]
    


```python
print(num[:3])
```

    [0, 1, 2]
    


```python
print(num[3:]) 
```

    [3, 4, 5]
    

Modifying List Elements


```python
A = ["pen", "pencil", "eraser"]
A[1] = "marker"

print(A) 
```

    ['pen', 'marker', 'eraser']
    


```python
A = ["pen", "pencil", "eraser"]
A[2] = "scale"

print(A) 
```

    ['pen', 'pencil', 'scale']
    

Adding Elements to a List


```python
num = [1, 2, 3]
num.append(4)
print(num)
```

    [1, 2, 3, 4]
    


```python
num = [1, 2, 3]
num.insert(1, 10)
print(num)
```

    [1, 10, 2, 3]
    

Removing Elements from a List


```python
data = [10, 20, 30, 40]
data.remove(20)
print(data)
```

    [10, 30, 40]
    


```python
data = [10, 20, 30, 40]
last = data.pop()
print(data)
```

    [10, 20, 30]
    

List Length and Membership


```python
values = [5, 10, 15]
print(len(values)) 
```

    3
    


```python
print(10 in values)  
```

    True
    


```python
print(189 not in values)
```

    True
    

 List Iteration


```python
c = ["New York", "London", "Tokyo"]
for city in c:
    print(city)
```

    New York
    London
    Tokyo
    

List Comprehension


```python
A = [x**2 for x in range(5)]
print(A)
```

    [0, 1, 4, 9, 16]
    


```python
A = [x**2 for x in range(10)]
print(A)
```

    [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
    


```python

```


---
**Score: 30**