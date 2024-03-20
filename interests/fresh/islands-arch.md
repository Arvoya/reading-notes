# Island Architecture

[Blog](https://jasonformat.com/islands-architecture/)

> render HTML pages on the server, and inject placeholders or slots around
highly dynamic regions. These placeholders/slots contain the server-rendered
HTML output from their corresponding widget. They denote regions that can then
be "hydrated" on the client into small self-contained widgets, reusing their
server-rendered initial HTML.

![Island Arch Image](https://res.cloudinary.com/wedding-website/image/upload/v1596766231/islands-architecture-1.png)

In traditional web-development you may have a `<script>` that looks for an
image carousel in the page and instantiates a jQuery plugin on it. Instead,
that image carousel would be rendered on the server and a dedicated `<script>`
emitted for it that loads the images carousel implementation and in-place
upgrade it to be interactive.

## Does it matter?

> As it turns out, there are number of benefits to the group of approaches
described here when compared to typical Single Page Application architectures.
