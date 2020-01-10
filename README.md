# Useful Web Developer Tools, tricks and tips in creating a web.

## Images tools, tips and tricks

### Lazy Sizes
[Lazy Size](https://github.com/aFarkas/lazysizes)     
[Lazy Size Web](https://afarkas.github.io/lazysizes/index.html)   
     
lazySizes is the ultimate and lightweight lazyLoader which lazy loads images (including responsive images (picture/srcset)), iframes and scripts. It is written in VanillaJS and with high performance in mind.( FUTURE PROOF )

Preferably use the [CSS API](https://github.com/aFarkas/lazysizes#css-api) trick

### Simple text animation

[Animation](https://tobiasahlin.com/moving-letters/#2)

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

## Web developments tricks and tips

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

### Winmerge

WinMerge - For comparing files
[WinMerge](http://winmerge.org/)

Easily compare files or folders to find differences.
Easily merge differences.

Every developer needs to use this!


### Relnoopener

[Google developer Relnoopener](https://developers.google.com/web/tools/lighthouse/audits/noopener)
When your page links to another page using target="_blank", the new page runs on the same process as your page. If the new page is executing expensive JavaScript, your page's performance may also suffer. 

n top of this, target="_blank" is also a security vulnerability. The new page has access to your window object via window.opener, and it can navigate your page to a different URL using window.opener.location = newURL. 

Add rel="noopener" or rel="noreferrer" to each of the links that Lighthouse has identified in your report. In general, always add one of these attributes when you open an external link in a new window or tab.

<a href="https://examplepetstore.com" target="_blank" rel="noopener">...</a>

### Loading fonts.

Avoid using webfonts as necessary.

Use the following format when using a specific font, this ensures that the font will be loaded in any devices. You must download the following format in order to use it. Font-display:swap is necessary.

```
  @font-face {
    font-family:ValueRegular;
    src: url('value-regular.eot');
    src: url('value-regular.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
         url('value-regular.woff2') format('woff2'), Super Modern Browsers */
         url('value-regular.woff') format('woff'), /* Pretty Modern Browsers */
         url('value-regular.ttf')  format('truetype'), /* Safari, Android, iOS */
         url('value-regular#ValueRegular') format('svg'); /* Legacy iOS */
    font-weight: 400;
    font-style: normal;
    font-display: swap;
}
```

### Use Semantics.

Use semantics in creating a web, instead of using div or span, use semantics or accessibility.

### Use keyframes and transform with transition for simple animations 

You can look for animations on [CodePen](https://codepen.io/search/pens?q=hover)
Keyframes animation on [CodePen](https://codepen.io/search/pens?q=keyframe)

# Shopify Theme Development
The goal is to learn Shopify Theme development, there isn't much a course on creating a theme for shopify but I hope you will learn a lot with this.

## Shopify Essentials for creating a theme 
[Skillshare Kurt Elster Course](https://www.skillshare.com/classes/Shopify-Essentials-for-Web-Developers-From-Store-Setup-to-Custom-Themes/1070001866)

## Shopify liquid

Shopify liquid creates a bridge between an HTML file and a data store    

Basically liquid templating language has a value that is on the data store, the example of this is an image 

#### Example.

Shopify liquid templating language for using image is ```{{ 'smirking_gnome.gif' | asset_url | img_tag }}``` and the equivalent of this line of code in HTML is ```<img src="//cdn.shopify.com/s/files/1/0147/8382/t/15/assets/smirking_gnome.gif?v=1384022871" alt="" />```

I will not go in details but there's much more to learn, here's a cheat sheet for shopify templating language.
[Cheat sheet](https://www.shopify.com.ph/partners/shopify-cheat-sheet)

 


