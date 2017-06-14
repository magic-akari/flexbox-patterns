---
layout: page
title: Stepper Input
chapter: "1.1"
thumb: stepperInput.jpg
---
<div class="demo">
{% include_relative assets/examples/stepper-input.html %}
</div>
Let’s start off with a simple Stepper Input component. When hooked up to some JavaScript, clicking the plus and minus buttons will increment and decrement the input field’s value.

Normally you would build something like this by inlining the button and input elements with `display: inline-block` (or maybe `float: left` if you’re old school).

But that will result in creating specific selectors for both of those elements. With flexbox, you won’t need those selectors: you can accomplish the same effect by adding `display: flex` to the container.

When you add this property to the container, you’re telling that element, “Hey buddy, you’re in charge here! Lay out your direct descendant children according to flexbox rules.” In their most basic form, these rules arrange the children along what’s called the “main axis”, by default the x–axis, from left to right.

```css
{% include_relative assets/styles/stepper-input.css %}
```

```html
{% include_relative assets/examples/stepper-input.html %}
```
<script>
const input = document.querySelector('.stepperInput__input');
const leftButton = document.querySelector('.button--addOnLeft');
const rightButton = document.querySelector('.button--addOnRight');
leftButton.onclick = ()=>{
  if(isNaN(input.value)){
    input.value = 0;
  }
  input.value = parseInt(input.value) - 1;
}
rightButton.onclick = ()=>{
  if(isNaN(input.value)){
    input.value = 0;
  }
  input.value = parseInt(input.value) + 1;
}
</script>
