---
layout: page
title: Side Bar
chapter: "3.1"
thumb: sideBar.jpg
---
<div class="demo">
{% include_relative assets/examples/side-bar.html %}
</div>
Here’s a pretty typical navigation component. You don’t even need flexbox to build something like this, just divs alone would be enough … unless you want to position those “Change theme” and “Legal” buttons down at the bottom. You could do this with absolute positioning, but flexbox works well, too.

By now you’re probably familiar with display: flex and justify-content: space-between. In addition to these we’ll need one more property:

flex-direction: column sets the main axis to be vertical instead of horizontal. As you may guess, this now lays out the children vertically instead of horizontally.

```css
{% include_relative assets/styles/side-bar.css %}
```
```html
{% include_relative assets/examples/side-bar.html %}
```
<script>
bindButtonToggle('sideBar','sideBar__item','is-side-bar-item-selected');
</script>
