# Class 5 Reading Assignment

Reading assignment 'Read 05'

## Questions and Answers

### HTML

1. What is a real world use case for the `alt` attribute being used in a website? To describe an image within the HTML file with text.
2. How can you improve accessibility of images in an HTML document? By the using the `alt` attribute within an `<img>` element.
3. Provide an example of when the `figures` element would be useful in an HTML document. When you want to have an image have a caption. Or when you want the space that the image will take be loaded up, so it isn't as jarring for the viewer/user.
4. Describe the difference between a `gif` image and an `svg` image pretend you are explaining to an elder in your community. You know how your phone or computer can show you different images? Some of them are small, some of them are large. Some can look really clear and others you start seeing various boxes of color. All of these images can be of a different type. `gif` is one of those types, and it only uses 250 colors. `svg` is another type, but those are mostly the shapes and logos, and no matter how big or how small you zoom in or out. It will always keep its high quality and crisp image.
5. What image type would you use to display a screenshot on your website and why? I would use either a PNG or JPG. Either seem to work well with websites, it depends on the quality and size of the image I would need.

-----------------------------------------------------------

### CSS

1. Describe the difference between foreground and background colors of an HTML element, pretend you are talking to someone with no technical knowledge. When you look at a website. Sometimes you can see that the background of the website is white or black or any color. This is the background colors of the `<body>` element. Elements are basically boxes and a website is boxes inside of boxes. Or boxes next to boxes. Each box can have a background. And the content inside each box can have its own color making it the foreground.
2. Your friend asks you to give his colorless blog website a touch up. How would you use color to give his blog some character? I'd ask for the tone and feel they want their website to be. Are they looking for dark and serious, or colorful and playful? Do they want vibrant colors or colors that are easy on the eyes? I'd have to know much more detail.
3. What should you consider when choosing fonts for an HTML document? Understand the use of 'web-safe' fonts, and consider the professionalism you are looking for in a website.
4. What do `font-size`, `font-weight`, and `font-style` do to HTML text element? These properties change the font size, if its bold, or italicized.
5. Describe two ways you could add spacing around the characters displayed in an `h1` element. Use the `letter-spacing` or `word-spacing` CSS properties to change the spacing.

## Notes

Here are the notes I’ve taken while reading the following blogs:

[Using Images in HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML) \| [Common Image Types](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types) \| [Choosing Image Formats](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#choosing_an_image_format) \| [Using Color in CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Colors/Applying_color) \| [Styling HTML Text Elements](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals)

## Using Images in HTML

`alt` - using this element allows those who may use or require a screen reader. It will give them an text description of the image. Also, for those who may experience connect errors that prevent the image from showing.

`<figure>` - element that represents self-contained content, with the optional caption. Usually attached with an image.

`<figcaption>` - element nested with the `<figure>` element that provides text to the figure.

## CSS Color

`color` - this CSS property defines the foreground color of the elements content
`background-color` - defines the elements background color.

### Fonts

Things to consider:

* Web-safe fonts- fonts that generally work with any browser
* Fonts that match the style you are looking for
* Font Stacks - Gives the browser multiple fonts it can choose from

### CSS properties for fonts

`font-size` - take various measurements to give the size of the font a value.
`font-style` - can give the value `normal`, `italic`, and `oblique`
`font-weight` - can give the value `normal`, `bold`, `lighter`, `bolder`, `100`-`900`.

### Spacing properties

`letter-spacing` - set the spacing between letters
`word-spacing` - set the spacing between words