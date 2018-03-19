What are props, What is state? (from:https://git.generalassemb.ly/ga-wdi-lessons/react-state-and-props)

* "props are passed into a component, but state is local or native to the component"
* "While we cannot change props (immutable) from within a component, we can change a component's state (mutable)."

- "Props are one of the things that make React so powerful and help us make independent and reusable components."
- "The limitation of props is that we can't change the data from within the component. The data that we can change within a component is called state."

How state connects to rendering?

* when state changes our components re-render
* "Our UI gets updated when state changes. The user takes some action, like submitting information via a form, and the component holding that form has a state that is updated with the value of the user's input."

Steps to building a react app: (from: https://reactjs.org/docs/thinking-in-react.html#start-with-a-mock)

1.  Start with a mock
2.  Break up user interface into components and component hierarchy - draw boxes around every component & subcomponent and give them all names - a component should ideally only do one thing - arrange components into hierarchy: "components that appear within another component in the mock should appear as a child in the hierarcy"
3.  Build a static version of the app
    * build a version that takes the model model and renders something but is not interactive
    * build components that reuse other components and pass in data using props
    * props are a way of passing data from parent to child
    * DO NOT USE STATE YET
    * components will only have render methods here
4.        Identify minimal (but complete) representation of the user iterface state
        - to make UI interactive, you need to be able to trigger changes to your underlying data model
        - narrow down which items need to be updated with state
5.  Figure out where state should go

    * For each piece of state in your application:

    - Identify every component that renders something based on that state.
    - Find a common owner component (a single component above all the components that need the state in the hierarchy).
    - Either the common owner or another component higher up in the hierarchy should own the state.
    - If you can’t find a component where it makes sense to own the state, create a new component simply for holding the state and add it somewhere in the hierarchy above the common owner component.

6.  Add inverse data flow
