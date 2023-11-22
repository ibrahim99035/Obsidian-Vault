Encapsulate a request as an object, thereby allowing for parameterization of clients with different requests, queuing of requests, and logging of the parameters.

```python
from abc import ABC, abstractmethod  
class Command(ABC):     
	@abstractmethod    
	def execute(self):        
		pass  
class ConcreteCommand(Command):    
	def __init__(self, receiver):        
		self._receiver = receiver    
	def execute(self):        
		self._receiver.action()  
class Receiver:   
	def action(self):      
		print("Receiver action") 
class Invoker:     
	def __init__(self):   
		self._command = None    
	def set_command(self, command):   
		self._command = command     
	def execute_command(self):       
		self._command.execute()
```
---
#### Use Cases:
- **GUI Systems:** Where user actions (commands) are encapsulated as objects, allowing for undo/redo functionality.
    
- **Remote Controls:** Implementing remote controls for electronic devices, where each button press corresponds to a specific command.

#DesignPatterns