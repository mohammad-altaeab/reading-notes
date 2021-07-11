# Domain Modeling

Domain Modeling Domain Modeling is a way to describe and model real world entities and the relationships between them, which collectively describe the problem domain space. Derived from an understanding of system-level requirements, identifying domain entities and their relationships provides an effective basis for understanding and helps practitioners design systems for maintainability, testability, and incremental development. Because there is often a gap between understanding the problem domain and the interpretation of requirements, domain modeling is a primary modeling area in Agile development at scale. Driven in part from object-oriented design approaches, domain modeling envisions the solution as a set of domain objects that collaborate to fulfill system-level scenarios. In SAFe, domain modeling connects to backlog items at the Team, Program, Large Solution and Portfolio levels and provides a common language for the entire organization. Especially important is its connection with the Nonfunctional Requirements (NFRs) that may affect certain areas where “alternative design approaches” are sometimes used to satisfy the corresponding NFRs. Domain modeling also provides the Agile organization with opportunities for use of Agile-friendly design patterns and approaches that enhance velocity over the long term. As the system design changes, refactoring and updating the domain model is vital to maintaining a continuing understanding of the system, and goes hand in hand with code refactoring to help control the inherent complexity of software systems.

## Domain Modeling in Agile at Large Scale 
In a large scale Agile development, domain modeling is continuously used to support: Analysis of Epics Backlog Refinement at Large Solution, Program and Team levels Design workshops at different levels Refining Vision and Roadmap (typically in preparation for Program Increment) Domain modeling is typically developed and continuously refined by the System Architect in collaboration with other stakeholders in order to understand the impact of epics and features on the system. These groups use domain modeling as part of the preparation for PI Planning at the modeling workshop in a highly visual and collaborative manner.  


![](https://www.scaledagileframework.com/wp-content/uploads/2012/11/Common-Language-figure-3.png)

## The Domain Model and System Design
 #### Domain-Oriented vs. Alternative Approaches
  Domain modeling is not only useful for analysis but is often a good conceptual model for the system design. Domain modeling is one of the key design patterns/approaches that assumes deriving the solution object model directly from the problem domain while preserving both behavior and data (see [3]). See [2] for a systematic and detailed outline of such best practices, known by the term of Domain-Driven Design. This approach provides a natural and very effective way of managing the inherent complexity of software development that is vital at large scale. Figure 4, adapted from [3], chapter 2, shows a comparison of effort spent on enhancing software functionality versus complexity by different approaches: When design is based on the domain When design is based on data structure or transaction scripts


# table
A table represents information in a grid format. Examples of tables include financial reports, TV schedules, and sports results.
## Basic Table St ructure
```
<table>
The <table> element is used to create a table. The contents of the table are written out row by row.
<tr>
You indicate the start of each row using the opening <tr> tag. (The tr stands for table row.) It is followed by one or more <td> elements (one for each cell in that row). At the end of the row you use a closing </tr> tag.
<td>
Each cell of a table is represented using a <td> element. (The td stands for table data.) At the end of each cell you use a closing </td> tag.
<th>
The <th> element is used just like the <td> element but its purpose is to represent the heading for either a column or a row. (The th stands for table heading.) 
Even if a cell has no content, you should still use a <td> or <th> element to represent the presence of an empty cell otherwise the table will not render correctly. (The first cell in the first row of this example shows an empty cell.)
Using <th> elements for headings helps people who use screen readers, improves the ability for search engines to index your pages, and also enables you to control the appearance of tables better when you start to use CSS.
You can use the scope attributeon the <th> element to indicate whether it is a heading for a column or a row. It can take the values: row to indicate a heading for a row or col to indicate a heading for a column.
```
![](https://vertex-academy.com/tutorials/wp-content/uploads/2016/08/table.png)
### Spanning ColumnS & rows
```
<td colspan =""> to make an empty space colmn
<td rowspan=""> to make an empty space row
```
### Long Tables
```
There are three elements that
help distinguish between the
main content of the table and
the first and last rows (which can
contain different content).
These elements help people
who use screen readers and also
allow you to style these sections
in a different manner than the
rest of the table (as you will see
when you learn about CSS).
<thead>
The headings of the table should
sit inside the <thead> element.
<tbody>
The body should sit inside the
<tbody> element.
<tfoot>
The footer belongs inside the
<tfoot> element.
```
![](https://www.w3.org/TR/1999/PR-html40-19990824/images/mergedcells.gif)
### DOM
The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects. That way, programming languages can connect to the page.

A Web page is a document. This document can be either displayed in the browser window or as the HTML source. But it is the same document in both cases. The Document Object Model (DOM) represents that same document so it can be manipulated. The DOM is an object-oriented representation of the web page, which can be modified with a scripting language such as JavaScript.
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