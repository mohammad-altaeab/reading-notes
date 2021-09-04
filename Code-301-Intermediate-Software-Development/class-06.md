# 1. What is node.js?
**Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.**

**node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.**

Hmmm, “event-based”, “non-blocking”, “asynchronous I/O” — that’s quite a lot to digest in one go. So let’s approach this from a different angle and begin by focusing on the other detail that both descriptions mention — the V8 JavaScript engine.

# 2. In your own words, what is Chrome’s V8 JavaScript Engine?

V8 is the name of the JavaScript engine that powers Google Chrome. It's the thing that takes our JavaScript and executes it while browsing with Chrome.

V8 provides the runtime environment in which JavaScript executes. The DOM, and the other Web Platform APIs are provided by the browser.

The cool thing is that the JavaScript engine is independent of the browser in which it's hosted. This key feature enabled the rise of Node.js. V8 was chosen to be the engine that powered Node.js back in 2009, and as the popularity of Node.js exploded, V8 became the engine that now powers an incredible amount of server-side code written in JavaScript.

The Node.js ecosystem is huge and thanks to V8 which also powers desktop apps, with projects like Electron.

# 3. What does it mean that node is a JavaScript runtime?

However, when we say that Node is built on the V8 engine, we don’t mean that Node programs are executed in a browser. They aren’t. Rather, the creator of Node (Ryan Dahl) took the V8 engine and enhanced it with various features, such as a file system API, an HTTP library, and a number of operating system–related utility methods.

This means that Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

# 4. What is npm?

**_npm is committed to making JavaScript development elegant, productive, and safe. The free npm Registry has become the center of JavaScript code sharing, and with more than one million packages, the largest software registry in the world. Our other tools and services take the Registry, and the work you do around it, to the next level._**

the world’s largest software registry. There are over 1,000,000 packages of JavaScript code available to download, with billions of downloads per week. Let’s take a quick look at how we would use npm to install a package.

# 5. What version of node are you running on your machine?

## version@4.1.0

# 6. What version of npm are you running on your machine?

## 1.4.1

# 7. What command would you type to install a library/package called ‘jshint’?

Installing a Package Globally
Open your terminal and type the following:

```
npm install -g jshint
```

This will install the jshint package globally on your system. We can use it to lint the index.js file from the previous example:

```
jshint index.js
```

You should now see a number of ES6-related errors. If you want to fix them up, add /_ jshint esversion: 6 _/ to the top of the index.js file, re-run the command and linting should pass.

# 8. What is node used for?

Now that we know what Node and npm are and how to install them, we can turn our attention to the first of their common uses: installing (via npm) and running (via Node) various build tools — designed to automate the process of developing a modern JavaScript application.

These build tools come in all shapes and sizes, and you won’t get far in a modern JavaScript landscape without bumping into them. They can be used for anything from bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking.

We have a wide range of articles covering build tooling on SitePoint. Here’s a short selection of my favorites:

A Beginner’s Guide to Webpack
Up and Running with ESLint — the Pluggable JavaScript Linter
An Introduction to Gulp.js
Unit Test Your JavaScript Using Mocha and Chai
And if you want to start developing apps with any modern JavaScript framework (for example, React or Angular), you’ll be expected to have a working knowledge of Node and npm (or maybe Yarn). This isn’t because you need a Node back end to run these frameworks. You don’t. Rather, it’s because these frameworks (and many, many related packages) are all available via npm and rely on Node to create a sensible development environment in which they can run.


![](https://www.rokkey.com/static/25e3f50e6e9b2ffc6fb5e4d2a1327828/2bef9/node.js-use-cases.png)
# What are the 6 reasons for pair programming?

## 1. Greater efficiency

## 2. Engaged collaboration

## 3. Learning from fellow students

## 4. Social skills

## 5. Job interview readiness

## 6. Work environment readiness
# In your experience, which of these reasons have you found most beneficial?
Engaged collaboration & Learning from fellow students Because sometimes there's something missing that your mate puts on and sometimes you don't know or you have a lack of knowledge, and through cooperation you get it. 
# How does pair programming work 
 one will be the navigator and the another will be the drive and after the time they will  to change there position 

 ![](https://www.cloudsavvyit.com/p/uploads/2019/07/2350564e.png?width=1198&trim=1,1&bg-color=000&pad=1,1)
