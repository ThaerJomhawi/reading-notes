# Lists

There are lots of occasions when we need to use lists. HTML provides us with three different types:

*● Ordered lists are lists where each item in the list is numbered. For example, the list might be a set of steps for a recipe that must be performed in order, or a legal contract where each point needs to be identified by a section number.*


**form:**

<ol>The ordered list is created with the <ol> element.<li>Each item in the list is placed between an opening <li> tag and a closing </li> tag.




*● Unordered lists are lists that begin with a bullet point (rather than characters that indicate order).*

**form:**


<ul>The unordered list is created with the <ul> element.<li>Each item in the list is placed between an opening <li> tag and a closing </li> tag. (The listands for list item).

*● Definition lists are made up of a set of terms along with the definitions for each of those terms.*



**form:**



<dl>The definition list is created with the <dl> element and usually consists of a series of terms and their definitions.Inside the <dl> element you will usually see pairs of <dt> and <dd> elements.<dt>This is used to contain the term being defined (the definition term).<dd>This is used to contain the definition.Sometimes you might see a list where there are two terms used for the same definition or two different definitions for the same term.
Nested Lists

You can put a second list inside an <li> element to create a sub-list or nested list.Browsers display nested lists indented further than the parent list. In nested unordered lists, the browser will usually change the style of the bullet point too.

# Boxes

At the beginning of this section on CSS, you saw how CSS treats each HTML element as if it lives in its own box.You can set several properties that affect the appearance of these boxes.

How to Control the dimensions of your boxes

● Create borders around boxes

● Set margins and padding for boxes

● Show and hide boxes

● Once you have learned how to control the appearance of each box, you will see how to position these boxes on your pages in Chapter 15 when we look at page layout.

### Box Dimensions width, height

By default a box is sized just big enough to hold its contents. To set your own dimensions for a box you can use the height and width properties.

The most popular ways to specify the size of a box are to use pixels, percentages, or ems.

Traditionally, pixels have been the most popular method because they allow designers to accurately control their size.When you use percentages, the size of the box is relative to the size of the browser window or, if the box is encased within another box, it is a percentage of the size of the containing box.When you use ems, the size of the box is based on the size of text within it.

Designers have recently started to use percentages and ems more for measurements as they try to create designs that are flexible across devices which have different-sized screens.

#### limiting WiDth min-width, max-width

These are very helpful properties to ensure that the content of pages are legible (especially on the smaller screens of handheld devices). For example, you can use the max-width property to ensure that lines of text do not appear too wide within a big browser window and you can use the min-width property to make sure that they do not appear too narrow.

We may find it helpful to try this example out in your browser so that you can see what happens when you increase or decrease the size of the browser window

#### limiting heightmin-height, max-height

In the same way that you might want to limit the width of a box on a page, you may also want to limit the height of it. This is achieved using the min-heightand max-height properties.

If the box is not big enough to hold the content, and the content expands outside the box it can look very messy. To control what happens when there is not enough space for the content of a box, you can use the overflowproperty, which is discussed on the next page.

### Border, margin & padding

1-Border:

Every box has a border (even if it is not visible or is specified to be 0 pixels wide). The border separates the edge of one box from another.

2-Margin:

Margins sit outside the edge of the border. You can set the width of a margin to create a gap between the borders of two adjacent boxes.

3-Padding

Padding is the space between the border of a box and any content contained within it. Adding padding can increase the readability of its contents.

## Control flow

The control flow is the order in which the computer executes statements in a script.

Code is run in order from the first line in the file to the last line, unless the computer runs across the (extremely frequent) structures that change the control flow, such as conditionals and loops.

## Basic JavaScript Instructions

The name must begin with a letter, dollar sign ($),or an underscore (_). It must not start with a number.

All variables are case sensitive, so score and Score would be different variable names

The name can contain letters, numbers, dollar sign ($), or an underscore (_).

Use a name that describes the kind of information that the variable stores.

you cannot use keywords or reserved words. Keywords are special words that tell the interpreter to do something.

If your variable name is made up of more than one word, use a capital letter for the first letter of every word after the first word.


#### USING A VARIABLE TO STORE A BOOLEAN
>

A Boolean variable can only have a value of true or false, but this data type is very helpful.

Programmers sometimes use shorthand to create variables. Here are three variations of how to declare variables and assign them values:

Variables are declared and values assigned in the same statement.

Three variables are declared on the same line, then values assigned to each.

Two variables are declared and assigned values on the same line. Then one is declared and assigned a value on the next line.

**CHANGING THE VALUE OF A VARIABLE**

Once you have assigned a value to a variable, you can then change what is stored in the variable later in the same script.

Once the variable has been created, you do not need to use the var keyword to assign it a new value. You just use the variable name, the equals sign (also known as t he assignment operator), and the new value for that attribute.