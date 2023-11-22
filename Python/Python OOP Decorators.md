### `@classmethod` and `@staticmethod` vs. Instance Methods

Both `@classmethod` and `@staticmethod` decorators can be used with class methods, but they differ in their first parameter:

- `@classmethod` methods take `cls` as their first parameter, referring to the class.
- `@staticmethod` methods don't have a reference to the class or instance.

pythonCopy code

```python 
class MyClass:
	class_variable = 10
	
	def __init__(self, instance_variable):        
		self.instance_variable = instance_variable      
	
	@classmethod     
	def class_method(cls):         
		print(f"This is a class method. Class variable: {cls.class_variable}")          
	
	@staticmethod    
	def static_method():    
		print("This is a static method.")   
		
	def instance_method(self):        
		print("This is an instance method.")  

# Using different types of methods 
MyClass.class_method() 
MyClass.static_method()  
obj = MyClass(42) 
obj.instance_method()
```
---
#python