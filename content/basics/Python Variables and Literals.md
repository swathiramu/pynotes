---
title: Python Variables And Literals
date: 2026-01-11
author: Your Name
cell_count: 31
score: 30
---

Declaring and Assigning Variables


```python
count = 10
price = 99.99
name = "Python"

print(count) 
print(price)   
print(name)    
```

    10
    99.99
    Python
    

Multiple Variable Assignment


```python
a, b, c = 1, 2, 3
print(a)  
print(b)  
print(c)
```

    1
    2
    3
    

Reassigning Variables


```python
value = 100
print(value)
```

    100
    


```python
value = "Reassigned"
print(value)
```

    Reassigned
    

Numeric Literals


```python
integer = 42
print(integer)  

```

    42
    


```python
float = 3.14
print(float) 
```

    3.14
    


```python
complex = 2 + 3j
print(complex)
```

    (2+3j)
    

String Literals


```python
single_quote = 'Hello'
print(single_quote)  

```

    Hello
    


```python
double_quote = "World"
print(double_quote) 
```

    World
    


```python
multi_line = """This is a multi-line string"""
print(multi_line)
```

    This is a multi-line string
    

Boolean Literals


```python
is_active = True
is_logged_in = False

print(is_active)    
print(is_logged_in)
```

    True
    False
    

Special Literal - None


```python
result = None
if result is None:
    print("No value assigned yet")
```

    No value assigned yet
    

Collection Literals


```python
list_literal = [1, 2, 3]
print(list_literal)
```

    [1, 2, 3]
    


```python
tuple_literal = (4, 5, 6)
print(tuple_literal)
```

    (4, 5, 6)
    


```python
set_literal = {7, 8, 9}
print(set_literal)
```

    {8, 9, 7}
    


```python
dict_literal = {"a": 1, "b": 2}
print(dict_literal)   
```

    {'a': 1, 'b': 2}
    

Binary, Octal, and Hexadecimal Literals


```python
binary = 0b1010
print(binary)
```

    10
    


```python
octal = 0o12
print(octal)
```

    10
    


```python
hexadecimal = 0xA
print(hexadecimal)  
```

    10
    

Using Variables in Expressions


```python
x = 5
y = 3

sum_result = x + y
product_result = x * y
print(sum_result) 
```

    8
    


```python
print(product_result)
```

    15
    


---
**Score: 30**