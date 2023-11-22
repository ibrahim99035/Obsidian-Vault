Allow an object to alter its behavior when its internal state changes. The object will appear to change its class.

---
```python
from abc import ABC, abstractmethod  
class State(ABC):     
	@abstractmethod     
	def handle_request(self):         
		pass  
class ConcreteStateA(State):     
	def handle_request(self):         
		return "ConcreteStateA handles the request."  
class ConcreteStateB(State):     
	def handle_request(self):         
	return "ConcreteStateB handles the request."  
class Context:     
	def __init__(self, state):         
		self._state = state      
	def set_state(self, state):         
		self._state = state      
	def request(self):         
		return self._state.handle_request()
```
---
#### Use Cases:

- **Workflow Management:** Changing the state of a document or task as it progresses through different stages.
    
- **Game Development:** Managing the state of a character in a game (e.g., idle, walking, attacking).
#DesignPatterns