---
layout: page
title: Card Group
chapter: "5.2"
thumb: cardGroup.jpg
prev: /card/
---
<div class="demo">
{% include_relative assets/examples/card-group.html %}
</div>
Now let’s say we want to group a bunch of cards into a single Card Group component. There are two tricky requirements to consider here:

1. We want each card to have equal width, even if one card contains more content than another card.
2. We want the height of all the card descriptions to be equal. Again, this should hold true even if one card’s description is longer than another card.
Without flexbox, you would probably have to resort to using a `table` element to meet these requirements. Or possibly you could absolutely position all of the elements and use a combination of percentage-based dimensions, pixel-based dimensions, and the `calc` function. That sounds pretty complex!

With flexbox, the solution becomes a bit more elegant, but it does require us to use a new flexbox property. Unlike the ones we’ve used so far, this property is applied to the **children**, not the container.

We'll set `flex: 1 1 0%` on each card, to make their widths equal within the container. This property is a short-hand for setting three specific flexbox properties:

- `flex-grow: 1` indicates how the element expands as its container gets larger. By default, the value is 0. We’ll set it to 1 so that the card will expand as much as possible to fill the container.
- `flex-shrink: 1` controls how the element shrinks as its container gets smaller. By default, this value is 1. When we set it to 1, we tell the card to shrink as much as it has to, to fit into its container.
- `flex-basis: 0%` determines the size of the card before the remaining space in its container is applied to it. By setting it to 0, we let its size be solely determined by the size of the container. We use a percentage because of an IE 11 bug in which the browser ignores unitless flex-basis values.

These properties take care of our first requirement. For our second requirement we can reuse the short-hand property, tweaked slightly, and applied to each card’s description: `flex: 1 1 auto`.

- `flex-basis: auto` will cause the size of the card’s description to affect its height. This means that the card with the longest description will be the tallest, causing the height of the container to grow. Because each card description also has `flex-grow: 1` set on it, the cards with shorter descriptions will expand to fill the container.

```css
{% include_relative assets/styles/card-group.css %}
```
```html
{% include_relative assets/examples/card-group.html %}
```
