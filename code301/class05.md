<<<<<<< HEAD
# Putting it all together

## How would you break a mock into a component heirarchy?

1- first thing to do is to draw boxes around every component (and subcomponent) in the mock and give them all names.

2- Use the single responsibility principle, that is, a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

3- After identified the components in our mock, we start arrange them into a hierarchy.

4- Components that appear within another component in the mock should appear as a child in the hierarchy.

## What is the single responsibility principle and how does it apply to components?

it mean that a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

## What does it mean to build a ‘static’ version of your application?

build a static version of your app that renders your data model, which is building components that reuse other components and pass data using props. props are a way of passing data from parent to child and it's a static data. We dont use state Since this is a static version of the app, because State is reserved only for interactivity, that is, data that changes over time.

You can build top-down or bottom-up. it’s usually easier to go top-down, and on larger projects, it’s easier to go bottom-up and write tests as you build

## Once you have a static application, what do you need to add?

 you need to be able to trigger changes to your underlying data model. React achieves this with state.
 
## What are the three questions you can ask to determine if something is state?

1- Is it passed in from a parent via props? If so, it probably isn’t state.

2- Does it remain unchanged over time? If so, it probably isn’t state.

3- Can you compute it based on any other state or props in your component? If so, it isn’t state.

## How can you identify where state needs to live?

For each piece of state in your application:

1- Identify every component that renders something based on that state.

2- Find a common owner component (a single component above all the components that need the state in the hierarchy).

3- Either the common owner or another component higher up in the hierarchy should own the state.

4- If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.
=======
# Putting it all together

## How would you break a mock into a component heirarchy?

1- first thing to do is to draw boxes around every component (and subcomponent) in the mock and give them all names.

2- Use the single responsibility principle, that is, a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

3- After identified the components in our mock, we start arrange them into a hierarchy.

4- Components that appear within another component in the mock should appear as a child in the hierarchy.

## What is the single responsibility principle and how does it apply to components?

it mean that a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

## What does it mean to build a ‘static’ version of your application?

build a static version of your app that renders your data model, which is building components that reuse other components and pass data using props. props are a way of passing data from parent to child and it's a static data. We dont use state Since this is a static version of the app, because State is reserved only for interactivity, that is, data that changes over time.

You can build top-down or bottom-up. it’s usually easier to go top-down, and on larger projects, it’s easier to go bottom-up and write tests as you build

## Once you have a static application, what do you need to add?

 you need to be able to trigger changes to your underlying data model. React achieves this with state.
 
## What are the three questions you can ask to determine if something is state?

1- Is it passed in from a parent via props? If so, it probably isn’t state.

2- Does it remain unchanged over time? If so, it probably isn’t state.

3- Can you compute it based on any other state or props in your component? If so, it isn’t state.

## How can you identify where state needs to live?

For each piece of state in your application:

1- Identify every component that renders something based on that state.

2- Find a common owner component (a single component above all the components that need the state in the hierarchy).

3- Either the common owner or another component higher up in the hierarchy should own the state.

4- If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.
>>>>>>> 4b89f249b88bec9556b5580f7e22ac7a4096fde6
