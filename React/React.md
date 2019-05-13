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

Component let you split the UI into independent, reusable pieces, and think about each piece in isolation. 

The simplest way to define a component is to write a JavaScript function:

```javascript
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

More commonly, you'll be using an ES6 class to define a component:

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

***

## State

States hold values throughout the component and can be passed to child components through props. States are immutable. To change state, you have to return a new array.

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

***

## Virtual DOM

React creates an in-memory data-structure cache, computes the resulting differences, and then updates the browser's displayed DOM efficiently. This allows the programmer to write code as if the entire page is rendered on each change, while the React libraries only render subcomponents that actually change. 

***

## Lifecycle Methods

Lifecycle methods are hooks which allow execution of code at set points during the component's lifetime.

#### shouldComponentUpdate()

Allows the developer to present unncessary re-rendering of a component by returning false if a render is not required.

#### componentDidMount()

Called once the component has 'mounted' (the component has been created in the user interface, often by associating it with a DOM node). Commonly used to trigger data loading from a remote source via an API.

#### componentWillUnmount()

Called immediately before the component is torn down or 'unmounted.' Commonly used to clear resource demanding dependencies to the component that will not simply be removed with the unmounting of the component.

#### render()

The most important lifecycle method and the only required one in any component. It is usually called every time the component's state is updated, reflecting changes in the user's interface. 

***

## Handling Events

***

## Lifting State Up

***

## Composition vs Inheritance

***