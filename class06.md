## Chapter 3: Object Literals


***WHAT IS AN OBJECT?***

- objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on new names

1. IN AN OBJECT: VARIABLES BECOME KNOWN AS PROPERTIES : If a variable is part of an object, it is called a property. Properties tell us about the object, such as the name of a hotel or the number of rooms it has. Each individual hotel might have a different name and a different number of rooms

2. IN AN OBJECT: FUNCTIONS BECOME KNOWN AS METHODS : If a function is part of an object, it is called a method. Methods represent tasks that are associated with the object. For example, you can check how many rooms are available by subtracting the number of booked rooms from the total number of rooms.




- variables and named functions, properties and methods have a name and a value. In an object, that name is called a key
- An object cannot have two keys with the same name. This is because keys are used to access their corresponding values.
- string, number, Boolean, array, or even another object. The value of a method is always a function.

### CREATING AN OBJECT : CONSTRUCTOR NOTATION

 the new keyword and the object constructor create a blank object . you can then add properties and method to the object

 ## Chapter 5: Document Object Model

- The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window

- The DOM is neither part of HTML, nor part of JavaScript; it is a separate set of rules. It is implemented by all major browser makers, and covers two primary areas

1. MAKING A MODEL OF THE HTML PAGE
2. ACCESSING AND CHANGING THE HTML PAGE

 THE DOM TREE IS A MODEL OF A WEB PAGE

 As a browser loads a web page, it creates a model of that page. The model is called a DOM tree, and it is stored in the browsers' memory. It consists of four main types of nodes

1. THE DOCUMENT NODE
2. ELEMENT NODES
3. ATTRIBUTE NODES
4. TEXT NODES

### WORKING WITH THE DOM TREE


***Accessing and updating the DOM tree involves two steps***

1. Locate the node that represents the element you want to work with.
2. Use its text content, child elements, and attributes.

### CACHING DOM QUERIES

- Methods that find elements in the DOM tree are called DOM queries. when you need to work with an element more than once , you should use a variable to store the result of this query

- When people talk about storing elements in variables, they are really storing the location of the elements within the DOM tree in a variable . the properties and methods of that element node work on the variable

### ACCESSING ELEMENTS

- DOM queries may return one element, or they may return a Nodelist, which is a collection of nodes

### METHODS THAT SELECT INDIVIDUAL ELEMENTS

getElementBuId() and querySelector() can both search an entire documents and return individual elements. both use a similar syntax

### SELECTING ELEMENTS USING ID ATTRIBUTES

get ElementById () allows you to select a single element node by specifying the value of its id attribute

This method has one parameter: the value of the id attribute on the element you want to select. This value is placed inside quote marks because it is a string. The quotes can be single or double quotes, but they must match

### NODELISTS: DOM QUERIES THAT RETURN MORE THAN ONE ELEMENT

- When a DOM method can return more than one element, it returns a Nodelist (even if it only finds one matching element)

### SELECTING AN ELEMENT FROM A NODELIST

- There are two ways to select an element from a Nodelist

1. The item() method
2. array syntax

- Both require the index number of the element you want

### SELECTING ELEMENTS BY TAG NAME

The getElementsByTagName () method allows you to select elements using their tag name

The element name is specified as a parameter, so it is placed inside the parentheses and is contained by quote marks

- Note that we do not include the angled brackets that surround the tag name in the HTML (just the letters inside the brackets)

### SELECTING ELEMENTS USING CSS SELECTORS

querySe 1 ector() returns the first element node that matches the CSS-style selector. querySe 1ectorA11 () returns a Nodelist of all of the matches

- Both methods take a CSS selector as their only parameter. The CSS selector syntax offers more flexibility and accuracy when selecting an element than
