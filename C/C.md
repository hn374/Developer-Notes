# C

C is a low level programming language.

*** 

## Variable Declarations

In C, variable declaration is required. If you forget to declare a variable, the compiler will send a warning.

***

## Constants

We use #define to create constants.

***

## Functions

All C code must be nested inside of functions and functions cannot be nested within eachother. A C program's architecture is pretty straightforward, it is a list of functions definitions called one after another. 

Functions also must be declared above the location where you intend to use it.

***

## Types

There are only four types in C: int, char, float and double.

C does not have a boolean, so it treats 0 as false and all other types as true. 

*** 

## Arrays

An array in C cannot grow or shrink, its size is fixed at the time of creation.

***

## Strings

Strings in C are represented by arrays of characters. The end of the string is marked with a special character, the null character which is just a character of 0.

***

## Headers

We create header files that contains each function prototype written just once, so we can import and use them in other files. We use #include to import.

*** 

## Pointers

Pointers in C language is a variable that stores/points the address of another variable. A pointer in C is used to allocate memory dynamically at run time. The & is used to get the address of the variable and the * is used to get the value of the variable that the pointer is pointing to.

Pointers are used in three different ways:

1. To create dynamic data structures.
2. To pass and handle variable parameters passed to functions.
3. To access information stored in arrays.

It is a good practice to assign a null value to a pointer variable in case you do not have an exact address to be assigned.

***

## Dynamic Memory Allocation

So far all of our programs have allocated variables statically by defining them in our program. This allocates them in the stack.

If we want to reallocate variables based on user input or other dynamic inputs, we would use dynamic memory allocation.

As opposed to the stack where it is automatically reclaimed, dynamic allocations must be tracked and free()'d when they are no longer needed. With every allocation, be sure to plan how that memory will get freed. Otherwise, you will have a memory leak.

***

## Sizeof()

Reports the size of a type in bytes.

***

## Malloc()

Returns a pointer to a memory block of at least size bytes aligned to 8 byte boundary.

***

## Free()

Returns the block pointed at by p to pool of available memory. P must come from a previous call to malloc() or realloc().

***

## Realloc()

Changes size of block p and returns pointer to new block.

***

## Calloc()

Allocates memory for N elements of size K, or returns null if it cannot allocate anything.

***