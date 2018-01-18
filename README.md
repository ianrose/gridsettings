**Not maintained. Use CSS Grid https://developer.mozilla.org/en-US/docs/Web/CSS/grid**

Gridsettings
============

Create either float based grids or flexbox based grids using Sass. **Why create another grid toolkit in Sass?** I wanted to and I couldn't find exactly what I was looking for. Gridsettings uses techniques from many amazing tools and tries to keep usage similar to other systems.

 * Its only dependency is Sass
 * It uses percentage columns within a fixed width or fluid width container
 * It generates all classes based on column number and breakpoints
 * It allows you to customize grid class names
 * It provides the ability of having static width column among fluid, even in a float based grid
 * It has optional default mobile first grid settings

## How to setup

There are three ways you can download Gridsettings.

* [Download the latest release](https://github.com/ianrose/gridsettings/releases/latest)
* Clone the repo: `git clone https://github.com/ianrose/gridsettings.git`
* Install with [Bower](http://bower.io/): `bower install gridsettings --save-dev`

To start using Gridsettings `@import` the `_gridsettings.scss` partial into your Sass project after your CSS reset.

```scss
@import "path/your-reset";

// Your settings for Gridsettings :)
// Grid Type 
$float-grid: false; 
$flexbox-grid: true; 

// Breakpoints
 $screen-xs-min: 480px;
 $screen-sm-min: 768px;
 $screen-md-min: 992px; 
$screen-lg-min: 1230px;  

// Grid attributes
 $grid-gutter: 12px; 
$grid-columns: 12;
 $static-col-width: 300px;
 $static-col-name: static;
 $grid-col-name: col-; 
$grid-xs-bp-name: xs-; 
$grid-sm-bp-name: sm-;
 $grid-md-bp-name: md-; 
$grid-lg-bp-name: lg-; 
$grid-push-name: push-; 
$grid-pull-name: pull-; 
$grid-offset-name: offset-;
 $grid-container-name: container; 
$grid-row-name: row; 
$grid-container-gutter-name: #{$grid-container-name}-gutter;
 $container-sm-width: 750px;
 $container-sm-width: 750px;
 $container-md-width: 970px;
 $container-lg-width: 1200px;

@import "path/gridsettings"; // Here is the _gridsettings.scss partial

@import "path/your-styles";
```

## How to use

The HTML:

```html
<div class="container-gutter">
  <div class="container">
    <!-- Two 6/12 columns -->
    <div class="row"> 
      <div class="col-xs-6"> 
        <div class="content">Content-</div>
      </div>
      <div class="col-xs-6"> 
        <div class="content">Content</div>
      </div>
    </div>
  </div>
</div>
```

## Requirements

Sass, that's it.

## Warning: In Development

Please be aware Gridsettings is still being heavily developed and you will probably come across bugs.

## Thanks and Resources

* [Bootstrap](https://github.com/twbs/bootstrap-sass)
* [Flexbox Grid](https://github.com/kristoferjoseph/flexboxgrid)

## License

[The MIT License (MIT)](https://github.com/ianrose/gridsettings/blob/master/LICENSE)
