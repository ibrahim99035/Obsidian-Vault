`__init__(self, ...)`
	- **Purpose**: Initializes a newly created object.
	- **Usage**: This method is called when an object is created, allowing you to set up its initial state.

`__str__(self, ...)`
	- **Purpose**: Returns the "informal" or user-friendly string representation of an object.
	- **Usage**: Used by `str(object)` and `print(object)` to display a human-readable string.

`__len__(self)`
	- **Purpose**: Returns the length of an object.
	- **Usage**: Used by `len(object)` to get the number of elements in an object.

`__getitem__(self, key)`
	- **Purpose**: Allows you to use square bracket notation to access an item from a collection.
	- **Usage**: Used by `object[key]`.

`__setitem__(self, key, value)`	
	- **Purpose**: Allows you to use square bracket notation to set the value of an item in a collection.
	- **Usage**: Used by `object[key] = value`.

`__delitem__(self, key)`
	- **Purpose**: Allows you to use the `del` statement to remove an item from a collection.
	- **Usage**: Used by `del object[key]`.

`__iter__(self)`
	- **Purpose**: Returns an iterator object.
	- **Usage**: Used by `iter(object)` to create an iterator for the object.

 `__next__(self)`
	- **Purpose**: Returns the next value from an iterator.
	- **Usage**: Used by `next(iterator)` to get the next value from an iterator.

`__enter__(self)`
	- **Purpose**: Used for resource management in a context manager (with statement).
	- **Usage**: Used in conjunction with `with` statements.

 `__exit__(self, exc_type, exc_value, traceback)`
	- **Purpose**: Used for resource management in a context manager (with statement).
	- **Usage**: Used in conjunction with `with` statements. It's called at the end of the `with` block.

 `__call__(self, ...)`
	- **Purpose**: Allows an object to be called as a function.
	- **Usage**: Used by `object()`.

---
#python