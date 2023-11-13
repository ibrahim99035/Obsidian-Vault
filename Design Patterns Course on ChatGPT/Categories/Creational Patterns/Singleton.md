A design pattern that falls under the category of creational design patterns.

It ensures that a class has only one instance and provides a global point to that instance.

Used when one object is needed to coordinate actions across the system, such as a single database connection or a logging service.

---
#### Use case 1: Database Connections.
Ensuring that all database operations are performed using one connection, and only that connection.
```python
import sqlite3

class DatabaseSingleton:
    _instance = None
    def __new__(cls):
        if cls._instance is None:
            cls._instance = super(DatabaseSingleton, cls).__new__(cls)
            cls._instance.connection = sqlite3.connect("example.db")
        return cls._instance

# Example usage:
db_instance = DatabaseSingleton()
```
---
#### Use case 2: Logging Services
Singleton can ensure that log entries are consistent and centralized.
```python
class Logger:
    _instance = None

    def __new__(cls):
        if cls._instance is None:
            cls._instance = super(Logger, cls).__new__(cls)
            # Initialize logger
        return cls._instance

    def log(self, message):
        # Log the message
        pass

# Example usage:
logger_instance = Logger()
logger_instance.log("This is a log message")
```
---
