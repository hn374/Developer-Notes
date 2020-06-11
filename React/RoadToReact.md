# Road To React

## Chapter 1: Fundamentals of React

JavaScript allows functional programming and object oriented programming to exist side by side.

You can declare functional components through function declaration or arrow function declaration (const).

An event handler is a function that handles an event that occurs through JSX elements. Always pass functions to these handlers, not the return value of the function.

There is no way to pass information as JavaScript data types up the component tree, since props are naturally only passed downwards. However, we can introduce a callback handler as a function.

A callback function gets introduced, is used elsewhere, but calls back to the place it was introduced.

Always manage the state at a component where every component that's interested in it is one that either manages the state, or a component below the managing component. If a component below needs to update the state, pass a callback handler down to it. If a component needs to use the state, pass it down as props.

A React application and its components start with an initial state. It's rendered for the first time and once a side-effect occurs, like user input or data loading from a remote API, the change is captured in React's state. Once state has been changed, all the components have affected by the modified state are re-rendered.

Hooks initialize only once when the component renders for the first time, after which React tracks them internally with their most recent values.

