# C Sharp

C# is a general purpose programming language encompassing strong typing, lexically coped, imperative, declarative, functional, generic, object-oriented, and component oriented programming disciplines.

## File Architecture

C Sharp follows an MVC architecture.

## Main Method

The main method is a static method that resides inside a class or a struct. It is the entry point of a C# application and there should only be one main method in a C# program. The main method is the first method that is invoked when a program is started. It has to be declared with a return value or it can return void.

## Using

If you include the word using along with a package at the beginning of a program, you can directly use the package's classes and methods without fully qualifying them. For example, you can call Console.WriteLine instead of System.Console.WriteLine if you called 'using System'.

## Namespaces

Namespaces are used to provide a named space in which your application resides. They provide the C# compiler a context for all the named information in your program. If your application is intended to be used in conjunction with another, namespaces exist to resolve ambiguities a compiler wouldn't otherwise be able to do. A namespace can contain types such as classes, structs, interfaces, enumerations, and delegates. (It can also contain other namespaces.)

## Read Only

Keyword which is used to define a read only field in our applications. The read only field values needs to be initialized either at the declaration or in a constructor of the same class.

We can only use the readonly modifier with the numbers, boolean values, strings or with null references.

## Static

A static modifier can be used with data and functions that do not require an instance of a class to be accessed. It is mostly used when the data and behavior of a class do not depend on object identity. The use of static classes and members improves code efficiency. Static basically means relating to the type itself, rather than an instance of the type. You can access a static member using the type name instead of a reference or a value. 

## Async

Use the async modifier to specify that a method is asynchronous. 

## Async and Await

The await keyword provides a non-blocking way to start a task, then continue execution when that task completes. You start a task and hold on to the Task object that represents the work. You'll await each task before working with its result. 

The composition of an asynchronous operation followed by synchronous work is an asynchronous operation. If any portion of an operation is asynchronous, the entire operation is asynchronous. 

The async modifier signals to the compiler that a method contains an await statement; it contains asynchronous operations. 