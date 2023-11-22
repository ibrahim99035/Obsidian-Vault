In Python, getters and setters are methods used to access and modify the values of attributes (class variables) in a class.

They are part of the encapsulation principle, allowing you to control how attributes are accessed and modified.

Python provides a convenient way to define getters and setters using the
	`@property`, 
	`@<attribute_name>.setter`, 
	and `@<attribute_name>.deleter` decorators.

#### Basic Getters & Setters:
```python
class MyClass:
    def __init__(self, value):
        self._value = value

    # Getter method
    @property
    def value(self):
        return self._value

    # Setter method
    @value.setter
    def value(self, new_value):
        if new_value < 0:
            print("Value cannot be negative. Setting to 0.")
            self._value = 0
        else:
            self._value = new_value

# Creating an instance
obj = MyClass(42)

# Using the getter
print(obj.value)  # Output: 42

# Using the setter
obj.value = -5
print(obj.value)  # Output: 0 (due to the setter logic)
```
---
### Scenario:
```python 
class Temperature:
    def __init__(self, celsius):
        self._celsius = celsius

    @property
    def celsius(self):
        return self._celsius

    @celsius.setter
    def celsius(self, value):
        if value < -273.15:
            raise ValueError("Temperature cannot be below absolute zero.")
        self._celsius = value

    @property
    def fahrenheit(self):
        return self._celsius * 9/5 + 32

# Creating an instance
temperature = Temperature(25)

# Using the getter
print(temperature.celsius)     # Output: 25

# Using the setter
temperature.celsius = 30
print(temperature.celsius)     # Output: 30

# Calculating fahrenheit using the getter
print(temperature.fahrenheit)  # Output: 86.0
```
---
#### Using Decorators with Deletion:
```python
class Temperature:
    # ... (previous code)

    @celsius.deleter
    def celsius(self):
        print("Deleting celsius attribute.")
        del self._celsius

# Deleting the attribute
del temperature.celsius
# Output: Deleting celsius attribute.
```
---
#python