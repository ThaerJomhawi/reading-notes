# Forms

An HTML form is used to collect user input. The user input is most often sent to a server for processing.

> The < form> Element 

The HTML < form> element is used to create an HTML form for user input:

< form>
.
form elements
.
</ form>

The < form> element is a container for different types of input elements, such as: text fields, checkboxes, radio buttons, submit buttons, etc.

> The < input> Element

The HTML < input> element is the most used form element.

An < input> element can be displayed in many ways, depending on the type attribute.

Here are some examples:

Type|	Description
------|-----------
< input type="text">|	Displays a single-line text input field
< input type="radio">	|Displays a radio button (for selecting one of many choices)
< input type="checkbox">|	Displays a checkbox (for selecting zero or more of many choices)
< input type="submit">|	Displays a submit button (for submitting the form)
< input type="button">|	Displays a clickable button

> Text Fields

The < input type="text"> defines a single-line input field for text input.

< form>
  < label for="fname">First name:</ label>< br>
  < input type="text" id="fname" name="fname">< br>
  < label for="lname">Last name:</ label>< br>
  < input type="text" id="lname" name="lname">
</ form>

This is how the HTML code above will be displayed in a browser:

First name:
<input>

Last name:
<input>


> The < label> Element

Notice the use of the < label> element in the example above.

The < label> tag defines a label for many form elements.

The < label> element is useful for screen-reader users, because the screen-reader will read out loud the label when the user focus on the input element.

The < label> element also help users who have difficulty clicking on very small regions (such as radio buttons or checkboxes) - because when the user clicks the text within the < label> element, it toggles the radio button/checkbox.

The for attribute of the < label> tag should be equal to the id attribute of the < input> element to bind them together.

> Radio Buttons

The < input type="radio"> defines a radio button.

Radio buttons let a user select ONE of a limited number of choices.

< form>
  < input type="radio" id="male" name="gender" value="male">
  < label for="male">Male</ label>< br>
  < input type="radio" id="female" name="gender" value="female">
  < label for="female">Female</ label>< br>
  < input type="radio" id="other" name="gender" value="other">
  < label for="other">Other</ label>
</ form>

This is how the HTML code above will be displayed in a browser:

- Male
- Female
- Other

> Checkboxes

The < input type="checkbox"> defines a checkbox.

Checkboxes let a user select ZERO or MORE options of a limited number of choices.

< form>
  < input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
  < label for="vehicle1"> I have a bike</ label>< br>
  < input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
  < label for="vehicle2"> I have a car</ label>< br>
  < input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
  < label for="vehicle3"> I have a boat</ label>
</ form>

This is how the HTML code above will be displayed in a browser:

[] I have a bike

[] I have a car

[] I have a boat