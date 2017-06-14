---
layout: page
title: Post
chapter: "5.3"
thumb: post.jpg
---
<div class="demo">
{% include_relative assets/examples/post.html %}
</div>
If you’re building a social media platform, you’ll want to take a look at this pattern, which is an implementation of the generic [media object pattern](http://www.stubbornella.org/content/2010/06/25/the-media-object-saves-hundreds-of-lines-of-code/). As Philip Walton demonstrates in [Solved by Flexbox](https://philipwalton.github.io/solved-by-flexbox/demos/media-object/), this pattern is incredible versatile.

A Post consists of a person’s portrait and name placed to the left of a body of text. We want the portrait to stay a fixed width and height while the body expands horizontally to fill the remaining space in its container, regardless of how much text it contains.

We’ll use the same properties we used in the Card Group example, but in slightly different ways. For the portrait, we’ll set `flex: 0 1 auto`. As I explained in the last example, this is short-hand for setting the `flex-grow`, flex-shrink, and flex-basis properties:

- `flex-grow: 0` will prevent this element from expanding to fill its container.
- `flex-shrink: 1` will cause this element to shrink as its container shrinks.
- `flex-basis: auto` will prevent it from shrinking below the width determined by its content.

For the body of text, we’ll set `flex: 1 1 0%`:

- `flex-grow: 1` will allow the body of text to expand to fill its container.
- `flex-shrink: 1` will allow it to shrink as its container shrinks.
- `flex-basis: 0%` will cause its size to be solely determined by the size of the container, instead of by its content.

```css
{% include_relative assets/styles/post.css %}
```
```html
{% include_relative assets/examples/post.html %}
```
