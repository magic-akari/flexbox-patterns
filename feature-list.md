---
layout: page
title: Feature List
chapter: "6.1"
thumb: featureList.jpg
---
<div class="demo">
{% include_relative assets/examples/feature-list.html %}
</div>
You know those marketing pages that display feature images and descriptions in alternating order? There’s one simple flexbox property that makes this easy to do:

- `flex-direction: row-reverse` displays the container’s children in the reverse order of how they appear in the markup.

```css
{% include_relative assets/styles/feature-list.css %}
```
```html
{% include_relative assets/examples/feature-list.html %}
```
