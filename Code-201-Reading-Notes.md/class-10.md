# Error Handling & Debugging
**JavaScript can be hard to learn and everyone makes mistakes when writing it. This chapter will help you learn how to find the errors in your code. It will also teach you how to write scripts that deal with potential errors gracefully.**   
![](https://i.morioh.com/200721/48d32e3d.webp)
When you are writing JavaScript, do not expect to write it perfectly the first time. Programming is like problem solving: you are given a puzzle and not only do you have to solve it, but you also need to create the instructions that allow the computer to solve it. too.   
When writing a long script, nobody gets everything right in their first attempt. The error messages that a browser gives look cryptic at first, but they can help you determine what went wrong in your JavaScript and how to fix it. In this chapter you will learn about:
+ THE CONSOLE & DEV TOOLS
Tools built into the browser
that help you hunt for errors.
+ COMMON PROBLEMS
Common sources of errors,
and how to solve them.
+ HANDLING ERRORS
How code can deal with
potential errors gra cefully.

## ORDER OF EXECUTION
**To find the source of an error, it helps to know how scripts are processed The order in which statements are executed can be complex; some tasks cannot complete until another statement or function has been run:**
+ This script above creates a greeting message, then writes it to an alert box (see right-hand page). In order to create that greeting, two functions are used: greetUser () and getName () . You might think that the order of execution (the order in which statements are processed) would be as numbered: one through to four. However, it is a little more complicated. To complete step one, the interpreter needs the results of the functions in steps two and three (because the message contains values returned by those functions). The order of execution is more like this: 1, 2, 3, 2, 1, 4.
+       1. The greeting variable gets its value from the greetUser() function.
        2. greetUser() creates the message by combining  the string 'Hello' with the result of getName ().
        3. getName () returns the name to greetUser() .
        2. greetUser() now knows the name, and combines it with the string. It then returns the message to the statement that ca lled it in step 1.
        1. The va lue of the greeting is stored in memory.
        4. This greeting variable is written to an alert box.

## EXECUT.ION CONTEXTS
**The JavaScript interpreter uses the concept of execution contexts. There is one global execution context; plus, each function creates a new new execution context. They correspond to variable scope.**
### EXECUTION CONTEXT
**Every statement in a script lives in one of three execution contexts:**
+ GLOBAL CONTEXT   
    Code that is in the script, but not in a function.
    There is only one global context in any page.
+ FUNCTION CONTEXT     
        Code that is being run within a function.
        Each function has its own function context.
+ EVALCONTEXT (NOT SHOWN)    
        Text is executed like code in an internal function
        called eva l {) (which is not covered in this book).
### VARIABLE SCOPE
**The first two execution contexts correspond with the notion of scope**
+ GLOBAL SCOPE  
If a variable is declared outside a function, it can
be used anywhere because it has global scope.
If you do not use the var keyword when creating
a variable, it is placed in global scope.
+ FUNCTION-LEVEL SCOPE    
When a variable is declared within a function,
it can only be used within that function. This is
because it has function-level scope.
## EXECUTION CONTEXT & HOISTING
Each time a script enters a new execution context, there are two phases
of activity:
1.  PREPARE
+ The new scope is created
+ Variables, functions, and arguments are created
+ The value of the this keyword is determined
2. EXECUTE
+ Now it can assign values to variables
+ Reference functions and run their code
+ Execute statements    
    Understanding that these two phases happen helps
    with understanding a concept called hoisting. You
    may have seen that you can:     
    + Call functions before they have been declared
    (if they were created using function declarations
     -not function expressions, see p96)    
    + Assign a value to a va ria ble that has not yet been
    declared          
    This is because any variables and functions within
    each execution context are created before they are
    executed.
    The preparation phase is often described as taking
    all of the variables and functions and hoisting them
    to the top of the execution context. Or you can think
    of them as having been prepared.
    Each execution context also creates its own
    vari ab 1 es object. This object contains details of all
    of the variables, functions, and parameters for that
    execution context.
    You may expect the following to fail, because
greetuser() is called before it has been defined:
```
var greeting= greetUser{);
function greetUser() {
II Create greeting
It works because the function and first statement are
in the same execution context, so it is treated like this:
function greetUser()
II Create greeting
}
var greeting= greetUser{);
The following would would fail because greetuser()
is created within the getName () function's context:
var greeting= greetUser();
function getName() {
function greetUser()
// Create greeting
}
// Return name with greeting
}
```
![](https://miro.medium.com/max/1400/1*ddKOVPd0nh4-3l9QisgJnQ.png)
## UNDERSTANDING ERRORS
**If a JavaScript statement generates an error, then it throws an exception At that point, the interpreter stops and looks for exception-handling code.**    
If you are anticipating that something in your code
may cause an error, you can use a set of statements
to **handle** the error (you meet them on p480).
This is important because if the error is not handled,
the script will just stop processing and the user will
not know why. So exception-handling code should
inform users when there is a problem.                   
           
Whenever the interpreter comes across an error,
it will look for error-handling code. In the diagram
below, the code has the same structure as the code
you saw in the diagrams at the start of the chapter.
The statement at step 1 uses the function in step 2,
which in turn uses the function in step 3. Imagine
that there has been an error at step 3.           

When an exception is thrown, the interpreter
stops and checks the current execution context for
exception-handling code. So if the error occurs in the
getName () function (3), the interpreter starts to look
for error handling code in that function.      
       
If an error happens in a function and the function
does not have an exception handler, the interpreter
goes to the line of code that called the function.
In this case, the get Name () function was called by
greetUser(), so the interpreter looks for exceptionhandling
code in the greetUser() function (2).
If none is found, it continues to the next level,
checking to see if there is code to handle the error
in that execution context. It can continue until it
reaches the global context, where it would have to it
terminate the script, and create an Error object.     

        
So it is going through the stack looking for errorhandling
code until it gets to the global context.
If there is still no error handler, the script stops
running and the Error object is created.
![](https://www.tutsmake.com/wp-content/uploads/2020/05/Types-of-Errors-In-JavaScript.jpeg
)
## ERROR OBJECTS
Error objects can help you find where your mistakes are
and browsers have tools to help you read them.
When an Er ror object is created, it will contain the
following properties:
|PROPERTY| DESCRIPTION|
|--------|-------------|
name |Type of execution
message |Description
file Number |Name of the JavaScript file
line Number| Line number of error    


When there is an error, you can see all of this
information in the JavaScript console I Error console
of the browser.          
You will learn more about the console on p464, but
you can see an example of the console in Chrome in
the screen shot below.         
There are seven types of built-in error objects in
JavaScript. You'll see them on the next two pages:    

|OBJECT|DESCRIPTION|
|------|-----------|
Error|Generic error - the other errorsare all based upon this error
Syntax Error|Syntax has not been followed
ReferenceError |Tried to reference a variable that is not declared/within scope
TypeError| An unexpected data type that cannot be coerced
Range Error|Numbers not in acceptable range
URI Error|encodeURI ().decodeURI(),and similar methods used incorrectly
EvalError|eval () function used incorrectly   
## ERROR OBJECTS CONTINUED
Please note that these error messages are from the Chrome browser. Other browsers' error messages may vary.
### Syntax Error
**SYNTAX IS NOT CORRECT**         
This is caused by incorrect use of the rules of the language. It is often  the result of a simple typo.              
MISMATCHING OR UNCLOSED QUOTES                      
document .write ("Howdyl );                    
SyntaxError: Unexpected EOF                 
MISSING CLOSING BRACKET                         
document .getElementByid('page' I                   
SyntaxErr or : Expected token ' ) '                     
MISSING COMMA IN ARRAY           
Would be same for missing] at the end               
var l ist = ['Item 1', 'Item 2 ' l 'rtem 3'];              
SyntaxError: Expected token ']'                  
MALFORMED PROPERTY NAME                  
It has a space but is not surrounded by quote marks                   
user = { f i rstl name: "Ben", lastName: "Lee"};                   
Synt axError: Expected an identifier but                     
found 'name ' instead      
Ref erenceError            
VARIABLE DOES NOT EXIST            
This is caused by a variable that is not declared or is              
out of scope.           
VA RIABLE IS UNDECLARED             
var wi dth = 12 ;            
var area = width * llt!ftNU! ;                
ReferenceError: Can ' t find vari able:             
height              
NAMED FUNCTION IS UNDEFINED           
document.write ( randomFunction() ) ;              
ReferenceError: Can't find variable :         
randomFunction            
### EvalError
INCORRECT USE OF eval() FUNCTION                        
The eva l () function evaluates text through the             
interpreter and runs it as code (it is not discussed             
in this book). It is rare that you would see this type             
of error, as browsers often throw other errors when                
they are supposed to throw an Eva 1 Error.             
### URI Error
INCORRECT USE OF URI FUNCTIONS                      
If these characters are not escaped in URls, they will         
cause an error: / ? & I : ;                        
CHARACTERS ARE NOT ESCAPED                
decodeURI('http: //bbc . com/ news . phplla=l') ;         
URlError: URI error          
![](https://miro.medium.com/max/1000/1*LHpmsxV3f2znpxhuAFuIqA.png)