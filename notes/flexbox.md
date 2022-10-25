# Flexbox
To summarize:

Flexbox is one of many “layout modes” in CSS, like Flow layout or Positioned layout.
Flexbox is most handy when we have a set of things, and we want to control their distribution along a primary axis, either horizontally or vertically.
Flexbox is still relevant, even with CSS Grid reaching wide browser support. It's a different tool for a different job: CSS Grid works best for two-dimensional layouts, while Flexbox offers more flexibility for working with a single dimension.
When we apply display: flex to an element, we toggle the "Flexbox" layout algorithm for the element's children. The parent element will still use Flow layout.

<br>
Flexbox example: <br>

```
.wrapper {
  display: flex;
  flex-direction: row; /* row, column */
  justify-content: flex-start; /* flex-end, space-between… */
  align-items: stretch; /* flex-end, baseline… */
}
```
![](screenshot/Screenshot%20from%202022-10-25%2020-57-08.png)
