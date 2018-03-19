What is React? (from: https://reactjs.org/tutorial/tutorial.html)

* "React is a declarative, efficient, and flexible JavaScript library for building user interfaces."

React Component Example:

                class ShoppingList extends React.Component {
                render() {
                return (

                <div className="shopping-list">
                <h1>Shopping List for {this.props.name}</h1>
                <ul>
                <li>Instagram</li>
                <li>WhatsApp</li>
                <li>Oculus</li>
                </ul>
                </div>
                );
                }
                }

* ShoppingList is a React component class
* A component takes in parameters called props and returns views to display via render (a method)
* Render returns "a description of waht you want to render, and then React takes that description and renders it to the screen"
* Render returns a React element
* JSX syntax: "you can put any JavaScript expression within braces inside JSX. Each React element isa JS object. These objects can be stored in a variable or passed in later

What is ReactJS? (from: https://git.generalassemb.ly/ga-wdi-lessons/react-intro)

* "React is a JavaScript library used to craft modern day UI and views for the front-end in web applications."
* In terms of MVC (models, views, controllers), React is the views layer
* React can work with any back-end langauge

Components (Verus Templates)

* In a fixed template one might build 3 separatep ages-- an about page, a homepage, and a products page, each content area is pre-made
* In a component model, specific pieces (components) are made-- for example, header, nav, text area and then are applied to pages as needed

What does F.I.R.S.T mean (in terms of components)?

* "A React component is built to expect an input and render a UI with it. More importantly, a well-structured component only receives data specific to its purpose."
* F= focused
* I= independent
* R= resuable
* S= small
* T= testable

How to do the initial setup for react?

1.  open terminal
2.  cd to folder you want to work in
3.  type "create-react-app" into the command line + what you want to call your react app --> "create-react-app blog-app"
4.  cd into blog-app
5.  run "code ."
6.  type in "npm run start" --> you should then be able to see what is currently rendering at "http://localhost:3000"

* along with installing dependencies for us create-react-app builds out a basic file structure that looks like this:

                ├──README.md
                ├──  favicon.ico
                ├──  index.html
                ├──  node_modules
                ├──  package.json
                └──  src
                    ├──  App.css
                    ├──  App.js
                    ├──  index.css
                    ├──  index.js
                    └──  logo.svg

What's the most basic unit in React?

* a component
* "Components can be thought of as functional elements that take in data and as a result, produce a dynamic UI."

Hello World React Component Example:

                // bring in React and Component instance from React
                import React, {Component} from 'react'

                // define our Hello component
                class Hello extends Component {
                // what should the component render
                render () {
                    // Make sure to return some UI
                    return (
                    <h1>Hello World!</h1>
                    )
                }
                }

                export default Hello

Broken down into little parts...

* class Hello: this is the component, in this case the component is called "Hello"
* extends Component: tells the newly created class to inherit the component definition of a class
* render: this method creates a virtual DOM
* export default Hello: exports or "exposes the Hello class to other files"

What is JSX?

* a langauge that compiles to Javascript & looks like HTML

What's the Virtual Dom?

* "The Virtual DOM is a Javascript representation of the actual DOM. The virtual DOM is a staging area for changes that will eventually be implemented.
* can keep track of changes in the DOM and compare instances

How to make things a little more dynamic( or not hard-coded)?

1.  pass in data where we are rendering our component (using same example, in src/index.js):

                 import React from 'react'
                 import ReactDOM from 'react-dom'
                 import Hello from './App.js'

                 ReactDOM.render(
                 <Hello name={"Nick"} />,
                 document.getElementById('root')
                 )

2.  in component definition, replace "world" with this.props.name:

                 class Hello extends Component {
                 render () {
                     return (
                     <h1>Hello {this.props.name}</h1>
                     )
                 }
                 }

What are .props?

* .props = properties
* props = immutable (can't be changed)
* props are defined in dev and then passed in as attributes to JSX element in the render method

How to work with .props?

1.  still in src/index.js add in another prop (age):
    import React from 'react';
    import ReactDOM from 'react-dom'
    import Hello from './App.js'

                 ReactDOM.render(
                 <Hello name={"Nick"} age={24} />,
                 document.getElementById('root')
                 )

2.  back in the component definition add...
    class Hello extends Component {
    render () {
    return (

                    <div>

                <h1>Hello {this.props.name}</h1>

            <p>You are {this.props.age} years old</p>

        </div>

    )
    }
    }
