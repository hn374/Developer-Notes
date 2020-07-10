# Design Patterns Explained

## Chapter 1: The Object Oriented Paradigm

Functional decomposition is a natural way to deal with complexity. You break down the problem into the functional steps that compose it. It is easier to deal with smaller pieces than it is to deal with the problem in its entirety. Each function is subdivided until it is manageable.

Design would be easier if we made each subfunction responsible for its own behavior and tell it to go do something and trust that it will know how to do it. This is called delegation.

Requirements always change. Rather than complaining about changing requirements, we should change the development process so that we can address change more effectively. 

You can change your code so that the impact of changing requirements is much less dramatic.

Cohesion refers to how closely the operations in a routine are related. The more operations are related in a routine or a class, the easier it is to understand things.

Weakly cohesive classes are those that do many, unrelated tasks.

Coupling refers to the strength of a connection between two routines. Coupling is a complement to cohesion. 

Cohesion describes how strongly the internal contents of a routine are related to each other. Coupling describes how strongly a routine is related to other routines. The goal is to create routines with strong cohesion and loose coupling.

Fixing bugs takes a short period of time in the maintenance and debugging process. The overwhelming amount of time involved in maintenance and debugging is spent on trying to discover how the code works and on finding bugs and taking the time to avoid unwanted side effects.

Communicating at one level (conceptually) while performing at another level (implementation) results in the requestor (the instructor) not having to know exactly what is happening, only having to know in general conceptually what is happening.

The object oriented paradigm is centered on the concept of the object. I write code organized around objects, not functions.

The advantage of using objects is that I can define things that are responsible for themselves. Objects inherently know what type they are. The data in an object allows it to know what state it is in, and the code in the object allows it to function properly. 

The best way to think about what an object is, is to think of it as something with responsibilities. A good design rule is that objects should be responsible for themselves and should have those responsibilities clearly defined. 

At the conceptual level, an object is a set of responsibilities.

At the specification level, an object is a set of methods (behaviors) that can be invoked by other objects or by itself.

At the implementation level, an object is code and data and computatioanl interactions between them.

Encapsulation refers to the hiding of data.

There are several advantages to encapsulation. The fact that it hides things from the user directly implies the following: using things is easier because the user does not need to worry about implementation issues. Implementations can be changed without worrying about the caller. The internals of an object are unknown to other objects they are used by the object to help implement the function specified by the object's interface.

Consider the problem of unwanted side effects that arise when functions are changed. This kind of bug is addressed effectively with encapsulation. The internals of objects are unknown to other objects. The object's data and the way it implements its responsibilities are shielded from changes caused by other objects.

When I encapsulate something, I am necessarily loosely coupled to it. Hiding implementations thus promotes loose coupling.

Polymorphism means having many different forms of behavior for the same call. 

A constructor is a special procedure that is automatically called when the object is created. Its purpose is to handle starting up the object. The constructor is the natural place to do initializations, set default information, set up relationships with other objects, or do anything else that is needed to make a well-defined object. 

Destructors clean up an object when it is no longer needed (when it has been deleted).

## Chapter 2: The UML (Unified Modeling Language)

UML is the modeling language of the object oriented community. It is a visual language used to create models of programs.

In this context, the term models of programs means diagrammatic representations of the programs that show the relationships among the objects in the code.

The UML is used primarily for communication with developers and customers. The UML gives us tools to elicit better requirements.

The most basic of UML diagrams is the class diagram. It both describes classes and shows the relationships among them.

An abstract class is a class that is used to define the interface for the classes that derive from it as well as being a place to put any common data and methods of these derived classes.

## Chapter 4: A Standard Object-Oriented Solution

One of the fundamentals of baseball is to keep your eye on the ball. Don't let yourself get distracted by secondary details. Focus on the most important task at hand, the thing you are trying to handle now.

Proper analysis and design requires a balancing act between competing interests. 

You have to decide which aspects of the problem you are designing to, or what sorts of changes you are trying to protect your system from. 

## Chapter 5: An Introduction To Design Patterns

A pattern is a solution to a problem in a context. 

A pattern involves four items: the name of the pattern, the purpose of the pattern, how we could accomplish this, and the constraints and forces we have to consider to solve it.

Patterns exist for almost any design problem.

Patterns can also be combined together to solve complex architectural problems.

Patterns help us see the forest and the trees.

## Chapter 6: The Facade Pattern

The Facade Pattern provides a unified interface to a set of interfaces in a subsystem. Facade defines a high level interface that makes the subsystem easier to use. For example, using a 3D drawing program in a 2D way.

This approach only works when using a subset of the system's capabilities or interacting with it in a particular way. 

Most of the work still needs to be done by the underlying system. The Facade provides a collection of easier-to-understand methods.

Facade can reduce the number of objects for the client.

The Facade Pattern is named that because it puts up a new interface in front of the original system.

The Facade Pattern applies when you want to encapsulate or hide the original system.

## Chapter 7: The Adapter Pattern

The Adapter Pattern converts the interface of a class into another interface that the client expects. 

Adapter lets classes work together that could not otherwise because of incompatible interfaces.

A Facade simplifies an interface while an Adapter converts a preexisting interface into another interface.

## Chapter 8: Expanding Our Horizons

An object is an entity that has responsibilities. These responsibilities define the behavior of the object.

Design patterns use inheritance to classify variations in behaviors.

Many design patterns use encapsulation to create layers between objects. This enables the designer to change things on different sides of the layer without adversely affecting the other side. This promotes loose coupling between the sides.

If variations are the specific concrete classes in the domain, commonality defines the concepts in the domain that tie them together.

The common concepts will be represented by abstract classes. The variations found by variability analysis will be implemented by the concrete classes. 

An abstract class represents the core concept that binds together all the derivatives of the class. This core concept is what defines the commonality.

When defining an abstract class, you must ask yourself what interface is needed to handle all the responsibilities of this class?

When defining derived classes, you must ask yourself given this particular variation, how can I implement it with the given specification?

The specification identifies the interface I need to use to handle all the cases of this concept. 

The concept of using objects to hold variations in behavior is not unlike the practice of using data members to hold variations in data.

## Chapter 9: The Strategy Pattern

The Strategy Pattern is the use of encapsulating an algorithm in an abstract class and using one of them at a time interchangeably. 

The intent for the Strategy Pattern is to define a family of algorithms, encapsulate each one, and make them interchangeable. 

The Strategy Pattern separates the selection of the algorithm from the implementation of the algorithm. Allows for the selection to be made upon context.

Technically, the Strategy Pattern is about encapsulating algorithms, but in practice, it can be used to encapsulate any kind of rule.

## Chapter 10: The Bridge Pattern

The intent of the Bridge Pattern is to decouple an abstraction from its implementation so that the two can vary independently. 

The Bridge Pattern often incorporates the Adapter Pattern.

When two or more patterns are tightly integrated like the Bridge and Adapter, the result is often called a compound design pattern.

One way to measure the quality of a design is to see how it handles variation.

Modifying code to improve its structure without adding function is called refactoring.

In general, you should identify which patterns to consider by matching them with the characteristics and behaviors in the problem domain.

## Chapter 11: The Abstract Factory Pattern

The intent of the Abstract Factory Pattern is to provide an interface for creating families of related or dependent objects without specifying their concrete classes.

Often a switch statement indicates the need for polymorphic behavior or the presence of misplaced responsibilities. 

The client object just knows who to ask for the objects it needs and how to use them.

The Abstract Factory Class specifies which objects can be instantiated by defining a method for each of these different types objects. Typically, an Abstract Factory object will have a method for each type of object that must be instantiated. 

The concrete factories specify which objects are to be instantiated.

This pattern isolates the rules of which objects to use from the logic of how to use these objects.

## Chapter 12: How Do Experts Design?

Start by looking at the problem in its simplest terms and then adding additional features, making the design more complex as we go because we are adding more information.

## Chapter 13

The process of thinking in patterns: identify the patterns, analyze and apply the patterns, and add detail.

A pattern in the system often relates to other patterns in the system by providing a context for these other patterns.

The Abstract Factory Pattern creates sets of related objects (families).

The Adapter Pattern adapts an existing class A to the interface needed by using class B. 

The Bridge Pattern allows for different implementations to be used by a set of related objects (concrete classes of the abstraction in the pattern).

The Facade Pattern simplifies an existing system A for a class using B.

Consider what you need to have in your system before you concern yourself with how to create it.

Outermost patterns is a term for the one or two patterns that establish a context for the other patterns in the system. This is the pattern that constrains what the other patterns can do.

## Chapter 14: The Principles and Strategies of Design Patterns

At the local level, patterns tell us how to solve particular problems for a given context. 

At the global level, patterns create a map of how the components of the application interrelate with one another.

The open closed principle states that the modules, methods and classes should be open for extension, while closed for modification. In other words, design your software so that you can extend its capabilities without changing it.

The dependency inversion principle states that high-level modules should not depend on low-level modules. Both high-level and low-level modules should depend upon abstractions. 

It also states that abstractions should not depend on details, details should depend upon abstractions.

It is important when designing classes within a context that they present the same external behavior.

Given a reference to a base class (or interface), the using object should not be able to tell whether a derivation (or implementation) is present. This makes all derivations of the base class interchangeable with each other.

To make design decisions, you should ask yourself: "Under what circumstances would this alternative be better than the other alternative?" and then ask "Which of these circumstances is most like my problem domain?"

## Chapter 15: Commonality and Variability Analysis

Design patterns can't be used in all designs, but the lessons learned from them can.

Experienced developers know that when adding new function to an existing system, the major cost is often not in writing the new code but in integrating it into the existing system. The reason for this is that the pieces in most existing systems are fairly tightly coupled. We must eliminate, or greatly limit, this coupling.

Use CVA to identify the concepts (commonalities) and concrete implementations (variabilities) that are present in the problem domain.

After the concept for the functionality you need has been identified, you go on to specify the interface for the abstraction that encapsulates this. Derive this interface by considering how the concrete implementations derived from this abstraction will be used.

## Chapter 16: The Analysis Matrix

