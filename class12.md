# Chart.js, Canvas

## Canvas:
The HTML `<canvas>` element is used to draw graphics, via JavaScript.

canvas is a rectangular area on an HTML page.

canvas syntax:`<canvas id="myCanvas" width="200" height="100"></canvas>`

With canvas we can draw Text, Graphics.

How to draw on the Canvas With JavaScript:
* Select the canvas element `var canvas = document.getElementById("firstCanvas");`
* Create a drawing object `var ctx = canvas.getContext("2d");`
* Draw on Canvas `ctx.fillStyle = "#FF0000"; ctx.fillRect(50,0,100,500);`

## Chart.js
 Chart.js, a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page.

To use Chart.js we must download it first and then we should import the script.

We can use Chart.js to draw the follows:
* line chart
* pie chart
* bar chart
* Radar Chart
* Polar Area Char
* Bubble Chart