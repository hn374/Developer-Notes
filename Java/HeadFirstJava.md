# Java

## Chapter 1: Introduction

Every Java application has to have at least one class and one main method.

The main() method is where you code starts running.

## Chapter 2: Classes and Objects

A class is a blueprint for the object. 

A real Java application is nothing but objects talking to other objects.

Each time an object is created in Java, it goes into an area of memory known as The Heap. Java manages memory for you. When the JVM sees that the object can't be used anymore, it is eligible for garbage collection.

The garbage collector will run, throw out the unreachable objects, and free up space so that space can be used later.

Marking something as public and static makes it behave like a global variable.

## Chapter 3: Primitives and References

Variables come in two flavors: primitives and object reference.

Primitives hold fundamental values, like integers, booleans and floating point numbers.

Object references hold references to objects. An object reference variable holds bits that represent a way to access an object. It doesn't hold the object itself, but a pointer to it.

Arrays are always objects, whether they're declared to hold primitives or object references.

## Chapter 4: How Objects Behave

Objects have state and behavior, represented by instance variables and methods.

Mark your instance variables private and mark your getters and setters public.

## Chapter 6: Get To Know the Java API

Arrays in Java can not change size, but ArrayLists can.

An array has to know its size at the time it is created. To put in an object inside an array, you must assign it to a specific location.

Angle brackets <> are a way to force the compiler to allow only a specific type of object in the ArrayList.

## Chapter 7: Better Living In Objectville

There are is-a and has-a relationships. For example, a bathroom is not a tub, but it has a tub. This means that bathroom has a reference to tub, but it does not extend tub.

Access levels control who sees what, and are crucial to having well defined, robust Java code.

Public members are inherited. Private members are not inherited.

Use inheritance when one class is a more specific type of a superclass. For example, a willow is a more specific type of a tree.

With polymorphism, the reference and the object can be different. When you declare a reference variable, any object that passes the is-a test for the declared type of the reference variable can be assigned to that reference.

This is useful for certain things like polymorphic arrays. For example, let's say you declared an array of animals. In this array, you could hold different animal objects, like dog, cat, cow, pig, etc.

You can also have polymorphic arguments and return types.

A non-public class can be subclassed only by the classes in the same package as the class.

The second thing that stops a class from being subclassed is the keyword modifier final. A final class means that it is the end of the inheritance line.

Whatever the superclass uses as an argument for a method, the subclass using that method must use the same argument. The same is for return value.

An overloaded method is just a different method that happens to have the same method name. It has nothing to do with inheritance or polymorphism.

## Chapter 8: Serious Polymorphism

An interface is a 100% abstract class. An abstract class is a class that can't be instantiated.

When you're designing your class inheritance structure, you have to decide which classes are abstract and which are concrete. 

Concrete classes are those that are specific enough to be instantiated. A concrete class just means that it is okay to make classes of that type.

You can make methods abstract. An abstract method means that the method must be overridden. An abstract method has no body. They exist solely for polymorphism.

Every class in Java extend the class Object.

All interface methods are abstract. They are also implicitly public.

The keyword super lets you invoke a superclass version of an overridden method from within the subclass.

## Chapter 9: Life and Death of an Object

The heap is an area of memory where objects live.

The stack is an area of memory where method invocations and local variables live. Local variables are known as stack variables because they live on the stack.

Instance variables are declared inside a class but not inside a method. Instance variables live on the heap insde the object they belong to.

Local variables are declared inside a method, including method parameters. They're temporary and live only as long as the method is on the stack. All local variables live on the stack, in the frame corresponding to the method where the variables are declared.

When you call a method, the methods lands on the top of a call stack. The method at the top of the stack is always the currently-running method for that stack.

If the local variable is a reference to an object, only the variable (reference/remote control) goes on the stack. The object itself still goes in the heap.

Knowing the fundamentals of Java stack and heap is crucial if you want to understand variable scope, object creation issues, memory management, threads and exception handling.

A constructor must have the same name as the class and must not have a return type.

The key feature of a constructor is that it runs before the object can be assigned to a reference. That means you get a chance to step in and do things to get the object ready for use.

Most people use constructors to initialize the state of an object. In other words, to make and assign values to the object's instance variables.

Overloaded constructors means you have more than one constructor in your class. To compile, each constructor must have a different argument list.

All the constructors in an object's inheritance tree must run when you make a new object.

The only way to call a super constructor is by calling super(). The compiler puts in a call to super() if you don't.

The superclass parts of an object have to be fully formed before the subclass parts can be constructed.

They keyword this is a reference to the current object. You can only say it within a constructor and it must be the first statement in the constructor.

An object's life depends entirely on the life of references referring to it.

## Chapter 10: Numbers Matter

Methods in the math class don't use any instance variables. The methods are static, so you don't have to have an instance of math.

The keyword static lets a method run without any instance of the class.

You call a static method using a class name. You call a non-static method with a reference variable name.

A static method can't refer to any instance variables of the class. They can't use non-static methods either.

A static variable gives you a valued shared by all instances of a class. Static variables are initialized when a class is loaded. 

A variable marked final means that it can never change once initialized.

## Chapter 11: Risky Behaviors

A method has to declare the exceptions it might throw.

An exception is an object of type exception.

A finally block is where you put code that must run regardless of an exception.

## Chapter 12: Getting GUI

The process of getting and handling a user event is called event handling.

A listener interface is the bridge between the listener and the event source. The interface is where the callback method is declared.

A listener's job is to implement the interface, register with the button and provide the event-handling.

An event source's job is to accept registrations (from listeners), get events from the user, and call the listener's event handling method (when the user clicks the event source).

An inner class can use all the methods and variables of the outer class, even the private ones.

## Chapter 13: Using Swing

Layout Manager objects control the size and location of the widgets in a Java GUI.

Components are the things you put in a GUI. All components are capable of holding other components.

## Chapter 14: Saving Objects

Connection streams represent a connection to a source or destination while chain streams can't connect on their own and must be chained to a connection stream.

It usually takes two streams hooked together to do something useful. One to represent the connection, and the other to call methods on.

When an object is serialized, all the objects it refers to from instance variables are also serialized.

If you want your class to be serializable, you must implement the Serializable interface.

Mark a variable as transient if it can't or shouldn't be saved.