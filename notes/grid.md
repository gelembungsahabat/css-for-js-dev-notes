# CSS Grid
At this point in the course, we've become familiar with a lot of layout modes: flow layout, positioned layout, Flexbox, and even some funky ones like multi-column layout and float.

In this module, we'll take a look at the latest and greatest CSS layout mode: Grid layout.

CSS Grid builds on a lot of the ideas and patterns from Flexbox, but with the goal of distributing children across two dimensions instead of one. It's sorta like Flexbox's older cousin.

## Mental Model
In CSS Grid, our element's content box is sliced into rows and columns. The rows/columns don't have to be the same size, but they do have to be consistent. If a column is 250px wide, each cell in that column will share that width.
![](screenshot/Screenshot%20from%202022-10-25%2021-33-05.png)
![](screenshot/Screenshot%20from%202022-10-25%2021-33-58.png)

<br>
CSS Grid doesn't support zig-zag columns like this. Every cell in the same column needs to have the same width. The same is true for rows: every cell in the same row needs to have the same height.

We also can't end a row or column prematurely; If our grid has 2 columns and 3 rows, each column will have 3 cells.