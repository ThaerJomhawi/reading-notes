# State and Props

## React Lifecycle
#### Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
	- render happens first

#### What is the very first thing to happen in the lifecycle of React?
	- the constructor

####  Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates

1. constructor 
2. render 
3. component did mount 
4. react updates 
5. componentWillUnmount

####  What does componentDidMount do?
* to load anything using a network request or initialize the DOM.
* it's also good to set up any subscriptions

### React Bootstrap Documentation
- react bootstrap completely reimplement bootsr
- the best way to install react bootstrap is by npm package
- if you want to customize bootstrap sass files, or dont want to use CDN for stylesheet,vanilla bootstrap might be the answer here

### Netlify
- we can deploy our react app to netlify
- it's basically a host server we use to deploy our pages
- we use netlify because github doesn't support react

### React State Vs Props

####  What types of things can you pass in the props?
	- the things you want to pass to a function
	 - what you want to initialize your component to or what you want your component to render like
	- mostly components
####  What is the big difference between props and state?
	- props gets passed into a component
	- props is handled and updated outside the component
	- state is handled and updated inside the component
	

#### When do we re-render our application?
	 - when we change the state inside the application

#### What are some examples of things that we could store in state?
	- inside a form 
	- checkboxes
	- inputs
	- selectbox


