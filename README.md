Generic HTML/LESS Block Product/Carousel
================

<h2>Version</h2>
version 0.2.4

<h2>Documentation</h2>

<h6>Require files:</h6>
[blocks-foundation.less](https://github.com/balmor/block-products-carousel/blob/master/less/blocks-foundation.less)
[vars-blocks.less](https://github.com/balmor/block-products-carousel/blob/master/less/vars-blocks.less)

blocks-foundation.less (don't change this file, if you want change style you must add new file like "custom-styles.less")<br>
vars-blocks.less (you can set generic styles)<br>

and generic HTML (we can't change this html, only add class to container "product-block"):
```html
    <!-- Wrapper Product Block -->
    <div class="product-block">
        <!-- Block Title -->
        <h3 class="block-title"><span class="icon"></span>BLOCK TITLE</h3>
        <h5 class="block-subtitle">BLOCK SUB-TITLE</h5>
        <!-- Product Stage -->
        <div class="product-stage">
            <!-- Product Items -->
            <ul class="product-items">
                <li itemtype="http://data-vocabulary.org/Product" itemscope="">
                    <!-- Item -->
                    <div class="product-item">
                        <!-- Number -->
                        <span class="number">1</span>
                        <!-- Product image -->
                        <!-- Product image with link -->
                        <a class="image-link" href="#" title="" ><img src="http://placehold.it/120x80/4C4266/ffffff" width="120" height="80" alt="" itemprop="image" /></a>
                        <!-- Product image without link -->
                        <img class="image" src="http://placehold.it/120x80/4C4266/ffffff" width="120" height="80" alt="" itemprop="image" />
                        <!-- Caption -->
                        <div class="caption"><p>Caption</p></div>
                        <!-- Product detail -->
                        <div class="detail">
                            <!-- Product info -->
                            <div class="info">
                                <!-- Product name -->
                                <h4 class="product-name"><a href="#" itemprop="name">Product name</a></h4>
                                <!-- Product category -->
                                <a class="product-category" href="#" itemprop="category">Product category</a>
                                <!-- Product discription -->
                                <p class="discription" itemprop="description">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
                            </div>
                            <!-- Product rating -->
                            <div class="rating" title="Quality" data-rating="4"></div>
                            <!-- Price Box -->
                            <div class="price-box" itemtype="http://data-vocabulary.org/Offer" itemscope="" itemprop="offerDetails">
                                <meta content="EUR" itemprop="currency">
                                <!-- Special price -->  
                                <p class="old-price">
                                    <span class="price-label">Previous price:</span>
                                    <span class="price">4,39&nbsp;€</span>
                                </p>                                        
                                <!-- Current price -->    
                                <p class="special-price" itemprop="price">
                                    <span class="price-label">Special price:</span>
                                    <span class="price">3,90&nbsp;€</span>
                                </p>
                            </div>
                            <!-- Product buttons -->
                            <div class="product-buttons">
                                <!-- Button add to cart -->
                                <a class="btn add-to-cart" href="#"><span>Add to cart</span></a>
                                <!-- Button add to wishlist -->
                                <a class="btn add-to-wishlist" href="#"><span>Add to wishlist</span></a>
                            </div>
                        </div>
                    </div>
                </li>           
            </ul>
        </div>

        <!-- Bottom text -->
        <div class="bottom-text">
            <a href="#"><span>VIEW MORE</span></a>
        </div>
    </div> 
```

<h5>Block products</h5>
We just add class to html .product-block for display:

.display-column  -  In Column (set default) <br>
.display-list    -  In List <br>
.display-grid    -  In Grid <br>

Example :
```html
    <!-- Wrapper Product Block -->
    <div class="product-block display-list">
        ...
    </div>  
```

<h5>Carousel products</h5>
To run carousel just add class:

.display-carousel (you must set js)

You can use <a href="http://caroufredsel.dev7studios.com/">carouFredSel</a> or <a href="https://github.com/jsor/jcarousel">jCarousel 0.3</a> carousels

If you want multiple carousels you can add new class to container (.block-product) and add custom styles for example:
```html
    <!-- Wrapper Product Block -->
    <div class="product-block display-carousel custom-styles">
        ...
    </div>
```

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