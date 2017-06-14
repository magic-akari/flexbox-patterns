---
layout: page
title: Scrolling Mosaic
chapter: "8.2"
thumb: mosaic.jpg
---
<div class="demo">
{% include_relative assets/examples/mosaic.html %}
</div>
What if your images are varying sizes, and you want to have a more interesting, organic layout? You can do this by changing the main axis with the `flex-direction` property. This causes your photos to flow vertically and wrap to subsequent columns (instead of rows).

As a side-effect, your content can now be scrolled horizontally. This introduces one small bug: when you scroll to the end of overflowing flexbox content, the scroll ends when the children themselves are scrolled into view.

This means that any margin around them or padding on the container is ignored, and you end up with the children flush against the edge of the container. From a visual perspective, this looks pretty weird.

So far, I’ve found the best solution is to add an invisible pseudo-element on the last child in the container. You can use this pseudo-element to make the container treat the last child as if it’s wider than it looks. This will create some space between the last child and the right edge of the container. See for yourself by scrolling all the way to the right side of the Scrolling Mosaic.

```css
{% include_relative assets/styles/mosaic.css %}
```
```html
{% include_relative assets/examples/mosaic.html %}
```
