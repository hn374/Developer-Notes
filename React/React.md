# React

![React Image](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/1200px-React-icon.svg.png)

React is a JavaScript library for building user interfaces that is maintained by Facebook. 

***

## JSX

React components are typically written using JSX. JSX is an extension to the JavaScript language syntax. It provides a way to structure component rendering using syntax familiar to many developers. JavaScript expressions can be used inside JSX with curly brackets.

***

## File Architecture

React doesn't have opinions on how you should put files into folders, so you can choose anyway you want. Some popular approaches for React file structures are grouping by features or routes, and grouping by file type. A good tip is to avoid too much nesting. You should have a maximum of three or four nested folders within a single project.

***

## Components

Component let you split the UI into independent, reusable pieces, and think about each piece in isolation. Each component can only return one element. You need to wrap all your HTML in one containing element, usually a div.

The simplest way to define a component is to write a JavaScript function. This is if the component does not need a state. It is considered a dumb component:

```javascript
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

More commonly, you'll be using an ES6 class to define a component. If a component needs a state, it is considered a smart component and needs to be created like so:

```javascript
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

***

## Props

Properties are passed to a component from the parent component. Components receive props as a single set of immutable values (a JavaScript object). Props should never be modified, only states.

Think of them similar to function parameters.

***

## State

States hold values throughout the component and can be passed to child components through props. Other than that, states are local to the components that own it. States are immutable. To change state, you have to return a new array using this.setState. State changes are asynchronous.

```javascript
class ParentComponent extends React.Component {
  state = { color: 'green' };
  render() {
    return (
      <ChildComponent color={this.state.color} />
    );
  }
}
```

Think of them similar to variables declared within a function.

***

## Virtual DOM

React creates an in-memory data-structure cache, computes the resulting differences, and then updates the browser's displayed DOM efficiently. This allows the programmer to write code as if the entire page is rendered on each change, while the React libraries only render subcomponents that actually change. 

***

## Lifecycle Methods

Lifecycle methods are hooks which allow execution of code at set points during the component's lifetime.

#### shouldComponentUpdate()

Allows the developer to present unnecessary re-rendering of a component by returning false if a render is not required.

#### componentDidMount()

Called once the component has 'mounted' (the component has been created in the user interface, often by associating it with a DOM node). Commonly used to trigger data loading from a remote source via an API.

#### componentWillUnmount()

Called immediately before the component is torn down or 'unmounted.' Commonly used to clear resource demanding dependencies to the component that will not simply be removed with the unmounting of the component.

#### render()

The most important lifecycle method and the only required one in any component. It is usually called every time the component's state is updated, reflecting changes in the user's interface. 

***

## Top-Down or Unidirectional Data Flow

Any state is always owned by some specific component, and any data or UI derived from the state can only affect components below them in the tree. A child component does not know whether props were passed in from a parent component's state, props, or typed by hand. If you imagine a component as a waterfall of props, each component's state is like an additional water source that joins it at an arbitrary point but also flows down. 

***

## Handling Events

Handling events with React elements is very similar to handling events on DOM elements. In React, you use camelCase, rather than lowercase. With JSX, you pass a function as the event handler instead of a string. In React, you also have to call preventDefault explicitly to prevent default behavior. In JavaScript, class methods are not bound by default, so you have to bind them to their classes. If you refer to a method with () after it, you need to bind that method in the constructor. 

***

## Lifting State Up

Lifting state up is for when several components need to reflect the same changing data. The shared state is lifted up to their closest common ancestor. There should be a single source of truth for any data that changes in a React application. 

***

## Composition vs Inheritance

Facebook recommends using composition instead of inheritance to reuse code between components. A more specific component renders a more generic one and configures it with props. 

***

## Bundling

The process of following imported files and merging them into a single file: a "bundle". People do this with Webpack or Browserify. This bundle can then be included on a webpage to load an entire app at once.

## Code Splitting

Creates multiple bundles that can be dynamically loaded at runtime. Code splitting helps your app "lazy-load" just the things that are currently needed by the user, which can dramatically improve the performance of your app. You've avoided loading code that the user may never need, and reduced the amount of code needed during the initial load.

## Higher Order Components

A higher-order component is an advanced technique in React for reusing component logic. They're a pattern that emerges from React's compositional nature. 

A higher-order component is a function that takes a component and returns a new component.

```javascript
const EnhancedComponent = higherOrderComponent(WrappedComponent);
```

Whereas a component transforms props into UI, a higher-order component transforms a component into another component.

Note that a HOC doesn't modify the input component, nor does it use inheritance to copy its behavior. Rather, a HOC composes the original component by wrapping it in a container component. A HOC is a pure function with zero-side effects.

You should not mutate a higher-order component, HOCs should use composition by wrapping the input component in a container component.

***

# React Libraries

## Redux

Redux is a state management solution. It makes it possible to connect every component directly to the entire state and thus eliminates the need to use props or callbacks. Basically, it brings all state to a global level so that any component can access any state. 

The common solution when you need to share data between different components is to lift the state up to the closest shared component and pass down the data to the different components that need it. However, this can be tedious and unscalable. This is the exact problem that Redux fixes. It helps keeping the state you share throughout your app clear and clean by creating a global state that can be accessible anywhere in your application.

## Material UI

Set of components created by Google using their Material Design philosophy. 

## React Router

One of the best React libraries for handling routing. The routes are considered as components. When the app is running, the routes are rendered to the screen. Instead of having to call the server everytime to load a new page, routes are processed and loaded in the client.

## React DnD

A library used to build complex drag and drop interfaces.

## Axios

Axis is a lightweight HTTP client based on the HTTP Service in Angular. It is promised based and we can take advantage of async and await for more readable asynchronous code. This is the library we would use to make API requests. 

***

# Interview Questions

## Why does react need a root element?

React is JavaScript, and it needs an element where it can render a DOM Tree.

## What is the difference between state and props?

State is for storing stuff that is internal to the current component.

Props are for passing down from parent components to child components.

## What is context?

Context is a globally available prop that should only be used on occasions where you need the prop globally. For example, a theme.

## What are prop types and what are the benefits/drawbacks of them?

Prop types is a way for you to know what types a component is expecting.

## What life cycle events are the most common?

`componentWillMount()` and `componentDidUnmount()`.

## Explain how React rendering works.

React listens for DOM updates and rerenders the DOM tree on every change. It uses component diffing to check whether there is a change to the component and only rerenders if there is one.

## What is Redux?

Redux is a popular tool for storing global state in React.

## Explain how Redux works.

You declare a reducer that takes in an action and a state. When you dispatch an action, the state gets updated and React rerenders the DOM with the state change.