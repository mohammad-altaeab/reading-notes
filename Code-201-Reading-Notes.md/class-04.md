# html links
Links are the defining feature of the web because they allow you to move from one web page to another — enabling the very idea of browsing or surfing.
+ links from one website to another
```
<a> other-sites.html HTML Links are created using the <a> element which has an attribute called href. The value of the href attribute is the page that you want people to go to when they click on the link.
Users can click on anything that appears between the opening <a> tag and the closing </a> tag and will be taken to the page specified in the href attribute. When you link to a different website, the value of the href attribute will be the full web address for the site, which is known as an absolute URL.
```
+ Links from one page to another on the same website
```
<a>
When you are linking to other pages within the same site, you do not need to specify the domain name in the URL. You can use a shorthand known as a relative URL. If all the pages of the site are in the same folder, then the value of the href attribute is just the name of the file.
If you have different pages of a site in different folders, then you can use a slightly more complex syntax to indicate where the page is in relation to the current page. You will learn more about
these on the pages 81-84. If you look at the download code for each chapter, you will see that the index.html file contains links that use relative URLs.
```
+ Links from one part of a web page to another part of the same page
+ Links that open in a new browser window
+ Links that start up your email program and address a new email to someone
## Writing Links
```
Links are created using the <a> element. Users can click on anything between the opening <a> tag and the closing </a> tag You specify which page you want to link to using the href attribute
```
```
The text between the opening <a> tag and closing </a> tag is known as link text. Where possible, your link text should explain where visitors will be taken if they click on it (rather than just saying "click here" .Below you can see the link to IMDB that was created on the previous page. 
```
```
Many people navigate websites by scanning the text for links. Clear link text can help visitors find what they want. This will give them a more positive impression of your site and may encourage them to visit it for longer. (It also helps people using screen reader software.)
```
```
To write good link text, you can think of words people might use when searching for the page that you are linking to. (For example, rather than write "places to stay" you could use something more specific such as "hotels in New York.")
```
## email links
mailto:
```
To create a link that starts up the user's email program and addresses an email to a specified email address, you use the <a> element. However, this time the value of the href attribute starts with mailto: and is followed by the email address you want the
email to be sent to. On the right you can see that an email link looks just like any other link but, when it is clicked on, the user's email program will open a new email message and address it to the person specified in the link. Email Links
```
## layout
**we are going to look at how to control where each element sits on a page and how to create attractive page layouts.**
***This involves learning about how designing for a screen can be different to designing for other mediums (such as print). In this chapter we will:**
+ Explore different ways to position elements using normal flow, relative positioning, absolute positioning and floats.
+ Discover how various devices have different screen sizes
and resolution, and how this affects the design process.
+ Learn the difference between fixed width and liquid layouts,
and how they are created.
+ Find out how designers use grids to make their page
designs look more professional.


## Building Blocks
CSS treats each HTML element as if it is in its
own box. This box will either be a block-level
box or an inline box.
Block-level boxes start on a new line and act as the main building blocks
of any layout, while inline boxes flow between surrounding text. You can
control how much space each box takes up by setting the width of the
boxes (and sometimes the height, too). To separate boxes, you can use
borders, margins, padding, and background colors.
## Containing Elements
If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element. 
```
It is common to group a number of elements together inside a <div> (or other block-level) element. For example, you might group together all of the elements that form the header of a site (such as the logo and the main navigation). The <div> element that contains this group of elements is then referred to as the containing element.
```
```
The orange lines in this diagram represent <div> elements. The header (containing the logo and navigation) are in one <div> element, the main content of the page is in another, and the footer is in a third. The <body> element is the containing element for these three <div> elements. The second <div> element is the containing element for two paragraphs of Latin text and images (represented by crossed squares).
```
# functions
**Browsers require very detailed instructions about what we want them to do. Therefore, complex scripts can run to hundreds (even thousands) of lines. Programmers use functions, methods, and objects to organize their code. This chapter is divided into three sections that introduce**

### WHAT IS A FUNCTION?
Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of st atements).

### A BASIC FUNCTION
```
var msg = 'Sign up to receive our newsletter for 10% off!';
function updateMessage() {
var el = document.getElementByld('message'};
el .textContent = msg;
}
updateMessage(};
```
## JavaScript Function Syntax
A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses ().

Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).

The parentheses may include parameter names separated by commas:
(parameter1, parameter2, ...)

The code to be executed, by the function, is placed inside curly brackets: {}
+ Function parameters are listed inside the parentheses () in the function definition.

+ Function arguments are the values received by the function when it is invoked.

+ Inside the function, the arguments (the parameters) behave as local variables.


# pair programming
Pair programming is an agile software development technique in which two programmers work together at one workstation.
## What is Pair Programming?
Pair programming, as the name suggests, is a software development practice in which two programmers collaborate on a single workstation at the same time. This collaboration can be done either in person or remotely, in which case you’ll need software for screen sharing and real-time editing.   

There are two alternating roles for developers to play in pair programming. One programmer acts as the driver who writes the code, and the other acts as the navigator who reviews the code and provides information and instructions. Both parties switch off roles at regular intervals, anywhere between 15 minutes to 1 hour.   

For many organizations, pair programming is still a hotly debated practice; some adopt it wholeheartedly, while others outright refuse to consider it. In the next two sections, we’ll discuss the advantages and disadvantages of pair programming to understand each of these viewpoints.
## why is pair progtamming is bad

Wrong tasks: Pairing at the wrong time can be both time consuming and inefficient. One can slow down two: If one is a slow thinker/typer or unfocused it can slow down the other one as well. More talk less coding: You might end up explaining things that would be faster to just code
what the benft of pair programming 


## What is pair programming in Scrum?
 ‪pair programming‬‏
Pair programming is an agile software development technique in which two programmers work together at one workstation. One, the driver, writes code while the other, the observer or navigator, reviews each line of code as it is typed in. 
  


    [programming](https://anarsolutions.com/wp-content/uploads/2015/08/Pair-Programming-300x225.jpg)