 
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

# Reducer

In React, a reducer is a pure function that takes the current state and an action as arguments and returns a new state. Reducers are commonly used in conjunction with the useReducer hook or within the Redux library to manage complex state logic in a predictable way. Here’s how a reducer works and triggers re-renders in React:

 1. Understanding the Reducer Function
    
A reducer function is a pure function, meaning it doesn't produce side effects and its output is solely determined by its input. The function signature looks like this:

   ```ruby
  function reducer(state, action) {
  switch (action.type) {
    case 'INCREMENT':
      return { count: state.count + 1 };
    case 'DECREMENT':
      return { count: state.count - 1 };
    default:
      return state;
  }
}
   ```

2. Using the useReducer Hook

  ```ruby
   React provides the useReducer hook to use a reducer function for managing state within a component. Here’s how it works:

   import React, { useReducer } from 'react';

// Define the reducer function
function reducer(state, action) {
  switch (action.type) {
    case 'INCREMENT':
      return { count: state.count + 1 };
    case 'DECREMENT':
      return { count: state.count - 1 };
    default:
      return state;
  }
}

function Counter() {
  // Initialize state with useReducer
  const [state, dispatch] = useReducer(reducer, { count: 0 });

  return (
    <div>
      <p>Count: {state.count}</p>
      <button onClick={() => dispatch({ type: 'INCREMENT' })}>
        Increment
      </button>
      <button onClick={() => dispatch({ type: 'DECREMENT' })}>
        Decrement
      </button>
    </div>
  );
}

export default Counter;

  ```

3. How the Reducer Works

   1 nitial State: The useReducer hook initializes the state with the second argument you pass to it ({ count: 0 } in this case).

   2. Dispatching Actions:

 . When the user clicks the "Increment" button, dispatch({ type: 'INCREMENT' }) is called.

 .The dispatch function sends an action to the reducer.

3. Reducer Function Execution:

   . The reducer function is called with the current state and the action.

    . Based on the action's type, the reducer computes the new state. For example, if the action type is 'INCREMENT', the new state will have count incremented by 1.

   4. Returning the New State:

      . The reducer returns the new state object.

      . In this case, if the current state was { count: 0 } and the action was { type: 'INCREMENT' }, the new state would be { count: 1 }.
      
4. Triggering Re-renders

. State Update: When the reducer returns a new state, React compares it to the previous state.

. Re-rendering: If the state has changed, React will trigger a re-render of the component that uses this state.

. Rendering the UI: The component re-renders, reflecting the new state in the UI. For example, the <p> element will now display Count: 1.

5. Pure Functions and Re-renders

   Because the reducer is a pure function:

    . Predictable Behavior: The state transitions are predictable, making it easier to debug and test the application.

   . Efficiency: React optimizes re-renders by comparing the previous state with the new state. If they are the same (shallow comparison), no re-render occurs. This optimization works well with pure functions like reducers.

## Example Breakdown

In the Counter component example:

. Initial Render: The component renders with Count: 0.

. On Click (Increment):

  . The dispatch function is called with { type: 'INCREMENT' }.

  . The reducer returns a new state { count: 1 }.

  . React detects the state change and re-renders the component.

  . The UI now displays Count: 1.

 Summary

 . Reducer: A pure function used to manage state transitions based on actions.

 . useReducer Hook: Integrates a reducer into a React component, handling state and triggering re-renders when the state changes.

 . Re-renders: React automatically re-renders components when the state managed by the reducer changes, ensuring the UI stays in sync with the current state.

 This approach provides a predictable and organized way to manage complex state logic in React components.

   
 # CSS-in-JS
   "CSS-in-JS" in React refers to a styling technique where CSS is written within JavaScript, typically within React components. This approach allows developers to define and apply styles using JavaScript, often in the same file as the component, instead of in separate CSS files. CSS-in-JS libraries provide various features, such as dynamic styling, scoped styles, and theming, making it a popular choice in modern React applications.

   ## Key Concepts of CSS-in-JS in React:

   1. Scoped Styles:

      . Styles are applied only to the component they are defined in, avoiding global namespace pollution and ensuring that styles don't leak out to other components.

   2. Dynamic Styling:

      Styles can be dynamic, meaning they can respond to props or state. This allows for more flexible and reusable components.

   3. Theming:

      . Many CSS-in-JS libraries support theming, which allows you to define a global theme and use it consistently across your application.

   4. Inline Styles:

      . CSS can be directly written within the component, often using a JavaScript object to define style properties.

   ## Popular CSS-in-JS Libraries in React:

   .Styled-components:

   Styled-components allow you to write actual CSS syntax inside your JavaScript. It creates a styled component that can be reused and styled dynamically.

   ```ruby
   import styled from 'styled-components';

   const Button = styled.button`
   background: ${props => props.primary ? 'blue' : 'white'};
   color: ${props => props.primary ? 'white' : 'blue'};
    `;
   ```

## Benefits of CSS-in-JS:

. Component-based: Styles are tightly coupled with components, which aligns well with React's component-based architecture.

. Dynamic: You can easily change styles based on props, state, or context.

. Scoped: Avoids CSS conflicts by scoping styles to specific components.

. Theming: Easier to implement themes and manage them across the application.

## Drawbacks of CSS-in-JS:

. Performance: May have a performance overhead due to runtime style generation, though many libraries mitigate this with optimization techniques.

. Learning Curve: The concept can be unfamiliar and initially more complex than traditional CSS or CSS preprocessors.

CSS-in-JS is a powerful approach that provides flexibility and modern styling capabilities in React applications, aligning with the trend towards more modular and maintainable front-end codebases.

  ## Example of nested style

   ```ruby
  import styled from 'styled-components';
  import {
  BaseButton, GoogleSignInButton, InvertedButton}
  from '..button/button.styles';

     export const darDropdownContainer =
     styled. div`
     position: absolute;
     width: 240px; height: 340px;
     display:
     flex;
     flex-direction: column;
     padding:
     20px;
     border: 1px solid black; background-color: white;
     top: 90px;
     right: 40px; z-index: 5;
     ${BaseButton},
     $｛G00gleSignInButton｝，
     ${InvertedButton} {
     margin-top:
     }
     `;

     export const EmptyMessage = styled. span`
      font-size: 18px;
      margin: 50px auto;
     `;
   ```
  # Redux
  
  Redux is a state management library often used with React to help manage the state of an application in a predictable and centralized way. It provides a structure for managing the state of your entire application in a single "store," allowing you to avoid complex state management issues that can arise when your application grows in size.

  ## Key Concepts in Redux:

  1. Store:

     . The store is a single JavaScript object that holds the entire state of your application. It is the central place where all the state in your app lives.

     . There is typically only one store in a Redux application, though you can have multiple slices of state within it.

  2. Actions:

     . Actions are plain JavaScript objects that describe what happened in the application. They have a type property and can optionally include a payload with additional data.

     . Actions are the only source of information for the store, meaning they dictate how the state should change.

   Example:

   ```ruby
     const incrementAction = { type: 'INCREMENT', payload: 1 };
   ```

 3. Reducers:

     . Reducers are pure functions that take the current state and an action as arguments and return the new state.

     . A reducer's job is to specify how the state changes in response to an action.

4. Store:

   . The Redux store is created using the createStore function and holds the entire state tree of your application.

   . The store also provides methods like dispatch to send actions to the reducer and getState to access the current state.

   Example:

     ```ruby
     import { createStore } from 'redux';

     const store = createStore(counterReducer);

    ```
5. Dispatch:

   . The dispatch function is used to send actions to the Redux store. When an action is dispatched, the store calls the reducer function with the current state and the action to compute the next state.

   Example:

   ```ruby
        store.dispatch({ type: 'INCREMENT', payload: 1 });
   
   ```
   6. Selectors:
  
      . Selectors are functions that extract specific parts of the state from the store. They are used to avoid directly accessing the state, allowing for more modular code.

   ## How Redux Integrates with React:

   To integrate Redux with React, you use a package called react-redux, which provides a way to connect your React components to the Redux store.

   . Provider: The <Provider> component wraps your React app and makes the Redux store available to all components within the app.

   
   ```ruby
       import { Provider } from 'react-redux';

       function App() {
         return (
           <Provider store={store}>
             <YourMainComponent />
           </Provider>
         );
       }

   
   ```

   connect: The connect function is a higher-order component that connects a React component to the Redux store. It allows the component to access state and dispatch actions as props.

      ```ruby
    import { connect } from 'react-redux';
    
    const mapStateToProps = (state) => ({
      count: state.count,
    });
    
    const mapDispatchToProps = (dispatch) => ({
      increment: () => dispatch({ type: 'INCREMENT', payload: 1 }),
    });
    
    export default connect(mapStateToProps, mapDispatchToProps)(YourComponent);

   
    ```

  useSelector and useDispatch Hooks: These are React hooks provided by react-redux that allow functional components to access the Redux store more easily.
      
   ```ruby
       import { useSelector, useDispatch } from 'react-redux';
     
     function Counter() {
       const count = useSelector((state) => state.count);
       const dispatch = useDispatch();
     
       return (
         <div>
           <p>{count}</p>
           <button onClick={() => dispatch({ type: 'INCREMENT', payload: 1 })}>
             Increment
           </button>
         </div>
       );
     }
  ```

## Why Use Redux?

. Predictable State: Redux ensures that state changes are predictable and traceable, which is especially useful for debugging.

. Centralized State Management: Redux centralizes state management, which is beneficial when your application has many components that need to share data.

. Immutability: Redux enforces immutability in state updates, which helps prevent bugs related to state mutations.

. Ecosystem: Redux has a rich ecosystem of middleware, developer tools (like Redux DevTools), and integrations, making it powerful and extensible.

Redux is a powerful tool, but it’s most beneficial in applications with complex state management needs. For simpler apps, React’s built-in useState and useReducer hooks might be sufficient.

## How can I use multiple reducers in redux?

In Redux, managing complex state often involves splitting the state management logic across multiple reducers. This is where combining reducers becomes essential. Redux provides a utility function called combineReducers that allows you to create a single root reducer from multiple reducers, each managing its own slice of the state.

Steps to Use Multiple Reducers in Redux:

1. Define Individual Reducers:

   Each reducer manages a specific part of the state. For example, you might have one reducer for user authentication, another for handling products, and another for cart items.

   ```ruby
        // authReducer.js
          const authReducer = (state = { isAuthenticated: false }, action) => {
            switch (action.type) {
              case 'LOGIN_SUCCESS':
                return { ...state, isAuthenticated: true };
              case 'LOGOUT':
                return { ...state, isAuthenticated: false };
              default:
                return state;
            }
          };

       // productsReducer.js
       const productsReducer = (state = [], action) => {
         switch (action.type) {
           case 'SET_PRODUCTS':
             return action.payload;
           default:
             return state;
         }
       };

       // cartReducer.js
       const cartReducer = (state = [], action) => {
         switch (action.type) {
           case 'ADD_TO_CART':
             return [...state, action.payload];
           case 'REMOVE_FROM_CART':
             return state.filter(item => item.id !== action.payload.id);
           default:
             return state;
         }
       };

   ```

   2. Combine Reducers:
  
      Use combineReducers to combine all the individual reducers into a single root reducer. Each reducer will handle its own slice of the state.

      
    ```ruby
     import { combineReducers } from 'redux';
    import authReducer from './authReducer';
    import productsReducer from './productsReducer';
    import cartReducer from './cartReducer';
    
    const rootReducer = combineReducers({
      auth: authReducer,
      products: productsReducer,
      cart: cartReducer,
    });
    
    export default rootReducer;

     }
   ```

  In this example, authReducer will manage the auth slice of the state, productsReducer will manage the products slice, and cartReducer will manage the cart slice.

  3. Create the Redux Store:

     Once you have the root reducer, you can create the Redux store using createStore.
     
      ```ruby
    import { createStore } from 'redux';
     import rootReducer from './reducers'; // Assuming all reducers are in a `reducers` folder
     
     const store = createStore(rootReducer);
     
     export default store;

     }
    ```

   4. Accessing State Slices in Components:

   In your React components, you can access the state slices managed by different reducers using the useSelector hook or by connecting the component to the Redux store using connect.

   ```ruby
    import React from 'react';
    import { useSelector } from 'react-redux';
    
    const MyComponent = () => {
      const isAuthenticated = useSelector((state) => state.auth.isAuthenticated);
      const products = useSelector((state) => state.products);
      const cartItems = useSelector((state) => state.cart);
    
      return (
        <div>
          {isAuthenticated ? <p>Logged In</p> : <p>Logged Out</p>}
          <ul>
            {products.map((product) => (
              <li key={product.id}>{product.name}</li>
            ))}
          </ul>
          <ul>
            {cartItems.map((item) => (
              <li key={item.id}>{item.name}</li>
            ))}
          </ul>
        </div>
      );
    };

    export default MyComponent;

   ```

   5. Dispatching Actions:

      Dispatching actions to update state slices is done as usual, but each action will only affect the corresponding part of the state managed by the reducer.

      ```ruby
    import { useDispatch } from 'react-redux';
    
    const AnotherComponent = () => {
      const dispatch = useDispatch();
    
      const addToCart = (product) => {
        dispatch({ type: 'ADD_TO_CART', payload: product });
      };
    
      return <button onClick={() => addToCart({ id: 1, name: 'Product 1' })}>Add to Cart</button>;
    };

     ```

   Summary:

   . Modular State Management: Each reducer manages its own slice of the state, making the code more modular and easier to maintain.

   . CombineReducers: The combineReducers function is used to create a root reducer by combining multiple reducers.

   . Root State Object: The resulting state object from combineReducers will have keys corresponding to the names of the reducers, with each key holding the state managed by its respective reducer.


   Using multiple reducers in Redux allows you to keep your state management organized and scalable, especially as your application grows in complexity.


## Middlewares in Redux

Middlewares in Redux are functions that sit between an action being dispatched and the action reaching the reducer. They allow you to intercept, modify, or perform side effects with actions before they get processed by the reducers. Middleware is a powerful tool in Redux for extending the behavior of the dispatch process.

### Key Concepts:

1. Interception: Middleware can intercept dispatched actions before they reach the reducer, allowing you to modify or cancel actions.
2. Side Effects: Middleware is often used to handle side effects like making asynchronous API calls, logging, or other non-pure operations that shouldn’t be in reducers.
3. Enhancement: Middleware can enhance the dispatch process by adding additional functionality, like logging, error handling, or debugging.

### How Middleware Works:

When you apply middleware to your Redux store, every time you dispatch an action, the middleware gets a chance to process the action before it reaches the reducer.

   
   ```ruby
const store = createStore(
  rootReducer,
  applyMiddleware(middleware1, middleware2, ...)
);

```
### Common Middleware Examples:

1. redux-thunk:

. Allows you to write action creators that return a function instead of an action. This is useful for handling asynchronous logic, such as fetching data from an API.

. Example:
  
   ```ruby
function fetchUser(userId) {
  return function(dispatch) {
    dispatch({ type: 'FETCH_USER_REQUEST' });
    fetch(`/api/users/${userId}`)
      .then(response => response.json())
      .then(data => dispatch({ type: 'FETCH_USER_SUCCESS', payload: data }))
      .catch(error => dispatch({ type: 'FETCH_USER_FAILURE', error }));
  };
}

```

2. redux-logger:

   . Logs every action dispatched and the resulting state change to the console. Useful for debugging.

   . Example:

      
      ```ruby
   import logger from 'redux-logger';
   const store = createStore(rootReducer, applyMiddleware(logger));


    ```
3. redux-saga:
   
   . A more advanced middleware for handling side effects. It uses generator functions to manage complex asynchronous workflows in a more declarative way.

   . Example:

   ```ruby
          import createSagaMiddleware from 'redux-saga';
       import { rootSaga } from './sagas';
       
       const sagaMiddleware = createSagaMiddleware();
       const store = createStore(rootReducer, applyMiddleware(sagaMiddleware));
       
       sagaMiddleware.run(rootSaga);
       ```
4. redux-promise:

   . Allows you to dispatch promises as actions. The middleware will wait for the promise to resolve and then dispatch the resolved value as an action.

   . Example:

   ```ruby
             function fetchUser(userId) {
         return {
           type: 'FETCH_USER',
           payload: fetch(`/api/users/${userId}`).then(response => response.json())
         };
       }
       ```

### How to Write Custom Middleware:

   ```ruby
      const loggerMiddleware = store => next => action => {
      console.log('Dispatching:', action);
      let result = next(action); // Pass the action to the next middleware/reducer
      console.log('Next State:', store.getState());
      return result;
    };
    
    const store = createStore(
      rootReducer,
      applyMiddleware(loggerMiddleware)
    );

   ```

   ### Middleware Flow:

   1. Dispatching an Action: When an action is dispatched, it first goes through the middleware chain.
   2. Middleware Processing: Each middleware can process the action, perform side effects, or modify the action before passing it to the next middleware.
   3. Reducer Update: Once all middleware has processed the action, it reaches the reducer, which updates the state accordingly.
   4. State Update: The new state is then available in the store, and any subscribed components are re-rendered if necessary.

### When to Use Middleware:

. Asynchronous Operations: For handling async operations like API calls (redux-thunk, redux-saga).

. Logging and Debugging: To log actions and state changes (redux-logger).

. Complex Side Effects: For managing complex workflows or side effects that involve multiple steps or dependencies (redux-saga).

. Custom Behavior: To extend Redux with custom logic, like authentication checks, analytics, or error handling.

### Summary:

Middleware in Redux is a powerful way to add functionality to your Redux store. It enhances the dispatching process by allowing you to handle side effects, perform asynchronous operations, log actions, and more, making it easier to manage complex state and actions in your application.

       
You can also write your own middleware to add custom behavior to your Redux store. Here’s a simple example of custom middleware that logs every action:

   ## What is redux logger?

   Redux Logger is a middleware for Redux that logs actions and the resulting state changes to the console, making it easier for developers to track how the state in a Redux application evolves over time. It’s primarily used during development to debug and monitor the flow of actions and state updates.

   ### Key Features:

   . Action Logging: Logs every action dispatched in the Redux application, including the type of action and any associated payload.

   . State Logging: Logs the state of the Redux store before and after each action is processed, allowing you to see exactly how the state has changed in response to an action.

   . Diffing: Shows a diff of the changes to the state, making it easy to see exactly what has changed after an action.

   . Time Travel: In combination with other tools, it can allow for time-travel debugging, where you can step through actions to see how each one affected the state.

   ### How to Use Redux Logger:

   1. Install Redux Logger:

      You can install it via npm or yarn:

      
 ```ruby
     npm install redux-logger

```

   or


   ```ruby
     yarn add redux-logger

   ```

   2. Add Redux Logger to Middleware:

      To use Redux Logger, you need to add it to your Redux middleware setup, usually when you create the Redux store.

 ```ruby
     import { createStore, applyMiddleware } from 'redux';
    import logger from 'redux-logger';
    import rootReducer from './reducers';
    
    const store = createStore(
      rootReducer,
      applyMiddleware(logger)
    );


 ```

   3. Customizing Redux Logger (Optional):

      Redux Logger can be customized to control what information is logged. For example, you can only log certain actions or disable logging in production.

   ```ruby
   import { createStore, applyMiddleware } from 'redux';
import { createLogger } from 'redux-logger';
import rootReducer from './reducers';

const logger = createLogger({
  collapsed: true, // Collapse the logs for easier reading
  diff: true,      // Show the difference between states
});

const store = createStore(
  rootReducer,
  applyMiddleware(logger)
);


  ```


### Why Use Redux Logger?

. Debugging: It provides clear visibility into the flow of actions and the state changes they cause, which is invaluable when debugging issues in your Redux application.

. Transparency: Redux Logger makes it easy to understand how your application’s state is being managed, especially in complex applications with many actions and reducers.

. Development Tool: It’s a tool primarily for development. It helps ensure that the state changes as expected and that actions are dispatched correctly.

Best Practices:

. Disable in Production: It’s recommended to disable Redux Logger in production builds to avoid performance overhead and excessive logging. This can be done by conditionally applying the middleware based on the environment.


   ```ruby
 const middleware = [];
if (process.env.NODE_ENV !== 'production') {
  middleware.push(logger);
}

const store = createStore(
  rootReducer,
  applyMiddleware(...middleware)
);
```
Redux Logger is an essential tool for any Redux developer, providing insight and transparency into the state management process, making it easier to develop, debug, and maintain Redux applications.

# Redux vs Context Access

The performance of Redux is often considered better than React Context in certain scenarios, especially in larger applications, due to several key factors. Here’s why:

 1. Granular State Updates in Redux

. Selective Subscriptions: In Redux, components can subscribe to specific slices of the state using connect() (for class components) or useSelector() (for function components). This means that when the state changes, only the components that rely on the specific part of the state that changed will re-render.

. Example: If you have a large application with many components, only the components that need to react to a specific change in state will re-render, rather than every component that consumes the context.


. In contrast: React Context triggers a re-render for all components that consume the context whenever the context value changes, regardless of whether they actually depend on the specific part of the data that changed. This can lead to unnecessary re-renders and degrade performance, especially in large applications with many consumers.

 2.  Memoization and Optimization Tools

. Redux Toolkit: Redux provides tools like reselect to create memoized selectors, ensuring that components only re-render when the relevant part of the state actually changes. Memoization reduces the number of renders and improves performance.

. React Context does not inherently offer a built-in way to avoid re-renders when only a portion of the context data changes, though you can implement memoization manually using useMemo and useCallback, it is more complex and error-prone.

3. Middleware Support in Redux

   . Middleware: Redux has a rich middleware ecosystem that allows for side effects like asynchronous data fetching, logging, or error handling, to be managed outside of components. This keeps components lean and focused on rendering, which can indirectly improve performance by reducing the complexity of individual components.

   . Thunk/Saga: Libraries like redux-thunk or redux-saga help manage complex side effects and asynchronous logic efficiently, which can further contribute to overall performance.

   . React Context does not have a native middleware system. You need to handle side effects within your components or custom hooks, which can make components heavier and potentially impact performance.


   4. Predictable State Changes
  
      . Redux: Because Redux enforces a strict unidirectional data flow and state changes are handled through pure functions (reducers), it’s easier to track and optimize performance bottlenecks. The predictability of state changes also makes it easier to reason about when and why components re-render, which is crucial for optimizing performance.

      . React Context: While it also follows a unidirectional flow, the lack of a centralized state management and the fact that any context update triggers re-renders across all consumers can make it more challenging to manage and optimize performance.


    5. Scale and Maintainability
  
       . Redux is generally better suited for larger applications where state management needs to scale across many components and features. The architecture of Redux supports scalable state management with performance optimizations built in, which is often crucial as an application grows.


       . React Context works well for smaller or medium-sized applications but can become unwieldy and harder to optimize as the complexity of the state and the number of consuming components increases.

   Summary

      . Redux: Offers better performance in large, complex applications due to its ability to manage granular state updates, provide memoization tools, support middleware for handling side effects, and maintain predictable state changes.
   
   . React Context: Simpler to use but can lead to performance issues in larger applications because it re-renders all consuming components whenever the context value changes.

In essence, while React Context is more straightforward and fine for simpler use cases, Redux offers more sophisticated mechanisms for optimizing performance in larger, more complex applications.

 # Memoization in Redux

 Memoization in Redux is a technique used to optimize the performance of selectors, which are functions that derive data from the Redux store. Memoization ensures that expensive calculations or operations are only performed when necessary, avoiding redundant computations by caching the results of these operations.

 How Memoization Works in Redux:

 1. Selectors:

    . Selectors are functions that extract and possibly transform data from the Redux store's state. A common library for creating selectors is reselect.

2. Memoization:

   . Memoization in the context of Redux selectors means caching the results of these selectors based on the input state. If the state hasn't changed, the memoized selector returns the cached result instead of recalculating it.

   ### Example Using reselect

   Let's go through an example to understand how memoization works with Redux selectors:

      ```ruby
       import { createSelector } from 'reselect';

      // A simple input selector
      const getItems = (state) => state.items;
      
      // A memoized selector using createSelector from reselect
      const getExpensiveCalculation = createSelector(
        [getItems],
        (items) => {
          // Expensive computation
          console.log('Expensive calculation running');
          return items.reduce((acc, item) => acc + item.value, 0);
        }
      );

      ```

   In the example:

   . getItems: This is a basic selector that returns the items array from the state.

   . getExpensiveCalculation: This is a memoized selector created using createSelector. It calculates a sum of item.value for all items. This calculation only runs if items has changed.

   ### Why Use Memoization in Redux?

   1. Performance Optimization: Memoization prevents unnecessary recomputations. When the input state hasn't changed, the selector returns the previously computed result.
  
   2. Efficiency: It reduces the number of re-renders in connected components. If the selector returns the same result (due to memoization), React components that rely on this data won't re-render unnecessarily.
  
   3. Avoiding Expensive Operations: If a selector performs a costly operation (like filtering a large array or processing a complex computation), memoization ensures that this operation is only performed when needed.
  
      Example Redux State and Memoized Selector

        ```ruby
      const state = {
          items: [
            { id: 1, value: 10 },
            { id: 2, value: 20 },
            { id: 3, value: 30 }
          ]
        };
        
        // First call: expensive calculation will run
        console.log(getExpensiveCalculation(state)); // Output: 60
        
        // Second call with the same state: cached result is returned, no expensive calculation
        console.log(getExpensiveCalculation(state)); // Output: 60 (from cache)

      ```


      Libraries like reselect

      . reselect: This is the most common library used for memoizing selectors in Redux. It provides the createSelector function, which makes it easy to define memoized selectors.

      . Custom Memoization: You can also implement memoization yourself using JavaScript techniques like caching results based on inputs, but using reselect or similar libraries is recommended for cleaner and more maintainable code.


      Key Points

      . Idempotency: Selectors should be pure functions, meaning they should not have side effects and should always produce the same output for the same input.

      . Dependencies: Only when the input selectors (getItems in the example) detect a change, the memoized selector recomputes its value.

   By leveraging memoization in Redux, you can significantly improve the efficiency and responsiveness of your applications, especially when dealing with large datasets or complex state transformations.

   # Redux Persist

   redux-persist is a library used in Redux to persist the Redux store's state across page reloads, app restarts, or any event that would normally clear the state. It does this by saving the Redux state to a storage mechanism (like localStorage or sessionStorage in a browser) and then rehydrating the state when the app initializes.

### Why Use redux-persist?

. State Persistence: Helps in retaining the state of the application even after a page refresh, allowing for a better user experience.

. Automatic Rehydration: The persisted state is automatically rehydrated into the Redux store on app startup, making the process seamless.

. Configurable: You can choose which parts of the state to persist and how to store them.

  ### Basic Setup of redux-persist

  Here’s a step-by-step guide on how to set up redux-persist in a Redux application:

  1.Install redux-persist:

   . First, you need to install the redux-persist package:

   
        ```ruby
      const state = {
          items: [
            { id: 1, value: 10 },
            { id: 2, value: 20 },
            { id: 3, value: 30 }
          ]
        };
        
        // First call: expensive calculation will run
        console.log(getExpensiveCalculation(state)); // Output: 60
        
        // Second call with the same state: cached result is returned, no expensive calculation
        console.log(getExpensiveCalculation(state)); // Output: 60 (from cache)

      ```
   2. Configure the Persistor:

      . You need to configure the store to use redux-persist. This involves wrapping your root reducer with a persistReducer and setting up a persistor.

         
        ```ruby
      import { createStore } from 'redux';
      import { persistStore, persistReducer } from 'redux-persist';
      import storage from 'redux-persist/lib/storage'; // defaults to localStorage for web
      import rootReducer from './reducers'; // your root reducer
      
      // Persist configuration
      const persistConfig = {
        key: 'root', // key is required
        storage, // storage is a required field
      };
      
      // Create a persisted reducer
      const persistedReducer = persistReducer(persistConfig, rootReducer);
      
      // Create the Redux store with the persisted reducer
      const store = createStore(persistedReducer);
      
      // Create the persistor
      const persistor = persistStore(store);
      
      export { store, persistor };
      

      ```

 3. Wrap Your App with PersistGate:

    . To ensure that your app is only rendered after the state has been rehydrated, you can use the PersistGate component from redux-persist/integration/react.

 ```ruby
   import React from 'react';
import ReactDOM from 'react-dom';
import { Provider } from 'react-redux';
import { PersistGate } from 'redux-persist/integration/react';
import { store, persistor } from './store';
import App from './App';

ReactDOM.render(
  <Provider store={store}>
    <PersistGate loading={null} persistor={persistor}>
      <App />
    </PersistGate>
  </Provider>,
  document.getElementById('root')
);


 ```

. PersistGate delays the rendering of your app's UI until the persisted state has been retrieved and loaded into the Redux store.

. The loading prop can be used to show a loading indicator while the state is being rehydrated.

Configuring redux-persist

. Blacklist and Whitelist:

   . You can control which parts of your state get persisted using the blacklist or whitelist options.
    

 ```ruby
  const persistConfig = {
  key: 'root',
  storage,
  whitelist: ['user'], // only user will be persisted
  // blacklist: ['navigation'], // navigation will not be persisted
};


 ```

. Transforms:

 . You can use redux-persist transforms to modify the state during persistence or rehydration. For example, you could encrypt the state or compress it before saving.
 

 ```ruby
import { createTransform } from 'redux-persist';

const transform = createTransform(
  // transform state on its way to being serialized and persisted
  (inboundState, key) => {
    // modify inboundState here
    return inboundState;
  },
  // transform state being rehydrated
  (outboundState, key) => {
    // modify outboundState here
    return outboundState;
  },
);

const persistConfig = {
  key: 'root',
  storage,
  transforms: [transform],
};


 ```


Common Storage Options

. Local Storage: The default storage engine is localStorage for web apps, which persists data indefinitely unless manually cleared.

. Session Storage: Persists data only for the duration of the page session (until the page is closed).

. AsyncStorage: Often used in React Native applications for persistent storage.

 ```ruby
import storageSession from 'redux-persist/lib/storage/session'; // for sessionStorage

 ```

### Clearing the Persisted State

If you need to clear the persisted state, you can do so by calling purge on the persistor.


 ```ruby
persistor.purge();

 ```

Conclusion

redux-persist is a powerful tool for making your Redux store persistent across sessions. It is highly configurable and supports a variety of storage mechanisms, making it flexible for different use cases. Whether you need to persist the entire state or just a part of it, redux-persist offers the tools to do so efficiently.

# Thunk

In Redux, a thunk is a middleware function that allows you to write action creators that return a function instead of an action object. This is particularly useful for handling asynchronous logic or complex synchronous logic in your Redux application. Here's a breakdown of how thunks work and how you can use them effectively.

### What is a Thunk?

A thunk is essentially a function that delays the execution of another function. In the context of Redux, it allows you to write action creators that return a function rather than an action. This function can then perform asynchronous operations and dispatch actions based on the results of those operations.

### Why Use Thunks?

1. Asynchronous Operations: Thunks allow you to handle asynchronous operations (like API calls) within your action creators. This is important because Redux actions should ideally be plain objects, but API calls and other async operations often require a more complex flow.
2. Complex Logic: Thunks enable you to write more complex logic that can be encapsulated within a function and can dispatch multiple actions, depending on various conditions.

### How to Set Up Redux Thunks

To use thunks in your Redux setup, you need to follow these steps:

1. Install Redux Thunk Middleware:

 ```ruby
npm install redux-thunk

 ```

2. Apply Middleware to the Store:

   When creating your Redux store, you need to apply the thunk middleware using
   applyMiddleware.
   ```ruby
       import { createStore, applyMiddleware } from 'redux';
       import thunk from 'redux-thunk';
       import rootReducer from './reducers';
       
       const store = createStore(rootReducer, applyMiddleware(thunk));

        
   ```

3. Write Thunk Action Creators:

   A thunk action creator is a function that returns another function. This inner function can perform asynchronous operations and dispatch actions.
 ```ruby
      // actions.js
export const fetchDataRequest = () => ({
  type: 'FETCH_DATA_REQUEST'
});

export const fetchDataSuccess = (data) => ({
  type: 'FETCH_DATA_SUCCESS',
  payload: data
});

export const fetchDataFailure = (error) => ({
  type: 'FETCH_DATA_FAILURE',
  payload: error
});

export const fetchData = () => {
  return (dispatch) => {
    dispatch(fetchDataRequest());
    return fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => dispatch(fetchDataSuccess(data)))
      .catch(error => dispatch(fetchDataFailure(error)));
  };
};

        
   ```

### Using Thunks in Components

In your React components, you can dispatch thunk actions just like regular actions.

 ```ruby
// In a React component
import React, { useEffect } from 'react';
import { useDispatch, useSelector } from 'react-redux';
import { fetchData } from './actions';

const DataComponent = () => {
  const dispatch = useDispatch();
  const data = useSelector(state => state.data);
  const loading = useSelector(state => state.loading);
  const error = useSelector(state => state.error);

  useEffect(() => {
    dispatch(fetchData());
  }, [dispatch]);

  if (loading) return <div>Loading...</div>;
  if (error) return <div>Error: {error.message}</div>;

  return (
    <div>
      <h1>Data</h1>
      <pre>{JSON.stringify(data, null, 2)}</pre>
    </div>
  );
};

export default DataComponent;

   ```

 Summary

 Thunks in Redux provide a powerful way to handle asynchronous actions and complex logic. By using redux-thunk, you can write action creators that return functions instead of plain action objects, enabling you to dispatch actions based on asynchronous operations and maintain cleaner and more manageable code.

 
   
