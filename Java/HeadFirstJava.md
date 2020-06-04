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