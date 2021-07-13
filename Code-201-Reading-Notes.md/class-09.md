# Forms 
**Traditionally, the term 'form' has referred to a printed document that contains spaces for you to fill in information HTML borrows the concept of a form to refer to different elements that allow you to collect information from visitors to your site.Whether you are adding a simple search box to your website or you need to create more complicated insurance applications, HTML forms give you a set of elements to collect data from your users.**
## Why Forms
**~The best known form on the web is probably the search box that sits right in the middle of Google's homepage. In addition to enabling users to search, forms also allow users to perform other functions online. You will see forms when registering as a member of a website, when shopping online, and when signing up for newsletters or mailing lists~**
## Form Controls
### ADDING TEXT:
#### Text input (single-line)
Used for a single line of text such
as email addresses and names.
![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRAIm16OHFq5LSmL3mD8A948Lskp0N4SowTAw&usqp=CAU)
#### Password input
Like a single line text box but it
masks the characters entered.
![](https://i.stack.imgur.com/Po7JT.jpg)
#### Text area (multi-line)
For longer areas of text, such as
messages and comments.
![](https://static.packt-cdn.com/products/9781788837361/graphics/B09472_39_01.jpg)
### Making Choices:
#### Radio buttons
For use when a user must select
one of a number of options.
![](https://miro.medium.com/max/506/1*mAU3lQVM6mdr1mHfvaRkeg.png)
#### Checkboxes
When a user can select and
unselect one or more options.
![](https://lh3.googleusercontent.com/7qd08UxTpMVRabax8hTQDcCDfkXGcThFSeMNMnK_0Vzz2Xg22F_8kQPS_v7YHaR9QD5uNKMCIBshpyULmPqnYVtPex5MMvWkPevCRg=w1064-v0)
#### Drop-down boxes
When a user must pick one of a
number of options from a list.
![](https://i.ytimg.com/vi/KGnvCKiOLM0/maxresdefault.jpg)
### Submitting Forms:
#### Submit buttons
To submit data from your form
to another web page.
####  Image buttons
Similar to submit buttons but
they allow you to use an image.
### Uploading Files
#### File upload
Allows users to upload files
(e.g. images) to a website.
## How Forms Work
**A form may have several form controls, each gathering different information. The server needs to know which piece of inputted data corresponds with which form element.**
```
username=Ivy
To differentiate between various pieces of inputted data, information
is sent from the browser to the server using name/value pairs. In this
example, the form asks for the visitor's username and also for their
favorite jazz musician. The name/value pairs sent to the server are:
username=Ivy
If the form control allows the
user to enter text, then the value
of the form control is whatever
the user has typed in.
vote=Herbie
If the form control allows you
to choose from a fixed set of
answers (e.g. radio buttons,
checkboxes or a drop down list),
the web page author will add
code that gives each option an
automatic value
You should never change the name of a form control in a page unless
you know that the code on the server will understand this new value.
```
```
<form>
Form controls live inside a
<form> element. This element
should always carry the action
attribute and will usually have a
method and id attribute too.
action
Every <form> element requires
an action attribute. Its value
is the URL for the page on the
server that will receive the
information in the form when it
is submitted.
method
Forms can be sent using one of
two methods: get or post.
With the get method, the values
from the form are added to
the end of the URL specified in
the action attribute. The get
method is ideal for:
●● short forms (such as search
boxes)
●● when you are just retrieving
data from the web server
(not sending information that
should be added to or deleted
from a database)
<form action="http://www.example.com/subscribe.php"
method="get">
<p>This is where the form controls will appear.
</p>
</form>
chapter-07/form-structure.html HTML
Form Structure
With the post method the
values are sent in what are
known as HTTP headers. As a
rule of thumb you should use the
post method if your form:
●● allows users to upload a file
●● is very long
●● contains sensitive data
(e.g. passwords)
●● adds information to, or
deletes information from, a
database
If the method attribute is not
used, the form data will be sent
using the get method.
id
We look at the id attribute on
page 183, but the value is used to
identify the form distinctly from
other elements on the page (and
is often used by scripts — such
as those that check you have
entered information into fields
that require values).
```
# Lists, Tables & Forms
There are several CSS properties that were created to work with specific types of HTML elements, such as lists, tables, and forms.
## Bullet Point Styles(list-style-type)
```
The list-style-type property
allows you to control the shape
or style of a bullet point (also
known as a marker).
It can be used on rules that
apply to the <ol>, <ul>, and <li>
elements.
Unordered Lists
For an unordered list you can use
the following values:
none
disc
circle
square
Ordered Lists
For an ordered (numbered) list
you can use the following values:
decimal
1 2 3
decimal-leading-zero
01 02 03
lower-alpha
a b c
upper-alpha
A B C
lower-roman
i. ii. iii.
upper-roman
I II III
```
## Images for Bullets(list-style-image)

You can specify an image to act
as a bullet point using the
list-style-image property.
The value starts with the letters
url and is followed by a pair
of parentheses. Inside the
parentheses, the path to the
image is given inside double
quotes.
This property can be used on
rules that apply to the <ul> and
<li> elements.
The example on this page also
shows the use of the margin
property to increase the vertical
gap between each item in the
list.       
```
ul {
list-style-image: url("images/star.png");}
li {
margin: 10px 0px 0px 0px;}
```


## Positioning the Marker(list-style-position)
Lists are indented into the page by default and the list-styleposition
property indicates whether the marker should
appear on the inside or the
outside of the box containing the
main points.
This property can take one of
two values:
outside      
The marker sits to the left of the block of text. (This is the default behaviour if this property is not
used.)     
inside
The marker sits inside the box of text (which is indented).     
In the example shown, the width of the list has been limited to 150 pixels. This ensures that the text wraps onto a new line so you can
see how the value of inside sits the bullet inside the first line of text.      
A margin has been added to each list item so that there is a clear gap between each.  
# Events
When you browse the web, your browser registers different
types of events. It's the browser's way of saying, "Hey, this
just happened." Your script can then respond to these events.
Scripts often respond to these events by updating the content of the web page (via the
Document Object Model) which makes the page feel more interactive. In this chapter, you
will learn how:    
1. INTERACTIONS 
Events occur when users click or tap on a link, hover or swipe over an element, type on the keyboard resize the window, or when the page they requested has loaded.
2. EVENTS TRIGGER CODE
When an event occurs or fires, it can be used to trigger a particular function. Different code can be triggered when users interact with different parts of the page.
3. CODE RESPONDS TO USERS
In the last chapter, you saw how the DOM can be used to update a page. The events can trigger the kinds of changes the DOM  is capable of. This is how a web page reacts to users.
## DIFFERENT EVENT TYPES
**Here is a selection of the events that occur in the browser while you are browsing the web. Any of these events can be used to trigger a function in your JavaScript code.**
|UIEVENTS| Occur when a user interacts with the browser's user interface (UI) rather than the web page|
|---------|-----------------|
EVENT| DESCRIPTION
load| Web page has finished loading
unload| Web page is unloading (usually because a new page was requested)
error| Browser encounters a JavaScript error or an asset doesn't exist
resize| Browser window has been resized
scroll| User has scrolled up or down the page
KEYBOARD EVENTS |Occur when a user interacts with the keyboard (see also input event)
EVENT| DESCRIPTION
keydown| User first presses a key (repeats while key is depressed)
keyup| User releases a key
keypress| Character is being inserted (repeats while key is depressed)
MOUSE EVENTS| Occur when a user interacts with a mouse. trackpad, or touchscreen
EVENT| DESCRIPTION
click |User presses and releases a button over the same element
dblclick |User presses and releases a button twice over the same element
mousedown| User presses a mouse button while over an element
mouseup| User releases a mouse button while over an element
mousemove| User moves the mouse (not on a touchscreen)
mouseover| User moves the mouse over an element (not on a touchscreen)
mouseout| User moves the mouse off an element (not on a touchscreen)

## HOW EVENTS TRIGGERJAVASCRIPT CODE
When the user interacts with the HTML on a web page, there are three
steps involved in getting it to trigger some JavaScript code.
Together these steps are known as event handling.
1. Select t he element
node(s) you want the
script to respond to.
For example, if you want to
trigger a function when a user
clicks on a specific link, you need
to get the DOM node for that
link element. You do this using a
DOM query (see Chapter 5).
2. Indicate which event on
the selected node(s) will
trigger the response.
Programmers call this binding an
event to a DOM node.
The previous two pages showed
a selection of the popular events
that you can monitor for.   
3. State the code you want
to run when the event
occurs.
When the event occurs, on a
specified element, it will trigger
a function. This may be a named
or an anonymous function.
## THREE WAYS TO BIND AN EVENT TO AN ELEMENT
**Event handlers let you indicate which event you are waiting for on any particular element. There are three types of event handlers.**
+ HTML EVENTHANDLERS  

This is bad practice, but you need to be aware of it because you may see it in older code. 
Early versions of HTML included a set of attributes that could respond to events on the element they were added to. The attribute names matched the event names. Their values called the function that was to run when that event occurred.
```
For example, the following:
<a onclick="hide()">
indicated that when a user clicked on this <a> element, the hide () function would be called. This method of event handling is no longer used because it is better to separate the JavaScript from the HTML. You should use one of the other approaches
shown on this page instead
```
+ TRADITIONAL DOM EVENT HANDLERS

DOM event handlers were introduced in the original specification for the DOM. They are considered better than HTML event handlers because they let you separate the JavaScript from the HTML. Support in all major browsers is very strong for this approach. The main drawback is that you can only attach a single function to any event. For example, the submit event of a form cannot trigger one function that checks the contents of a form, and a second to submit the form data if
it passes the checks. As a result of this limitation, if more than one script is used on the same page, and both scripts
respond to the same event, then
one or both of the scripts may
not work as intended
+ DOM LEVEL 2 EVENT LISTENERS

Event listeners were introduced
in an update to the DOM
specification (DOM level 2,
released in the year 2000).
They are now the favored way of
handling events.
The syntax is quite different and,
unlike traditional event handlers,
these newer event listeners allow
one event to trigger multiple
functions. As a result, there
are less likely to be conflicts
between different scripts that
run on the same page.
This approach does not work
with IE8 (or earlier versions of
IE) but you meet a workaround
on p258. Differences in
browser support for the DOM
and events helped speed
adoption of jQuery (but you
need to know how events work
to understand how jQuery uses
them).