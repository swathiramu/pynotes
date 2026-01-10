---
title: Python Data Types
date: 2026-01-10
author: Your Name
cell_count: 35
score: 35
---

Python Numbers and Mathematics

Numeric Data Types in Python


```python
int = 10
print(type(int))
```

    <class 'int'>
    


```python
float = 3.14
print(type(float))
```

    <class 'float'>
    


```python
complex = 2 + 5j
print(type(complex))
```

    <class 'complex'>
    

Basic Mathematical Operations


```python
a = 12
b = 5
print(a + b) 
```

    17
    


```python
print(a - b)
```

    7
    


```python
print(a * b)
```

    60
    


```python
print(a / b)
```

    2.4
    

Floor Division and Modulus


```python
x = 17
y = 5

print(x // y) 
```

    3
    


```python
print(x % y)
```

    2
    


```python
base = 2
exponent = 4

res = base ** exponent
print(res)
```

    16
    

Math Module Basics


```python
import math
print(math.sqrt(25))
```

    5.0
    


```python
print(math.ceil(4.3))
```

    5
    


```python
print(math.floor(4.9))
```

    4
    

Trigonometric Functions


```python
import math
a = math.radians(30)
print(math.sin(a)) 
```

    0.49999999999999994
    


```python
print(math.cos(a))
```

    0.8660254037844387
    


```python
print(math.tan(a)) 
```

    0.5773502691896257
    

 Rounding Numbers


```python
val = 3.5678
print(round(val)) 
```

    4
    


```python
print(round(val, 2)) 
```

    3.57
    

 Absolute and Sign Functions


```python
num = -25
print(abs(num)) 
```

    25
    


```python
print(math.copysign(10, -1))
```

    -10.0
    

Random Number Generation


```python
import random
print(random.randint(1, 30))
```

    16
    


```python
print(random.uniform(1.0, 5.0))
```

    2.4907373255645604
    

Statistical Operations


```python
import statistics
num = [10, 20, 30, 40, 50]
print(statistics.mean(num))   
```

    30
    


```python
print(statistics.median(num)) 
```

    30
    


```python
print(statistics.stdev(numbers))  
```


---
**Score: 35**