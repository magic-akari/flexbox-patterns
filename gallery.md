---
layout: page
title: Gallery
chapter: "8.1"
thumb: gallery.jpg
---
<div class="demo">
{% include_relative assets/examples/gallery.html %}
</div>
This would be pretty easy to do without flexbox, right? You would just set each Photo to have `display: inline-block`, and you would get the same basic layout.

But inline-block elements can be tricky! They [interpret white-space in the markup](https://css-tricks.com/fighting-the-space-between-inline-block-elements/) in a way that introduces extra unwanted space between each item. You can get rid of this extra space, but you’ll have to implement one of several workarounds.

Fortunately, one of those workarounds is to just use flexbox! We need to use one new flexbox property called `flex-wrap` to do this. Normally, a flexbox container will try to fit all of its children onto one row. `flex-wrap` tells the container to wrap children onto subsequent rows instead.

```css
{% include_relative assets/styles/gallery.css %}
```
```html
{% include_relative assets/examples/gallery.html %}
```
