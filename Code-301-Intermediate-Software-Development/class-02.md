
# What types of things can you pass in the props?
*props you can think about is like arguments to a function when you create a component inside a reactant you want to render it you're going to pass at the price that you want to give to it. For example, essay that we have a counter application. The thing that you're most likely going to pass to that counter is going to be the initial count essentially what your account should start at. So you're going to pass your counter component its initial count inside of the props. And the reason we're using props for this is because it is kind of four things that you passed like a function there what you want to initialize your component to or what you want your component to render like so in this counter example, we want our initial count to be were going to pass that threw in the props something else that you can think of where you might need process. Let's say that you want to display something's to user that has a title and subtitle you're going to also store that in the props because what you want your function or your component actually take is going to be the problem in our case. Our component is to write a title. Subtitle for passing those to the props and then our application knows if those props change at some point. So for example, something else their application changes those props it'll rear-ender that component for us because I turned out different but stay on the other hand is quite a bit different state is something inside of a component.*
![](https://i.stack.imgur.com/3pkGz.jpg)
# What is the big difference between props and state?
**It's quite a bit different state is something inside of a component to the big difference between props and state is props you passed into a component and state is handled inside of that component and props are handled outside the component. So in the example of our counter application, your current up-to-date count is handled inside of the state. So while we passed in the initial count in our props or just saying our state to account and then inside of our component that's handling our counter. We actually manage updating our counter to increase or decrease it depending on what the user does the big difference between State and props and you can update it inside the cab while props or handle outside the component and must be updated outside of the component**
![](https://i.ytimg.com/vi/aLmwln09Tbs/maxresdefault.jpg)

# When do we re-render our application?
***when you change the state inside of your application is going to render that section your application. You can't actually change them. You need to change them outside the most likely it's going to be state store somewhere else in your application that's being passed down as props going back to our subtitle and most likely this component is not going to have any state at all cuz it's all it's doing is rendering some text. I meant text is never going to change. There's nothing in that component that can change so it doesn't need anything going to take those two props and display them in and all the component does which is great. It's just super simple, but what they counter we're actually updating the account. So we need state to store that thing that we're going to be updating and that's really worst state is there for when you need to actually rear-ender and update your application based on something that user has done. So if you want to change something in your application you need to store that in-state, so it'll probably render. Actually changes cross on the other hand are useful for when you want to display some information inside of the component without hard coating it essentially it's a variable to a function. You can also think about it when you create a class instructor class are going to be the things that are your props for component in react. So, for example, we're going to be passing that title and description down because we want to render those don't just want a component that renders the same title description description to be different. So we're going to use props in order to make that Dynamic on it. But with our counter application, we have some count that we need to update instead of our state we're going to use state to make sure we continually are able to update that based on user input***
# What are some examples of things that we could store in state?
example of a form you have an input element check box Lucky Box, whatever it is that needs to be able to be updated by the user. So we're going to actually use State just or what they're updating at Value to and what they're changing about you too, and so on the place where people get confused and wondering
![](https://i.stack.imgur.com/wqvF2.png)
## 1. Rebuilt with React
**~~React-Bootstrap replaces the Bootstrap JavaScript. Each component has been built from scratch as a true React component, without unneeded dependencies like jQuery.~~**

As one of the oldest React libraries, React-Bootstrap has evolved and grown alongside React, making it an excellent choice as your UI foundation.
## 2. Bootstrap at its core
Built with compatibility in mind, we embrace our bootstrap core and strive to be compatible with the world's largest UI ecosystem.

By relying entirely on the Bootstrap stylesheet, React-Bootstrap just works with the thousands of Bootstrap themes you already love.

## 3. Accessible by default
The React component model gives us more control over form and function of each component.

Each component is implemented with accessibility in mind. The result is a set of accessible-by-default components, over what is possible from plain Bootstrap.
# React: Component Lifecycle Events
## What are component lifecycle events?
React lets you define components as classes or functions. The methods that you are able to use on these are called lifecycle events. These methods can be called during the lifecycle of a component, and they allow you to update the UI and application states.
![](https://miro.medium.com/max/2000/0*0saPKFiTUk6W3FYp)
### Mounting
When an instance of a component is being created and inserted into the DOM it occurs during the mounting phase. Constructor, static getDerivedStateFromProps, render, componentDidMount, and UNSAFE_componentWillMount all occur in this order during mounting.
Updating
Anytime a component is updated or state changes then it is rerendered. These lifecycle events happen during updating in this order.
static getDerivedStateFromProps, shouldComponentUpdate, render,
getSnapshotBeforeUpdate, componentDidUpdate, UNSAFE_componentWillUpdate, UNSAFE_componentWillReceiveProps
### Unmounting
The final phase of the lifecycle if called when a component is being removed from the DOM. componentWillUnmount is the only lifecycle event during this phase.
constructor()
The constructor for a React component is called before it is mounted.If the component is a subclass you should call super(props), or the props will be undefined. constructors can be used to assign state using this.state or to bind event handle methods to an instance. Let’s take a look at some example code.
```
class FishTableRow extends React.Component {
constructor() {
super(props); //gives us access to props
//Don’t call this.setState() here
this.state = { //intitialize local state
showDescription: false
}; }
```
Avoid using this.setState() in the constructor because it can lead to side effects, and it is unnecessary. Doing this will ignore all updates to props, so it shouldn’t be done unless it is intentional.
static getDerivedStateFromProps()
This method exists for rare cases where the state relies on changes in props over time.
render()
Render is the only required method in a class component. It will examine this.props and this.state when called. The render function should not modify the component state because it would cause a lot of bugs by changing the state every time it rerenders. I also should not directly interact with the browser. render will not be invoked if shouldComponentUpdate() returns false. Here is an example of using render.
```
ReactDOM.render(
<FishTable fishes= {fishData}/>,//set fishes document.getElementById(‘app’)
);
```
### componentDidMount()
This method is invoked immediately after a component is mounted. If you need to load anything using a network request or initialize the DOM, it should go here. This method is a good place to set up any subscriptions. If you do that, don’t forget to unsubscribe in componentWillUnmount().
setState() can be called here, but it should be used sparingly, because it will cause a rerender, which can lead to perfomance issues.
Here we use componentDidMount() to connect to the YouTube API and get videos when the components is rendered.
```
componentDidMount() {
console.log(‘got videos’);
this.getVideos(‘cats’);
}
getVideos(query) {
var options = {
key: this.props.YOUTUBE_API_KEY,
query: query
};
```
## Things I want to know more about