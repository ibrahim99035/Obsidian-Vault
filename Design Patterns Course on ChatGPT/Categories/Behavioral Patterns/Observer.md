Define a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.

---
```python
from abc import ABC, abstractmethod  
class Subject(ABC):
	def __init__(self):         
		self._observers = []      
	def add_observer(self, observer):         
		self._observers.append(observer)      
	def remove_observer(self, observer):         
		self._observers.remove(observer)      
	@abstractmethod     
	def notify_observers(self):         
		pass  
class ConcreteSubject(Subject):     
	def __init__(self, state):         
		super().__init__()         
		self._state = state      
	def get_state(self):         
		return self._state      
	def set_state(self, state):         
		self._state = state         
		self.notify_observers()      
	def notify_observers(self):         
		for observer in self._observers:             
			observer.update(self._state)  
class Observer(ABC):     
	@abstractmethod     
	def update(self, state):         
		pass  
class ConcreteObserver(Observer):     
	def update(self, state):         
		print(f"Received state update: {state}")`
```
---
#### Use Cases:

- **Event Handling Systems:** Notifying multiple components in a GUI framework when the state of a particular object changes.
    
- **Stock Market Monitoring:** Updating various displays when the value of a stock changes.
    
#DesignPatterns