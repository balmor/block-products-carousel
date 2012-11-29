Generic HTML/LESS Block Product/Carousel
================

<h2>Version</h2>
version 0.2.0

<h2>Documentation</h2>

<h6>We just add class to html .product-block for display:</h6>
.display-column  -  In Column (set default) <br>
.display-list    -  In List <br>
.display-grid    -  In Grid <br>


<h6>and to run carousel just add class:</h6>
.display-carousel (you must set js)

You can use <a href="http://caroufredsel.dev7studios.com/">carouFredSel</a> or <a href="https://github.com/jsor/jcarousel">jCarousel 0.3</a> carousels

Structure to show pagination, next & prev buttons you must set in javascript!

    <!-- Control -->
    <div class="control-wrap">
        <a class="control carousel-prev" href="#"><span>prev</span></a>
        <a class="control carousel-next" href="#"><span>next</span></a>
    </div>
    <!-- Pagination -->
    <div class="carousel-pagination"></div>

If you want multiple carousels you can add new class to container (.block-product) and add custom styles for example:

    <!-- Control -->
    <div class="product-block display-carousel custom-styles">
    	...
    </div>

<h2>How it works</h2>
You can see how it works <a href="http://generic.balmor.eu/generic-block-carousel/">here</a>.

It also works on IE7+