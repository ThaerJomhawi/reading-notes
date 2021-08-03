# Passing Functions as Props

### 

## React Docs - lists and keys

### 1-What does .map() return?

 map function in general to go through each element inside array

### 2-If I want to loop through an array and display each value in JSX, how do I do that in React?

You can build collections of elements and include them in JSX using curly braces {}.

We return a (li) element for each item and we assign the resulting array of elements to listItems, then include the listItems array inside a (ul) element, and render it to the DOM (ReactDOM.render)

### 3-Each list item needs a unique ____.

key 

### 4-What is the purpose of a key?

Keys help React identify which items have changed, are added, or are removed, so it give the element stable identity. you can pick a key by using a string that uniquely identifies a list item among its siblings. usually we are using IDs from the data as keys. But only if items have no stable IDs we use item index as a key.

*-------------------------------*


## The Spread Operator

###

### 1-What is the spread operator?

syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.

In JavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments

### 2-List 4 things that the spread operator can do.

1-Using Math functions
2-Using an array as arguments
3-Adding an item to a list
4-Adding to state in React

### 3-Give an example of using the spread operator to combine two arrays.

const cars = ['🚗', '🚙'];
const trucks = ['🚚', '🚛'];

// Method 1: Concat
const combined1 = [ ].concat(cars, trucks);

// Method 2: Spread
const combined2 = [...cars, ...trucks];

// Result
// [ '🚗', '🚙', '🚚', '🚛' ]

### 4-Give an example of using the spread operator to add a new item to an array.

const fewFruit = ['🍏','🍊','🍌']
const fewMoreFruit = ['🍉', '🍍', ...fewFruit]
console.log(fewMoreFruit) //  Array(5) [ "🍉", "🍍", "🍏", "🍊", "🍌" ]

### 5-Give an example of using the spread operator to combine two objects into one.

const objectOne = {hello: "🤪"}
const objectTwo = {world: "🐻"}
const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}
console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }
const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}
objectFour.laugh() // 😂😂😂😂😂

###

### How to Pass Functions Between Components


### 1-In the video, what is the first step that the developer does to pass functions between components?

creat the function wherever the state that we are going to change

### 2-In your own words, what does the increment function do?

receiving the arrays item, loop through the array and find the matching one to update

### 3-How can you pass a method from a parent component into a child component?

by passing it as props

### 4-How does the child component invoke a method that was passed to it from a parent component?

by using special attribute that attach to the component ( Refs. React)