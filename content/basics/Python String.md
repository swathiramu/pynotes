---
title: Python String
date: 2026-01-15
author: Your Name
cell_count: 37
score: 35
---

Creating Strings


```python
 A = 'Hello'
print(A)
```

    Hello
    


```python
B = "World"
print(B)
```

    World
    


```python
C = """This is a multi-line string"""
print(C)
```

    This is a multi-line string
    

Accessing String Characters (Indexing)


```python
text = "Python"
print(text[0]) 
```

    P
    


```python
text = "Python"

print(text[1]) 
```

    y
    


```python
text = "Python"

print(text[3]) 
```

    h
    


```python
text = "Python"

print(text[-1]) 
```

    n
    

String Slicing


```python
word = "Programming"

print(word[0:6])
```

    Progra
    


```python
word = "Programming"

print(word[2:6])
```

    ogra
    


```python
print(word[:4])
```

    Prog
    


```python
print(word[:6])
```

    Progra
    


```python
print(word[4:]) 
```

    ramming
    


```python
print(word[7:]) 
```

    ming
    

String Immutability


```python
name = "Python"
print(name)
```

    Python
    


```python
first = "Hello"
second = "World"
print(first + " " + second)
```

    Hello World
    


```python
print(first * 3)
```

    HelloHelloHello
    

String Length and Membership


```python
name = "Swathiii"
print(len(name))
```

    8
    


```python
print("Swa" in name)
```

    True
    


```python
print("AI" not in name)
```

    True
    

Common String Methods


```python
text = "  python programming  "

print(text.upper())  
```

      PYTHON PROGRAMMING  
    


```python
text = "  python programming  "  
print(text.lower())
```

      python programming  
    


```python
print(text.strip())
```

    python programming
    


```python
print(text.replace("python", "Java"))
```

      Java programming  
    

Splitting and Joining Strings


```python
sentence = "Python is powerful"
words = sentence.split(" ")
print(words)
```

    ['Python', 'is', 'powerful']
    


```python
joined = "-".join(words)
print(joined)
```

    Python-is-powerful
    

String Formatting


```python
name = "Swathiii"
score = 100

print(f"{name} scored {score} marks.")  
```

    Swathiii scored 100 marks.
    


```python
print("{} scored {} marks.".format(name, score)) 
```

    Swathiii scored 100 marks.
    

 Iterating Through a String


```python
word = "Swathii"

for char in word:
    print(char)
```

    S
    w
    a
    t
    h
    i
    i
    


---
**Score: 35**