---
title: Python Flow Control
date: 2026-01-09
author: Your Name
cell_count: 20
score: 20
---

Basic if Statement





```python
age = 21
if age >= 10:
    print("Eligible")
```

    Eligible
    

Using if else Statement


```python
Number = 30
if Number < 20:
    print("Number is small")
else :
    print("Number is big")
```

    Number is big
    

Using if & elif & else Chain


```python
Mark = 89

if Mark >= 90:
    print("A")
elif Mark >= 75:
    print("B")
else:
    print("C")
```

    B
    

Nested if Statements


```python
user = "swathi"
pas = "1234"

if user == "swathi":
    if pas == "1234":
        print("Access")
    else:
        print("Incorrect")
```

    Access
    

Using Logical Operators in Conditions


```python
age = 25
verified = True

if age > 18 and verified:
    print("proceed")
```

    proceed
    

Short-Hand if Statement 


```python
x = 45
if x > 10: print("x is greater than 5")
```

    x is greater than 5
    

Short-Hand if & else


```python
num = 89

res = "Even" if num % 2 == 0 else "Odd"
print(res) 
```

    Odd
    

Checking Multiple Values with in


```python
day = "Monday"

if day in ["Saturday", "Sunday"]:
    print("Weekend")
else:
    print("Weekday")
```

    Weekday
    

Comparing Strings in Conditions


```python
user = "Swathi"

if user.lower() == "swathi":
    print("Welcome Swathi...")
```

    Welcome Swathi...
    

Using pass in if Statement


```python
value = 5

if value > 0:
    pass  

print("Program continues...")
```


---
**Score: 20**