---
title: Python For Loop
date: 2026-01-12
author: Your Name
cell_count: 19
score: 15
---

Basic for Loop with a Sequence


```python
fruits = ["apple", "banana", "orange"]

for fruit in fruits:
    print(fruit)
```

    apple
    banana
    orange
    

Using range() in for Loop


```python
for i in range(7):
    print(i)
```

    0
    1
    2
    3
    4
    5
    6
    

Custom Start and Step with range()


```python
for i in range(2, 10, 3):
    print(i)
```

    2
    5
    8
    

Iterating Through a String


```python
name = "Swathi"

for char in name:
    print(char)
```

    S
    w
    a
    t
    h
    i
    

Using for with Index via enumerate()


```python
lang = ["Python", "Java", "C++"]

for index, lan in enumerate(lang):
    print(index, lan)

```

    0 Python
    1 Java
    2 C++
    

Nested for Loops


```python
for i in range(4):
    for j in range(2):
        print(f"i={i}, j={j}")
```

    i=0, j=0
    i=0, j=1
    i=1, j=0
    i=1, j=1
    i=2, j=0
    i=2, j=1
    i=3, j=0
    i=3, j=1
    

Using break in for Loop


```python
for num in range(1, 10):
    if num == 8:
        break
    print(num)
```

    1
    2
    3
    4
    5
    6
    7
    

Using continue in for Loop


```python
for num in range(1, 10):
    if num == 4:
        continue
    print(num)
```

    1
    2
    3
    5
    6
    7
    8
    9
    

for Loop with else Clause


```python
for num in range(3):
    print(num)
else:
    print("Loop completed")
```

    0
    1
    2
    Loop completed
    


```python

```


---
**Score: 15**