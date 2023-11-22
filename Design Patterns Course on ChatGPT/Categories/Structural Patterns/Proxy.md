A design pattern that provides a surrogate or placeholder for another object to control access to it.

It is often used to add a level of control over the access to an object, such as delaying the creation and initialization of the real object until it is actually needed or providing additional functionality like access control.

---
```python
from abc import ABC, abstractmethod

# Subject interface
class Subject(ABC):
    @abstractmethod
    def request(self):
        pass

# RealSubject
class RealSubject(Subject):
    def request(self):
        return "RealSubject: Handling request"

# Proxy
class Proxy(Subject):
    def __init__(self, real_subject):
        self._real_subject = real_subject

    def request(self):
        # Additional logic can be added here
        result = f"Proxy: Logging, {self._real_subject.request()}"
        return result

# Example usage
real_subject = RealSubject()
proxy = Proxy(real_subject)

result1 = real_subject.request()
print(result1)  # Output: RealSubject: Handling request

result2 = proxy.request()
print(result2)  # Output: Proxy: Logging, RealSubject: Handling request
```
---
#### Use Cases:
1. **Lazy Initialization:** Use a proxy to delay the creation and initialization of an expensive object until it is actually needed.
    
2. **Access Control:** Use a proxy to control access to an object, enforcing security or permission checks.
    
3. **Logging and Auditing:** Use a proxy to log method calls or perform auditing before or after the real object's methods are invoked.
    
4. **Caching:** Use a proxy to implement caching mechanisms. The proxy can check if the result is already cached before delegating to the real object.
    
5. **Remote Proxies:** Use a proxy to represent an object that is in a different address space, such as a remote object in a distributed system.

---
#DesignPatterns