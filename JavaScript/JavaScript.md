# JavaScript

JavaScript is a multi-paradigm, dynamic language with types and operators, standard built-in objects, and methods. JavaScript supports object-oriented programming with object prototypes, instead of classes. JavaScript also supports functional programming - because they are objects, functions may be stored in variables and passed around like any other object.

***

## Types

* Number
* String
* Boolean
* Function
* Object
    - Function
    - Array
    - Date
    - RegExp
* Undefined - Describes an unintialized variable.
* Null - Indicates a deliberate non-value.

***

## Closures

A closure is an inner function that has access to the outer function's variables. It has access to its own scope, it has access to the outer functions variables, and it has access to the global variables. It is the combination of a function and the scope object in which it was created. It lets you save state, and as such, they can often be used in the place of objects. 

It is basically a function inside of another function. 

```javascript

function makeAdder(a) {
    return function(a) {
        return a + b;
    };
}

var add5 = makeAdder(5);
var add20 = makeAdder(20);
add5(6); // Returns 11
add20(7); // Returns 27

```

When **makeAdder()** is called, a scope object is created with one property: **a**, which is the argument passed to the **makeAdder()** function. **makeAdder()** then returns a newly created function. Normally, JavaScript's garbage collector would clean up the scope object created for **makeAdder()** at this point, but the returned function maintains a reference back to that scope object. As a result, the scope object will not be garbage collected until there are no more references to the function object that **makeAdder()** returned. 

***

## Variables

New variables are declared using one of three keywords: **let**, **const**, or **var**.

**let** allows you to declare block-level variables. The declared variable is available from the block it is enclosed in. 

**const** allows you to declare variables whose values are never intended to change. The variable is available from the block it is declared in. 

**var** is the most common declarative keyword. A variable declared with the var keyword is available from the function it is declared in.

If you declare a variable without assigning any value to it, its type is undefined.

***

## Variable Scope

The context in which the variable exists. The scope specifies from where you can access a variable and whether you have access to the variable in that context.

An important difference between JavaScript and other languages like Java is that in JavaScript, blocks do not have scope; only functions have a scope. So if a variable is defined using var in a compound statement like an if control structure, it will be visible to the entire function. 

**let** and **const** declarations allow you to create block-scoped variables.

***

## Variable Hoisting

All variable declarations are lifted and declared to the top of the function or the top of the global context. 

Only variable declarations are hoisted to the top, not variable initialization or assignments. 

Function declarations take precedence over variable declarations.

***

## Callback Functions

A callback function is a function that is passed to another function. 

The callback is executed at some point inside the containing function's body just as if the callback were defined in the containing function. This means the callback is a closure. 

Callbacks are a way to make sure certain code doesn't execute until other code has already finished execution.

***

## Objects

JavaScript objects can be thought of as simple collections of name-value pairs. They are similar to dictionaries in Python.

***

## JavaScript Object Oriented

JavaScript is a prototype-based language that contains no class statement like in Java. Instead, JavaScript uses functions as classes. 

```javascript
    function Person(first, last) {
        return {
            this.first: first,
            this.last: last,
            this.fullName: function () {
                return this.first + ' ' + this.last;
            },
            this.fullNameReversed: function () {
                return this.last + ', ' + this.first;
            }
        };
    }

    var person = new Person('Zion', 'Williamson');
```

Note on the **this** keyword used inside the function, **this** refers to the current object. If you called it using dot notation or bracket notation on an object, that object becomes **this**. Else, **this** refers to the global object. 

**new** is strongly related to **this**. It creates a brand new empty object, and then calls the function specified, with **this** set to that new object. Functions that are designed to be called by **new** are called constructor functions.

There is a better way we can write this object without having to create two brand new function objects within it every time. It would be better if this code was shared.

```javascript

function Person(first, last) {
    this.first = first;
    this.last = last;
}

Person.prototype.fullName = function() {
    return this.first + '' + this.last;
};

Person.prototype.fullNameReversed = function() {
    return this.last + ', ' + this.first;
};

```

**Person.prototype** is an object shared by all instances of **Person**. It forms part of a lookup chain called the prototype chain: anytime you attempt to access a property of **Person** that isn't set, JavaScript will check **Person.prototype** to see if that property exists there instead. As a result, anything assigned to **Person.prototype** becomes available to all instances of that constructor via the **this** object. 

JavaScript lets you modify something's prototype at any time in your program, which means you can add extra methods to existing objects at runtime. 

***

## Inner Functions

JavaScript function declarations are allowed inside other functions. An important detail of nested functions in JavaScript is that they can access variables in their parent function's scope. If a called function relies on one or two other functions that are not useful to any other part of your code, you an nest those utility functions inside it. This keeps the number of functios that are in the global scope down, which is always a good thing. 

***