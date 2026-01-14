---
title: Python Global Keyword
date: 2026-01-14
author: Your Name
cell_count: 21
score: 20
---

Basic Use of Global Variable


```python
count = 10

def display():
    print(count)

display()
```

    10
    

 Modifying Global Variable Without global


```python
value = 5

def update():
    value = value + 1  

update()
```


    ---------------------------------------------------------------------------

    UnboundLocalError                         Traceback (most recent call last)

    Cell In[9], line 6
          3 def update():
          4     value = value + 1  
    ----> 6 update()
    

    Cell In[9], line 4, in update()
          3 def update():
    ----> 4     value = value + 1
    

    UnboundLocalError: cannot access local variable 'value' where it is not associated with a value


 Using global to Modify Global Variable


```python
counter = 0

def increment():
    global counter
    counter += 1
increment()
print(counter)
```

    1
    

Global Variable Across Multiple Functions


```python
status = "inactive"

def activate():
    global status
    status = "active"

def show_status():
    print(status)

activate()
show_status()
```

    active
    

Global Keyword Inside Nested Functions


```python
x = 100
def outer():
    def inner():
        global x
        x = 200
    inner()
outer()
print(x)
```

    200
    

Difference Between global and nonlocal


```python
x = 50

def outer():
    x = 10
    
    def inner():
        global x
        x = 99

    inner()
    print("Outer x:", x)

outer()
print("Global x:", x)
```

    Outer x: 10
    Global x: 99
    

Tracking State Using Global Variable


```python
requests = 0

def handle_request():
    global requests
    requests += 1

handle_request()
handle_request()
print(requests)  
```

    2
    

Global Variable with Conditional Logic


```python
mode = "light"

def toggle_mode():
    global mode
    if mode == "light":
        mode = "dark"
    else:
        mode = "light"

toggle_mode()
print(mode)
```

    dark
    

Avoiding Global Abuse


```python
config = {"theme": "dark"}
def update_config(new_theme):
    config["theme"] = new_theme
```


```python
update_config("light")
print(config)
```

    {'theme': 'light'}
    

Best Practice: Encapsulation Instead of Global


```python
class Counter:
    def __init__(self):
        self.value = 0

    def increment(self):
        self.value += 1

counter = Counter()
counter.increment()
print(counter.value)
```

    1
    


---
**Score: 20**