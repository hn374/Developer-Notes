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
