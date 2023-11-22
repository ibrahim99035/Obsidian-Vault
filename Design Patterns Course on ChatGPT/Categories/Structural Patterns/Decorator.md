A design pattern that allows behavior to be added to an individual object, either statically or dynamically, without affecting the behavior of other objects from the same class.

---
```python
from abc import ABC, abstractmethod

# Component interface
class Coffee(ABC):
    @abstractmethod
    def cost(self):
        pass

# Concrete Component
class SimpleCoffee(Coffee):
    def cost(self):
        return 5

# Decorator
class CoffeeDecorator(Coffee, ABC):
    def __init__(self, coffee):
        self._coffee = coffee

    @abstractmethod
    def cost(self):
        pass

# Concrete Decorators
class MilkDecorator(CoffeeDecorator):
    def cost(self):
        return self._coffee.cost() + 2

class SugarDecorator(CoffeeDecorator):
    def cost(self):
        return self._coffee.cost() + 1

# Example usage
simple_coffee = SimpleCoffee()
print("Cost of Simple Coffee:", simple_coffee.cost())

milk_coffee = MilkDecorator(simple_coffee)
print("Cost of Coffee with Milk:", milk_coffee.cost())

sugar_milk_coffee = SugarDecorator(milk_coffee)
print("Cost of Coffee with Milk and Sugar:", sugar_milk_coffee.cost())
```
---
#### Use Cases:
1. **Extending Functionality:** Use the Decorator Pattern when you want to extend the functionality of objects in a flexible and reusable way, allowing you to add new behaviors to an object without altering its structure.
    
2. **Dynamic Behavior:** When you need to add or remove responsibilities dynamically at runtime, the Decorator Pattern provides a way to do this without modifying the code of the decorated object.
    
3. **Combining Features:** When you have a need for combining features in various ways, such as combining different toppings on a pizza or adding different filters to an image processing pipeline.

---
#DesignPatterns