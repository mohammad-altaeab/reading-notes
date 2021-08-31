# What is a ‘Controlled Component’?
In HTML, form elements such as `<input>, <textarea>, and <select> `typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with `setState()`.

We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a `“controlled component”`.
# Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
The most basic way of working with forms in React is to use what are referred to as “uncontrolled” form inputs. What this means is that React doesn’t track the input’s state. HTML input elements naturally keep track of their own state as part of the DOM, and so when the form is submitted we have to read the values from the DOM elements themselves.
- instant input validation: we can give the user instant feedback without having to wait for them to submit the form (e.g. if their password is not complex enough)
- instant input formatting: we can add proper separators to currency inputs, or grouping to phone numbers on the fly
- conditionally disable form submission: we can enable the submit button after certain criteria are met (e.g. the user consented to the terms and conditions)
- dynamically generate new inputs: we can add additional inputs to a form based on the user’s previous input (e.g. adding details of additional people on a hotel booking)
![](https://getbootstrap.com/docs/5.1/assets/img/bootstrap-themes.png)


# How do we target what the user is entering if we have an event handler on an input field?
When you need to handle multiple controlled input elements, you can add a name attribute to each element and let the handler function choose what to do based on the value of event.target.name
```
class Reservation extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      isGoing: true,
      numberOfGuests: 2
    };

    this.handleInputChange = this.handleInputChange.bind(this);
  }

  handleInputChange(event) {
    const target = event.target;
    const value = target.type === 'checkbox' ? target.checked : target.value;
    const name = target.name;

    this.setState({
      [name]: value
    });
  }

  render() {
    return (
      <form>
        <label>
          Is going:
          <input
            name="isGoing"
            type="checkbox"
            checked={this.state.isGoing}
            onChange={this.handleInputChange} />
        </label>
        <br />
        <label>
          Number of guests:
          <input
            name="numberOfGuests"
            type="number"
            value={this.state.numberOfGuests}
            onChange={this.handleInputChange} />
        </label>
      </form>
    );
  }
}
```
![](https://www.noorix.com.au/images/blog/hugo-bootstrap-banner.png)

# Why would we use a ternary operator?
Using a conditional, like an if statement, allows us to specify that a certain block of code should be executed if a certain condition is met.
Consider the following example:
We have a person object that consists of a name, age, and driver property.
```
let person = {
  name: 'tony',
  age: 20,
  driver: null
};
We want to test if the age of our person is greater than or equal to 16. If this is true, they’re old enough to drive and driver should say 'Yes'. If this is not true, driver should be set to 'No'.
We could use an if statement to accomplish this:
if (person.age >= 16) {
  person.driver = 'Yes';
} else {
  person.driver = 'No';
}
But what if I told you we could do the same exact thing in just one line of code? Well, here it is:
person.driver = person.age >=16 ? 'Yes' : 'No';
This shorter code yields us the same result of person.driver = 'Yes';
Now that you’ve seen the conditional ternary operator in action, we can explore how it works!
The Conditional (Ternary) Operator
First, we’ll take a look at the syntax of a typical if statement:
if ( condition ) {
  value if true;
} else {
  value if false;
}
```

# Rewrite the following statement using a ternary statement:
```
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }
  ```
 ## the answer 💯
  ~~~
  let x = ..:
let y = ...;
let bool = (x===y) ? true : false 
console.log(bool)
~~~
![](https://getbootstrap.com/docs/5.1/assets/img/bootstrap-icons.png)