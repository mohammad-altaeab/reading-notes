# All Things React

The React Roadmap to Success
React is one of the most popular JavaScript frameworks currently in use, and even if you are not using it yourself, you are no doubt at least reasonably familiar with its existence. Used primarily for the development of Single Page Applications (SPA), React is an open-source library used for web development. A lot of extra development has been done to augment the basic React offering, and the eco-system is quite large. There are many tutorials, sites and other resources that will take you from the basic elements to advanced topics for React. In fact, there are so many resources and new developments available that it can be difficult to keep track of them all. Fortunately, we've assembled a set of resources and key information about React that will be useful for beginners and experienced developers alike. Enjoy!

1. React Hot Topics
The latest and greatest, hot off the presses news about React. We've started off with a quick look at some topics that are trending today and are of particular interest to the React community. Be sure to check back here often. Web development is a fast-paced environment and what's new and hot can change frequently. Here we list some key hot topics for today but we'll update this as needed!

Render Props
When using components in React you are able to re-use your code, but it may not be clear how to share data between these components. A render prop is basically a prop whose value is a function, and which allows you to share code between components. A component with a render function will call a render prop, which takes a function that returns a React element. Then the component uses this instead of using its own render logic. The React Router and Downshift libraries both use render props. Looking at the React documentation you can see a great code example of using render props on a component to dynamically decide what to render. Here is a snippet of what that looks like:
```
class MouseTracker extends React.Component {                  
  render() {                
    return (                   
      <div>                  
        <h1>Move the mouse around!</h1>                
        <Mouse render={mouse => (               
          <Cat mouse={mouse} />             
        )}/>              
      </div>                   
    );                  
  }                   
}                         
```
You do not have to use a prop specifically called "render". Basically, any function that tells a component what to render will be considered a render prop. Be aware that when you use render props inside of a React.PureComponent the shallow prop comparison will return false for new props, which means that each render will generate a new value for your render prop.

### Context API
Passing data between components is a common hurdle when using components in any framework. One of React's solutions to this is to take advantage of the Context API. Usually one would need to pass data top-down from parent components to children components. The larger and more nested your components become, the more complicated this will be. Using createContext you can pass a value deep into the component tree without having to explicitly drill down through the components. React documentation advises users to only use this approach when you need the same data accessed in many components at multiple levels. When taking advantage of the Context API you'll first use a Provider and a Consumer:
```
React.createContext(
  const { Provider, Consumer } = React.createContext(defaultValue);
);
```
## Async Rendering & Suspense
In a tldr; version, React's new Suspense feature gives you the power to delay rendering a part of your application until a certain condition is met, With the ability to show another component like a loading spinner until the content is ready. This was introduced by Dan Abramov from the JSConf.is stage with a warning that the API will change but that it was using a real build of React. Along with suspending rendering, in order to give users a better experience regardless of their computing speed or network connection, React now has a way to make updates more asynchronous. With the new API React can start rendering but hit the server to see if there is a higher priority event that it should handle first. As Dan describes it, they've, “built a generic way to ensure that high-priority updates like user input don't get blocked by rendering low-priority updates.” To see this all in action check out Dan's demos from the talk listed above.

## CSS-in-JS
CSS-in-JS sounds just like what it is - instead of creating separate files for styling, the CSS is placed inside the JS files of the component. Writing CSS inside of your JS files may feel wrong and against your usual clean code standards, but some think this is beneficial as it helps keep everything you need for a component in one place. Actual CSS is generated when you use CSS-in-JS libraries and some even add support for non-native CSS features like nesting. Using this approach lets you stay in the context of your components, add isolation, scoped selectors, vendor prefixing, unit tests and more. Here are some of the most popular CSS-in-JS libraries: Styled Components, JSS-React, glamourous, Aphrodite and Styletron.

## Progressive Web Apps
Progressive Web Apps (PWAs) represent a new way to approach web development, especially for responsive and mobile web apps. By following a few new web APIs and a number of development practices and guidelines, PWAs are intended to allow developers to build mobile web apps that behave a lot more like natively-installed applications.

Why does this matter? Because, in reality, people primarily use native apps, not web apps, on their phones. According to comScore, people spend 87% of their on-device time in native apps, and only 13% on the mobile web.

And while we can't completely generalize why this is, native apps have a number of built-in advantages that make users more likely to engage with them over a mobile web experience, including home screen launch icons, push notifications, offline support and better performance. Generally speaking, in the eyes of consumers, native apps are more dependable.

But the other side of this coin is that native app usage is highly concentrated among a few apps, for most consumers. Many studies have found that users tend to use only a few installed apps on a regular basis, and all that time and money you are looking to spend to create a fully-native app that mimics what your web app already does might be a waste if you're not immensely sticky.

Thankfully, PWAs exist to make it easier for web developers to create mobile web apps that have many of the advantages of native apps, including installability and offline support, without having to creative a fully-native mobile app.

In practice, PWAs center around a new level of care for the experiences your users have while using your app. According to Google, one of the primary drivers of PWAs, PWAs are all about delivering user experiences that are reliable, fast and engaging. They are experiences that have the reach of the web, and which:
- Load instantly and never become nonfunctional, even in uncertain network conditions
- Respond quickly to user interactions with smooth, fluid animations and no jankiness
- Feel like a native app on the device, and provide an immersive experience



![](https://images.ctfassets.net/51xdmtqw3t2p/2w0H06U9MYaJNsonXhyD3I/0cd72a4b4e01460bcd7145e984b05c38/Portada_react.jpg?w=1100&h=800&q=50)