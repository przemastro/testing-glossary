# Garbage Collection and Collections in Java

**Garbage Collector** - a memory management process. In Java, when creating an object, memory is allocated using the `new` keyword.  

### Collections in Java:
- **List** - an ordered collection of elements that may contain duplicates, e.g., `ArrayList`.
- **Set** - a collection of unique elements that does not guarantee order, e.g., `HashSet`.
- **Queue** - an ordered collection that sorts elements.

### Maps:
Maps are collections not part of the `Collection` interface. They contain key-value pairs, where the key is unique.
- **HashMap** - does not guarantee key order.

### Methods:
- **`equals()`** - a method for comparing objects, specifically their memory addresses. It works similarly to the `==` operator.
- **`hashCode()`** - associated with `equals()`. When an object is created, memory is allocated. The hash code is dynamically assigned based on the memory address when requested. Interestingly, objects with the same hash code may return `false` when compared using `equals()`—a quirk of hash-based collections.

### Keywords:
- **`final`** - a keyword that denotes immutability. A `final` class cannot be inherited, and methods marked as `final` cannot be overridden, preventing modification of the method's logic. `final` variables become constants. For primitive types like `int`, they can only be assigned once. For object types, new objects cannot be assigned, but the contents of the object can still be modified (e.g., modifying elements in a `HashMap`).
- **`static`** - static fields are shared between all instances of a class. If a static field is modified in one instance, it will affect all others. Static methods do not require creating an instance of the class and cannot be overridden.

### Exceptions:
- **Checked Exceptions** - must be handled by the programmer, enclosed in a `try-catch` block, e.g., `IOException`, `SQLException`, `FileNotFoundException`.
- **Unchecked Exceptions** - e.g., `NullPointerException`, indicating programming errors.

### `enum`:
An enum is a special data type that contains a set of constants. It can store constants or keys. You can assign values to enum keys (e.g., `key.name() = "value"`), and later retrieve this value by key. Enums are used to define a restricted set of values.

### Singleton:
A design pattern where only one instance of a class is created throughout the application. This instance serves as an access point. For example, the JDBC connector for database connections is often created as a static method to instantiate the singleton.

### Abstract Class:
An abstract class contains both abstract (without implementation) and non-abstract methods. You can inherit from an abstract class, but you cannot create an instance of it.

### Interface:
An interface contains only abstract methods and static methods. It generally defines method declarations that must be implemented. Interfaces are implemented by classes, and classes inherit from other classes. Interfaces can inherit from other interfaces. When implementing an interface in a class, you must provide implementations for all declared methods.

### Class:
A class is a mechanism used to define object types. When creating an object, it is instantiated with a specific type defined by the class.

### Object:
The mechanism used to create a single instance of an object, i.e., a singleton.

### Data Model:
A class used to represent objects.

### Deadlock:
A situation where threads wait for each other indefinitely due to shared resources.

### Constructor:
A special method with the same name as the class, automatically called when creating an object. It has no return type, not even `void`, and is used to initialize fields and assign values. It can be a default constructor (without parameters) or parameterized.

### `this`:
Refers to the current object, distinguishing between object fields and local variables. You can return `this` to return the object itself, enabling method chaining.

### `super`:
Refers to methods, fields, and constructors of the parent class. For example, when overriding a method in a subclass or when both classes have fields with the same name.

### Object Field:
A variable defined outside of methods or constructors within the class.

### Local Variable:
A variable declared inside methods or constructors.

### Constructor Overloading:
Allows a class to have more than one constructor, enabling the creation of objects with different parameters.

### `Thread`:
A thread is a process or a single task executed by multiple actions.

### `Throw`:
Used inside a method to throw an exception.

### `Throws`:
A declaration that a method may throw an exception. This requires the use of `try-catch`. Inside the `try-catch` block, you call the method with the `throws` declaration. If there is no exception, the code continues execution.

### Streams:
A mechanism used for working with data, such as in collections. You can filter, sort, and manipulate this data.

### `NullPointerException`:
Occurs when `null` is assigned to an object.

### Encapsulation:
Hiding the internal details of a class to protect its data.

### Polymorphism:
The ability to override methods in derived classes.

### Inheritance:
The `extends` keyword allows a class to inherit from another class.

### Access Modifiers:
- **Private**: Accessible only within the class.
- **Default**: Accessible only within the same package.
- **Protected**: Accessible within the same package and in subclasses.
- **Public**: Accessible from anywhere.

## Method Invocation:

| **Method Invocation**                  | **When to Use**                                                | **Example**                                 |
|----------------------------------------|---------------------------------------------------------------|---------------------------------------------|
| **Directly from the class (static)**   | Static methods (do not require class instantiation)           | `MyClass.staticMethod();`                   |
| **Through an object instance**         | Instance methods (must create a class object)                 | `MyClass myObject = new MyClass(); myObject.instanceMethod();` |
| **Through inheritance**                | Methods can be invoked by the subclass                        | `DerivedClass.staticMethod();` (for static methods) |

### Summary of Basic Method Invocation Types:
- **Directly from the class** (for static methods).
- **Through the class instance** (for instance methods).
- **Through inheritance** (for both static and instance methods).
