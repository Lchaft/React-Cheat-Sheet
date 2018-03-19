What is React?

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
