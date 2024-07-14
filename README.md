
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
