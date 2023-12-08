### Process
1. Commit or Backup a working copy of the code;
2. Verify the code behavior (preferably using Unit Tests);
	- Create a new set if needed.
1. Apply the code Refactoring;
2. Verify if the code behavior was preserved.

### Principle of Least Astonishment
- "Do what users / consumers expect";
- The Code should:
	1. Be simple;
	2. Be Clear;
	3. Be Consistent.

### "Code Smells"
1. **Bloaters**
	- Make codebase bigger than it should be;
	- Impact comes slowly and over-time;
	- Can be prevented with more focused code.
2. **Object-Orientation Abusers**
	- Break Polymorphism;
	- Create inappropriate tight coupling;
	- Increase code repetition.
3. **Change Preventers**
	- Interact with many parts of the system;
	- Create inappropriate tight coupling;
	- Lacks separation.
4. **Dispensables**
	- Code with little to no real value;
	- Made unused in update or commented-out;
	- Can be removed safely.
5. **Couplers**
	- Creates excessive coupling;
	- Tie unrelated parts of the system together. 
6. **Obfuscators**
	- Impede code clarity;
	- Hide real / original intent of the code;
	- Confuse code reader / reviewer.

### "Smells" Hierarchy
	LOW to HIGH
1. Statement Smells;
2. Method Smells;
3. Class Smells.
### Method Refactoring
- **Extract Method**
>Identify extractable code;
>Create new Method and copy the code to it;
>Identify local variables;
>Replace old code with the new Method;
>Compile and run tests.

- **Rename Method**
>Create new Method with same parameters;
>Give it a new name;
>Copy the old code to the new method;
>Replace old code with call to new method;
>Compile and run tests;
>Replace old references to new Method;
>Remove old Method;
>Compile and run tests.

- **Inline Method**
>Verify if it's not overwritten;
>Find all calls to the Method;
>Replace calls with Method body;
>Compile and run tests;
>Remove original Method;
>Compile and run tests.

- **Introduce Explaining Variables**
>Declare new Variable with a clear name;
>set it as part of complex expression;
>Replace result with the Variable;
>Compile and run tests;
>Repeat process as needed;

- **Inline Temp**
>Verify Temp if Variable is only assigned once;
>Replace reference to Temp with it's operation;
>Compile and run tests;
>Remove Temp declaration and assignment;
>Compile and run tests.

- **Replace Temp with Query**
>Verify if Temp is only assigned once;
>Extract Variable to a new Method;
>Compile and run tests;
>Replace all Temp references to the new Method;
>Remove Temp declaration;
>Compile and run tests.

- **Split Temp Variable**
>Change the name of the Temp in it's first assignment;
>Change all of it's references up to next assignment;
>Declare original Temp name in the second assignment
>Compile and run tests;
>Repeat process as needed.

- **Parameterize Methods**
>Create new parameterized Method;
>Replace calls to old Method with the new one;
>Compile and run tests;
>Remove original Method;
>Compile and run tests;
>Repeat process as needed.

- **Replace Parameter with explicit Method**
>Create explicit Methods for each Parameter;
>Move condition body to new Methods;
>Replace old conditions with calls to the new Methods;
>Compile and run tests;
>Replace calls to old Method with new the ones;
>Remove old Methods;
>Compile and run tests;

- **Add Parameter**
>Declare a new Method with the new Parameters;
>Copy the old Method body to the new Method;
>Change old Method to call the new one;
>Compile and run tests;
>Replace references to new Method;
>Remove original Method;
>Compile and run tests;

- **Remove Parameter**
>Declare a new Method without Parameters;
>Copy the old Method body to the new Method;
>Change old Method to call the new one;
>Compile and run tests;
>Replace references to new Method;
>Remove original Method;
>Compile and run tests;

- **Separate Query from Modifier**
>Create Query Method that returns the same;
>Change original Method to call new one;
>Compile and run tests;
>Replace references to the new Method
>Update original Method to return *void*;
>Compile and run tests.

### Class Refactoring
- **Encapsulate Field**
>Create property accessors for the Field;
>Replace all references to the Field;
>Compile and run tests;
>Change Field to *private*

- **Encapsulate Collection**
>Add explicit Methods (Add / Remove);
>Initialize Field to an empty Collection;
>Compile and run tests;
>Find references that get the Collection;
>Modify them to use the explicit Methods;
>Compile and run tests;
>Modify *get* to return a *read-only*;
>Compile and run tests.

- **Move Methods**
>Declare Method in target Class;
>Copy code to new method;
>Reference target's Class from original one;
>Compile and run tests.

- **Extract Class**
>Determine how to split Class;
>Create new Class to hold the responsibility;
>Add a field in the old Class with the type of the new one;
>Compile and run tests;
>Decide whether to expose new Class through original one.

- **Replace Inheritance with Delegation**
>Create a field in a Subclass with the type of the Super;
>Change Methods in Subclass to use new field;
>Compile and run tests;
>Remove Subclass declaration;
>Add delegation Methods for Superclass;
>Compile and run tests.

- **Replace Condition with Polymorphism**
>Extract Method so the condition will have it's own Method;
>Move the Method so condition is top in hierarchy;
>Choose Subclass to override conditional Method;
>Compile and run tests;
>Remove leg of the condition;
>Compile and run tests;
>Repeat the process until all parts of the condition have their own separate Method;
>Make the Superclass Method *abstract*.