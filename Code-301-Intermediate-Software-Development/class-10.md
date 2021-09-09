# What is a ‘call’?
At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).

Let’s break down our definition:

LIFO: When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

Let us take a look at a code sample to demonstrate LIFO by printing a stack trace error to the console.
# How many ‘calls’ can happen at once?
secondFunction() then calls firstFunction()which is pushed into the 2
# What does LIFO mean?
LIFO: When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

Let us take a look at a code sample to demonstrate LIFO by printing a stack trace error to the console.
# Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
![](https://eecs280staff.github.io/notes/_images/02_stack.svg)
![](https://eecs280staff.github.io/notes/_images/02_stack_downward.svg)

# What causes a Stack Overflow?
A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.         
The callMyself() will run until the browser throws a “Maximum call size exceeded”. And that is a stack overflow.




# What is a ‘refrence error’?
Below, you'll find a list of errors which are thrown by JavaScript. These errors can be a helpful debugging aid, but the reported problem isn't always immediately clear. The pages below will provide additional details about these errors. Each error is an object based upon the Error object, and has a name and a message.

Errors displayed in the Web console may include a link to the corresponding page below to help you quickly comprehend the problem in your code.

For a beginner's introductory tutorial on fixing JavaScript errors, see What went wrong? Troubleshooting JavaScript.

# What is a ‘syntax error’?

I know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.
`
JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1
`
This can be solved by just fixing the syntax, in this case the object should be a JSON.           
`JSON.parse('{"foo":"bar"}')`                               
Some syntax errors like sending a trailing comma when calling a function are handled without error by most recent browsers, but older ones you have to be careful.
# What is a ‘range error’?

Range errors
Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.
`                               
var foo= []
foo.length = foo.length -1 // Uncaught RangeError: Invalid array length
`                                     
An array for instance cannot have a negative length, why would you mess with the array length? Some people use it to set an array to empty, something of the likes of:
`
var foo = [0, 0]
foo.length = foo.length - 2 // (or foo.length - foo.length)
foo // would log [] instead of [0, 0]
`                  
I prefer not to mutate my variables whenever possible (making them constants and not variables) but this is a method that is available and now you know it.
# What is a ‘tyep error’?
Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.
`
var foo = {}
foo.bar // undefined
foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined
`
This is probably the most frequent error in JS, trying to access a property/method thinking that bar is of the type object when in reality, since it hasn’t been declared yet, it’s undefined which doesn’t have any baz available.
The fix is simple, just make sure that bar exists before trying to access it, either by creating bar or by checking for undefined.

`
var foo = { bar: {} }
foo.bar.baz // undefined but you avoid the error

`
or
`
var foo = {}
if (typeof foo.bar !== 'undefined') {
  foo.bar.baz // this will never be executed while bar does not exist
}

`
There are also warnings, for instance telling you about a deprecated method, which can be found more frequently in firefox developer tools.
# What is a breakpoint?
The breakpoint can also be achieved by putting a debugger statement in your code in the line you want to break.

You can also add conditional breakpoints by right-clicking a previous set breakpoint, which will make your program stop at that point only if a condition is met, this is awesome for when you want to debug huge cycles for specific values. In this example the breakpoint will point stop when the index reaches 40.
# What does the word ‘debugger’ do in your code?
 **debugger is a computer program used by programmers to test and debug a target program. Debuggers may use instruction-set simulators, rather than running a program directly on the processor to achieve a higher level of control over its execution. ... They also can often modify the state of programs while they are running**
I’ve added a debugger statement and when running the code above you can see the “history” before reaching that breakpoint. In this case it’s not a long call stack but you can start to see why it is useful, you know the function add was executed in line 14, with what parameters (which you an see in the scope below the call stack) and you can evaluate whatever will well you at that point in the console, in this case evaluation result.split(‘’) would show you that the result being returned would be [“1”, “2”].
If you press continue the call stack will show the changes, this time add being called in line 15 instead of 14 with numbers instead of strings, try and evaluate result.split(‘’) at this point and an error should be thrown.
Hopefully at this point it will make you realise sooner that you should maybe change the name of the function to something like “concatenateAndSplit” and validate the type of the arguments.
The call stack it’s better to navigate when you have names to your functions, meaning that if you use anonymous functions you will most probably have an harder time since the call stack will not show the name of the parent function.
For example, if we remove it from the object and call it directly not much changes, but if we remove the name of, let us say testing function, the call stack will no longer be able to point you the origin of the call (you can still press the underline and it will show you but that is an extra step that could be avoided.
![](https://eecs280staff.github.io/notes/_images/02_call_stack_example_a.svg)
![](https://eecs280staff.github.io/notes/_images/02_pass_by_reference.svg)