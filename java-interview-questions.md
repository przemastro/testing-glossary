## Java Interview Questions

### Easy Questions:
1. What is Java?

 - Java is a high-level, class-based, object-oriented programming language designed to have as few implementation dependencies as possible. It is a general-purpose language intended to let application developers write once, run anywhere (WORA).

2. What are the main features of Java?

Main features include:
 - Simple
 - Object-oriented
 - Platform-independent
 - Secure
 - Multithreaded
 - Robust
 - Architecture-neutral
 - Portable
 - High performance
 - Interpreted

3. What is the difference between JDK, JRE, and JVM?

 - JDK (Java Development Kit): Provides tools to develop Java applications, including JRE and development tools.
 - JRE (Java Runtime Environment): Provides libraries, Java Virtual Machine (JVM), and other components to run Java applications.
 - JVM (Java Virtual Machine): Executes Java bytecode and provides a runtime environment.

4. What is the main difference between a Class and an Object?

 - A class is a blueprint for objects; it defines properties and behaviors. An object is an instance of a class with actual values.

5. What is inheritance in Java?

 - Inheritance is a mechanism in Java where one class inherits the properties and behaviors of another class. It promotes code reuse and establishes a parent-child relationship between classes.

6. What is polymorphism in Java?

 - Polymorphism allows methods to do different things based on the object it is acting upon. It can be achieved through method overriding and method overloading.

7. What is encapsulation in Java?

 - Encapsulation is the wrapping of data (variables) and code (methods) into a single unit called a class. It restricts direct access to some components, which can help prevent the accidental modification of data.

8. What are constructors in Java?

 - Constructors are special methods that initialize objects. They have the same name as the class and do not have a return type.

9. What is the purpose of the final keyword in Java?

 - The final keyword can be used to mark a variable as constant, a method as unoverridable, and a class as non-inheritable.

10. What is an interface in Java?

 - An interface is a reference type in Java, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types. Interfaces cannot contain instance fields or constructors.

11. What is an abstract class in Java?

 - An abstract class is a class that cannot be instantiated and is intended to be subclassed. It can have abstract methods (without a body) and concrete methods (with an implementation).

12. What is method overloading?

 - Method overloading is a feature that allows a class to have more than one method with the same name, but different parameters.

13. What is method overriding?

 - Method overriding occurs when a subclass provides a specific implementation for a method that is already defined in its superclass.

14. What is the static keyword in Java?

 - The static keyword denotes that a member belongs to the class, rather than instances of the class. It can be used with variables, methods, blocks, and nested classes.

15. What is the difference between == and equals()?

 - == compares object references, while equals() compares the values within the objects.

16. What is a package in Java?

 - A package is a namespace that organizes a set of related classes and interfaces. It helps avoid name conflicts and can control access with protected and default access.

17. What are the access modifiers in Java?

Java has four access modifiers:
 - Private: Accessible only within the class.
 - Default: Accessible only within the same package.
 - Protected: Accessible within the same package and subclasses.
 - Public: Accessible from anywhere.

18. What is a constructor chaining in Java?

 - Constructor chaining is the process of calling one constructor from another constructor within the same class or a superclass.

19. What is a String in Java?

 - String is a class in Java representing a sequence of characters. Strings are immutable, meaning once created, their values cannot be changed.

20. What are the different ways to create a String in Java?

 - By string literal: String str = "Hello";
 - By using the new keyword: String str = new String("Hello");

### Moderate Questions:
1. What is the super keyword in Java?

 - The super keyword refers to the superclass (parent class) of the object. It can be used to call superclass methods, constructors, and to access superclass fields.

2. What is the difference between ArrayList and LinkedList in Java?

 - ArrayList: Uses a dynamic array to store elements, offers fast random access but slower insertions and deletions.
 - LinkedList: Uses a doubly linked list, offers fast insertions and deletions but slower random access.

3. What is the purpose of the transient keyword?

 - The transient keyword in Java is used to indicate that a field should not be serialized.

4. What is a singleton class, and how do you create one?

 - A singleton class ensures that only one instance of the class exists throughout the application. It can be created by making the constructor private and providing a static method to get the instance.
 > public class Singleton {
private static Singleton instance;
private Singleton() {}
public static Singleton getInstance() {
if (instance == null) {
instance = new Singleton();
}
return instance;
}
}

5. What is the difference between HashMap and Hashtable?

 - HashMap: Non-synchronized, allows null keys and values, faster.
 - Hashtable: Synchronized, does not allow null keys or values, slower.

6. What is the use of the volatile keyword?

 - The volatile keyword in Java indicates that a variable's value will be modified by different threads. It ensures visibility of changes to variables across threads.

7. What is a thread in Java?

 - A thread is a lightweight process that allows a program to perform multiple tasks concurrently.

8. How do you create a thread in Java?

 - Threads can be created by extending the Thread class or implementing the Runnable interface.
 > // Extending Thread class
public class MyThread extends Thread {
public void run() {
System.out.println("Thread is running");
}
}
// Implementing Runnable interface
public class MyRunnable implements Runnable {
public void run() {
System.out.println("Thread is running");
}
}


9. What is the difference between synchronized method and synchronized block?

 - Synchronized method: Locks the entire method for the thread.
 - Synchronized block: Locks only a specified block of code, allowing finer control over synchronization.

10. What is the purpose of the finalize() method?

 - The finalize() method is called by the garbage collector before an object is destroyed. It allows the object to clean up resources before being collected.

11. What is the difference between throw and throws?

 - throw: Used to explicitly throw an exception.
 - throws: Declares that a method can throw exceptions.

12. What is the Java Memory Model (JMM)?

 - The Java Memory Model defines how threads interact through memory and what behaviors are allowed in concurrent executions. It provides rules for visibility and ordering of variables in shared memory.

13. What is a deadlock?

 - A deadlock is a situation in multithreading where two or more threads are blocked forever, waiting for each other to release resources.

14. How can you avoid deadlocks in Java?

Avoid deadlocks by:
 - Using a consistent order for acquiring locks.
 - Avoiding nested locks.
 - Using timeout for lock attempts.
 - Using higher-level concurrency utilities like java.util.concurrent.

15. What is the use of wait(), notify(), and notifyAll()?

These methods are used for inter-thread communication in synchronized blocks:
 - wait(): Causes the current thread to wait until another thread calls notify() or notifyAll() on the same object.
 - notify(): Wakes up a single thread that is waiting on the object's monitor.
 - notifyAll(): Wakes up all threads that are waiting on the object's monitor.

16. What are the types of exceptions in Java?

 - Checked Exceptions: Must be declared or caught (e.g., IOException, SQLException).
 - Unchecked Exceptions: Runtime exceptions, not required to be caught or declared (e.g., NullPointerException, ArrayIndexOutOfBoundsException).

17. What is a lambda expression in Java?

 - Lambda expressions are a feature in Java 8 that allow you to write anonymous methods. They provide a clear and concise way to represent a method interface using an expression.
 > (parameters) -> expression

18. What is a stream in Java?

 - Streams are a new abstraction introduced in Java 8 that allow processing sequences of elements. They support functional-style operations on collections, like filtering, mapping, and reducing.

19. What is the Optional class in Java?

 - The Optional class is a container object used to contain not-null objects. It is used to represent optional values that may or may not be present.

20. What is a functional interface in Java?

 - A functional interface is an interface with a single abstract method. They can be implemented using lambda expressions, method references, or constructor references.

### Difficult Questions:
1. What is garbage collection in Java, and how does it work?

 - Garbage collection is the process of automatically freeing memory by reclaiming objects that are no longer reachable in the application. The JVM's garbage collector performs this task, typically using algorithms like mark-and-sweep, generational collection, and reference counting.

2. What is the Java ClassLoader, and how does it work?

 - A ClassLoader in Java is a part of the Java Runtime Environment that dynamically loads Java classes into the JVM. It works by finding the bytecode of the class, typically from the file system or network, and defining the class in the JVM.

3. What are the different types of ClassLoaders in Java?

 - Bootstrap ClassLoader: Loads core Java classes (from the rt.jar).
 - Extension ClassLoader: Loads classes from the ext directory.
 - System/Application ClassLoader: Loads classes from the classpath.

4. What is the difference between java.util.HashMap and java.util.concurrent.ConcurrentHashMap?

 - HashMap: Not thread-safe, allows null keys and values.
 - ConcurrentHashMap: Thread-safe, does not allow null keys and values, and uses finer-grained locking for better concurrency.

5. How does the HashMap work in Java?

 - HashMap stores key-value pairs in buckets. It uses the hashCode() of the key to determine the bucket and equals() to resolve collisions. It provides constant-time performance for basic operations, assuming good hash function distribution.

6. What is the difference between synchronized and Lock in Java?

 - synchronized: A keyword for intrinsic locks, simpler to use but less flexible.
 - Lock: An interface from java.util.concurrent.locks providing more flexible and sophisticated locking mechanisms (e.g., ReentrantLock).

7. What are some common design patterns used in Java?

Common design patterns include:
 - Creational: Singleton, Factory, Abstract Factory, Builder, Prototype.
 - Structural: Adapter, Decorator, Proxy, Composite, Flyweight, Facade.
 - Behavioral: Observer, Strategy, Command, State, Template Method, Iterator, Chain of Responsibility.

8. What is the difference between Callable and Runnable in Java?

 - Runnable: Does not return a result and cannot throw checked exceptions.
 - Callable: Returns a result and can throw checked exceptions.

9. What is the ForkJoin framework in Java?

 - The ForkJoin framework is a framework for parallel execution of tasks. It uses a work-stealing algorithm to efficiently manage a pool of worker threads. It is designed to efficiently handle a large number of small tasks.

10. What is the Java Reflection API?

 - The Java Reflection API allows the inspection and manipulation of classes, methods, and fields at runtime. It enables dynamic behavior and introspection capabilities but can impact performance and security.

11. What is the difference between Serializable and Externalizable in Java?

 - Serializable: A marker interface, uses default serialization.
 - Externalizable: Allows custom serialization by implementing writeExternal and readExternal methods.

12. What are annotations in Java, and how are they used?

 - Annotations provide metadata for Java code. They can be used for documentation, compile-time checks, and runtime processing. Common annotations include @Override, @Deprecated, and custom annotations.

13. What is the Java Memory Model (JMM), and why is it important?

 - The Java Memory Model defines how threads interact through memory and the rules for reading and writing shared variables. It is crucial for writing correct and thread-safe concurrent programs.

14. How do you implement custom annotations in Java?

 - Custom annotations are implemented by defining an interface with the @interface keyword and specifying the retention policy and target.
 > @Retention(RetentionPolicy.RUNTIME)
@Target(ElementType.METHOD)
public @interface CustomAnnotation {
String value();
}

15. What is the difference between ReentrantLock and synchronized?

 - ReentrantLock: More flexible and feature-rich, supports fair and unfair locking, can be interrupted, and can try to acquire a lock.
 - synchronized: Simpler to use but less flexible.

16. How do you handle memory leaks in Java?

Memory leaks can be handled by:
 - Using memory profiling tools (e.g., VisualVM, YourKit).
 - Ensuring proper release of resources (e.g., streams, connections).
 - Avoiding static references to large objects.
 - Using weak references where appropriate.

17. What is the difference between shallow copy and deep copy in Java?

 - Shallow Copy: Copies the object structure but not the objects it refers to.
 - Deep Copy: Copies the entire object graph, including all referenced objects.

18. How do you implement a thread-safe singleton in Java?

A thread-safe singleton can be implemented using:
 - Bill Pugh Singleton Design: Using a static inner helper class.
 > public class Singleton {
private Singleton() {}
private static class SingletonHelper {
private static final Singleton INSTANCE = new Singleton();
}
public static Singleton getInstance() {
return SingletonHelper.INSTANCE;
}
}
 
19. What is the difference between Future and CompletableFuture in Java?

 - Future: Represents a result of an asynchronous computation, allows checking if the computation is complete, and retrieving the result.
 - CompletableFuture: Extends Future, provides more methods for combining and composing tasks, and supports callbacks.

20. What is the Stream API in Java, and how is it used?

 - The Stream API in Java provides a functional approach to processing sequences of elements. It supports operations like filtering, mapping, and reducing.
 > List<String> names = Arrays.asList("John", "Jane", "Jack");
List<String> filteredNames = names.stream()
.filter(name -> name.startsWith("J"))
.collect(Collectors.toList());

21. What is Lombok
    
 - Lombok is a Java library that helps to reduce boilerplate code by generating common methods such as getters, setters, toString, equals, hashCode, and constructors automatically at compile time using annotations. It makes the code more readable and maintainable by reducing the amount of boilerplate code.

Here is a typical Java class with getters, setters, and other methods:


> private String firstName;
private String lastName;
private int age;

    public Person() {}

    public Person(String firstName, String lastName, int age) {
        this.firstName = firstName;
        this.lastName = lastName;
        this.age = age;
    }

    public String getFirstName() {
        return firstName;
    }

    public void setFirstName(String firstName) {
        this.firstName = firstName;
    }

    public String getLastName() {
        return lastName;
    }

    public void setLastName(String lastName) {
        this.lastName = lastName;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "Person{" +
                "firstName='" + firstName + '\'' +
                ", lastName='" + lastName + '\'' +
                ", age=" + age +
                '}';
    }

    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (o == null || getClass() != o.getClass()) return false;

        Person person = (Person) o;

        if (age != person.age) return false;
        if (firstName != null ? !firstName.equals(person.firstName) : person.firstName != null) return false;
        return lastName != null ? lastName.equals(person.lastName) : person.lastName == null;
    }

    @Override
    public int hashCode() {
        int result = firstName != null ? firstName.hashCode() : 0;
        result = 31 * result + (lastName != null ? lastName.hashCode() : 0);
        result = 31 * result + age;
        return result;
    }}

Here’s the same class using Lombok annotations to reduce boilerplate code:

> import lombok.AllArgsConstructor;
import lombok.Data;
import lombok.NoArgsConstructor;
@Data
@NoArgsConstructor
@AllArgsConstructor
public class Person {
private String firstName;
private String lastName;
private int age;
}
@Data: A shortcut for @Getter, @Setter, @ToString, @EqualsAndHashCode, and @RequiredArgsConstructor.
@NoArgsConstructor: Generates a no-argument constructor.
@AllArgsConstructor: Generates a constructor with one parameter for each field.
Usage Example
java
Skopiuj kod
public class Main {
public static void main(String[] args) {
Person person = new Person("John", "Doe", 30);

        System.out.println(person.getFirstName()); // Output: John
        System.out.println(person); // Output: Person(firstName=John, lastName=Doe, age=30)

        Person anotherPerson = new Person("Jane", "Doe", 25);
        
        System.out.println(person.equals(anotherPerson)); // Output: false
    }}

Benefits of Lombok
 - Less Boilerplate Code: Lombok significantly reduces the amount of boilerplate code in your classes.
 - Improved Readability: With less boilerplate, the essential parts of your code are easier to read and understand.
 - Time-Saving: Lombok saves time by auto-generating common methods, so developers can focus on business logic.
Drawbacks
 - Learning Curve: New developers need to learn Lombok’s annotations and understand its behavior.
 - Dependency: Your project depends on Lombok at compile-time, which could be an issue if Lombok is not compatible with future Java versions or other libraries.