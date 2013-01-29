simple-responsive-grid-scss
===========================

Use the default:
```shell
stylesheets/screen.css
```

Or run [SASS + COMPASS](http://thesassway.com/beginner/getting-started-with-sass-and-compass) and configure the variable options in:
```shell
sass/screen.scss

$wrapper-class: "wrapper"; // full width wrapper
$row-class: "content";     // content within a wrapper (or not). like a row
$column-class: "col-span"; // column class prefix

$row-width: 980px;         // max content width
$gutter: 20px;             // gutter between columns

$num-columns: 8;           // number of max columns 

$big-break: 1280px;        // responsive breaking points
$medium-break: 800px;      // most tablets in portrait, iphone5 landscape
$small-break: 480px;       // most mobiles in portrait, iphone3-4S in landscape
```


## Configure Options:
 - Width
 - Gutter
 - Column number
 - Wrapper, row, and column class names
 - Small, medium, and big break points

## Demo
http://stefhatcher.com/simple-responsive-grid-scss/
