# Useful Web Developer Tools, tricks and tips in creating a web.

## Images tools, tips and tricks

### Lazy Sizes
[Lazy Size](https://github.com/aFarkas/lazysizes)     
[Lazy Size Web](https://afarkas.github.io/lazysizes/index.html)   
     
lazySizes is the ultimate and lightweight lazyLoader which lazy loads images (including responsive images (picture/srcset)), iframes and scripts. It is written in VanillaJS and with high performance in mind.( FUTURE PROOF )

Preferably use the [CSS API](https://github.com/aFarkas/lazysizes#css-api) trick

#### NOT WORKING FOR
1. Slick slider - it has it's own lazy loading stuff, has conflict with other frameworks.

### Show a loading icon until the page is load completely

[Loaded](https://stackoverflow.com/questions/23906956/show-loading-icon-until-the-page-is-load)

### How to stop content jumping when images load?

[Stop image jumping trick](https://itnext.io/how-to-stop-content-jumping-when-images-load-7c915e47f576)     
It's best to combine this trick with lazysizes CSS API + content jumping trick.

### Optimize images

Optimize images for about 60%, just to maintain the quality and reduce the size of an image.

### Useful tools.

1. [GIF Loader](https://loading.io/)

## Scripts, Stylesheet and images.

### Scripts
Add async attribute for script's that has no dependencies.     
Defer attribute for scripts that has dependencies.       
You can now add the script tag at the header portion of the HTML while using the async or defer attribute, adding it at the bottom of the body won't make sense.

### Add crossorigin attribute for scripts, images and stylesheets.
This speeds up the performance of the website.
[Crossorigin](http://gavinballard.com/tiny-tweaks-for-shopify-theme-performance/)     

crossorigin="anonymous"

### Combine CSS File into 1 stylesheet file and JS file into 1 JS file,

Combine CSS file into 1 stylesheet, this lessen up the http requests that slows the load.

### Minify CSS and JS

This lessens the size of the stylesheet and script filed deliver, Use Gzip to achieve a much better compiling result.

## Relnoopener

[Google developer Relnoopener](https://developers.google.com/web/tools/lighthouse/audits/noopener)
When your page links to another page using target="_blank", the new page runs on the same process as your page. If the new page is executing expensive JavaScript, your page's performance may also suffer. 

n top of this, target="_blank" is also a security vulnerability. The new page has access to your window object via window.opener, and it can navigate your page to a different URL using window.opener.location = newURL. 

Add rel="noopener" or rel="noreferrer" to each of the links that Lighthouse has identified in your report. In general, always add one of these attributes when you open an external link in a new window or tab.

<a href="https://examplepetstore.com" target="_blank" rel="noopener">...</a>
