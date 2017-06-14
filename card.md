---
layout: page
title: Card
chapter: "5.1"
thumb: card.jpg
next: /card-group/
---
<div class="demo">
{% include_relative assets/examples/card.html %}
</div>
This component makes use of the same properties we’ve been using so far:

- `display: flex`
- `flex-direction: column`
- `justify-content: center`
- `align-items: center`

We’re using these properties in the same way as in previous examples, primarily to order children along a vertical main axis, and to center children within their container.

This is really nothing new, but when we get to the next example, things will get interesting…
```css
{% include_relative assets/styles/card.css %}
```
```html
{% include_relative assets/examples/card.html %}
```
