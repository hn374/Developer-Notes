# Angular

![Angular Image](https://blog.ninja-squad.com/assets/images/angular.png)

Angular is a TypeScript-based application framework led by the Angular Team at Google. Everything is more opinionated in Angular but it has a lot features "out of the box".

## File Architecture

Angular follows an MVC architecture.

***

## MVC

MVC stands for Model, View, and Controller. 

The Model would be anything that has to do with business logic, including manipulating data or accessing databases. For Angular, the model would be the services.

The View is anything that is displayed to the user. For Angular, this would be the HTML and the CSS/SCSS files.

The Controller communicates between the model and the view. For Angular, this would be the component TypeScript files. 

***

## Components

A component is a class that serves as the basic building block for Angular applications. It consists of three parts, a TypeScript file, an HTML template, and CSS styles. There are a few ways to serve data from parent to child components and vice versa.

***

## Property Binding

Binding is a way to connect data from the TypeScript code to the HTML. We can use [] to connect a variable from the TS file to an HTML element.

***

## @Input()

We can use @Input() to pass data from a parent component to a child component through an HTML attribute.

```javascript
export class ChildComponent {
  @Input() color;
}
```

This allows us to pass data into the component:

```html
<child-component color="blue"></child-component>
```

***

## @Output()



***

## Interpolation

We can also interpolate values from the TypeScript file using handlebars syntax.

 ```html
 <h1>{{ appName }}</h1>
 ```

***

## Directives

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

## Services

Services allow us to have code that can be used everywhere on the page. It can be used for data connection that needs to be shared across components. We can access methods and properties across other components in the entire project.

***

## Modules

A place where you can group the components, directives, pipes and services that are related to the application.

***

## Lifecycle Hooks

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

## Reactive Forms

Reactive forms provide a model-driven approach to handling form inputs.

#### Form Groups

A form group tracks the form state of a group of form control instances. 

#### Form Controls

Form Controls are the basic building blocks when using Reactive forms. 

***