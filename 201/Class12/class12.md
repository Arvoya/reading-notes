# Class 12 Reading Assignment

Reading assignment 'Read 12'

## Questions and Answers

### JavaScript Canvas

1. What does the `<canvas>` allow a developer to achieve? Allows one to draw or code 2D graphics
2. What is the importance of closing `</canvas>` tag? Ensures that whatever is between the tags will run incase there is an error with the browser.
3. Explain what the `getContext()` method does. JS uses this method to create the context of how the canvas will run.

---

### Chart.js Documentation

1. What is Chart.js and how can it be brought into your project? It is a library that currently needs to be brought similar to attaching a seperate JS file. Use the `<script>` element and use the `src` property.
2. List 3 different Chart types you can create using Chart.js. You can make Bar charts, Pie charts, Line charts.

---

### Easily Create Stunning Animated Charts with Chart.js

1. What are some advantages to displaying data via a chart over a table? Visually easier to understand, so the user can read the information required.
2. How could Chart.js aid your previously created applications visually? Probably could have used it for Salmon Cookies project.

## Notes

Here are the notes I’ve taken while reading the following blogs:

[JavaScript Canvas](https://www.javascripttutorial.net/web-apis/javascript-canvas/) \| [Chart.js Documentation](https://www.chartjs.org/docs/latest/) \| [Easily Create Stunning Animated Charts with Chart.js](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

## Understanding JS Canvas

`<canvas>` - is an HTML element that allows JavaScript to draw 2D graphics. It required 2 attributes: `width` & `height`.

``` HTML
<canvas width="500" height="300" id="canvas"></canvas>
```

Everything within the element `<canvas></canvas>` is used to display in situations where the canvas doesn't properly load. So the programer can leave information letting the user know.

`getContext()` - is a method in JavaScript used to return a context object. The parameter to create these objects is:

* `'2d'` - Which will give ways for drawing 2D shapes

## Understanding Chart.js Documentation

Chart.js is a charting library for JavaScript. You can create multiple types of charts and even combine them within the same `<canvas>` element using JavaScript.

Types of charts:

1. Area Chart
2. Bar Chart
3. Bubble Chart
4. Doughnut and Pie Charts
5. Line Chart
6. Mixed Chart TYpes
7. Polar Area Chart
8. Radar Chart
9. Scatter Chart

