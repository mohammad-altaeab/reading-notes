# Understanding The Problem Domain Is The Hardest Part Of Programming
What is the hardest thing about writing code?

There are many common answers to this question:

+ Learning a new technology
+ Naming things
+ Testing your code
+ Debugging
+ Fixing bugs
+ Making software maintainable
A familiar problem
In a good portion of [my Pluralsight courses](https://www.youtube.com/watch?v=HvjQ3Mx-jWg) I show the viewer how to build the “Protein Tracker” application.

I am often asked why I keep demonstrating how to build the same simple application over and over again in each of my courses.
The answer is “familiarity.”

When I first started using the Protein Tracker example in my [Android course](https://www.youtube.com/watch?v=HvjQ3Mx-jWg), I was just looking for a simple example of an application that could be easily understood and implemented.
The idea behind the Protein Tracker application is that it allows a user to set a goal for the amount of protein to consume in a day.  The user can add protein amounts which are added to a total protein count that is tracked for that user.
![](https://spzone-simpleprogrammer.netdna-ssl.com/wp-content/uploads/2013/07/Protein_Tracker_2013-07-03_16-44-41.png)
Very simple functionality, easily explainable, but most importantly, easily understood.

What I found with this simple application was that because it was so easy to understand, the focus was taken off of the problem domain and put instead on the technology.

Not only this, but as I reused this same exact application for teaching a variety of different technologies, it served as a reference problem domain that didn’t have to be re-learned, and provided a way to compare and contrast different technologies—I was getting this teaching mechanism for free if a viewer had already watched one of my other Pluralsight courses.

By creating a familiar problem domain, I found that both the tasks of me teaching a new technology and the viewer learning that technology were much easier, because it is very difficult to learn more than one thing at once.

So what am I trying to say here?

Simply that by taking away the problem domain, or making it so trivial that it is easily understood, I am able to make both teaching and learning easier.

Why problem domains are hard
Have you ever tried to put together a jigsaw puzzle that didn’t have any picture on it?  How about one like this one, that has a very similar pattern repeated on it and is double-sided?
There was however something really interesting about the waterfall approach and the extreme amount of specification that was done before anything was built—it was very easy to write the code for a feature.

I remember writing a tab control for the user interface of a printer and having the complete pixel perfect specs handed to me before I began to write any code.  I was also given all the possible use cases and told exactly how it should function and what it should do under just about every circumstance.

Guess how easy it was to write the code to produce this tab control?  Super easy.

As much as I frown upon this approach for software development today, there is something interesting to think about here.

I was essentially given the entire problem domain in the form of a spec that was clear and unambiguous.  I was easily able to learn that problem domain and because of it, I was able to write the code very easily as well.

Perhaps you have had a similar experience, not necessarily working on a waterfall project where you were given the spec, but perhaps on an Agile project where you took the time to clearly understand the problem domain before writing any code.

I’ve spent days trying to implement a feature only to finally go back and talk to a product owner and hash out completely how something should work and why it should work in a particular way, only to go back to my desk and crank out the code in a matter of hours


## Object Literals
Objects group together a set of variables and functions to create a model
of a something you would recognize from the real world. In an object,
variables and functions take on new names.
1. **IN AN OBJECT: VARIABLES BECOME KNOWN AS PROPERTIES**       
        If a variable is part of an object, it is called a
        property. Properties te ll us about the object, such as
        the name of a hotel or the number of rooms it has.
        Each individual hotel might have a different name
        and a different number of rooms.
2. **IN AN OBJECT: FUNCTIONS BECOME KNOWN AS METHODS**        
        If a function is part of an object, it is called a method.
        Methods represent tasks that are associated with
        the object. For example, you can check how many
        rooms are available by subtracting the number of
        booked rooms from the total number of rooms.
+ *Like variables and named functions, properties and methods have a name and a value. In an object, that name is called a key.*
+ *An object cannot have two keys with the same name. This is because keys are used to access their corresponding values*
+ *The value of a property can be a string, number, Boolean, array, or even another object. The va lue of a method is always a function.*


## Programmers use a lot of name/value pairs:
- HTML uses attribute names and values.
- CSS uses property names and values.
## In JavaScript:
- Variables have a name and you can assign them a value of a string, number, or Boolean.
- Arrays have a name and a group of values. (Each item in an array is a name/value pair because it has an index number and a value.)
- Named functions have a name and value that is a set of statements to run if the function is called.
- Objects consist of a set of name/value pairs (but the names are referred to as keys).


### JavaScript Objects
In JavaScript, almost "everything" is an object.

Booleans can be objects (if defined with the new keyword)
Numbers can be objects (if defined with the new keyword)
Strings can be objects (if defined with the new keyword)
Dates are always objects
Maths are always objects
Regular expressions are always objects
Arrays are always objects
Functions are always objects
Objects are always objects
All JavaScript values, except primitives, are objects.

### JavaScript Primitives
A **primitive value** is a value that has no properties or methods.

A **primitive data type** is data that has a primitive value.

JavaScript defines 5 types of primitive data types:

string
number
boolean
null
undefined

Value|	Type|	Comment|
|----|------|----------|
"Hello"	|string	|"Hello" is always "Hello"
3.14	|number	|3.14 is always 3.14
true	|boolean|	true is always true
false	|boolean	|false is always false
null	|null (object)	|null is always null
undefined	|undefined	|undefined is always undefined

### Object Properties
The named values, in JavaScript objects, are called properties.

|Property|	Value|
|--------|-------|
firstName|	John
lastName |	Doe
age	     |   50
eyeColor |	blue

Objects written as name value pairs are similar to:

+ Associative arrays in PHP
+ Dictionaries in Python
+ Hash tables in C
+ Hash maps in Java
+ Hashes in Ruby and Perl

### Object Methods
Methods are **actions** that can be performed on objects.

Object properties can be both primitive values, other objects, and functions.

An *object method* is an object property containing a **function definition**.

|Property|	Value  |
|--------|---------|
firstName|	John
lastName|	Doe
age	|50
eyeColor|	blue
fullName|	function() {return this.firstName + " " + this.lastName;}


### Creating a JavaScript Object
With JavaScript, you can define and create your own objects.

There are different ways to create new objects:

+ Create a single object, using an object literal.
+ Create a single object, with the keyword new.
+ Define an object constructor, and then create objects of the constructed type.
+ Create an object using Object.create().
### Using an Object Literal
This is the easiest way to create a JavaScript Object.

Using an object literal, you both define and create an object in one statement.

An object literal is a list of name:value pairs (like age:50) inside curly braces {}.

![](https://www.programmersought.com/images/324/143dfca7f3023bec280e4cd5e9cc69cc.png)




# Document Object Model
The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.
*The DOM is neither part of HTML, nor part of JavaScript; it is a separate set of rules.It is implemented by all major browser makers, and covers two primary areas:*
### MAKING A MODEL OF THE HTML PAGE
When the browser loads a web page, it
creates a model of the page in memory.
The DOM specifies the way in which the
browser should structure this model using
a **DOM tree**.
The DOM is called an object model
because the model (the DOM tree) is
made of objects.
Each object represents a different part of
the page loaded in the browser window.
### ACCESSING AND CHANGING THE HTML PAGE
The DOM also defines methods and
properties to access and update each
object in this model, which in turn updates
what the user sees in the browser.
You will hear people call the DOM an
**Application Programming Interface (API)**.
User interfaces let humans interact with
programs; APls let programs (and scripts)
talk to each other. The DOM states what
your script can "ask the browser about the
current page, and how to tell the browser
to update what is being shown to the user.

## THE DOM TREE IS A MODEL OF A WEB PAGE
As a browser loads a web page, it creates a model of that page.
The model is called a DOM tree, and it is stored in the browsers' memory.
It consists of four main types of nodes.
```
BODY OF HTML PAGE
<html>
    <body>
        <div id="page">
          <hl id="header">List</hl>
          <h2>Buy groceries</h2>
          <ul>
            <li id="one" class="hot"><em>fresh</em> figs</li>
            <li id="two" class="hot">pine nuts</l i>
            <l i id="three" class="hot">honey</l i>
            <l i id="four">balsamic vinegar</l i>
          </ ul>
          <script src="js/list.js "></scri pt>
        </ div>
    </ body>
</ html>
```
### THE DOCUMENT NODE
Above, you can see the HTML code for a shopping
list, and on the right hand page is its **DOM tree**.
Every element, attribute, and piece of text in the
HTML is represented by its own **DOM node**.
At the top of the tree a **document node** is added; it
represents the entire page (and also corresponds to
the document object, which you first met on p36).
When you access any element, attribute, or text
node, you navigate to it via the document node. It is
the starting point for all visits to the DOM tree.
### ELEMENT NODES
HTML elements describe the structure of an HTML
page.
```
(The <h l > - <h6> elements describe what
parts are headings; the <p> tags indicate where
paragraphs of text start and finish; and so on.)
```
To access the DOM tree, you start by looking for
elements. Once you find the element you want, then
you can access its text and attribute nodes if you
want to. This is why you start by learning methods
that allow you to access element nodes, before
learning to access and alter text or attributes.
### ATTRIBUTE NODES

The opening tags of HTML elements can carry
attributes and these are represented by attribute
nodes in the DOM tree.
Attribute nodes are not children of the element thar
carries them; they are part of that element. Once
you access an element, there are specific JavaScript
methods and properties to read or change that
element's attributes. For example, it is common to
change the values of cl ass attributes to trigger new
CSS rules that affect their presentation.

### TEXT NODES
```
Once you have accessed an element node, you
can then reach the text within that element. This is
stored in its own text node.
Text nodes cannot have children. If an element
contains text and another child element, the child
element is not a child of the text node but rather
a child of the containing element. (See the <em>
element on the first <l i > item.) This illustrates how
the text node is always a new branch of the DOM
tree, and no further branches come off of it
```


![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/DOM-model.svg/1200px-DOM-model.svg.png)