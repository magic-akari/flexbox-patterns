---
layout: page
title: Photo
chapter: "7.1"
thumb: photo.jpg
---
<div class="demo">
{% include_relative assets/examples/photo.html %}
</div>
What’s a photo without a caption? Without flexbox, you would have to absolutely position this caption inside of the photo. But this is a little inefficient because it means you can’t use the `padding` property on the photo to control the label’s distance from the edge, and you have to manually set the `width` on the label to make the text wrap. With flexbox, you get all of this out of the box! (Get it? Out of the **box**.)

By this point, you’re already familiar with all of the properties we need for this. The only difference is now you’re going to use different values to achieve the intended result:

- `justify-content: flex-end` aligns all of the children to the end of the main axis. In this case, we’re using the default main axis, which is horizontal. So the label gets aligned to the right side of the container.
- `align-items: flex-end does` the same thing, but perpendicular to the main axis. This direction is also known as the secondary axis. So all of the children get aligned to the bottom of the container.

```css
{% include_relative assets/styles/photo.css %}
```
```html
{% include_relative assets/examples/photo.html %}
```
