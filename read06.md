# css 
*CSS (Cascading Style Sheets) allows you to create great-looking web pages
In the Introduction to HTML module we covered what HTML is, and how it is used to mark up documents. These documents will be readable in a web browser. Headings will look larger than regular text, paragraphs break onto a new line and have space between them. Links are colored and underlined to distinguish them from the rest of the text. What you are seeing is the browser's default styles — very basic styles that the browser applies to HTML to make sure it will be basically readable even if no explicit styling is specified by the author of the page.*


![](https://cdn.pixabay.com/photo/2017/03/30/17/42/css-2189148_640.png)
## CSS syntax
CSS is a rule-based language — you define rules specifying groups of styles that should be applied to particular elements or groups of elements on your web page. For example "I want the main heading on my page to be shown as large red text."  
The rule opens with a selector . This selects the HTML element that we are going to style. In this case we are styling level one headings (<h1>).
![CSS syntax](https://www.w3schools.com/css/img_selector.gif)

We then have a set of curly braces { }. Inside those will be one or more declarations, which take the form of property and value pairs. Each pair specifies a property of the element(s) we are selecting, then a value that we'd like to give the property.
![](https://s3.eu-west-2.amazonaws.com/uploads.3alampro.com/old/monthly_2018_01/css-selectors-1f0064.png.d03086c298b6ce0f85c394976d9ccacb.png)
## CSS Modules
As there are so many things that you could style using CSS, the language is broken down into modules. You'll see reference to these modules as you explore MDN and many of the documentation pages are organized around a particular module  
![](https://www.javascriptstuff.com/static/css-modules-diagram-example-edcd723b0e6ff2f1a6f7cbd1050b1c33-4f823.png)
## How To Add CSS
+ External CSS  
With an external style sheet, you can change the look of an entire website by changing just one file!
Each HTML page must include a reference to the external style sheet file inside the <link> element, inside the head section.
+ Internal CSS 

 An internal style sheet may be used if one single HTML page has a unique style.The internal style is defined inside the (<style>) element, inside the head section.    


+ Inline CSS   
 An inline style may be used to apply a unique style for a single element.To use inline styles, add the style attribute to the relevant element. The style attribute can contain any CSS property.