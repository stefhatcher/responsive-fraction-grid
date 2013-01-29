simple-responsive-grid-scss
===========================

Use the minified, default [stylesheets/screen.css](https://raw.github.com/stefhatcher/simple-responsive-grid-scss/master/stylesheets/screen.css) or run [SASS + COMPASS](http://thesassway.com/beginner/getting-started-with-sass-and-compass) and configure the variable options in:
```shell
// sass/screen.scss

$wrapper-class: "wrapper"; // full width wrapper
$row-class: "row";         // content within a wrapper (or not). like a row
$column-class: "col";      // column class prefix

$row-width: 980px;         // max content width
$gutter: 20px;             // gutter between columns

$num-columns: 8;           // number of max columns 

$big-break: 1280px;        // responsive breaking points
$medium-break: 800px;      // most tablets in portrait, iphone5 landscape
$small-break: 480px;       // most mobiles in portrait, iphone3-4S in landscape
```


## Basic usage:
```shell
<!-- default row class is "row" -->
<!-- default column class is "col-#-#" -> col-1-2 -> 1 / 2, or 50% -->
<!-- default max number of columns is 8 -->

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
