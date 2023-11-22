A design pattern that allows the interface of an existing class to be used as another interface. 

It is often used to make existing classes work with others without modifying their source code.

---
```python
# Target Interface
class Target:
    def request(self):
        pass

# Adaptee (the class to be adapted)
class Adaptee:
    def specific_request(self):
        return "Adaptee's specific request"

# Adapter
class Adapter(Target):
    def __init__(self, adaptee):
        self.adaptee = adaptee

    def request(self):
        return f"Adapter: {self.adaptee.specific_request()}"

# Client code
def client_code(target):
    result = target.request()
    print(result)

# Example usage
adaptee = Adaptee()
adapter = Adapter(adaptee)

client_code(adapter)
# Output: Adapter: Adaptee's specific request
```
---
#### Use Cases:
1. **Legacy Code Integration:** When you have existing classes (legacy code) that have interfaces incompatible with the rest of your system, you can use adapters to make them work together.
    
2. **Third-Party Libraries:** When you want to use a third-party library in your application, but its interface doesn't match the interface your code expects, you can create an adapter to bridge the gap.
    
3. **Interface Standardization:** When you have multiple classes that have similar functionality but different interfaces, you can use adapters to standardize their interfaces and make them interchangeable.
    
4. **Testing:** Adapters can be useful in testing, allowing you to create mock or stub implementations that adapt to the interfaces expected by the code being tested.

#DesignPatterns