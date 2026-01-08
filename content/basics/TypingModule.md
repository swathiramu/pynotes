---
title: Typingmodule
date: 2026-01-08
author: Your Name
cell_count: 20
score: 20
---

Specifying Function Input and Output Types


```python
from typing import List
def sum_of_integers(numbers: List[int]) -> int:
    return sum(numbers)

print(sum_of_integers([1, 2, 3])) 
```

    6
    

Using Optional for Nullable Parameters


```python
from typing import Optional
def greet(name: Optional[str] = None) -> str:
    if name:
        return f"Hello, {name}!"
    return "Hello, Guest!"
print(greet())           
print(greet("Alice")) 
```

    Hello, Guest!
    Hello, Alice!
    

Type Hint for Dictionaries


```python
from typing import Dict
def count_fruits(fruit_counts: Dict[str, int]) -> int:
    return sum(fruit_counts.values())
fruits = {"apple": 5, "banana": 3, "orange": 2}
print(count_fruits(fruits)) 
```

    10
    

Using Union for Multiple Types


```python
from typing import Union
def square_or_length(value: Union[int, str]) -> int:
    if isinstance(value, int):
        return value ** 2
    return len(value)
print(square_or_length(4))       
print(square_or_length("test"))
```

    16
    4
    

Custom Type Aliases


```python
from typing import List
Vector = List[float]
def dot_product(vec1: Vector, vec2: Vector) -> float:
    return sum(x * y for x, y in zip(vec1, vec2))
print(dot_product([1.0, 2.0], [3.0, 4.0])) 
```

    11.0
    

Using Callable for Functions


```python
from typing import Callable

def apply_operation(a: int, b: int, operation: Callable[[int, int], int]) -> int:
    return operation(a, b)

result = apply_operation(2, 3, lambda x, y: x + y)
print(result)
```

    5
    

Using Tuple for Fixed-Length Sequences


```python
from typing import Tuple
def process_coordinates(coords: Tuple[float, float]) -> str:
    return f"Latitude: {coords[0]}, Longitude: {coords[1]}"
print(process_coordinates((40.7128, -74.0060)))
```

    Latitude: 40.7128, Longitude: -74.006
    

Using Any for Flexible Input


```python
from typing import Any
def stringify(value: Any) -> str:
    return str(value)
print(stringify(42))         
print(stringify([1, 2, 3]))
```

    42
    [1, 2, 3]
    

Using Literal for Specific Values


```python
from typing import Literal
def choose_plan(plan: Literal["free", "premium", "enterprise"]) -> str:
    return f"You selected the {plan} plan."
print(choose_plan("premium"))
```

    You selected the premium plan.
    

Using TypedDict for Structured Dictionaries


```python
from typing import TypedDict
class User(TypedDict):
    name: str
    age: int
    email: str
def display_user(user: User) -> str:
    return f"{user['name']} ({user['age']}) can be reached at {user['email']}."
user = {"name": "Alice", "age": 30, "email": "alice@example.com"}
print(display_user(user))
```

    Alice (30) can be reached at alice@example.com.
    


---
**Score: 20**