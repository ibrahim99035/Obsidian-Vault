Define a family of algorithms, encapsulate each one, and make them interchangeable. Strategy lets the algorithm vary independently from clients that use it.

---
```python
from abc import ABC, abstractmethod  
class Context:     
	def __init__(self, strategy):         
		self._strategy = strategy      
	def set_strategy(self, strategy):         
		self._strategy = strategy      
	def execute_strategy(self):         
		return self._strategy.execute()  
class Strategy(ABC):     
	@abstractmethod     
	def execute(self):         
		pass  
class ConcreteStrategyA(Strategy):     
	def execute(self):         
		return "ConcreteStrategyA"  
class ConcreteStrategyB(Strategy):     
	def execute(self):         
		return "ConcreteStrategyB"
```
---
#### Use Cases:

- **Sorting Algorithms:** Different sorting strategies (e.g., quicksort, bubblesort) can be encapsulated and switched at runtime.
    
- **Payment Processing:** Various payment strategies (e.g., credit card, PayPal) can be implemented and selected dynamically.
#DesignPatterns