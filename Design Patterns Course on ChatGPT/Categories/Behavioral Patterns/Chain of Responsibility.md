Avoid coupling the sender of a request to its receiver by giving more than one object a chance to handle the request. Chain the receiving objects and pass the request along the chain.

---
```python
from abc import ABC, abstractmethod  
class Handler(ABC):     
	def __init__(self, successor=None):         
		self._successor = successor      
	@abstractmethod     
	def handle_request(self, request):         
		pass  
class ConcreteHandlerA(Handler):     
	def handle_request(self, request):         
		if request == "A":             
		return "ConcreteHandlerA handled the request."         
	elif self._successor:             
		return self._successor.handle_request(request)         
	else:             
		return "Request not handled."  
class ConcreteHandlerB(Handler):     
	def handle_request(self, request):         
		if request == "B":             
			return "ConcreteHandlerB handled the request."         
		elif self._successor:             
			return self._successor.handle_request(request)         
		else:             
			return "Request not handled."
```
---
#### Use Cases:
- **Event Propagation:** In graphical user interfaces, where events can be handled by different components in a hierarchical structure.
    
- **Middleware Processing:** Handling requests in a web middleware pipeline where each middleware can choose to pass the request to the next one.
    

#DesignPatterns