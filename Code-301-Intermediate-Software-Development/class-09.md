# What is functional programming?
Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data — Wikipedia
# What is a pure function and how do we know if something is a pure function?
Pure functions are essential for a variety of purposes, including functional programming, reliable concurrency, and React+Redux apps. But what does “pure function” mean?
A pure function is a function which:
Given the same input, always returns the same output.
Produces no side effects.
We’re going to answer this question with a free lesson from “Learn JavaScript with Eric Elliott”:
The first fundamental concept we learn when we want to understand functional programming is pure functions. But what does that really mean? What makes a function pure?
So how do we know if a function is pure or not? Here is a very strict definition of purity:
- It returns the same result if given the same arguments (it is also referred as deterministic)
- It does not cause any observable side 
# What are the benefits of a pure function?
The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:
+ Given a parameter A → expect the function to return value B
+ Given a parameter C → expect the function to return value D
A simple example would be a function to receive a collection of numbers and expect it to increment each element of this collection.
# What is immutability?
`Unchanging over time or unable to be changed.`
When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.
In Javascript we commonly use the for loop. This next for statement has some mutable variables.
`
var values = [1, 2, 3, 4, 5];
var sumOfValues = 0;

for (var i = 0; i < values.length; i++) {
  sumOfValues += values[i];
}

sumOfValues // 15
`
For each iteration, we are changing the i and the sumOfValue state. But how do we handle mutability in iteration? Recursion!
`
let list = [1, 2, 3, 4, 5];
let accumulator = 0;

function sum(list, accumulator) {
  if (list.length == 0) {
    return accumulator;
  }

  return sum(list.slice(1), accumulator + list[0]);
}

sum(list, accumulator); // 15
list; // [1, 2, 3, 4, 5]
accumulator; // 0
`
So here we have the sum function that receives a vector of numerical values. The function calls itself until we get the list empty (our recursion base case). For each "iteration" we will add the value to the total accumulator.
With recursion, we keep our variables immutable. The list and the accumulator variables are not changed. It keeps the same value.
Observation: Yes! We can use reduce to implement this function. We will cover this in the Higher Order Functions topic.
It is also very common to build up the final state of an object. Imagine we have a string, and we want to transform this string into a url slug.
In OOP in Ruby, we would create a class, let’s say, UrlSlugify. And this class will have a slugify! method to transform the string input into a url slug.
# What is Referential transparency?
Let’s implement a square function:
`

const square = (n) => n * n;
`
This pure function will always have the same output, given the same input.
`
square(2); // 4
square(2); // 4
square(2); // 4
`
Passing 2 as a parameter of the square function will always returns 4. So now we can replace the square(2) with 4. That's it! Our function is referentially transparent.
Basically, if a function consistently yields the same result for the same input, it is referentially transparent.
pure functions + immutable data = `referential transparency`
With this concept, a cool thing we can do is to memoize the function. Imagine we have this function:`const sum = (a, b) => a + b;`
And we call it with these parameters:`sum(3, sum(5, 8));`
The sum(5, 8) equals 13. This function will always result in 13. So we can do this:`sum(3, 13);`
And this expression will always result in 16. We can replace the entire expression with a numerical constant and ~~memoize~~ it.
![](https://www.rokkey.com/static/25e3f50e6e9b2ffc6fb5e4d2a1327828/2bef9/node.js-use-cases.png)
# What is a module?
the module is js file that have a function inside of it that can be send it to another file by codeing in the end 

`module.exports= the name afunction `

# What does the word ‘require’ do?
it is pass the function from the module of=r another file in the file that we want to use it 

`require('the path of the file')`
# How do we bring another module into the file the we are working in?
by codeing in the end of the  module file 
`module.exports= the name afunction `and in the file that we want to use the module `require('the path of the file')`


# What do we have to do to make a module available?
**calling the function inside the file .js**
`module.exports= the name afunction `
`require('the path of the file')`
![](https://miro.medium.com/max/2000/1*fQyEyu_9upvynA4REV3bsw.png)
