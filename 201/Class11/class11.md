# Class 11 Reading Assignment

Reading assignment 'Read 11'

## Questions and Answers

### Video & Audio Content

1. Explain how the ability to use video and audio on the web has evolved since the early 2000's. There used to be other technologies like Flash and Silverlight, but due to accessibility and security concerns they are now obsolete.
2. Describe the use of the `src` and `controls` attributes in the video `<video>` element. `src`, like in images is used to give the source of the video. `controls` is there to give the user playback control.
3. Why is it important to have fallback content inside the `<video>` element? Incase the video doesn't load.

---

### Guide to Grid

1. How does Grid layout differ from Flex? It's 2-dimensional rather than 1. I think its a bit better for static context.
2. Grid container, grid item, and grid line are a few important terms to understand when using Grid. Yea these terms help understand which parts of the grid one may be manipulating. The container its self, the content, or its layout.

---

### Responsive Images

1. Besides making a site visually appealing across different screen sizes, why should developers make images responsive? Mobile phones bandwidth is another important factor to consider.
2. Define the following `<img>` attributes `srcset` and `sizes`. Write an example how they are used. `<img>` - is the HTML element used to place an image. `srcset` - gives the browser a variety of images and sizes to choose from. `sizes` -helps the browser pick which image based on some rules.
3. How is `srcset` more helpful for responsive images than CSS or JavaScript? It's more helpful because it runs before the CSS or JS files are executed.

## Notes

Here are the notes I’ve taken while reading the following blogs:
[Video and Audio Content](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content) \| [A Complete Guide To Grid](https://css-tricks.com/snippets/css/complete-guide-grid/) \| [Responsive Images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)

## Audio & Video

To put in a video you will use the HTML element `<video>`. Inside this element you can use the same `src` attribute that you use form images, and link the the video. You will need to add the `controls` attribute so that the user can have control over the playback of the video.

A paragraph can be placed inside of the `<video>` tags so that incase there is an issue, you can display a description or a link.

## Understanding CSS Grid

`grid` - is a display type in CSS that is a two-dimensional grid-based layout.

When created you use a parent container element. Then you `display: grid` to create the grid.

`grid-template-columns` - sets the number and size of the columns

`grid-template-rows` - sets the number and size of the columns.

### Other important terms:

* `Grid Line` - divided lines betweens the rows and columns.
* `Grid Cells` - The space between adjacent rows and columns. Where the actual content sits.
* `Grid Track` - Space between two grid lines running horizontal or vertical
* `Grid Area` - Space surrounded by 4 grid lines consisting of multiple grid cells.

## Understanding Responsive Images

Responsive images within a website can adjust and adapt to the screen size of the user. If they are in fullscreen or half of the screen on a desktop. If it is being viewed on a phone, or in landscape mode. The images ability to respond is what this concept is referring to.

Another way to image responsive is necessary is to help with bandwidth, specifically for mobile users who don't need to download such a large image compared to a desktop or laptop with a giant monitor.

* `srcset` - an attribute that can provide several source images and sizes to provide the browser options
* `sizes` - an attribute that can provide hints to help the browser pick from the `srcset`

These attributes are more helpful because these changes happen before the CSS or JS files are run.
