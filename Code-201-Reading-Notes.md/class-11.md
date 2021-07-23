# IMAGES
![](https://d2h0cx97tjks2p.cloudfront.net/blogs/wp-content/uploads/sites/2/2020/07/html-images-df.jpg)
Controlling the size and alignment of your images using CSS keeps rules that affect the presentation of your page in the CSS and out of the HTML markup.
## Controlling sizes of images in CSS
**You can control the size of an image using the width and height properties in CSS, just like you can for any other box. Specifying image sizes helps pages to load more smoothly because the HTML and CSS code will often load before the images, and telling the browser how much space to leave for an image allows it to render the rest of the page without waiting for the image to download. You might think that your site is likely to have images of all different sizes, but a lot of sites use the same sized image across many of their pages.**         
First you need to determine the sizes of images that will be used commonly throughout the site, then give each size a name.
For example:       
small             
medium                
large                  
```
Where the <img> elements appear in the HTML, rather than using width and height attributes you can use these names as values for the class attribute. In the CSS, you add selectors for each of the class names, then use the CSS width and height properties to control the image dimensions.
```
## AligNi ng images Using CSS
```
In the last chapter, you saw how the float property can be used to move an element to the left or the right of its containing block, allowing text to flow around it. Rather than using the <img> element's align attribute, web page authors are increasingly using the float property to align images. There are two ways that this is commonly achieved:
```
1. The float property is added to the class that was created to represent the size of the image (such as the small class in our example).
2. New classes are created with names such as align-left or align-right to align the images to the left or right of the page. These class names are used in addition to classes that indicate the size of the image. In this example you can see the align-left and align-right classes used to align the image. It is also common to add a margin to the image to ensure that the text does not touch their edges.
## Centering images Using CSS
By default, images are inline elements. This means that they flow within the surrounding text. In order to center an image, it should be turned into a blocklevel element using the display property with a value of block. Once it has been made into a block-level element, there are two common ways in which you can horizontally center an image: 
1. On the containing element,
you can use the text-align
property with a value of center.
2. On the image itself, you can
use the use the margin property
and set the values of the left and
right margins to auto.
You can specify class names
that allow any element to be
centered, in the same way that
you can for the dimensions or
alignment of images
![](https://www.mediacollege.com/internet/html/images/image-tag1.gif)
## Background Images(background-image)
The background-image property allows you to place an image behind any HTML element. This could be the entire page or just part of the page. By default, a background image will repeat to fill the entire box. The path to the image follows the letters url, and it is put inside parentheses and quotes.
```
In the first example, you can
see a background image being
applied to an entire page
(because the CSS selector
applies to the <body> element).
In the second example, the
background image just applies to
a paragraph.
If you search online, you will
find lots of resources that offer
background textures that you
can use on your pages.
```
## Repeating Images *background-repeat background-attachment*
The background-repeat
property can have four values:
repeat           
The background image is                    
repeated both horizontally and
vertically (the default way it
is shown if the backgroundrepeat
property isn't used).                  
repeat-x                
The image is repeated
horizontally only (as shown in 
the first example on the left).                      
repeat-y                      
The image is repeated vertically
only.                      
no-repeat                 
The image is only shown once.
The background-attachment
property specifies whether a
background image should stay in
one position or move as the user
scrolls up and down the page. It
can have one of two values:                    
fixed                  
The background image stays in
the same position on the page.
scroll                    
The background image moves
up and down as the user scrolls up and down the page.
## shorthand background
The background property acts
like a shorthand for all of the
other background properties
you have just seen, and also the
background-color property.
The properties must be specified
in the following order, but you
can miss any value if you do not
want to specify it.                           
1: background-color      
2: background-image                 
3: background-repeat                    
4: background-attachment              
5: background-position                       
CSS3 will also support the use
of multiple background images
by repeating the background
shorthand. Because few
browsers supported this
property at the time of writing, it
was not commonly used.                  
div {     
background:                   
url(example-1.jpg)          
top left no-repeat,                              
url(example-2.jpg)                  
bottom left no-repeat,                 
url(example-3.jpg)                 
centre top repeat-x;}             
# Practical Information
To wrap up the book we are going to look
at some practical information that will
help you launch a successful site.
## A tabbed info-box
**The first example we'll look at is a classic tabbed info box — a very common feature used when you want to pack a lot of information into a small area. This includes information-heavy apps like strategy/war games, mobile versions of websites where the screen is narrow and space is limited, and compact information boxes where you might want to make lots of information available without having it fill the whole UI. Our simple example will look like this once we are finished:**
![](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Practical_positioning_examples/tabbed-info-box.png)


You might be thinking "why not just create the separate tabs as separate webpages, and just have the tabs clicking through to the separate pages to create the effect?" This code would be simpler, yes, but then each separate "page" view would actually be a newly-loaded webpage, which would make it harder to save information across views, and integrate this feature into a larger UI design. In addition, so-called "single page apps" are becoming very popular — especially for mobile web UIs — because having everything served as a single file cuts down on the number of HTTP requests required to view all the content, thereby improving performance.
```
So here we've got a <section> element with a class of info-box, which contains a <ul> and a <div>. The unordered list contains three list items with links inside, which will become the actual tabs to click on for displaying our content panels. The div contains three <article> elements, which will make up the content panels that correspond to each tab. Each panel contains some sample content.

The idea here is that we will style the tabs to look like a standard horizontal navigation menu, and style the panels to sit on top of one another using absolute positioning. We'll also give you a bit of JavaScript to include on your page to display the corresponding panel when a tab is pressed, and style the tab itself. You won't need to understand the JavaScript itself at this stage, but you should think about learning some basic JavaScript as soon as possible — the more complex your UI features become, the more likely it is that you'll need some JavaScript to implement your desired functionality.
```

![](https://slidetodoc.com/presentation_image/a3433d6a2ec782488b9e40e18d0c9ea6/image-14.jpg)