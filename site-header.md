---
layout: page
title: Site Header
chapter: "2.1"
thumb: siteHeader.jpg
---
<div class="demo">
{% include_relative assets/examples/site-header.html %}
</div>
You could use this kind of component for a header on your website or web app.

The typical method for building this component would be to wrap the logo and nav buttons inside of one element, and the “Settings” and “Log out” buttons inside another element. And then you would use `float` to push one container to the left, and the other container to the right. And then you would need a clearfix on the site header itself. That’s a lot of rigamarole for a simple layout!

With flexbox, you still need the container elements, but you don’t need special classes for these containers since flexbox puts the parent in charge of the layout.

Our trusty `display: flex` property is at work here, but a couple other flexbox properties further adjust the layout:

- `justify-content`: space-between pushes the child elements are far away from one another as possible. This pushes the logo and nav buttons left and the settings button right.
- `align-items`: center centers all of the children elements vertically along the main axis within the containers themselves. This is important because the logo and nav buttons are of different heights. Without setting this property, they would align to their top edges by default.

```css
{% include_relative assets/styles/site-header.css %}
```

```html
{% include_relative assets/examples/site-header.html %}
```
<script>
document.querySelector(".fa").style["pointer-events"] = "none";
const siteHeader = document.querySelector(".siteHeader");
const siteHeader__item = Array.from(document.querySelectorAll(".siteHeader__item"));
siteHeader.onclick = (e)=>{
  siteHeader__item.map(el => el.classList.remove("is-site-header-item-selected"));
  e.target.classList.add("is-site-header-item-selected");
}
</script>
