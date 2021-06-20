# JavaScript Guide
## Functions
***Functions are one of the fundamental building blocks in JavaScript. A function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output. To use a function***
### Function declarations
A function definition (also called a function declaration, or function statement)
- The name of the function.
- A list of parameters to the function, enclosed in parentheses and separated by commas. - The JavaScript statements that define the function, enclosed in curly brackets, {...}
### Function expressions
While the function declaration above is syntactically a statement, functions can also be created by a function expression.
Such a function can be anonymous; it does not have to have a name
Function expressions are convenient when passing a function as an argument to another function. The following example shows **a map** function that should receive a function as first argument and an array as second argument.
### Calling functions
Defining a function does not execute it. Defining it names the function and specifies what to do when the function is called.

Calling the function actually performs the specified actions with the indicated parameters. For example, if you define the function **square**.
## Expressions and operators:


1. operators:JavaScript has the following types of operators
   + Assignment operators
   + Comparison operators
   + Arithmetic operators
   + Bitwise operators
   + Logical operators
   + String operators 
   + Conditional (ternary) operator
   + Comma operator
   + Unary operators
   + Relational operators       



Name |	Shorthand operator |Meaning
-----|---------------------|-------
Assignment z|	x = y	| x = y
Addition assignment |	x += y |	x = x + y
Subtraction assignment|	x -= y |	x = x - y
Multiplication assignment|	x *= y | 	x = x * y
Division assignment|	x /= y|	x = x / y
Remainder assignment|	x %= y|	x = x % y
Exponentiation assignment|	x **= y|	x = x ** y
Left shift assignment|	x <<= y|	x = x << y
Right shift assignment|	x >>= y|	x = x >> y
Unsigned right shift assignment|	x >>>= y|	x = x >>> y
Bitwise AND assignment|	x &= y|	x = x & y
Bitwise XOR assignment|	x ^= y|	x = x ^ y
Logical AND assignment|	x &&= y|	x && (x = y)
Logical nullish assignment|	x ??= y|	x ?? (x = y)    


  
 ##  Arithmetic operators
An arithmetic operator takes numerical values (either literals or variables) as their operands and returns a single numerical value. The standard arithmetic operators are addition (+), subtraction (-), multiplication (*), and division (/). These operators work as they do in most other programming languages when used with floating point numbers (in particular, note that division by zero produces Infinity)
  

![](https://datavisioner.net/wp-content/uploads/2020/04/javascript-illustration.png)