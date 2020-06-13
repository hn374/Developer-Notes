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

The useEffect hook takes in two arguments. The first argument is a function where the side effect occurs. The optional second argument is a dependency array of variables. If one of these variables changes, the function for the side-effect is called.

The useEffect hook lets us opt into React's component life cycle. It can be triggered when the component is first mounted, but also when one of its dependencies are updated.

We can also create custom hooks in React. The convention is that they must be named with the word `use` in the beginning, and the values should be returned in an array.

A custom hook can encapsulate non-trivial implementation details that should be kept away from a component; can be used in more than one React component, and can even be used an as open source library.

A React fragment wraps other elements into a single top-level element without adding to the rendered output. If you prefer to omit the `<div>` or `<span>` tag, you can replace it with a fragment.

React has a children prop that can be used to get the values from insde the opening and closing tags of the component.

You can create a ref object with React's useRef hook. The ref object is a persistent value which stays intact over the lifetime of a React component. It comes with a property called `current`, which can be changed.

We can use JavaScript's ternary operator to do conditional rendering in JSX. The simplest example of conditional rendering is a boolean flag state that's toggled with a button.

For more advanced state management, you need to use React's `useReducer` hook. The hook receives a reducer function and an initial state as arguments and returns an array with two items. The first item is the current state, the second item is the state updater (dispatch) function.

A reducer function always receives state and action, and based on these two arguments, the reducer returns a new state.

In a reducer function, we return a new state object which contains all the key/value pairs from the current state object (via JavaScript's spread operator) and the new overwriting properties.