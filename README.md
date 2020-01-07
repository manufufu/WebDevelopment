# Useful Web Developer Tools in creating a web.

## lazySizes
[Lazy Size](https://github.com/aFarkas/lazysizes)     
[Lazy Size Web](https://afarkas.github.io/lazysizes/index.html)   
     
lazySizes is the ultimate and lightweight lazyLoader which lazy loads images (including responsive images (picture/srcset)), iframes and scripts. It is written in VanillaJS and with high performance in mind.

When lazy loading a slider, you need to lazyload the image first; and then apply the slick slider using settimeout function or apply the gif loading as a replacement

###### Example

```
  setTimeout(function(){
  $('.slider-desk').slick({
    lazyLoad: 'ondemand',
    infinite: true,
    slidesToShow: 1,
    slidesToScroll: 1,
    arrows: false
  });
 }, 1000);
```

## Show a loading icon until the page is load completely

[Loaded](https://stackoverflow.com/questions/23906956/show-loading-icon-until-the-page-is-load)

## Useful tools.

1. [GIF Loader](https://loading.io/)
