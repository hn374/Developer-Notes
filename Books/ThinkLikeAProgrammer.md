# Think Like A Programmer

## Introduction

Learning programming syntax, reading programs, memorizing elements of an API, these are mostly analytical left brain activities.

Writing an original program using previously learned tools and skills is a creative right brain activity.

A great cook understands ingredients, preparation methods, and cooking methods and knows how they can be combined to make great meals. All a cook needs to produce a tasy meal is a fully stocked ktichen.

In the same way, a great programmer understands language syntax, application frameworks, algorithms, and software engineering principles and knows how they can be combined to make great programs.

In general, current programming education doesn't offer much guidance in the area of problem solving.

You can learn problem solving in a systematic way. You can learn techniques to organize your thoughts, procedures to discover solutions and strategies to apply to certain classes of problems. By studying these approaches, you can unlock your creativity.

## Chapter 1

Problems include constraints, unbreakable rules about the problem or the way in which the problem must be solved.

For programmers, we can define problem solving as writing an original program that performs a particular set of tasks and meets all stated constraints.

Expert problem solvers are quick to recognize an analogy, an exploitable similarity between a solved problem and an unsolved problem. If we recognize that a feature of problem A is analogous to a feature of problem B and we have already solved problem B, we have a valuable insight into solving problem A.

If you are unaware of all possible actions you could take, you may be unable to solve the problem.

Restating the problem in a more formal manner is a great technique for gaining insight into a problem.

Many programmers seek out other programmers to discuss a problem, not justb ecause other programmers may have the answer but also because articulating the problem out loud often triggers new and useful thoughts. Restating a problem is like having that discussion with another programmer, except that you are playing both parts.

The broader lesson is that thinking about the problem may be as productive, or in some cases more productive than thinking about the solution.

Our inability to plan a complete solution does not prevent us from making strategies or employing techniques to systematically solve the puzzle.

In solving programming problems, we are sometimes faced with situations where we can't see a clear path to code the solution, but we must never allow this to be an excuse to forgo planning and systematic approaches.

It's better to develop a strategy than to attack the problem through trial and error.

Sometimes problems are divisible in ways that are not immediately obvious.

While constraints are often what make a problem difficult to begin with, they may also simplify our thinking about the solution because they eliminate choices.

There is a strategy called the Most Constrained Variable. It means that in a problem where you are trying to assign different values to different variables to meet constraints, you should start with the variable that has the most constraints, or the variable that has the lowest number of possible values.

If one part of the problem is heavily constrained, that's a great place to start because you can make progress without worrying that you are spending time on work that will later be undone.

If we discover an analogy early enough, we can avoid most of the work of the problem by translating our solution from the first problem rather than creating a new solution.

You should always have a plan, rather than engaging in directionless activity.

Without a plan, you have only one goal: solve the whole problem. Until you solved the problem, you won't feel you have accomplished anything. If instead, you create a plan with a series of minor goals, even if some seem tangential to the main proble, you will make measurable progress toward a solution and feel that your time has been spent usefully. 

A common theme in problem solving is making useful progress to build confidence that you will ultimately complete the task. By starting with what you know, you build confidence and momentum toward the goal.

If we think of programming skills as tools and a programming problem as a home repair project, you should try to make the repair using the tools already in your garage before heading to the hardware store.

When faced with a problem you are unable to solve, you reduce the scope of the problem, by either adding or removing constraints, to rpoduce a problem that you do know how to solve.

Although recognizing analogies is the most important way you will improve your speed and skill at problem solving, it is also the most difficult skill to develop. The reason it is so difficult at first is that you can't look for analogies until you have a storehouse of previous solutions to reference.

Sometimes the best way to make progress is to try things and observe the results.

## Chapter 2

The primary goal in problem solving is to find a program that solves the stated problem and meets all constraints.

The secondary goal is to find that program in the minimal amount of time.

Use the technique of breaking up the problem into components, writing code to solve those components individually, and then using the knowledge gained from writing the programs or even directly using lines of code from the programs, solve the original problem.

## Chapter 3

Refactoring means improving working code, not changing what it does but how it does it.

A long journey is not a waste of time if you learned something from it that you wouldn't have learned by going the short way.

An array is just a tool. As with any tool, an important part of learning how to use an array is learning when to use it and when not to use it.

Performance tuning is the systematic analysis and improvement of a program's efficiency in time and space. Performance tuning a program is a lot like performance tuning a race car: an exacting job, where small adjustments can have large effects and expert knowledge of how mechanisms work under the hood is required.

Random access means that we can access any element in an array or vector at any time.

## Chapter 4

By using pointers, we can make an array with a size determined at runtime, rather than having to choose the size before building our application. This saves us from having to choose between potentially running out of space in the array and making the array as large as could possibly be needed.

In C++, you might explicitly create your own stack for use in a particular algorithm, but there is always one stack in your program that you will be using and that is the runtime stack.

Every time a function is called, a block of memory is allocated on the top of the runtime stack, which is called the activation record. The main content of the activation record is the storage space for variables. 

A block of memory is a contiguous series of addresses; thus, over the lifetime of a program with many memory allocations and deallocations, we'll end up with lots of gaps between the remaining allocated memory blocks. This problem is known as memory fragmentation.

Modern computer systems have so much memory that it's easy to think of it as an infinite resource, but in fact each program has a limited amount of memory. Programs need to use memory efficiently to avoid overall system slow-down.

A memory leak is a situation in which memory is allocated from the heap but never deallocated and not referenced by any pointer.

Solving by sample case is a technique where you start with a nontrivial sample input for the function or program. Write down all the details of that input along with all the details of the output. Then when you write your code, you'll be writing for the general case while also double-checking how each step transforms your sample to make sure that you reach the desired output state. 

A well-drawn diagram for a problem example is like having a mapped-out route to your destination before starting on a long vacation drive. It's a little bit of extra effort at the start to potentially avoid much more effort and frustration at the end.

In programming, a special case or edge case is a situation in which valid data will cause the normal flow of code to produce erroneous results.

A pointer external to the list that points to the first node in a linked list is known as a head pointer.

## Chapter 5

A class is a blueprint for constructing a particular package of code and data; each variable created according to a class's blueprint is known as an object of that class.

Code outside of a class that creates and uses an object of that class is known as a client of the class.

A class declaration names the class and lists all of the members, or items inside that class.

Each item is either a data member, a variable declared within the class, or a method, which is a function declared within the class.

