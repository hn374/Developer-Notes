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