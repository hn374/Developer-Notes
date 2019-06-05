# CSS

CSS is a styling language to transform your HTML. 

***

## Media Queries

Media queries are simple filters that can be applied to CSS styles. They make it easier to change styles based on the characteristics of the device.

Media queries enable us to create a responsive experience where specific styles are applied to small screens, large screens, and anywhere in between.

Define breakpoints based on specific devices, products, brand names, or operating systems. 

The general rule of thumb is to design for the smallest mobile device first, then progressively enhance the experience as more screen real estate becomes available. 

We can use `@media` and `@import` to use media queries.

#### min-width 

Rules applied for any browser width greater than the value defined in the query.

#### max-width

Rules applied for any browser width less than the value defined in the query. 

#### min-height

Rules applied for any browser height greater than the value defined in the query.

#### max-height

Rules applied for any browser height less than the value defined in the query.

#### orientation = portrait

Rules applied for any browser where the height is greater than or equal to the width.

#### orientation = landscape

Rules for any browser where the width is greater than the height.

```CSS
@media (min-width: 700px) {
  .weather-forecast {
    width: 700px;
  }
}
```

*** 

## BEM (Blocks, Elements and Modifiers)

BEM is a type of CSS architecture.

#### Blocks

Standalone entity that is meaningful on its own.

#### Elements

A part of a block that has no standalone meaning and is semantically tied to its block.

#### Modifiers

A flag on a block or element. Use them to change appearance or behavior. 

#### Benefits

Block styles are never dependent on other elements on a page. You will get the ability to transfer blocks from your finished projects to new ones. 

Composing independent blocks in different ways reduces the amount of CSS code that you will have to maintain.

BEM methodology gives your CSS code a solid structure that remains simple and easy to understand.

***

## Floats

Floats allow you to put block-level elements side-by-side instead of on top of each other. Float-based layouts have mostly been replaced with Flexbox in modern websites. 

If we float an element to the left, we're telling the browser to align it to the left side of the page. It also tells surrounding elements that they can flow around the floated element instead of beginning underneath it. 

Floats do not count as part of the flow of the page. The height of our floated elements don't contribute to the vertical position.

Clearing a float is when we tell a block to ignore any floats that appear before it. Instead of flowing around the floated box, a cleared elemnt always appears after any floats. 