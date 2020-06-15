# Road To Redux

Single Page Applications have to keep state consistent without making any more requests to the back-end.

They are called single page applications because the application is only served once on the back-end as a single page and then operate through the front-end. SPAs only interact with the back-end to pull or push new data from or to it. Thus, the only thing that changes is the state inside the application.

## Local State Management

Entity state is data retrieved from the back-end.

View state does not need to be stored in the back-end. It is used when opening up a modal or switch a box from preview to edit mode.

The container and presentational component pattern is a widely used pattern. The container component deals with how things work and the presentational component deals with how things look. Container components are the ideal candidates to manage state while the presenter components often display it and act on callback functions.

Sharing state vertically and horizontally are a common issue in state management. You can lift the state up to keep your local state architecture maintainable. 