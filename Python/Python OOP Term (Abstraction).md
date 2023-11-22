Abstraction allows you to focus on the essential features of an object while ignoring the non-essential details.

#### Key aspects of abstraction:
1. **Hiding Implementation Details:** Abstraction involves hiding the complex internal details of how a class or object works. 
	 - Users of the class interact with it through a well-defined interface without needing to understand the intricacies of its implementation.
    
2. **Defining Interfaces:** Abstraction often involves defining interfaces (methods or properties) that represent the essential functionalities of an object. 
	- These interfaces provide a way for users to interact with the object without knowing its internal workings.
    
3. **Creating Abstract Classes and Interfaces:** In some programming languages, you can use abstract classes or interfaces to define the common structure and behavior that subclasses must implement. These abstract entities act as templates for more concrete implementations.
---
```python
from abc import ABC, abstractmethod

# Abstract class representing a Shape
class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

# Concrete class Circle implementing Shape
class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius ** 2

# Concrete class Square implementing Shape
class Square(Shape):
    def __init__(self, side_length):
        self.side_length = side_length

    def area(self):
        return self.side_length ** 2

# Using abstraction
circle = Circle(5)
square = Square(4)

print(circle.area())  # Output: 78.5
print(square.area())  # Output: 16
```
---
#python