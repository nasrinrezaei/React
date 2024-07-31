 
<details>
<summary> Some fundamental knowledge</summary>

## SPA
Before any framework each page needs a request to the server to be got and an HTML page with CSS and JS is returned to the user’s browsers and this process is done for all links of pages. Furthermore, SPA applications like React are introduced in which efficient JS codes create and manipulate the dom, and just an HTML page once is got when a user clicks on a link to see a website, and JS links handle other changes of displaying the page and interacting with parts of it. To be exact when user click on a link to see a website the broswer gets an HTML file in which there are links of JS and CSS files of website.
## NPM
It is a node package manager and these packages are just node-related libraries which are created by different tool developers
that can help us with node and JS projects like React projects and we can download them by NPM. Indeed, by NPM we can install libraries globally or locally. The point is that when we run npm i -g create-react-app you just download the latest version of the React library then you should run it and when it is updated you should install the new version.

## NPX
By using NPX when you run npx creat-react-app app-name, the npx installs and runs creating and downloading React then deletes it and by doing so you can always have projects with the latest version of React
</details>


# React

# Why React?
<details>
<summary> 1. Don't touch the DOM. I'll do it. </summary>
  
### .What is DOM?
DOM (document object model) is what the browser uses to display a web app and JS simply manipulates this DOM. 
### .Declarative vs Imperative
#### Imperative
Imperative programming is instructional and cares about the step-by-step process.
#### Declarative
Declarative programming is driven by the result and describing this end result rather than the step-by-step process of getting to the result.
### For example

```ruby
//Imperative 
function addArtistNameToBody() {
  const bodyTag = document.querySelector('body')
  const divTag = document.createElement('div')
  let h1Tag = document.createElement('h1')
  h1Tag.innerText = "Mitski"
  divTag.append(h1Tag)
  bodyTag.append(divTag)
}
```
```ruby
//Declarative
class Artist extends Component {
  render() {
    return(
      <div>
        <h1>{this.props.name}</h1>
      </div>)
  }
}
```

The first is a prime example of the imperative search as it lays out each step of how the search function works and how it got to the result. This really illustrates the HOW and gives discrete ‘instructions’ to get to the desired result. In contrast, the declarative example focuses on purely the result and describes what this result will look like.
##.Differences between Declarative programming and Imperative one in changing DOM
In fact, in Imperative programming, you should tell JS what should do step by step to change the DOM in order for showing what you want as a result of an action of the user. Still, by Declarative programming it is React that decides what changes should be done to show what you want. Moreover, you just need to declare what the final state is and it finds the best way to do so inasmuch as changing DOM is a really expensive and it must done beneficially.

</details>
<details>

<summary> 2. Build websites like lego blocks.</summary>

### .Component Architecture
React has the idea of creating components for our web. Indeed, components are small and large parts of our app which are used to create our app. Generally, they are used in different sections of our project even in other projects. The point is that in React the components are simple JS functions which receive some data and inputs as props and return HTML inside of JS. In addition, components can be defined as functions or classes in React.
### Class component
```ruby
class Car extends React.Component {
  render() {
    return <h2>Hi, I am a Car!</h2>;
  }
}
```
```ruby
### Function Component
function Car() {
  return <h2>Hi, I am a Car!</h2>;
}
```
</details>

<details>
<summary> 3. Unidirectional data flow.</summary>
  
### What is Virtual DOM?

 In our React app, we have states which contain our data and JSX components. In fact, the React library function uses them as inputs to create Virtual Dom. Virtual Dom is a JS tree-liked object that describes our app and says React and how it should update the actual DOM.
### What is unidirectional data flow?
It means that the flow of changing Virtual DOM and passing data is from the parent components to their children and consequently one-way data flow makes debugging much easier. When the developer knows where the data is coming from and where it is going, they can dry run (or use tools) to find the problems more efficiently.
</details>

<details>
<summary> 4. UI, The rest is up to you.</summary>

  
Because React is just a library to create the Virtual DOM to change the UIs of different apps it can be used in other types of applications namely Desktop applications, and VR applications.

The point is that when we install the React library we install both the core React library to create Virtual DOM and the React Dom library which interacts with the actual DOM and implements Virtual DOM’s changes on the actual DOM on the browser.
</details>

> [!NOTE]
> What is JSX?
> It is an HTML code inside the JS function.

# Differences between React and React DOM

 React
 
React is the core library for building user interfaces in a component-based architecture. It provides the tools for defining and managing UI components and their state.

 React DOM
 
React DOM is a separate package that provides DOM-specific methods for React. It serves as the bridge between React components and the actual DOM, enabling React to interact with the browser's DOM.

# what exactly is react-scripts?
Well, simply put, it’s an NPM package that is designed by Facebook and is used by Create React App to perform all the heavy lifting such as module bundling so that you don’t have to manage a Webpack file.
### What do these four React Scripts do?
 Well, think of it like this; how would you start a React app without npm start?
You’d likely do the following:
1. You’d create a basic HTML file and include a div element with the id of root to let React render its components.
2. You’d then write React code using JSX with the help of React and ReactDOM libraries.
3. You’d transpile and bundle your code using Babel and Webpack.
4. You’d point your transpiled JavaScript code in the HTML file you created back in Step 01 using a <script> tag.

This is an old school approach to building React. It’s time-consuming, error-prone and doesn’t add business value. Therefore, react-scripts start replaces the following process by automating the process with the single command. So, as a user, all you have to do is run the command npm start which would trigger react-scripts start, which would perform steps 1 to 4 automatically and launch the React app for development purposes.

<details>
  <summary> npm start</summary>
  
This command will start the development server, and it will also react and display the latest version each time a change occurs with the webpack’s Hot Module Replacement (HMR) feature. In addition, it will show lint errors on the terminal if it fails to start the server in the form of meaningful error messages.

### Rendering
In our app we have main.jsx or index.js file in which this code is located 
```ruby
ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
)
```
The point is that what exactly happened in ‘npm start’ command is that it renders the react app and runs it on the local server
This code means that react dom should render the entire app that is in App component in root element which is in index.html file
</details>
<details>
   <summary> npm build</summary>
  
Building a React app involves compiling the application's source code into a format that can be efficiently delivered and executed in a web browser. This process typically includes several steps, which ensure that the app is optimized for performance and compatibility across different environments. Here’s an overview of what building a React app entails:

1. Source Code Compilation:

   . React apps are often written using modern JavaScript features (ES6+), JSX (JavaScript XML), and CSS-in-JS.
   
   . During the build process, tools like Babel are used to transpile the code into a format compatible with all browsers, converting modern JavaScript and JSX into plain JavaScript.
   
2. Bundling:

   . Bundlers like Webpack or Vite are used to combine the app's JavaScript, CSS, and other assets into a few optimized bundles.
   
   . These bundles are typically minimized to reduce file size and improve loading times.
   
3. Minification and Optimization:

   . The build process includes minifying the JavaScript and CSS files to remove unnecessary characters (like whitespace and comments) and reduce the file sizes.
   
   . Other optimizations, such as tree shaking (removing unused code), are performed to make the app more efficient.
   
4. Asset Management:
   
   . Assets like images, fonts, and other static files are processed and copied to the build directory.
   
   . This may include optimizing images and generating hashed filenames for cache busting.
   
5. Environment Configuration:

   . Environment variables can be configured to differentiate between development and production settings.
   
   . This might include API endpoints, feature flags, and other configurations that vary between environments.
   
6. Generating the Build Output:
    
    . The build process outputs the final static files (HTML, CSS, JavaScript, images, etc.) into a build or dist directory.
    
    . These files are ready to be served by a web server.
    
7. Running the Build Command:
    
    . Most React projects use tools like Create React App, Next.js, or custom Webpack configurations.
   
    . Running a command like npm run build or yarn build initiates the build process.
   
9. Deployment:
    
   . The build output is deployed to a web server or a hosting service.
   
   . Popular options include services like Vercel, Netlify, GitHub Pages, AWS S3, and traditional web hosting services.
   
In summary, building a React app transforms your development code into optimized, production-ready files that can be efficiently loaded and executed in web browsers, ensuring your app performs well and is accessible to users.
</details>
<details>
   <summary> npm eject</summary>
  
  ### Babel
  
  Babel is a widely-used JavaScript compiler which can compile the latest JS codes to the basic codes that can be understandable for all browsers. It helps in transforming new and upcoming JavaScript standards (ES6/ES2015+ and beyond) into a version of JavaScript that is compatible with older browsers and environments.
  
  ### Webpack
  
  Webpack is a powerful and popular module bundler for JavaScript applications. It takes modules with dependencies and generates static assets representing those modules.
  
  ### Main function of eject
  
 The main function of eject is that we can modify and change the process of Babel and Webpack's job and run npm reject to execute the different and modified processes.
</details>

# What are components?
  
  Components are the basic units of the UI of a React app. In fact, the UI of  a site is broken down into different components and each component has its own logic and UI.
  There are two different types of components:
 1. Functional components
 2. Class components
### For example

```ruby
// Functional components
function WelcomeMessage(props) {  
  return <h1>Welcome, {props.name}</h1>;  
}
```
```ruby
// Class components
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

> [!TIP]
> At the end both of them are used to say React what should render.

> [!NOTE]
> The point about the JSX HTML tags is that, they are components which are created by react to attach the event handelers and other options to the components instead of using pure JS and as a result some atributes' name vary from the atributes of HTML tags. 

# What is local state or state?
States are the information which just a component which these states are defined in, are aware. In addition, they can keep the changes of data in the curtain component.

### Hooks

In React, hooks are functions that allow you to use state and other React features and lifecycles in functional components. 

1. Built-in Hooks:
 React provides several built-in hooks, such as useState, useEffect, useContext, useReducer, and more. Each hook serves a specific purpose in managing state, handling side-effects, or accessing context.

2. Custom Hooks:
 You can also create custom hooks to encapsulate reusable stateful logic that can be shared across components. Custom hooks follow the naming convention useSomething to denote that they are hooks.


## How we can define states?

<details>
  <summary> Class components</summary>

  ### Constructor
  In React class components, the constructor is a special method used for initializing the component's state and binding event handlers. The constructor is called before the component is mounted and is the first method called when an instance of the component is created.

### Super
In React class components, super is a keyword used to call the constructor of the parent class. When you define a class component, it typically extends React.Component, which is the parent class. The super call is necessary to properly initialize the component and ensure that the component inherits the properties and methods from React.Component.

### Basic Example
Here is a simple example that shows how to define and use state in a React class component:
```ruby
import React, { Component } from 'react';

class Counter extends Component {
  constructor(props) {
    super(props);
    // Initialize state
    this.state = {
      count: 0,
    };
  }

  incrementCount = () => {
    // Update state
    this.setState((prevState) => ({
    //prevState is the value which was in the count before changing it
      count: prevState.count + 1,
    }));
  }

  render() {
    return (
      <div>
        <p>Count: {this.state.count}</p>
        <button onClick={this.incrementCount}>Increment</button>
      </div>
    );
  }
}

export default Counter;
```
### Detailed Breakdown

1. Constructor:
   
   . The constructor is used to initialize the component’s state.
   
   . The super(props) call is necessary to properly initialize the component and allow access to this.props.
   
2. State Initialization:

   . The state is initialized as an object with a count property set to 0.
   
   . this.state holds the initial state of the component.

4. Updating State:

   . The incrementCount method updates the state using this.setState.
   
   .this.setState is called with a function that takes the previous state and returns an updated state object.

   .This approach ensures the correct state update when the new state depends on the previous state.

5. Rendering:

   . The render method returns JSX that displays the current state and includes a button to trigger the state update.

</details>
<details>
   <summary> Function components</summary>
   In React functional components, state management is handled using the useState hook. The useState hook allows you to add state to functional components, making them capable of managing and updating state just like class components.
  ### Basic Example
Here's a simple example of using state in a functional component:
  
```ruby
import React, { useState } from 'react';

const Counter = () => {
  // Initialize state with useState hook
  const [count, setCount] = useState(0);

  const incrementCount = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={incrementCount}>Increment</button>
    </div>
  );
};

export default Counter;

```
### Detailed Breakdown

1. useState Hook:

   . const [count, setCount] = useState(0); initializes the state.

   . count is the current state value.

   . setCount is the function used to update the state.

   . useState(0) sets the initial state value to 0.
   
4. Updating State:

   . setCount(count + 1); updates the state when the button is clicked.

3. Rendering:

   . The component renders the current state value and includes a button to trigger the state update.

</details>

## Why by changing state, the class component will re-render?
To be exact when you change the value of a state object in the class component the JS in React will point to another object as a state in the component consequently by doing so the component understands that the state has been changed and re-render the DOM. The fact is that if you change the value of a state without using setstate method the component can not figure out that the state has been changed inasmuch as the state points to the same object compared with before it was changed.

## What is a shallow merge?
When you use the setState method in a React class component, React performs a shallow merge of the new state with the existing state. This means that only the properties specified in the setState call will be updated, while other properties in the state will remain unchanged.

## Example of Shallow Merge

Consider the following example of a React class component with a state object containing multiple properties:
  
```ruby
class UserProfile extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: 'John Doe',
      age: 30,
      location: 'New York'
    };
    this.updateName = this.updateName.bind(this);
  }

  updateName() {
    this.setState({ name: 'Jane Smith' });
  }

  render() {
    return (
      <div>
        <p>Name: {this.state.name}</p>
        <p>Age: {this.state.age}</p>
        <p>Location: {this.state.location}</p>
        <button onClick={this.updateName}>Update Name</button>
      </div>
    );
  }
}


```

Explanation

1. Initial State:
   
   . The initial state is set in the constructor with three properties: name, age, and location.
   
3. State Update:
   
   . When the updateName method is called (e.g., by clicking the button), setState is used to update the name property of the state.
   
   . The setState call looks like this: this.setState({ name: 'Jane Smith' }).
   
5. Shallow Merge:
   
   . React performs a shallow merge, meaning it updates only the name property and leaves age and location unchanged.
   
   . The new state will be: { name: 'Jane Smith', age: 30, location: 'New York' }.
   
## Asynchronous setState

The setState method in React is considered asynchronous because it doesn't immediately mutate the state object. Instead, it schedules an update to the component's state and informs React that this component and its children need to be re-rendered with the updated state. This allows React to batch multiple state updates together and optimize rendering for better performance. Let's delve deeper into the reasons and mechanisms behind this asynchronous behavior:

# Batching of State Updates

React's setState is asynchronous primarily to enable batching. Batching refers to the process of grouping multiple state updates and re-renders into a single update cycle. This helps improve performance by reducing the number of renders and DOM updates.

# Event Loop and State Update Mechanism

When setState is called, React schedules an update. This update is placed into an internal queue, and React processes this queue in the next event loop tick. This delay allows React to batch multiple updates together.

# Example of Asynchronous setState

Consider the following example:

```ruby
class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
    this.increment = this.increment.bind(this);
  }

  increment() {
    this.setState({ count: this.state.count + 1 });
    console.log(this.state.count); // This might log the old state value
    this.setState({ count: this.state.count + 1 });
    console.log(this.state.count); // This might still log the old state value
  }

  render() {
    return (
      <div>
        <p>Count: {this.state.count}</p>
        <button onClick={this.increment}>Increment</button>
      </div>
    );
  }
}

```

# Explanation

1. First setState Call:

   . this.setState({ count: this.state.count + 1 }); schedules an update where count is incremented by 1.

   . The state is not immediately updated. Instead, it is placed in a queue.

2. Console Log:

   . console.log(this.state.count); is called immediately after the first setState. At this point, the state has not yet been updated, so it logs the old value of count.

3. Second setState Call:

   . this.setState({ count: this.state.count + 1 }); schedules another update. Since the state has not yet been updated, this call is also based on the old state.

4. React Processes Updates:

   . React processes the state updates at the end of the event loop. It batches the updates together and then updates the state.

   . The component re-renders with the new state.

# Using Functional setState

To handle state updates correctly, especially when the new state depends on the previous state, you should use the functional form of setState:

```ruby
increment() {
  this.setState((prevState) => ({ count: prevState.count + 1 }));
  this.setState((prevState) => ({ count: prevState.count + 1 }));
}
```

# Explanation of Functional setState

1. First Functional setState Call:

   . this.setState((prevState) => ({ count: prevState.count + 1 })); schedules an update. React internally keeps track of prevState, ensuring it references the current state at the time of processing.

2. Second Functional setState Call:

   . this.setState((prevState) => ({ count: prevState.count + 1 })); schedules another update, again referencing the current state at the time of processing.

3. React Processes Updates:

   . React processes both updates, ensuring that each update correctly references the most recent state.

# Asynchronous Nature and Callback

To execute code after the state has been updated, you can pass a callback function as the second argument to setState:

```ruby
this.setState({ count: this.state.count + 1 }, () => {
  console.log(this.state.count); // This logs the updated state value
});
```
> [!NOTE]
> Asynchronous is a non-blocking architecture, so the execution of one task isn't dependent on another. Tasks can run simultaneously. Synchronous is a blocking architecture, so the execution of each operation depends on completing the one before it. Each task requires an answer before moving on to the next iteration.
> 
## Why keys are important in a loop?

The point is that by dedicating the key to each item of a loop, React can just re-render the modified item in case of changing it’s data. Moreover if you check the DOM on console, you can see there are no keys on elements and the keys are just used by React to identify each item.

## What is componentDidMount() method?

componentDidMount is a lifecycle method in React class components that is called once immediately after a component is mounted (inserted into the tree). It is an ideal place to perform side effects, such as data fetching, subscriptions, or manual DOM manipulations. Here are the key aspects of componentDidMount:

### Key Features of componentDidMount

1. Runs After Initial Render:
   
   . componentDidMount is invoked immediately after the first rendering of the component. This means that the component's initial HTML has been rendered and is now part of the DOM.
   
2. Perfect for Side Effects:
   
   . Since it runs after the component is mounted, componentDidMount is an ideal place for side effects. This includes fetching data from an API, setting up subscriptions, initializing         third-party libraries, and other actions that require a DOM node to be present.

3. Safe to Update State:

## Immutability
Immutability means that an object cannot be modified after it is created. Instead of changing the original object, any update or modification results in the creation of a new object. This concept is often contrasted with mutability, where objects can be altered directly.

### Example of Mutable vs Immutable Operations

Mutable Example:

```ruby
let person = { name: "John", age: 30 };
person.age = 31; // The person object is directly modified.
```

Immutable Example:

```ruby
let person = { name: "John", age: 30 };
let updatedPerson = { ...person, age: 31 }; // A new object is created with the updated age.

```

### Immutability in React

In React, immutability is crucial for several reasons:

1. State Management: React components often rely on state to manage dynamic data. Immutable state updates ensure that the state changes are predictable and trackable.
2. Re-rendering Optimization: React uses a virtual DOM to optimize re-rendering. By leveraging immutability, React can quickly determine which parts of the state have changed, making the reconciliation process more efficient.
3. Pure Components: Immutability helps in writing pure components, which are easier to test and debug. Pure components render the same output for the same input props and state, ensuring predictable behavior.

### Example in React

Consider a state update in a React component:

### Mutable State Update (Not Recommended):

```ruby
const [items, setItems] = useState([1, 2, 3]);

const addItem = () => {
  items.push(4); // Directly modifying the state (mutable)
  setItems(items); // Updating the state with the modified array
};

```

### Immutable State Update (Recommended):

```ruby
const [items, setItems] = useState([1, 2, 3]);

const addItem = () => {
  setItems([...items, 4]); // Creating a new array with the updated item (immutable)
};


```
# Anonymous function

In React, an anonymous function is a function that is defined without a name. Anonymous functions are often used as callbacks or event handlers in JSX. These functions can be declared inline within JSX, which is a common pattern in React development.

## Examples and Use Cases

1. Inline Event Handlers: Using an anonymous function directly in the onClick attribute.

```ruby
<button onClick={() => alert('Button clicked!')}>Click me</button>


```
2. Passing Arguments to Event Handlers: When you need to pass arguments to an event handler.

```ruby
<button onClick={() => handleClick(item.id)}>Click me</button>

```
3. Conditional Rendering: Using an anonymous function within JSX to conditionally render content.
   ```ruby
   {items.map((item, index) => (
      <div key={index} onClick={() => handleItemClick(item)}>
        {item.name}
      </div>
    ))}
    ```
## Pros and Cons

### Pros:
. Conciseness: Anonymous functions can make the code more concise and readable, especially for simple operations.
. Scoping: They automatically capture the scope they are defined in, which can be useful for accessing props and state without additional binding.

### Cons:
. Performance: Defining functions inline can lead to performance issues because a new function is created every time the component renders. This can cause unnecessary re-renders, especially in lists or frequent updates.

. Readability: While they can be concise, using too many anonymous functions can also make the code harder to read and debug.

## Best Practices

Avoid Inline Functions in Render Methods: When possible, define event handlers and other functions outside of the render method to avoid performance issues.

  ```ruby
       class MyComponent extends React.Component {
      handleClick = () => {
        alert('Button clicked!');
      }
    
      render() {
        return (
          <button onClick={this.handleClick}>Click me</button>
        );
      }
    }
 ```
# Props

In React, props can cause a component to re-render under certain conditions. Here's a detailed explanation of how this process works:

## 1. Initial Render

When a React component is initially rendered, it goes through the following lifecycle:

. The component's constructor is called.

. The render method is called, and the component's output (typically JSX) is returned.

. React then updates the DOM to reflect the rendered output.

## 2. Prop Changes Trigger Re-render

When a component's props change, React will trigger a re-render of that component. This happens as follows:

. The parent component re-renders and passes new or updated props to the child component.

. React compares the previous props with the new props.

. If the new props are different (by reference for objects/arrays or by value for primitives), React will schedule an update for the component.

## 3. Component Re-render Lifecycle

When a component receives new props, it goes through the following lifecycle methods (if defined):

. shouldComponentUpdate(nextProps, nextState): This method allows the component to decide whether it should re-render or not. By default, it returns true, but you can override it to return false if you determine that the component should not update. This can help optimize performance.

. componentWillReceiveProps(nextProps): This method is called before rendering when new props are received. (Note: This method is deprecated in favor of static getDerivedStateFromProps.)

. static getDerivedStateFromProps(nextProps, prevState): This is a static method that is called right before rendering. It allows the component to update its state based on the received props. This is the recommended method to use instead of componentWillReceiveProps.

. render(): The render method is called again to determine the updated output based on the new props.

. componentDidUpdate(prevProps, prevState, snapshot): This method is called after the component has been re-rendered. It can be used to perform side-effects like network requests or updating the DOM.

## 4.React's Reconciliation Algorithm

React uses a reconciliation algorithm to efficiently update the DOM:

. It creates a virtual DOM (a lightweight copy of the actual DOM).

. It computes the difference (diff) between the previous virtual DOM and the new virtual DOM created by the updated render method.

. It updates only the parts of the actual DOM that have changed, minimizing the number of changes and improving performance.

## Example

Here's an example to illustrate how props can cause a component to re-render:

``` ruby
import React, { Component } from 'react';

class ChildComponent extends Component {
  // This method decides if the component should re-render
  shouldComponentUpdate(nextProps) {
    // Only re-render if the 'value' prop has changed
    return nextProps.value !== this.props.value;
  }

  render() {
    console.log('ChildComponent rendered');
    return <div>{this.props.value}</div>;
  }
}

class ParentComponent extends Component {
  state = {
    value: 0,
  };

  componentDidMount() {
    setInterval(() => {
      this.setState(prevState => ({ value: prevState.value + 1 }));
    }, 1000);
  }

  render() {
    return <ChildComponent value={this.state.value} />;
  }
}

export default ParentComponent;
```
In this example:
. The ParentComponent updates its state every second.

. The ParentComponent passes the value state as a prop to ChildComponent.

. ChildComponent will only re-render if the value prop changes, as determined by the shouldComponentUpdate method.

# CSS in React

The point about CSS styles in React is that they are applied to the entire app and it does not matter where they are written. In fact, there is no scope for them if some libraries are not used.


> [!TIP]
> We just import CSS files like this import './styles.css'; to understand where a component's styles are written.

<blockquote class="imgur-embed-pub" lang="en" data-id="6B556uf"><a href="https://imgur.com/6B556uf">View post on imgur.com</a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>

[![Alt text]((https://i.imgur.com/6B556uf.png)]([https://imgur.com/])

# What are the differences between impure and pure functions in JavaScript?

In JavaScript, functions can be classified as either pure or impure based on their behavior and side effects. Understanding the differences between them is crucial for writing clean, maintainable, and predictable code. Here’s a detailed explanation of both types:

## Pure Functions

A pure function is a function that, given the same input, will always return the same output and does not have any side effects.

Characteristics of Pure Functions:

1. Deterministic: The output is determined solely by the input values.
2. No Side Effects: The function does not modify any external state (e.g., global variables, I/O operations, etc.).
3. Immutability: The function does not alter the input values or any external data.

### Example:

```ruby
 function add(a, b) {
   return a + b;
 }
 
 const result = add(2, 3); // result is always 5

```
In this example, add is a pure function because it always returns the same result for the same inputs and does not affect any external state.

## Impure Functions

An impure function is a function that may return different results given the same input and/or has side effects.

## Characteristics of Impure Functions:

1. Non-Deterministic: The output can vary even with the same input values.
2. Side Effects: The function interacts with or modifies external state (e.g., global variables, I/O operations, database calls, etc.).
3. Mutability: The function may alter the input values or external data.

### Example

```ruby
let counter = 0;

function increment() {
  counter += 1;
  return counter;
}

const result1 = increment(); // result1 is 1
const result2 = increment(); // result2 is 2

```

```ruby
let c = 4;

function increment(a,b) {
  return a+b+c;
}

const result1 = increment(2,3); // result1 is 9
c=6
const result2 = increment(2,3); // result2 is 11

```
```ruby
let c = 4;

function increment(a,b) {
c= a*b*600
  return a+b;
}

const result1 = increment(2,3); // result1 is 5
const result2 = increment(2,3); // result2 is 5

```
## Differences between rendering a functional component and a class component
 The fact is that in class components it is the render that just re-render every time but in functional components whole function re-render.

> [!IMPORTANT]
> The point about setState in functional components is that it is not the setState which makes the component re-render, it is the different value of the state that re-renders the component. In addition if you called setState with the same value of the current state, it would not re-render the component.

<details>
   <summary> Some Challenges </summary>

In the below code, we will have an infinity loop of re-rendering because the users array from the api is different from the one which is stored in storage despite the fact that they have the same value.

```ruby
const [monsters, setMonsters] = usestate([]);
fetch( https://jsonplaceholder.typicode.com/users')
.then ((response) => response. json())
.then((users)=>setMonesters(users))
```
</details>

# useEffect 

useEffect is a hook in React, introduced with the release of React 16.8, which allows you to perform side effects in function components. Side effects can include data fetching, subscriptions, or manually changing the DOM, and useEffect provides a way to handle these operations in a manner that aligns with the React component lifecycle.

Here’s a basic overview of how useEffect works:

### Syntax

```ruby
import React, { useEffect } from 'react';

function MyComponent() {
  useEffect(() => {
    // This code runs after the component renders
    
    return () => {
      // This code runs when the component unmounts or before the effect runs again
    };
  }, [/* dependencies */]);

  return <div>My Component</div>;
}

```
### Explanation

1. First Argument: Effect Function
   
   . The first argument to useEffect is a function where you can perform your side effect.

   . This function is executed after the component renders (including after the initial render and subsequent updates).

2. Cleanup Function

   . The effect function can return a cleanup function, which is executed before the component unmounts or before the effect runs again.

   . This is useful for cleaning up subscriptions, timers, or other resources to avoid memory leaks.

3. Second Argument: Dependencies Array

   . The second argument to useEffect is an optional array of dependencies.

   . If this array is provided, the effect will only re-run if one of the dependencies has changed since the last render.

   . If the array is empty, the effect runs only once after the initial render.

   . If no second argument is provided, the effect runs after every render.

### Example: Fetching Data

Here’s an example of using useEffect to fetch data from an API when the component mounts:


```ruby
import React, { useState, useEffect } from 'react';

function DataFetchingComponent() {
  const [data, setData] = useState(null);

  useEffect(() => {
    // Perform data fetching
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => setData(data))
      .catch(error => console.error('Error fetching data:', error));

    // Cleanup function (if necessary)
    return () => {
      // Cleanup code here
    };
  }, []); // Empty array ensures this runs only once after the initial render

  return (
    <div>
      {data ? <pre>{JSON.stringify(data, null, 2)}</pre> : 'Loading...'}
    </div>
  );
}

export default DataFetchingComponent;

```
### Example: Using Dependencies

Here’s an example where useEffect depends on a prop or state value:


```ruby
import React, { useState, useEffect } from 'react';

function Countdown({ start }) {
  const [count, setCount] = useState(start);

  useEffect(() => {
    const timer = setInterval(() => {
      setCount(prevCount => prevCount - 1);
    }, 1000);

    return () => clearInterval(timer); // Cleanup the interval on unmount
  }, [start]); // Only re-run the effect if `start` changes

  return <div>Countdown: {count}</div>;
}

export default Countdown;


```
In this example, the interval is set up when the component mounts or when the start prop changes, and it's cleaned up when the component unmounts or before the effect runs again.

# Reflow and Paint Flashing

In React (and web development in general), "reflow" and "paint flashing" are concepts related to the rendering performance of web applications. Understanding these concepts is important for optimizing performance and ensuring a smooth user experience. Here’s an explanation of each:

## Reflow

Reflow (also known as layout) is the process by which the browser calculates the layout of the webpage. When a web page initially loads or when changes are made to the DOM (Document Object Model), the browser needs to determine the size and position of each element. This process is known as reflow.

 Causes of Reflow:

. Adding, removing, or updating DOM elements.
. Changing the content (e.g., text) within an element.
. Resizing the browser window.
. Applying new styles that affect the layout (e.g., changing width, height, margin, padding, etc.).
. Adding or removing CSS classes.

Reflow can be an expensive operation because it may require the browser to recalculate the layout of a large portion of the page, or even the entire page, which can impact performance.

## Paint Flashing
Paint flashing is a debugging tool used to visualize areas of a web page that are being repainted. When elements on a webpage are changed, the browser repaints the affected area. This process is known as painting.

In modern browsers, there are tools that can highlight these repaint areas, helping developers see which parts of the page are being repainted and how often. This visualization is known as paint flashing.

Causes of Repaint:

. Changing the visibility of an element (e.g., show/hide).
. Changing styles that affect the look but not the layout (e.g., background color, visibility, outline).
. Scrolling.

Repaints are generally less expensive than reflows, but excessive repaints can still degrade performance, especially on pages with complex graphics or animations.

## React and Performance

In React, understanding reflow and paint flashing is crucial for optimizing rendering performance. React components can cause reflows and repaints when they update the DOM. Here are a few tips to minimize these performance costs in React:

1. Minimize DOM Manipulations: Batch DOM updates and minimize the number of changes that cause reflow.
2. Use shouldComponentUpdate or React.memo: Prevent unnecessary re-renders of components by using shouldComponentUpdate (in class components) or React.memo (in functional components).
3. Virtualize Long Lists: Use techniques like windowing or virtualization (e.g., react-window, react-virtualized) to render only the visible portion of large lists.
4. Avoid Inline Styles for Performance-Critical Elements: Use CSS classes instead of inline styles when performance is a concern, as inline styles can trigger reflow.
5. Optimize CSS Animations and Transitions: Use properties that only affect paint, not layout, when animating elements.

By being aware of reflow and paint flashing and applying these optimization techniques, you can improve the performance of your React applications.

# React Router DOM

React Router DOM v6 is a major version of the React Router library that introduces several significant changes and improvements over previous versions. It provides tools for handling routing in React applications, allowing for dynamic navigation and rendering of components based on the URL.

## Key Features and Changes in React Router DOM v6

1. Declarative Routing with <Routes>:
   
   . Replaces the <Switch> component with <Routes>, providing a more intuitive and simpler API.
   
   .Ensures only one route renders at a time by default.

2. Route Element Prop:

   . The element prop specifies the React element to be rendered when the route matches the current URL.

   ```ruby
    <Route path="/" element={<Home />} />
   ```

3. Hooks for Programmatic Navigation:

   .Provides hooks such as useNavigate, useParams, useLocation, and useMatch for handling navigation, accessing route parameters, and other routing-related tasks.

4. Relative Routes and Links:

   . Enhances support for relative routing and linking, making it easier to navigate within nested routes.

### Example Usage

Here’s an example of how to set up and use React Router DOM v6:

1. Install React Router DOM v6:

   ```ruby
    npm install react-router-dom@6
    # or
    yarn add react-router-dom@6
   ```

2. Application Structure:

   Create the following files:

   . src/index.js

   . src/App.js

   . src/components/Home.js

   . src/components/About.js

   . src/components/Contact.js

3. Create Components:

   . Home Component (src/components/Home.js):

    ```ruby
   import React from 'react';

    const Home = () => {
      return <h2>Home</h2>;
    };
    
    export default Home;
    
    ```
 . About Component (src/components/About.js):

    ```ruby
    import React from 'react';
    
    const About = () => {
      return <h2>About</h2>;
    };
    
    export default About;

    
    ```


. Contact Component (src/components/Contact.js):

    ```ruby
 
    import React from 'react';
   
    const Contact = () => {
      return <h2>Contact</h2>;
    };
    
    export default Contact;

    
    ```

 4. Set Up the App Component:

    . App Component (src/App.js):

       ```ruby
      import React from 'react';
     import { BrowserRouter as Router, Routes, Route, Link } from 'react-router-dom';
     import Home from './components/Home';
     import About from './components/About';
     import Contact from './components/Contact';
     
     function App() {
       return (
         <Router>
           <div>
             <nav>
               <ul>
                 <li><Link to="/">Home</Link></li>
                 <li><Link to="/about">About</Link></li>
                 <li><Link to="/contact">Contact</Link></li>
               </ul>
             </nav>
     
             <Routes>
               <Route path="/" element={<Home />} />
               <Route path="/about" element={<About />} />
               <Route path="/contact" element={<Contact />} />
             </Routes>
           </div>
         </Router>
       );
     }
     
     export default App;
    ```

5. Set Up the Entry Point:
   .Index File (src/index.js)
     ```ruby
       import React from 'react';
    import ReactDOM from 'react-dom';
    import App from './App';
    
    ReactDOM.render(
      <React.StrictMode>
        <App />
      </React.StrictMode>,
      document.getElementById('root')
    );
   ```

### Explanation

1. Components:

   .Home.js, About.js, and Contact.js are simple functional components rendering an  element.

2. App Component:

   . BrowserRouter (aliased as Router) wraps the application to enable routing.

   . The <nav> element contains navigation links using the <Link> component for client-side navigation.

   . The <Routes> component replaces <Switch> and ensures that only one <Route> renders.

   . Each <Route> specifies a path and an element prop, where element is a JSX element of the component to render.

3. Index File:

   . The index.js file renders the App component into the root DOM element.

### Summary

React Router DOM v6 introduces significant improvements and simplifications over previous versions. It emphasizes a more declarative approach to routing, provides powerful hooks for navigation and state management, and makes working with nested routes more straightforward. The switch from <Switch> to <Routes> and the new element prop for routes are some of the notable changes that aim to make routing in React applications more intuitive and maintainable.

# React Context

React Context is a feature in React that allows you to share state and other data between components without passing props down manually at every level. It provides a way to manage global state and data that need to be accessed by many components in a React application, making it easier to avoid "prop drilling" (the process of passing props through many levels of components).

## Key Concepts of React Context

1. Creating a Context:

    . You create a Context using React.createContext(). This function returns a Context object with two components: Provider

   . Example:

     ```ruby
     const MyContext = React.createContext();
   ```
2. Provider:

   . The Provider component is used to wrap parts of your application and makes the context available to all child components.

. The Provider takes a value prop, which is the data or state you want to share.

Example:

  ```ruby
     <MyContext.Provider value={someValue}>
       <ChildComponent />
     </MyContext.Provider>
   ```

3. useContext Hook:

   . In modern React, the useContext hook is often used in the component to access context values.

   .It simplifies the syntax and allows you to consume context in functional components.

   Example:

   
  ```ruby
    const value = useContext(MyContext);
   ```
## When to Use React Context

. Global State Management: When you have state that needs to be shared across many components at different levels of the component tree (e.g., user authentication status, theme, or locale).

. Avoiding Prop Drilling: When passing props through multiple layers of components becomes cumbersome and makes your code harder to manage.


## Example of React Context in Action

```ruby
const BusinessContext = createContext()
const useBusinessContext = () => {
  const context = useContext?.(BusinessContext)

  if (context === undefined) {
    throw new Error('useAppContext was used outside of its Provider')
  }

  return context
}

function BusinessContextProvider({ children }) {
  const {
    isLoading: isLoadingGetPermission,
    mutate: getUserPermissions,
    data: res,
  } = useGetAllPermissions()
  const { isLoading: profileLoading, data: profile } = useGetProfile(({ data }) => {
    getUserPermissions({ businessId: data?.businessId, userId: data?.id })
  })
  const contextValue = useMemo(
    () => ({
      firstName: `${profile?.data?.firstName || ''}`,
      name: `${profile?.data?.firstName || ''} ${profile?.data?.lastName || ''}`,
      avatar: profile?.data?.user?.data?.avatar?.data?.path,
    
    }),
    [
      res?.data,
    ]
  )
  return (
    <BusinessContext.Provider value={contextValue}>
      {(profileLoading || isLoadingGetPermission) && isSecondStageAuthenticated() ? (
        <PageLoading />
      ) : (
        <>{children}</>
      )}
    </BusinessContext.Provider>
  )
}

export { useBusinessContext, BusinessContextProvider }

   ```
   
# Rendering in React Context

Rendering in React is closely related to how React Context works, especially when it comes to managing state and triggering updates in components that consume context values.

1. Re-renders due to Context Changes:

   . When a context value changes, any component that consumes this context will re-render. This is because React needs to update the UI to reflect the new context value.

   . For example, if you update the value prop of a Context.Provider, all components that are consuming that context (either via useContext or Context.Consumer) will re-render to reflect the new data.

    ```ruby
    <MyContext.Provider value={newValue}>
      <SomeComponent />
    </MyContext.Provider>

   ```

    In this example, if newValue changes, SomeComponent and any other components consuming MyContext will re-render

   2. Avoiding Unnecessary Re-renders:
  
    . One of the key considerations when using React Context is to manage how and when components re-render. If many components depend on a context value, changing that value will cause all those components to re-render, which can lead to performance issues if not managed properly.

      . Techniques like memoization (using React.memo for functional components or shouldComponentUpdate in class components) can help prevent unnecessary re-renders by ensuring that components only re-render when they actually need to.

   3. Selective Context Consumption:
  
      . Another strategy to minimize unnecessary re-renders is to consume context selectively. Instead of passing the entire context value to deeply nested components, you can split context into smaller pieces or only consume parts of the context in components that really need them.

      . For example, if you have a theme context with both colors and font sizes, but some components only need the colors, you might create separate contexts for colors and fonts to reduce re-renders.

   ```ruby
   const ColorContext = React.createContext();
   const FontContext = React.createContext();
   
   // Components can consume only the context they need

   ```

      
