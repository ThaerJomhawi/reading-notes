### HTML5 : It is a simple client side database that allows the users to save the data in the form of *key/value pairs*. 
* Web storage is more secure, and large amounts of data can be stored locally, without affecting website performance.

* This data persists even after you go away from the web site, close your browser tab, exit your browser, or what have you. HTML5 supported by many browsers. 

* After store your data (which based on a key) you can call the data by that key (The key is a string) , and by the way the data which stored by that key cosidered as a **string**. The types of data can be stored are : strings, Booleans, integers or floats (any type supported by JavaScript).

### HTML web storage provides two objects for storing data on the client:

* 1- `localStorage` - stores data with no expiration date.Where the data will not be deleted when the browser is closed, and will be available the next day, week, or year.
* 2- `SessionStorage` - It is equal to the *`localStorage`* object, except that it stores the data for only one session. The data is deleted when the user closes the specific browser tab.