---
title: "Difference between state and props?"
date: "2021-02-14"
---

Props and state are related. The state of one component will often become the props of a child component. Props are passed to the child within the render method of the parent as the second argument to React.createElement() or, if you're using JSX, the more familiar tag attributes.

`<MyChild name={this.state.childsName} />`

The parent's state value of childsName becomes the child's this.props.name. From the child's perspective, the name prop is immutable. If it needs to be changed, the parent should just change its internal state:

`this.setState({ childsName: 'New name' });`

and React will propagate it to the child for you. A natural follow-on question is: what if the child needs to change its name prop? This is usually done through child events and parent callbacks. The child might expose an event called, for example, onNameChanged. The parent would then subscribe to the event by passing a callback handler.

`<MyChild name={this.state.childsName} onNameChanged={this.handleName} />`

The child would pass its requested new name as an argument to the event callback by calling, e.g., this.props.onNameChanged('New name'), and the parent would use the name in the event handler to update its state.


`handleName: function(newName) {
   this.setState({ childsName: newName });
}`
