
<details>
<summary> Some fundamental knowledge</summary>

## SPA
Before any framework each page needs a request to the server to be got and an HTML page with CSS and JS is returned to the user’s browsers and this process is done for all links of pages. Furthermore, SPA applications like React are introduced in which efficient JS codes create and manipulate the dom, and just an HTML page once is got when a user clicks on a link to see a website, and JS links handle other changes of displaying the page and interacting with parts of it.
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
## What do these four React Scripts do?
### Well, think of it like this; how would you start a React app without npm start?
### You’d likely do the following:
1. You’d create a basic HTML file and include a div element with the id of root to let React render its components.
2. You’d then write React code using JSX with the help of React and ReactDOM libraries.
3. You’d transpile and bundle your code using Babel and Webpack.
4. You’d point your transpiled JavaScript code in the HTML file you created back in Step 01 using a <script> tag.

This is an old school approach to building React. It’s time-consuming, error-prone and doesn’t add business value. Therefore, react-scripts start replaces the following process by automating the process with the single command. So, as a user, all you have to do is run the command npm start which would trigger react-scripts start, which would perform steps 1 to 4 automatically and launch the React app for development purposes.

### start
This command will start the development server, and it will also react and display the latest version each time a change occurs with the webpack’s Hot Module Replacement (HMR) feature. In addition, it will show lint errors on the terminal if it fails to start the server in the form of meaningful error messages.

# Rendering
In our app we have main.jsx or index.js file in which this code is located 
```ruby
ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
)
```
This code means that react dom should render the entire app that is in App component in root element which is in index.html file



