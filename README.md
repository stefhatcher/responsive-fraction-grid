responsive-fraction-grid
===========================

Use the minified, default [stylesheets/fraction-grid.css](https://raw.github.com/stefhatcher/responsive-fraction-grid/master/stylesheets/fraction-grid.css) or run [SASS + COMPASS](http://thesassway.com/beginner/getting-started-with-sass-and-compass) and configure the variable options in:
```shell
// sass/fraction-grid.scss

$wrapper-class: "wrapper"; // full width wrapper
$row-class: "row";         // content within a wrapper (or not). like a row
$column-class: "col";      // column class prefix

$row-width: 980px;         // max content wdith of content within a row before responsive land
$gutter: 20px;             // gutter between columns. gutter = 0px for full fraction widths

$num-columns: 8;           // number of max columns 

// responsive breaking points
$big-break: $row-width + $gutter; // most tablets in landscape
$medium-break: 768px;             // most tablets in portrait
$small-break: 568px;              // most mobiles in portrait, iphone3-5 in landscape
                                  // collapses to single column within small-break
```


## Basic usage:
```shell
<!-- default row class is "row" -->
<!-- default column class is "col-#-#" -> col-1-2 -> 1 / 2, or 50% -->
<!-- default max number of columns is 8 -->

<div class="row">
  <div class="col-full"> 1/1 = 100% </div>
</div> <!-- 100% ! -->

<div class="row">
  <div class="col-1-2"> 1/2 = 50% </div>
  <div class="col-1-2"> 1/2 = 50% </div>
</div> <!-- 1/2 + 1/2 = 100% ! -->

<div class="row">
  <div class="col-1-3"> 1/3 = 33.33333% </div>
  <div class="col-1-2"> 2/3 = 66.66667% </div>
</div> <!-- 1/3 + 2/3 = ~100% ! -->

<!-- just make sure the fractions add up per row! -->
```

## Demo
http://stefhatcher.com/simple-responsive-grid-scss/

Big shout-out to [CSS-TRICKS](http://css-tricks.com/dont-overthink-it-grids/)!
