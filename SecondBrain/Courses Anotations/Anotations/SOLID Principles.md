	 S | O | L | I | D
	-------------------
	 R | C | S | S | I
	 P | P | P | P | P

### Single Responsibility Principle (SRP)
- Loose Coupling
>Facilitate modularity and changes.

- Separation of Concerns
>Programs should be separated into distinct sections with separate concerns.

- Class Cohesion
>Methods should be separated when data isn't shared between them;
>Separate into multiple classes if possible.

### Open / Closed Principle (OCP)
- Open to Extension
>New behavior can be easily  implemented when needed;
>The code doesn't have a fixed behavior.

- Closed to Modification
>Changes to the code are not required;
>The only way to change the behavior of the code closed to extension is to change the code itself.

### Liskov Substitution Principle (LSP)
- Subtypes must be substitutable for their base Types;
- Base Types invariants are enforced;
- **Symptoms:**
>Type checking (*"is"* and *"as"* keywords);
>*null* checking;
>*NotImplementedException*;

### Interface Segregation Principle (ISP)
- Clients shouldn't depend on Methods they don't use
>Client is the conde that interacts with an existing Interface.

- Prefer small and cohesive Interfaces;
- Following *ISP* helps with implementing *SRP* and *LSP*;
- Break large Interfaces
>With Interface Inheritance;
>With adapter design pattern;

### Dependency Inversion Principle (DIP)
- High-level Modules should not depend on Low-level Modules, both should depend on Abstractions;
- Abstractions should not depend on details;
- Details should not depend on Abstractions;
- **Dependency Levels:**
>High-Level:
>
>	Process;
>	Business Rules.
>
>Low-Level:
>
>	Database;
>	File System;
>	Email;
>	Web API;
>	Configuration;
>	Clock.