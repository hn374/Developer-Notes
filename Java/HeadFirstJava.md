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