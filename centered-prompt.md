---
layout: page
title: Centered Prompt
chapter: "4.1"
thumb: centeredPrompt.jpg
---
<div class="demo">
{% include_relative assets/examples/centered-prompt.html %}
</div>
Centering content without flexbox usually involves some hacks, like using absolute positioning and then offsetting the centered content with a 2D transform. With flexbox you just need to set 4 properties on the container element:

- display: flex which by now we know and love.
- flex-direction: column rotates the main axis so that content is laid out vertically instead of horizontally.
- justify-content: center groups the children as close as possible to one another, in the center of their container.
- align-items: center centers the children along this axis, having a similar effect as setting text-align: center.

```css
{% include_relative assets/styles/centered-prompt.css %}
```
```html
{% include_relative assets/examples/centered-prompt.html %}
```
