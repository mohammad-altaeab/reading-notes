# lAYOUT
![](https://i1.wp.com/www.cssscript.com/wp-content/uploads/2018/12/Tiny-Flexbox-Grid-Layout-In-Pure-CSS-infinity-css-grid.png?fit=565%2C376&ssl=1)
how to control where each element sits
on a page and how to create attractive
page layouts. 
+ Explore different ways to position e ●● lements using normal flow, relative positioning, absolute positioning and floats.
+ Discover how various devices have different screen sizes and resolution, and how this affects the design process.
+ Learn the difference between fixed width and liquid layouts, and how they are created.
+ Find out how designers use grids to make their page designs look more professional.
## Positioning El ements
###  1. Building Blocks
CSS treats each HTML element as if it is in its
own box. This box will either be a block-level
box or an inline box.
Block-level boxes start on a new line and act as the main building blocks
of any layout, while inline boxes flow between surrounding text. You can
control how much space each box takes up by setting the width of the
boxes (and sometimes the height, too). To separate boxes, you can use
borders, margins, padding, and background colors.
```
Block-level elements
start on a new line
Examples include:
<h1> <p> <ul> <li>
Inline elements
flow in between
surrounding text
Examples include:
<img> <b> <i>
```
### 2. Containing Elements
```
If one block-level element sits inside another
block-level element then the outer box is
known as the containing or parent element.
It is common to group a number of elements together inside a <div>
(or other block-level) element. For example, you might group together
all of the elements that form the header of a site (such as the logo and
the main navigation). The <div> element that contains this group of
elements is then referred to as the containing element. 


A box may be nested inside
several other block-level
elements. The containing
element is always the direct
parent of that element.

The orange lines in this diagram represent <div> elements. The
header (containing the logo and navigation) are in one <div> element,
the main content of the page is in another, and the footer is in a third.
The <body> element is the containing element for these three <div>
elements. The second <div> element is the containing element for two
paragraphs of Latin text and images (represented by crossed squares).
```
##  Controll ing the Position of Elements
CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. You specify the positioning scheme using the position property in CSS. You can also float elements using the float property.
### 1. Normal flow
Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one. Even if you specify the width of the boxes and there is space for two elements to sit side-byside, they will not appear next to each other. This is the default behavior (unless you tell the browser to do something else).
### 2. Relative Positioning
This moves an element from the position it would be in normal flow, shifting it to the top, right,bottom, or left of where it would have been placed. This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.
### 3. Absolute positioning
This positions the element in relation to its containing element. It is taken out of normal flow, meaning that it does not affect the position of any surrounding elements (as they simply ignore the space it would have taken up). Absolutely positioned elements move as users scroll up and down the page.
**To indicate where a box should be positioned, you may also need to use box offset properties to tell the browser how far from the top or bottom and left or right it should be placed. (You will meet these when we introduce the positioning schemes on the following pages.)**
### 4. Fixed Positioning
This is a form of absolute positioning that positions the element in relation to the browser window, as opposed to the containing element Elements with fixed positioning do not affect the position of surrounding elements and they do not move when the user scrolls up or down the page.
### 5. Floating Elements
Floating an element allows you to take that element out of normal flow and position it to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow.
 
## Clearing Floats
**clear**

 The clear property allows you
to say that no element (within
the same containing element)
should touch the left or righthand
sides of a box.    
**left**   
The left-hand side of the box
should not touch any other
elements appearing in the same
containing element.     
**right**   
The right-hand side of the
box will not touch elements
appearing in the same containing
element.    
**both**    
Neither the left nor right-hand
sides of the box will touch
elements appearing in the same
containing element.      
**none**    
Elements can touch either side.
In this example, the fourth
paragraph has a class called
clear. The CSS rule for this
class uses the clear property
to indicate that nothing should
touch the left-hand side of it. The
fourth paragraph is therefore
moved further down the page
so no other element touches its
left-hand side.   
## Creating Multi-ColumnLayouts with Fl oats
Many web pages use multiple
columns in their design. This
is achieved by using a <div>
element to represent each
column. The following three CSS
properties are used to position
the columns next to each other:   
**width**   
This sets the width of the
columns.
**float**   
This positions the columns next
to each other.   
**margin** 
```  
This creates a gap between the
columns.
A two-column layout like the one
shown on this page would need
two <div> elements, one for the
main content of the page and
one for the sidebar.
Inside each of the <div>
elements there can be headings,
paragraphs, images, and even
other <div> elements
```
## Liquid Layouts
Liquid layout designs stretch and contract as the user increases or decreases the size of their browser window. They tend to use percentages. 
![](https://bs-uploads.toptal.io/blackfish-uploads/uploaded_file/file/197755/image-1583190798408-7af80aeb943477b9375814bc95245a4e.png)  
### Advantages
+ Pages expand to fill the entire
browser window so there are
no spaces around the page
on a large screen.
+ If the user has a small
window, the page can
contract to fit it without the
user having to scroll to the
side.
+ The design is tolerant of
users setting font sizes larger
than the designer intended
(because the page can
stretch).
### Disadvantages
+ If you do not control the
width of sections of the page
then the design can look very
different than you intended,
with unexpected gaps around
certain elements or items
squashed together.
+ If the user has a wide
window, lines of text can
become very long, which
makes them harder to read.
+ If the user has a very narrow
window, words may be
squashed and you can end up
with few words on each line.
+ If a fixed width item (such as
an image) is in a box that is
too small to hold it (because
the user has made the
window smaller) the image
can overflow over the text.
![](https://miro.medium.com/max/1024/1*XCZZZmhQN4rHLw2dW14BZQ.png)