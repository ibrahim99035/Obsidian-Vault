Functions inside classes are called "methods".

When creating a method inside a Python class, it MUST have at least 1 parameter usually called `self`, this class basically passes the instance inside the function to use it in the process.

using `@classmethod` before the method in the class means that the parameter is not the instance anymore, it is the class itself.

```python
class Item:
	def __init__(self, name):
		self.name = name
	@classmethod
	def classMethod(cls):
		pass
```
---
#### [[Python OOP Magic Methods]]
---
#### [[Python OOP Decorators]]
---
#### [[Python OOP Getters & Setters]]
---
#### [[Property Privacy]]
---
#### [[Python OOP Term (Abstraction)]]
---
#### [[Python OOP Term (Polymorphism)]]

#python