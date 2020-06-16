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