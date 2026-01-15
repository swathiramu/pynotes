---
title: Python Function Arguments
date: 2026-01-15
author: Your Name
cell_count: 22
score: 20
---

Positional Arguments


```python
def display(name, age):
    print(f"Name: {name}, Age: {age}")

display("Swathiii", 21)
```

    Name: Swathiii, Age: 21
    

Keyword Arguments


```python
def display(name, age):
    print(f"Name: {name}, Age: {age}")

display(age=21, name="Swathi")
```

    Name: Swathi, Age: 21
    

Default Arguments


```python
def greet(name="Guest"):
    print(f"Hello, {name}")

greet()
greet("Swathii")
```

    Hello, Guest
    Hello, Swathii
    

 Required Arguments


```python
def login(username, password):
    print(f"User: {username}")

login("Swathii", "1234")
```

    User: Swathii
    

*Variable-Length Positional Arguments (args)



```python
def calc(*num):
    return sum(num)

print(calc(1, 2, 3))   

```

    6
    


```python
print(calc(5, 10, 15, 5))
```

    35
    

**Variable-Length Keyword Arguments (kwargs)


```python
def user(**details):
    for key, value in details.items():
        print(f"{key}: {value}")

user(name="Swathii",role="Developer", level="Junior")
```

    name: Swathii
    role: Developer
    level: Junior
    

**Combining Normal, *args, and kwargs


```python
def profile(name, *skills, **info):
    print("Name:", name)
    print("Skills:", skills)
    print("Details:", info)

profile("Swathii", "Python", "GenAI", age=21, city="London")
```

    Name: Swathii
    Skills: ('Python', 'GenAI')
    Details: {'age': 21, 'city': 'London'}
    

Positional-Only Arguments


```python
def div(a, b, /):
    return a / b
print(div(10, 2))
```

    5.0
    

Keyword-Only Arguments


```python
def config(*, mode="light"):
    print(f"Mode: {mode}")

config(mode="dark")
```

    Mode: dark
    

Argument Unpacking


```python
def mul(a, b, c):
    return a * b * c

val = (2, 3, 4)
print(mul(*val))
```

    24
    


```python
data = {"a": 1, "b": 2, "c": 3}
print(mul(**data))
```

    6
    


---
**Score: 20**