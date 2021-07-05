# HTML lists & boxes
## 1. lists 
in html we have alot type of lists like ordered list , Unordered lists and Definition lists , and you can nake alist inside called ***Nested list***:     
            1. Ordered lists  
                    ```
                    The ordered list is created with the <ol> element.,<li>  Each item in the list is placed between an opening <li> tag and a closing </li> tag. (The **li** stands for list item.)
                    ```     
            2. Unordered lists
                    ```
                    The unordered list is created with the <ul> element.<li>  Each item in the list is placed between an opening <li> tag and a closing </li> tag. (The **li** stands for list item.)
                    ```  
            3. Definition lists      
                    ```
                    <dl>
                    The definition list is created with the <dl> element and usually consists of a series of terms and their definitions. Inside the <dl> element you will usually see pairs of <dt> and <dd> elements.
                    <dt>
                    This is used to contain the term being defined (the definition term).
                    <dd>
                    This is used to contain the definition. Sometimes you might see a list where there are two terms used for the same definition or two different definitions for the same term.
                    ```

## 2. boxes
You can set several properties that affect the appearance of these boxes. you can:
+ Control the dimensions of your boxes
+ Create borders around boxes
+ Set margins and padding for boxes
+ Show and hide boxes
### box  (width , height )
by **css** you can give each box width or height in px or cm or any measurment if ypu want to give the box max or min to box by coding min-width.
### overflowing content  
The overflow property tells the browser what to do if the content contained within a box is larger than the box itself. It can have one of two values:
1. hidden
This property simply hides any extra content that does not fit in the box.
2. scroll
This property adds a scrollbar to the box so that users can scroll to see the missing content.
### Hiding Boxes & visibility
The visibility property allows you to hide boxes from users but It leaves a space where the element would have been. This property can take two values:
- hidden
    This hides the element.
- visible
    This shows the element. If the visibility of an element is set to hidden, a blank space will appear in its place.
# structure of box
the main structure of the box on them we can control the width or color or etc ... 
1. margin        
    Margins sit outside the edge
    of the border. You can set the
    width of a margin to create a
    gap between the borders of two
    adjacent boxes
2. border   
    Every box has a border (even if
    it is not visible or is specified to
    be 0 pixels wide). The border
    separates the edge of one box
    from another.
 3. padding     
    Padding is the space between
    the border of a box and any
    content contained within it.
    Adding padding can increase the
    readability of its contents
# javascript creat an array
you create an array and give ita name just like you would any other variable (using the var keyword followed by the name of the array). The values are assigned to the array inside a pair of square brackets, and each value is separated by a comma. The\ values in the array do not need to be the same data type, so you can store a string, a number and a Boolean all in the same array. This technique for creating an array is known as an array literal. It is usually the preferred method for creating an array. You can also write each value on a separate line: colors= ['white', 'black', 'custom'];
## USING IF ... ELSE STATEMENTS
Here you can see that an if ... e 1 se statement al lows you to provide two sets of code:
1. one set if the condition evaluates to true
2. another set if the condition is false
In this test, there are two possible outcomes: a user can either get a score equal to or greater than the pass mark (which means they pass), or they can score less than the pass mark (which means they fail). One response is required for each eventuality. The response is then written to the page. Note that the statements inside an if statement should be ollowed by a semicolon, but there is no need to place one after the closing curly brace of the code blocks
## SWITCH STATEMENTS
A switch statement starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if the variable matches that value.
Here, the variable named 1 eve l is the switch value. If the value of the l eve 1 variable is the string One, then the code for the first case is executed. If it is Two, the second case is executed. If it is Three, the third case is executed. If it is none of these, the code for the defaul t case is executed.
The entire statement lives in one code block (set of curly braces), and a colon separates the option from the statements that are to be run if the case matches the switch value.
At the end of each case is the break keyword. It tells the JavaScript interpreter that it has finished with this switch statement and to proceed to run any subsequent code that appears after it.      
IF ... ELSE
+ There is no need to provide an el se option. (You can just use an if statement.)
+ With a series of if statements, they are all checked even if a match has been found (so it performs more slowly than switch)    
SWITCH
• You have a default option that is run if none of the cases match.
• If a match is found, that code is run; then the break statement stops the rest of the switch statement running (providing better performance than multiple i f statements).    
## JavaScript loops:
Loops are handy, if you want to run the same code over and over again, each time with a different value.

### jvaScript supports different kinds of loops:

+ for - loops through a block of code a number of times
+ for/in - loops through the properties of an object
+ for/of - loops through the values of an iterable object
+ while - loops through a block of code while a specified condition is true
+ do/while - also loops through a block of code while a specified condition is true
