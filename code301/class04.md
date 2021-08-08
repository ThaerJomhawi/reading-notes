# React and Forms
## React Docs - Forms

### What is a ‘Controlled Component’?

An input form element whose value is controlled by React in this way is called a “controlled component”.

### Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.

In HTML, form elements such as input, textarea, and select typically maintain their own state and update it based on user input. 
In React, mutable state is typically kept in the state property of components, and only updated with setState().


### How do we target what the user is entering if we have an event handler on an input field?

When you need to handle multiple controlled input elements, you can add a name attribute to each element and let the handler function choose what to do based on the value of event.target.name.

## Reference React Docs - Forms


### Why would we use a ternary operator?

The condition is what you’re actually testing. The result of your condition should be true or false or at least coerce to either boolean value. A ? separates our conditional from our true value. Anything between the ? and the : is what is executed if the condition evaluates to true. Finally a : colon. If your condition evaluates to false, any code after the colon is executed.

### Rewrite the following statement using a ternary statement:
~~~
 if(x===y){ console.log(true); } else { console.log(false); }

if ( x===y ) { value if true; } else { value if false; }

if(x===y) ? value if true : value if false

~~~

