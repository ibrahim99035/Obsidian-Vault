- It is a structural diagram that shows the internal structure of a classifier (e.g., a class) and the collaborations among its internal parts or roles.

- It allows you to depict the components that make up a complex structure and how they interact with each other to fulfill the behavior of the larger structure.

### Key Components of a Composite Structure Diagram:

1. **Class:**
    
    - Represents a classifier, which can be a class, interface, or other types.
    - Displayed as a rectangle with three compartments (name, attributes, and operations).
2. **Part:**
    
    - Represents a constituent part of a classifier.
    - Shown as a rectangle inside the enclosing classifier, connected by a line.
3. **Port:**
    
    - Represents a point of interaction between a classifier and its environment or with other parts.
    - Used to model how parts are connected or linked.
    - Can be associated with specific parts of a classifier.
4. **Connector:**
    
    - Represents a link between parts within a classifier.
    - Shown as a line connecting the parts or ports, indicating how they are connected or interact.
5. **Collaboration:**
    
    - Represents the collaboration or interaction between parts.
    - Can include messages or other interactions.

---
![[Pasted image 20231122120905.png]]
![[Pasted image 20231122120930.png]]

---
```
   +-------------------------+
   |       <<Class>>         |
   |           Car           |
   +-------------------------+
   | + engine: Engine        |
   | + wheels: Wheel[4]      |
   | + chassis: Chassis      |
   +-------------------------+
           |           |
           v           v
   +---------------+  +------------------+
   |    <<Class>>  |  |     <<Class>>    |
   |     Engine    |  |      Wheel       |
   +---------------+  +------------------+
   | - cylinders   |  | - diameter: int  |
   | - fuelSystem  |  | - tire: Tire     |
   +---------------+  +------------------+
                              |
                              v
                      +------------------+
					  |    <<Class>>     |
                      |      Tire        |
                      +------------------+
                      | - treadDepth: int|
                      | - pressure: int  |
                      +------------------+

```

#UML