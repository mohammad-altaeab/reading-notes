## 1. What does .map() return?
use the map() function to take an array of numbers and double their values. We assign the new array returned by map()
## 2. If I want to loop through an array and display each value in JSX, how do I do that in React?
You can build collections of elements and include them in JSX using curly braces {}.

Below, we loop through the numbers array using the JavaScript map() function. We return a <li> element for each item. Finally, we assign the resulting array of elements to listItems
## 3. Each list item needs a unique ____.
The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys:
```
const todoItems = todos.map((todo) =>
  <li key={todo.id}>
    {todo.text}
  </li>
);
```

## 4. What is the purpose of a key?
Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity
![](https://vegibit.com/wp-content/uploads/2019/04/react-set-attribute-prop.png)
## 1. What is the spread operator?
The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.
in JavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments.
The spread operator was added to JavaScript in ES6 (ES2015), just like the rest parameters, which have the same syntax: three magic dots …
## 2. List 4 things that the spread operator can do.
Spread operator to the rescue! It looks similar to rest parameters, also using ..., but does quite the opposite.
* Copying an array
* Concatenating or combining arrays
* Using Math functions
* Using an array as arguments
* Adding an item to a list
* Adding to state in React
* Combining objects
* Converting NodeList to an array
## 3. Give an example of using the spread operator to combine two arrays.
```
const myArray = [`🤪`,`🐻`,`🎌`]
const yourArray = [`🙂`,`🤗`,`🤩`]
const ourArray = [...myArray,...yourArray]
console.log(...ourArray) // 🤪 🐻 🎌 🙂 🤗 🤩
```


## 4. Give an example of using the spread operator to add a new item to an array.
```
const fruits = ['🍏','🍊','🍌','🍉','🍍']
const moreFruits = [...fruits];
console.log(moreFruits) // Array(5) [ "🍏", "🍊", "🍌", "🍉", "🍍" ]
fruits[0] = '🍑'
console.log(...[...fruits,'...',...moreFruits]) //  🍑 🍊 🍌 🍉 🍍 ... 🍏 🍊 🍌 🍉 🍍
```
## 5. Give an example of using the spread operator to combine two objects into one.
```
let A = {
    name: "geeksforgeeks",
};
  
let B = {
    domain: "https://geeksforgeeks.org"
};
  
let Sites = { ...A, ...B };
  
console.log(Sites)
```
![](https://scriptverse.academy/img/tutorials/reactjs-update-array-state.png)
## 1. In the video, what is the first step that the developer does to pass functions between components?

There can be multiple ways of passing data from one component to another :
Using Props. You can use props to pass data from parent to child component. ...
Using React ContextAPI or State management library like Redux. ...
Using Props as Callback Function
## 2. In your own words, what does the increment function do?
increment function pass through state people and search for the name matching using map and when loop throw if then name matched the count will increase by one by using the key to increase for the specific name
## 3. How can you pass a method from a parent component into a child component?
### So let's first see how the data flows during this :
- A parent component defines a function
- The function is passed as a prop to a child component
- The child component then invokes the prop
- The parent function is then called, usually changing something
- Then the parent component is re-rendered along with its children


Now let's see how it's done. I'm going to discuss two ways of doing it. The first one has some cons and the second one is a better approach.


1) Passing method as a prop using the arrow function :

### Bakery.js
```
import New from "./New";

class Bakery extends React.Component {
  constructor(props) {
    super(props);
  }

  bake(e) {
    alert(e); // it will execute when child component will invoke it
  }

  render() {
    let e = "Baked!";
    return (
      <div>
        <h1>Bakery!!!</h1>
        <New functionBake={() => this.bake(e)} /> {/* child component is called with a prop passing the function using arrow function */}
      </div>
    );
  }
}

ReactDOM.render(<Bakery />, document.getElementById('root'));
```

### New.js
```
class New extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <div>
        <h1>New</h1>
        <button onClick={this.props.functionBake}>Bake!!!</button> {/* event handler calling the function from parent class */}
      </div>
    );
  }
}
```
export default New;
## 4. How does the child component invoke a method that was passed to it from a parent component?
```
export default function Parent() {
	const myref=useRef();

        const handleOnClick = () => {
           if(myref.current) {
              myref.current.sayHi();
           }
        }

	return (
            <Child ref={myref} />
	    <button onClick={handleOnClick}>Click me</button>
	);
}
export default function Child() {
	const sayHi = () => {
		console.log('hi');
	};
	return (<div>Hello</div>);
}
```
In order to execute a function from a child component, you will need to use Refs. React supports a special attribute that you can attach to any component, that's the ref attribute, it takes a callback function, and you can access the functions of the child component in the parent accessing this.refs.REF_NAME.METHOD_NAME.

We are going to create a Parent element, it will render a <Child/> component. As you can see, the component that will be rendered, you need to add the ref attribute and provide a name for it. Then, the triggerChildAlert function, located in the parent class will access the refs property of the this context (when the triggerChildAlert function is triggered will access the child reference and it will has all the functions of the child element).
```
class Parent extends React.Component {
    triggerChildAlert(){
        this.refs.child.showAlert();
    }

    render() {
        return (
            <div>
                {/* Note that you need to give a value to the ref parameter, in this case child*/}
                <Child ref="child" />
                <button onClick={this.triggerChildAlert}>Click</button>
            </div>
        );
    }
}
```
![](https://idkblogs.com/images/react/react_idk.png)
## Things I want to know more about