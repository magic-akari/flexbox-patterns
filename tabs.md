---
layout: page
title: Tabs
chapter: "1.2"
thumb: tabs.jpg
---
<div class="demo">
{% include_relative assets/examples/tabs.html %}
</div>
Simply using `display: flex` is pretty versatile. These tabs are laid out the exact same way as the Stepper Input example.

```css
{% include_relative assets/styles/tabs.css %}
```

```html
{% include_relative assets/styles/tabs.css %}
```
<script>
const tabs = document.querySelector(".tabs");
const tabArray = Array.from(document.querySelectorAll(".tab"));
tabs.onclick = (e)=>{
  tabArray.map(el => el.classList.remove("is-tab-selected"));
  e.target.classList.add("is-tab-selected");
}
</script>
