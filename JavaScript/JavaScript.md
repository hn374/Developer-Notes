# JavaScript

***

## Closures

A closure is an inner function that has access to the outer function's variables. It has access to its own scope, it has access to the outer functions variables, and it has access to the global variables. 

It is basically a function inside of another function. 

***

## Variable Scope

The context in which the variable exists. The scope specifies from where you can access a variable and whether you have access to the variable in that context.

Variables have either a local scope or a global scope. 

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