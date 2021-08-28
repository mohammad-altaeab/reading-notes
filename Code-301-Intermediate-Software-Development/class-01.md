## What is a component?
***A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface***            

***A component is a software object, intended to interact with other components, encapsulating certain functionality or a set of functionalities. It has an obviously defined interface and conforms to a recommended behavior common to all components within an architecture.***           

*A software component can be defined as a unit of composition with a contractually specified interface and explicit context dependencies only. That is, a software component can be deployed independently and is subject to composition by third parties.*
### Object-oriented view

A component is viewed as a set of one or more cooperating classes. Each problem domain class (analysis) and infrastructure class (design) are explained to identify all attributes and operations that apply to its implementation. It also involves defining the interfaces that enable classes to communicate and cooperate.

### Conventional view

It is viewed as a functional element or a module of a program that integrates the processing logic, the internal data structures that are required to implement the processing logic and an interface that enables the component to be invoked and data to be passed to it.

### Process-related view

- In this view, instead of creating each component from scratch, the system is building from existing components maintained in a library. As the software architecture is formulated, components are selected from the library and used to populate the architecture.

- A user interface (UI) component includes grids, buttons referred as controls, and utility components expose a specific subset of functions used in other components.

* Other common types of components are those that are resource intensive, not frequently accessed, and must be activated using the just-in-time (JIT) approach.

* sMany components are invisible which are distributed in enterprise business applications and internet web applications such as Enterprise JavaBean (EJB), .NET components, and CORBA components.
## What are the charactistics of a component?
- Reusability − Components are usually designed to be reused in different situations in different applications. However, some components may be designed for a specific task.

- Replaceable − Components may be freely substituted with other similar components.

- Not context specific − Components are designed to operate in different environments and contexts.

- Extensible − A component can be extended from existing components to provide new behavior.

- Encapsulated − A A component depicts the interfaces, which allow the caller to use its functionality, and do not expose details of the internal processes or any internal variables or state.

- Independent − Components are designed to have minimal dependencies on other components.
## What are the advantages of using component based architecture?
### Advantages
+ Ease of deployment − As new compatible versions become available, it is easier to replace existing versions with no impact on the other components or the system as a whole.

+ Reduced cost − The use of third-party components allows you to spread the cost of development and maintenance.

+ Ease of development − Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system.

+ Reusable − The use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems.

+ Modification of technical complexity − A component modifies the complexity through the use of a component container and its services.

+ Reliability − The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse.

+ System maintenance and evolution − Easy to change and update the implementation without affecting the rest of the system.

+ Independent − Independency and flexible connectivity of components. Independent development of components by different group in parallel. Productivity for the software development and future software development.

# What is props short for?
**React is a component-based library** which divides the UI into little reusable pieces. In some cases, those components need to communicate (send data to each other) and the way to pass data between components is by using **props**.
“**Props**” is a special keyword in React, which stands for properties and is being used for passing data from one component to another.
But the important part here is that data with props are being passed in a uni-directional flow. (one way from parent to child)
Furthermore, props data is read-only, which means that data coming from the parent should not be changed by child components.
# How are props used in React?
1. Firstly, define an attribute and its value(data)
2. Then pass it to child component(s) by using Props
3. Finally, render the Props Data
In my previous article, I’ve shown how to create & call a React component inside another component. So in this example, we have a **ParentComponent** including another component (child):
```
class ParentComponent extends Component {  
  render() {
    return (
      <h1>
        I'm the parent component.
        <ChildComponent />
      </h1>
    );
  }
}
```
And this is our ChildComponent:
```
const ChildComponent = () => {  
  return <p>I'm the 1st child!</p>; 
};
The problem here is that, when we call the ChildComponent multiple times:
class ParentComponent extends Component {  
  render() {
    return (
      <h1>
        I'm the parent component.
        <ChildComponent />
        <ChildComponent />
        <ChildComponent />
      </h1>
    );
  }
}
```

But what we like to do here is to get dynamic outputs, because each child component may have different data and let’s see how we can solve this issue by using props…
1st Step: Defining Attribute & Data
We already know that we can assign attributes and values to HTML tags:
```
<a href="www.google.com">Click here to visit Google</a>;
```
Likewise, we can do the same for React components. We can define our own attributes & assign values with interpolation { }:
```
<ChildComponent someAttribute={value} anotherAttribute={value}/>
```
Here I’m declaring a “text” attribute to the ChildComponent and then assign a string value: “I’m the 1st child”.
```
<ChildComponent text={“I’m the 1st child”} />
```
Now the ChildComponent has a property and a value. Next, we need to pass it via Props.
2nd Step: Passing Data using Props
OK, now let’s take the “I’m the 1st child!” string and pass it by using props.
Passing props is very simple. Like we pass arguments to a function, we pass props into a React component and props bring all the necessary data.
Arguments passed to a function:
```
const addition = (firstNum, secondNum) => {  
  return firstNum + secondNum; 
};
```
Arguments passed to a React component:
```
const ChildComponent = (props) => {  
  return <p>I'm the 1st child!</p>; 
};
```
Props are arguments passed into React components. — w3schools.com
Final Step: Rendering Props Data
Alright so far, we have created an attribute and its value, then we passed it through props but we still can’t see it because we haven’t rendered it yet.
Prop is an Object
In the final step, we will render the props object by using string interpolation:
```
{props}
```
But first log props to console and see what it shows:
```
console.log(props);
```
As we can see, Props returns back an object. In JavaScript, we can access to object elements with dot(.) notation. So, let’s render our text property with interpolation:
```
const ChildComponent = (props) => {  
  return <p>{props.text}</p>; 
};
```
# What is the flow of props?
ReactJS comes with a slew of new words and new definitions for existing ones. “Props” is no exception.
To understand the meaning of “props” in ReactJS, I turned to the context where it is used — in this case, React components.
## Components tell React what you want to render
Facebook introduced declarative components, or components for short, as the heart of ReactJS (2). In fact, everything in ReactJS is a component made up of cheap-to-create React Elements. Components return exactly one DOM element having only one parent element. If you are using JSX, for example, you can only have one parent HTML element and all other elements must be children nested under that parent.
![](https://miro.medium.com/max/875/1*nvQ3jAPwnU7cnlLMPNJnzA.png)
## Components vs. JS functions
Breaking components down further, components are “conceptually like JavaScript functions. They accept arbitrary, read-only inputs (props) and return React elements describing what should appear on the screen.” (4) What does that mean for you and me? It means that our components can be more dynamic and a lot more reusable. (Learn.co Props)
As far as conventions go, Component names are always capitalized - so you’ll know a component when you see one in React.
## The Anatomy of a Basic Component
As any good JavaScript function would do, in order to return a value other than the default, a component must have a return statement that specifies the value to return. In this case, the default return value is undefined.(3) There are only two requirements that define a JavaScript function as a React component:
1. The function accepts a single “props” object argument with data
2. It returns a React element
![](https://miro.medium.com/max/875/1*bsS8ETUQqgBpAoT2D6tjmw.png)

