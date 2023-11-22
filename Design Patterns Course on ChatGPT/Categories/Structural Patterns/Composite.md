A structural design pattern that allows clients to treat individual objects and compositions of objects uniformly. 
It is used to compose objects into tree structures to represent part-whole hierarchies.

---
```python
from abc import ABC, abstractmethod

# Component
class Component(ABC):
    @abstractmethod
    def operation(self):
        pass

# Leaf
class Leaf(Component):
    def operation(self):
        return "Leaf operation"

# Composite
class Composite(Component):
    def __init__(self):
        self.children = []

    def add(self, component):
        self.children.append(component)

    def remove(self, component):
        self.children.remove(component)

    def operation(self):
        results = []
        for child in self.children:
            results.append(child.operation())
        return f"Composite operation: {', '.join(results)}"

# Example usage
leaf1 = Leaf()
leaf2 = Leaf()

composite = Composite()
composite.add(leaf1)
composite.add(leaf2)

result = composite.operation()
print(result)
# Output: Composite operation: Leaf operation, Leaf operation
```
---
#### Use Cases:
1. **Graphics Systems:** In a graphics system, graphical elements (circles, rectangles) can be represented as leaves, and composite elements (e.g., a group of shapes) can be represented as composites. 
	- This allows you to treat a single shape or a group of shapes uniformly.
    
2. **File Systems:** In a file system, files and directories can be represented using the Composite Pattern. 
	 - Directories can contain files or other directories, and you can perform operations (e.g., display, delete) uniformly on files and directories.

#DesignPatterns