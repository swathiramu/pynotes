---
title: Python Type Conversion
date: 2026-01-11
author: Your Name
cell_count: 40
score: 40
---

Implicit Type Conversion


```python
integer_value = 10
float_value = 3.5
result = integer_value + float_value
```


```python
print(result)
```

    13.5
    


```python
print(type(result))
```

    <class 'float'>
    

Explicit Type Conversion to Integer


```python
float_value = 9.99
string_value = "42"
int_from_float = int(float_value)
int_from_string = int(string_value)
```


```python
print(int_from_float)
```

    9
    


```python
print(int_from_string)
```

    42
    

Explicit Type Conversion to Float


```python
int_value = 7
string_value = "3.14"
float_from_int = float(int_value)
float_from_string = float(string_value)
```


```python
print(float_from_int)
```

    7.0
    


```python
print(float_from_string)
```

    3.14
    

Explicit Type Conversion to String


```python
int_value = 100
float_value = 25.5
bool_value = True

str_int = str(int_value)
str_float = str(float_value)
str_bool = str(bool_value)
```


```python
print(str_int)
```

    100
    


```python
print(str_float)
```

    25.5
    


```python
print(str_bool)
```

    True
    

Converting to Boolean


```python
print(bool(0))
```

    False
    


```python
print(bool(1))
```

    True
    


```python
print(bool(""))
```

    False
    


```python
print(bool("text"))
```

    True
    


```python
print(bool([]))
```

    False
    


```python
print(bool([1, 2]))
```

    True
    

Converting Between Strings and Lists


```python
text = "python"
char_list = list(text)
```


```python
print(char_list)
```

    ['p', 'y', 't', 'h', 'o', 'n']
    


```python
words = ["Python", "Type", "Conversion"]
joined = " ".join(words)
```


```python
print(joined) 
```

    Python Type Conversion
    

Converting Between Tuples, Lists, and Sets


```python
numbers_list = [1, 2, 2, 3]

numbers_tuple = tuple(numbers_list)
numbers_set = set(numbers_list)
```


```python
print(numbers_tuple) 
```

    (1, 2, 2, 3)
    


```python
print(numbers_set)
```

    {1, 2, 3}
    

Converting to Dictionary


```python
pairs_list = [("a", 1), ("b", 2)]
pairs_tuple = (("x", 10), ("y", 20))

dict_from_list = dict(pairs_list)
dict_from_tuple = dict(pairs_tuple)
```


```python
print(dict_from_list) 
```

    {'a': 1, 'b': 2}
    


```python
print(dict_from_tuple) 
```

    {'x': 10, 'y': 20}
    

Handling Conversion Errors with try / except


```python
def safe_int_convert(value: str) -> int:
    try:
        return int(value)
    except ValueError:
        print(f"Cannot convert '{value}' to int. Defaulting to 0.")
        return 0

```


```python

```


---
**Score: 40**