# Computer Science

***

## Object Oriented Programming

Object-oriented programming is a pattern of programming whereby the solution to a programming problem is modeled as a collection of collaborating objects. Objects collaborate by sending messages to each other. An object is an entity that possesses both state (properties) and behavior (methods).

A class is a special kind of object that's used as a template for creating instances of itself. Think of it like a blueprint.

***

## Encapsulation

Encapsulation is achieved when each object keeps its state private, inside a class. Other objects don't have direct access to this state. Instead, they can only call a list of public functions, called methods. 

*** 

## Abstraction

Abstraction hides internal implementation details. It should only reveal operations relevant for the other objects. For example, there's a lot of things happening when you use your phone but you are only exposed to the buttons the developers want you to be exposed to. This is abstraction. You don't have to know what's happening under the hood to use your phone.

***

## Polymorphism

When we have a parent class, and several different child classes inherit from it, and the child classes need to use a method from the parent class but they all implement it a different way. The child class can override this method to fit its own object. For example, an Animal class could derive a Cat, Dog and Cow class. The Animal class could have a speak method, but each of the derived animal classes would speak differently. You would have to change the speak method for each of these derived animal classes, so that the Cat would print meow, the Dog would print bark and the Cow would print moo.

***

## Composition vs Inheritance

Both composition and inheritance are object-oriented programming concepts.

Composition is a design technique to implement a "has-a" relationship between objects. When you think composition, think of what the object is composed of. For example, a Person object has a Job object. Composition is achieved by using instance variables of other objects.

Inheritance is a design technique to implement a "is-a" relationship between objects. The child object that inherits from a parent object will have all the attributes of that parent object. For example, a Honda Civic object inherits from a Car object.

***

## Single Page Applications vs Multi Page Applications

Single Page applications are asynchronous. SPAs do not require page reloading during use. SPA requests the markup and data independly and renders pages straight in the browser.

Multi Page applications are synchronous. Every change sends a request to the server, rendering a new page everytime. 

***

## Functional Programming

Functional programming is the process of building software by composing pure functions, avoiding shared state, mutable data, and side effects. A pure function is a function given the same inputs, always returns the same output and has no side-effects.

***

## Client-Server Model

A client is a computing device or software (phone, browser, etc.) that accesses a service made available by a server.

A server is a computer program or device that provides functionality for other programs or devices, called clients. 

Generally, a client communicates to a server through HTTP requests. If a client needs to call an API, it would call the server, then the server would call the API and send the data back to the client.

***