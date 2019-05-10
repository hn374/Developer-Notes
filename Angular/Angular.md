# Angular

### Components

A component is a class that serves as the basic building block for Angular applications. It consists of three parts, a TypeScript file, an HTML template, and CSS styles. There are a few ways to serve data from parent to child components and vice versa.

### Property Binding

Binding is a way to connect data from the TypeScript code to the HTML. We can use [] to connect a variable from the TS file to an HTML element.

### Interpolation

We can also interpolate values from the TypeScript file using handlebars syntax.

 ```html
 	<h1>{{ appName }}</h1>
 ```

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