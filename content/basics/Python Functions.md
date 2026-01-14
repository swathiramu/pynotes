---
title: Python Functions
date: 2026-01-14
author: Your Name
cell_count: 20
score: 20
---

Defining a Basic Function


```python
def greet():
    print("Hello, Swathiii!")

greet()
```

    Hello, Swathiii!
    

Function with Parameters


```python
def user(name):
    print(f"Hello, {name}!")

user("Swathii")
```

    Hello, Swathii!
    

Function with Return Value


```python
def add(a, b):
    return a + b

res = add(5, 3)
print(res)
```

    8
    

Default Parameters


```python
def greet(name="Guest"):
    print(f"Hello, {name}!")

greet()
greet("Swathii")
```

    Hello, Guest!
    Hello, Swathii!
    

Keyword Arguments


```python
def student(name, age):
    print(f"Name: {name}, Age: {age}")

student(age=20, name="Alice")
```

    Name: Alice, Age: 20
    

Variable-Length Arguments (args)


```python
def sums(*args):
    return sum(args)

print(sums(1, 2, 3, 4))
```

    10
    

Keyword Variable-Length Arguments (kwargs)


```python
def display(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

display(name="Swathii", role="Engineer")
```

    name: Swathii
    role: Engineer
    

**Function with Both *args and kwargs


```python
def complete(*args, **kwargs):
    print("Positional:", args)
    print("Keyword:", kwargs)

complete("Python", level="Advanced", year=2025)
```

    Positional: ('Python',)
    Keyword: {'level': 'Advanced', 'year': 2025}
    

Lambda (Anonymous) Functions


```python
squa = lambda x: x ** 2
print(squa(5))
```

    25
    

Recursive Functions


```python
def fact(n):
    if n == 0:
        return 1
    return n * fact(n - 1)

print(fact(5))
```

    120
    


---
**Score: 20**