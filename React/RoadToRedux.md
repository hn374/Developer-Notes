# Road To Redux

Single Page Applications have to keep state consistent without making any more requests to the back-end.

They are called single page applications because the application is only served once on the back-end as a single page and then operate through the front-end. SPAs only interact with the back-end to pull or push new data from or to it. Thus, the only thing that changes is the state inside the application.

## Local State Management

Entity state is data retrieved from the back-end.

View state does not need to be stored in the back-end. It is used when opening up a modal or switch a box from preview to edit mode.

The container and presentational component pattern is a widely used pattern. The container component deals with how things work and the presentational component deals with how things look. Container components are the ideal candidates to manage state while the presenter components often display it and act on callback functions.

Sharing state vertically and horizontally are a common issue in state management. You can lift the state up to keep your local state architecture maintainable. 

Updating state is asynchronous, this can cause problems because there is a chance that you could be using stale state.

Always use `this.setState()` with a function when you depend on previous state or props.

Only use `this.setState()` with an object when you don't depend on previous properties. 

The provider pattern takes the clutter away of passing mandatory props that are needed by every component, down your whole component tree.

Contexts give you a way out of this mess. Instead of passing down the props explicitly down each component, you can hide props, that are necessary for each component, in the React context object and pass them down implicitly to each component. When a component needs access to the context object, it can access it.

The provider component can be used anywhere in your component tree, but it makes the most sense to se it at the top of your component hierarchy to make the context accessible to everyone. 

You can use local storage and session storage to store data in your browser. Local storage persists even when you close the tab but session storage only exists while it is open.

Local state does not scale in large applications, implementation wise. Too many components across your application share state.

Redux has actions that encapsulate information about the state update. An action is a JavaScript object. It has a type and an optional payload. Executing an action is called to dispatch in Redux. You can dispatch an action to alter the state in the Redux store.

It has a store to save the state too. The store is a singleton.

Redux also has reducers, which pick up information from actions and reduce it to a new state that is saved in the store. A reducer is a pure function. A reducer has two inputs: state and action. The state is always the whole state object from the Redux store. The action is the dispatched action with a type and an optional payload.

When state in the store is changed, a view can act on this by subscribing to the store.

`View -> Action -> Reducer -> Store -> View`

## Advanced Actions

Keeping the payload in the action to a minimum is a best practice in Redux. If you need to add anything, add it in the reducer.

Action creators encapsulate the action with its action type and optional payload in a reusable function. They give you the flexibility to pass in any payload.

## Advanced Reducers

Before you dispatch your first action, the Redux store will initialize by running through all reducers once. 

Your initial state for the createStore() function should be an object that represents the state object.

Nested data structures are fine in Redux, but you want to avoid deeply nested data structures. 

Redux gives you a helper to combine multiple reducers into one root reducer: `combineReducers()`. This function takes an object as an argument that has a state as property name and a reducer as a value.

The root reducer can be used to initialize the Redux store instead of a single reducer.

Scaling reducers horizontally can be done in the following ways: A reducer can care about the different action types and a reducer can be split up into multiple reducers yet be combined as one root reducer for the store initialization. 

You can use nested reducers to introduce vertically clear levels of substate. 

## Redux In React

There is a library called `react-redux` that allows you to wire up Redux with React. It gives you a provider component that should be at the root of your application. The provider component takes the store that you created with `createStore()` as an input.

After you've done this, every child component in the whole component tree has implicit access to the store.

You can use a higher order component that is called connect from the `react-redux` library. It makes the Redux store functionality dispatch and the state from the store itself available to the enhanced component.

`mapStateToProps` is a function that can be passed to the connect HOC. If passed, the input component of the HOC will subscribe to updates from the Redux store. Every time the store subscription notices an update, the `mapStateToProps` function will run. The function takes the global state object and optionally a props from the parent component. The function returns an object that is derived from the global state.

`mapDispatchToProps` is a function or object that can be passed down to the connect HOC. This gives access to the dispatch method of the store. It makes it possible to dispatch actions but passes down only plain functions that wire up the dispatching in a higher order function. 

`View -> (mapDispatchToProps) -> Action -> Reducer(s) -> Store -> (mapStateToProps) -> View`

## Middleware In Redux

In Redux, you can use a middleware. Every dispatched action in Redux flows through this middleware. You can opt in a specific feature in between dispatching an action and the moment it reaches the reducer. 

The `createStore` function takes an enhancer as a third argument. The Redux library comes with one of these enhancers, `applyMiddleware()`. 

## Immutable State

Redux embraces an immutable state. Your reducers will always return a new state object. You will never mutate the incoming state. In order to keep your data structures immutable, you have to use `array.map()` and `array.concat(item)` for arrays or `Object.assign()` for objects.

## Normalizing State

The further you have to reach into a deeply nested data structure, the more you have to be careful to keep your data structure immutable.

You should use a library called `normalizr`. The library uses scheme definitions to transform deeply nested data structures into dictionaries that have entities and a corresponding list of ids. 

Normalizing your state has two benefits. It keeps your state flat and thus easier to manage with immutable data structures. In addition, it groups entities to single sources of truth without any duplications. 

When you normalize your state, you will automatically get groupings of entities that could lead to their own reducers managing them.

## Selectors

Selectors are used to retrieve derived properties from your state. 

A selector is a function that takes the state as an argument and returns are a substate or derived properties of it. 

Selectors are not mandatory in Redux, but they can be used to improve developer experience in a Redux architecture.

## Asynchronous Redux

`Redux-Thunk` creates a middleware for your action creators. In the middleware, you are enabled to dispatch asynchronous actions. You can also dispatch functions from `Redux-Thunk`. 

The dispatch method of the Redux store when using Redux Thunk will differentiate between passed objects and functions. A passed function is called a thunk. You can dispatch as many actions synchronously and asynchronously as you want in a thunk. 

Thunks work great in combination with promises. You can return a promise from your thunk.

## Redux Naming Conventions

Action Creators: doSomething

Reducers: applySomething

Selectors: getSomething

Sagas: watchSomething, handleSomething

## The Relationship Between Actions and Reducers

Redux can be seen as the event bus of your application.

You can send events (actions) with a paylaod and an identifier (action types) into the bus and it will pass a potential consumer (reducers). This is known as the event pattern that Redux embraces.

## Technical Folder Organization

The technical separation of concerns is used in smaller applications. The files are separated by their technical aspects. 

This approach does not scale well.

## Feature Folder Organization

You have a greater flexibility in grouping the features, because you can always split up bigger features to smaller ones and thus keep the folders lightweight.

Teams can work on separate feature folders and don't run into conflicts.

This approach does scale well.

## Testing

There are unit tests, integration tests and end-to-end tests.

Input Pattern: 
-Actions creators can have an optional input that becomes their optional payload.
-Selectors can have an optional input that supports them to select the substate.
-Reducers will always receive a previous state and action.

Output Pattern:
-Action creators will always return an object with a type and an optional payload.
-Selectors will always return a substate of the state.
-Reducers will always return a new state.

Test Pattern:
-When invoking an action creator, the correct return object should be expected.
-When invoking a selector, the correct substate should be expected.
-When invoking a reducer, the correct new state should be expected.

## Error Handling

An error in an application can be represented as a state.

When the view layer notices an error in the state, it could use conditional rendering to show an error message instead of the assumed result.

## Redux and Local State

In general, the usage of Redux state should be kept to a minimum. A good rule of thumb is to keep the state close to your component with local state but evaluate later whether another party is interested in the state.

If lifting state doesn't solve the problem because the state is shared across an application, you should consider using Redux for it.

## Connected Components Revisited

Connect has two more optional arguments.

`mergeProps()` basically gives you an intermediate layer to mix up state props and dispatch props before they reach the wrapped component.

The fourth argument is called `options`. It is an object to configure the connect higher order component. 