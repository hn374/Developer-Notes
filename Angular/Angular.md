# Angular

### Components

A component is a class that serves as the basic building block for Angular applications. It consists of three parts, a TypeScript file, an HTML template, and CSS styles. There are a few ways to serve data from parent to child components and vice versa.

***

### Property Binding

Binding is a way to connect data from the TypeScript code to the HTML. We can use [] to connect a variable from the TS file to an HTML element.

***

### Interpolation

We can also interpolate values from the TypeScript file using handlebars syntax.

 ```html
 <h1>{{ appName }}</h1>
 ```

***

### Directives

Directives allow you to extend HTML elements with custom attributes

#### ngIf

Renders some HTML if a condition is true.

#### ngFor

Repeats elements by looping over an array of data.

#### ngClass

Applies CSS classes conditionally.

#### ngStyle 

Applies styles conditionally.

***

### Services

Services allow us to have code that can be used everywhere on the page. It can be used for data connection that needs to be shared across components. We can access methods and properties across other components in the entire project.

***

### Modules

***

### Lifecycle Hooks

Components have a lifecycle. They are created, things change, and then they're destroyed. You can hook into these lifecycle events and perform any needed logic. 

#### Constructor()

Class instantiation.

#### ngOnInit()

Use this hook to perform any logic needed right away, like fetching data with HTTP calls, property definitions, and form setup.

#### ngAfterViewInit()

Child views loaded.

#### ngDoCheck()

Happens on each change detection check.

#### ngOnDestroy()

Teardown.

***