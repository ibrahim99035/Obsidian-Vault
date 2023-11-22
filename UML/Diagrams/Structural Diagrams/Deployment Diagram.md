- The deployment diagram visualizes the physical hardware on which the software will be deployed.

- It portrays the static deployment view of a system. It involves the nodes and their relationships.

- The main purpose of the deployment diagram is to represent how software is installed on the hardware component.

- Both the deployment diagram and the component diagram are closely interrelated to each other as they focus on software and hardware components.

- The deployment diagram does not focus on the logical components of the system, but it put its attention on the hardware topology.

---
### Key Components of a Deployment Diagram:

1. **Node:**
    
    - Represents a hardware device or a processing node in the deployment environment.
    - Examples include servers, workstations, routers, and other computing devices.
    - Displayed as a box with the node's name at the top.
2. **Artifact:**
    
    - Represents a deployable software component, such as executable files, libraries, or databases.
    - Displayed as rectangles within the nodes.
3. **Deployment Relationship:**
    
    - Represents the relationship between a node and an artifact.
    - Shown as a dashed line connecting the artifact to the node.
4. **Association:**
    
    - Represents a communication path or a connection between nodes.
    - Shown as a line connecting two nodes, often with an optional association name.
5. **Dependency:**
    
    - Represents a relationship between nodes, indicating that one node depends on another.
    - Shown as a dashed line with an arrow pointing from the dependent node to the independent node.

---
##### The deployment diagram consist of the following notations:
1. A component.
2. An artifact.
3. An interface.
4. A node.
![[Pasted image 20231122115703.png]]

---
##### Deployment diagrams can be used for the followings:
1. To model the network and hardware topology of a system.
2. To model the distributed networks and systems.
3. Implement forwarding and reverse engineering processes.
4. To model the hardware details for a client/server system.
5. For modeling the embedded system.
---
![[Pasted image 20231122115918.png]]

#UML