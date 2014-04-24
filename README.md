responsive-fraction-grid
===========================

Use the minified, default [stylesheets/fraction-grid.css](https://raw.github.com/stefhatcher/responsive-fraction-grid/master/stylesheets/fraction-grid.css) or run [SASS + COMPASS](http://thesassway.com/beginner/getting-started-with-sass-and-compass) and configure the variable options in:

```shell
// sass/fraction-grid.scss

$row-class: "row";         // content within a wrapper (or not). like a row
$column-class: "col";      // column class prefix
$block-class: "block";     // block class applied to a row to preserve columns

$row-width: 980px;         // max content width of content within a row
$gutter: 20px;             // gutter between columns. set to 0 for full fraction widths

$num-columns: 12;          // number of max columns

// responsive breaking points
$grid-break: $row-width + ($gutter * 2); // most tablets
$phone-break: 767px;                     // collapses to single column
```


## Basic usage:
```shell
<!-- defaults:
  row class is "row"
  column width class is "col--#-#" -> col--1-2 -> 1 / 2, or 50%
  for full columns, add "col" class too -> "col col--1-2"
  max number of columns is 12
-->

<div class="row">
  <div class="col -width-whole"> 1/1 = 100% </div>
</div> <!-- 100% ! -->

<div class="row">
  <div class="col -width-1-2"> 1/2 = 50% </div>
  <div class="col -width-1-2"> 1/2 = 50% </div>
</div> <!-- 1/2 + 1/2 = 100% ! -->

<div class="row">
  <div class="col -width-1-3"> 1/3 = 33.33333% </div>
  <div class="col -width-1-2"> 2/3 = 66.66667% </div>
</div> <!-- 1/3 + 2/3 = 100% ! -->

<div class="row block">
  <div class="col -width-1-2"> 1/2 = 50% </div>
  <div class="col -width-1-2"> 1/2 = 50% </div>

  <div class="col -width-1-2"> 1/2 = 50% </div>
  <div class="col -width-1-2"> 1/2 = 50% </div>
</div><!-- end row  2x2 block that will not collapse to one column -->

<!-- just make sure the fractions add up per row! -->
```

## Demo
[http://stefhatcher.com/projects/responsive-fraction-grid/](http://stefhatcher.com/projects/responsive-fraction-grid/)

