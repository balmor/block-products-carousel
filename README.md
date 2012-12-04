Generic HTML/LESS Block Product/Carousel
================

<h2>Version</h2>
version 0.2.3

<h2>Documentation</h2>

<h6>We just add class to html .product-block for display:</h6>
.display-column  -  In Column (set default) <br>
.display-list    -  In List <br>
.display-grid    -  In Grid <br>


<h6>and to run carousel just add class:</h6>
.display-carousel (you must set js)

You can use <a href="http://caroufredsel.dev7studios.com/">carouFredSel</a> or <a href="https://github.com/jsor/jcarousel">jCarousel 0.3</a> carousels

Structure to show pagination, next & prev buttons you must set in javascript!
```html
    <!-- Control -->
    <div class="control-wrap">
        <a class="control carousel-prev" href="#"><span>prev</span></a>
        <a class="control carousel-next" href="#"><span>next</span></a>
    </div>
    <!-- Pagination -->
    <div class="carousel-pagination"></div>
```
If you want multiple carousels you can add new class to container (.block-product) and add custom styles for example:
```html
    <!-- Wrapper Product Block -->
    <div class="product-block display-carousel custom-styles">
    	...
    </div>
```

and example code javascript to run carousel:

```javascript
    /* ----- carouFredSel default ----- */
    // Create Pagination
    $('.custom-styles .product-stage').after('<div class="carousel-pagination pages"></div>');
    // Create Prev & Next Button
    $('.custom-styles .product-stage').after('<div class="control-wrap"><a class="control carousel-prev" href="#"><span>prev</span></a> <a class="control carousel-next" href="#"><span>next</span></a></div>');

    // Run the carouFredSel
    $(".custom-styles .product-items").carouFredSel({
        circular    : true,
        infinite    : false,
        auto        : true,
        prev        : ".custom-styles .carousel-prev",
        next        : ".custom-styles .carousel-next",             
        pagination  : ".custom-styles .pages"
    });   
```

<h2>How it works</h2>
You can see how it works <a href="http://generic.balmor.eu/block-carousel/">here</a>.

It also works on IE7+

<h2>To do</h2>
Some fixes and complete the generic less