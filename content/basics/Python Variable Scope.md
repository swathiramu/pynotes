---
title: Python Variable Scope
date: 2026-01-15
author: Your Name
cell_count: 23
score: 20
---

Local Scope

def value():
    x = 10
    print(x)
value()


```python
print(x)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[6], line 1
    ----> 1 print(x)
    

    NameError: name 'x' is not defined


Global Scope


```python
x = 20  
def display():
    print(x)

display()
print(x)
```

    20
    20
    

Local vs Global Variable Conflict


```python
value = 50

def update():
    value = 10
    print(value)

update()
print(value)

```

    10
    50
    

Using the global Keyword





```python
count = 0

def increment():
    global count
    count += 1

increment()
print(count)
```

    1
    

Enclosing Scope (Nested Functions)


```python
def outer():
    message = "Hello"

    def inner():
        print(message)
    inner()
outer()

```

    Hello
    

Using the nonlocal Keyword


```python
def outer():
    count = 0

    def inner():
        nonlocal count
        count += 1
        print(count)

    inner()
    inner()

outer()
```

    1
    2
    

LEGB Rule (Scope Resolution Order)

Python resolves variables using the LEGB rule:

Local

Enclosing

Global

Built-in


```python
x = "Global"

def outer():
    x = "Enclosing"

    def inner():
        x = "Local"
        print(x)

    inner()

outer()
```

    Local
    

Built-in Scope


```python
print(len([1, 2, 3]))
```

    3
    

Scope Inside Loops


```python
for i in range(3):
    loop = i

print(loop)
```

    2
    

Practical Example of Scope Management


```python
total = 100

def calculate():
    total = 50

    def adjust():
        nonlocal total
        total += 10

    adjust()
    return total

print(calculate())
```

    60
    


```python
print(total)  
```

    100
    


```python

```


---
**Score: 20**