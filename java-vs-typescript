# Comparison of Java vs TypeScript Issues

| **Issue**                 | **Java**                                                    | **TypeScript**                                                |
|---------------------------|-------------------------------------------------------------|---------------------------------------------------------------|
| **Garbage Collector**      | Java has a built-in Garbage Collector that automatically manages memory. | TypeScript works in the JavaScript environment, which uses a garbage collection mechanism in the V8 engine. |
| **Object Creation**        | `new` allocates memory, e.g. `User user = new User();`       | `new` creates an instance of a class, e.g. `const user = new User();` |
| **Collections**            | `List`, `Set`, `Queue` – interfaces with adding, removing, and storing elements. | `Array<T>`, `Set<T>`, `Map<K,V>` – no `Collection` interface, but similar operations on data structures. |
| **Maps**                   | `Map<K,V>` – key-value collection, keys are unique.         | `Map<K,V>` – similar concept, allows iteration and manipulation of data. |
| **equals()**               | The `equals()` method compares objects, by default comparing references. | #ERROR! |
| **hashCode()**             | Generates a hash based on the memory address.               | No equivalent, TypeScript does not have a built-in object hashing mechanism. |
| **final**                  | `final` prevents modification of variables/methods/classes. | `const` prevents assigning a new value to a variable, but objects can be modified. |
| **static**                 | Static fields/methods are shared among instances.          | `static` works similarly – methods and fields belong to the class, not the instance. |
| **Exceptions**             | Checked (e.g., `IOException`) and Unchecked (e.g., `NullPointerException`). | No checked exceptions, but exception handling via `try/catch`. |
| **enum**                   | Creates a set of constant values.                           | Similar concept of `enum`, but after compilation it becomes a regular object. |
| **singleton**              | A single instance is created through a `private static final` field. | Singleton created via `static` and a private constructor. |
| **Abstract Class**         | Can contain both abstract methods and implementations.      | `abstract class` works similarly – can contain methods with and without implementations. |
| **Interface**              | Defines a contract for methods but contains no implementation. | `interface` defines types and structures of objects, but has no implementation. |
| **Object**                 | The base class of all classes.                              | Everything in TypeScript inherits from `Object`. |
| **Data Model**             | A class representing data.                                  | A class or interface (e.g., `interface User { id: number; name: string; }`). |
| **Deadlock**               | Thread deadlock when shared resources are involved.         | No multithreading – no deadlocks in TypeScript. |
| **Constructor**            | A special method with the same name as the class, called when an object is created. | `constructor()` works similarly, initializing class properties. |
| **this**                   | Refers to the object in which the method is invoked.        | `this` refers to the object, but requires `bind()` in anonymous functions. |
| **super**                  | Refers to the method/constructor of the parent class.       | `super` works identically, referring to the base class. |
| **Object Field**           | Defined outside methods within the class.                   | Works identically – class properties. |
| **Local Variable**         | A variable defined within a method/constructor.             | A variable declared within a function/method. |
| **Constructor Overloading**| Possible – you can define multiple constructors with different parameters. | No direct support, but can be simulated using optional arguments. |
| **Thread**                 | `Thread` – a thread executing tasks.                        | JavaScript is single-threaded, but `setTimeout()`, `Promise`, `async/await` simulate concurrency. |
| **Throw**                  | `throw` throws an exception within a method.                | `throw` works identically. |
| **Throws**                 | Declares that a method can throw an exception (e.g., `throws IOException`). | No equivalent, but exceptions can be handled with `try/catch`. |
| **Streams**                | Stream API for collection operations (filter, map, reduce). | `Array.prototype.map`, `filter`, `reduce` work similarly. |
| **NullPointerException**   | Occurs when trying to use `null`.                            | `undefined` and `null` can cause errors, but TypeScript has `strictNullChecks`. |
| **Encapsulation**          | `private`, `protected`, `public` to hide implementation.    | TypeScript also supports `private`, `protected`, `public`. |
| **Polymorphism**           | The ability to override methods in derived classes.         | TypeScript supports polymorphism via interfaces and abstract classes. |
| **Inheritance**            | `extends` allows for class inheritance.                     | `extends` works identically in TypeScript. |
| **Access Modifiers**       | `private`, `protected`, `public`.                           | `private`, `protected`, `public` work the same. |

---

### Summary:

Java is an object-oriented, strongly-typed language running on the JVM with memory management via Garbage Collector.  
TypeScript is a superset of JavaScript, running on V8, supporting classes and interfaces but without a memory management mechanism like Java.  
Common concepts: classes, interfaces, inheritance, polymorphism, access modifiers, exception handling.  
Main differences: no checked exceptions in TypeScript, no `Thread`, different memory management, no `hashCode()`, no multithreading.

---

### Primitive Types

| **Category**              | **Java**                                                        | **TypeScript**                                                  |
|---------------------------|---------------------------------------------------------------|---------------------------------------------------------------|
| **Primitive Types**        | `byte`, `short`, `int`, `long`, `float`, `double`, `char`, `boolean` | `number`, `bigint`, `string`, `boolean`, `symbol`, `null`, `undefined` |
| **Default Values**         | `0` for numbers, `false` for boolean, `'\u0000'` for char, `null` for objects | `undefined` for uninitialized variables, `null` can be assigned manually |
| **Integer Range**          | `byte`: -128 to 127, `short`: -32,768 to 32,767, `int`: -2³¹ to 2³¹-1, `long`: -2⁶³ to 2⁶³-1 | `number`: 64-bit float (IEEE 754), `bigint`: arbitrarily large integers |
| **Floating-point Numbers** | `float`, `double`                                              | `number` (supports both integers and floating-point numbers)   |
| **Character Handling**     | `char` (16-bit Unicode)                                        | `string` (no separate `char` type)                              |
| **Boolean Values**         | `boolean` (true or false)                                      | `boolean` (true or false)                                       |
| **Nullable Values**        | `null` (for object references)                                 | `undefined` and `null` (different concepts)                     |
| **Are primitives objects?**| ❌ No (stores values directly in memory)                       | ✅ Yes, `number`, `boolean`, `string` have object counterparts (`Number`, `Boolean`, `String`) |
| **Autoboxing**             | ✅ `int` ↔ `Integer`, `double` ↔ `Double`                       | ❌ No automatic boxing, but object versions of types can be used |
| **Handling `null` and `undefined`** | `null` for object types, primitives cannot have `null`       | `undefined` for uninitialized variables, `null` for manually assigned values |
| **Enum Types**             | ✅ `enum` (full-fledged data type)                              | ✅ `enum` (but works differently – assigns numeric or string values) |

---

### `null` vs `undefined`

| **Feature**               | **null (TypeScript)**                                      | **undefined (TypeScript)**                                      |
|---------------------------|------------------------------------------------------------|-----------------------------------------------------------------|
| **Definition**            | No value, but intentionally assigned.                      | A value that was never assigned.                                |
| **When does it occur?**    | User can explicitly assign `null`.                         | If a variable is not initialized, it is by default `undefined`. |
| **For which types?**       | `null` can be assigned to a variable if TypeScript allows it. | `undefined` is the default value for uninitialized variables.   |
| **Error Handling?**       | Can cause errors if the value is not checked.              | Can cause errors if trying to call a method on `undefined`.     |
