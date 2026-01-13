---
title: Data Classes
date: 2026-01-13
author: Your Name
cell_count: 21
score: 20
---

Basic Data Class


```python
from dataclasses import dataclass
@dataclass
class Person:
    name: str
    age: int
person = Person(name="Swathi", age=21)
print(person)
```

    Person(name='Swathi', age=21)
    

Default Values in Data Classes


```python
from dataclasses import dataclass
@dataclass
class Book:
    tit: str
    auth: str
    pri: float = 999.99
book = Book(tit="ikigai", auth="Hector Garcia")
print(book)
```

    Book(tit='ikigai', auth='Hector Garcia', pri=999.99)
    

Immutable Data Classes


```python
from dataclasses import dataclass
@dataclass(frozen=True)
class Point:
    x: int
    y: float

point = Point(3, 4.5)
print(point)

```

    Point(x=3, y=4.5)
    

Post-Initialization Processing


```python
from dataclasses import dataclass

@dataclass
class Rectangle:
    w: float
    h: float
    a: float = 0.0

    def __post_init__(self):
        self.a = self.w * self.h

rect = Rectangle(w=5, h=10)
print(rect.a) 
```

    50
    

Comparing Data Class Instances


```python
from dataclasses import dataclass

@dataclass
class Item:
    name: str
    price: float
    
def __eq__(self, other):
    return self.name == other.name and self.price == other.price

item1 = Item(name="Laptop", price=1000.0)
item2 = Item(name="Mobile", price=1000.0)

print(item1 == item2) 
```

    False
    

Default Factory for Mutable Fields


```python
from dataclasses import dataclass, field
from typing import List

@dataclass
class ShoppingCart:
    items: List[str] = field(default_factory=list)

cart = ShoppingCart()
cart.items.append("Apple")
cart.items.append("banana")
print(cart)
```

    ShoppingCart(items=['Apple', 'banana'])
    

Excluding Fields from repr


```python
from dataclasses import dataclass

@dataclass
class User:
    username: str
    password: str = "rjss"

    def __repr__(self):
        return f"User(username='{self.username}')"

user = User(username="Swathiii")
print(user)
```

    User(username='Swathiii')
    

Data Classes with Type Hints


```python
from dataclasses import dataclass
from typing import List

@dataclass
class Classroom:
    students: List[str]
    teacher: str

classroom = Classroom(students=["Swathi", "Shruthii"], teacher="Mr. Smith")
print(classroom)  
```

    Classroom(students=['Swathi', 'Shruthii'], teacher='Mr. Smith')
    

Inheriting from Data Classes


```python
from dataclasses import dataclass

@dataclass
class Animal:
    name: str

@dataclass
class Dog(Animal):
    breed: str

dog = Dog(name="Buddy", breed="Golden Retriever")
print(dog) 
```

    Dog(name='Buddy', breed='Golden Retriever')
    

Using asdict and astuple


```python
from dataclasses import dataclass, asdict, astuple

@dataclass
class Employee:
    name: str
    role: str
    salary: float

employee = Employee(name="Swathiii", role="Developer", salary=75000.0)
print(asdict(employee)) 

```

    {'name': 'Swathiii', 'role': 'Developer', 'salary': 75000.0}
    


```python
print(astuple(employee))  
```

    ('Swathiii', 'Developer', 75000.0)
    


---
**Score: 20**