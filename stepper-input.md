---
layout: page
title: Stepper Input
chapter: "1.1"
thumb: stepperInput.jpg
---
<div class="demo">
{% include_relative assets/examples/stepper-input.html %}
</div>
让我们从一个简单的 Stepper Input 组件开始。 当绑定了一些 JavaScript 后，点击加和减按钮，会增加或减少输入框里的值。

通常你会用一个 `display: inline-block` 来内联按钮和输入框。 (或者使用 `float: left` 这些老掉牙的方案)。

但这将导致为这两个元素创建特定的选择器。使用 flexbox 的话, 并不需要这些选择器：只要把 `display: flex` 添加到容器，就能完成同样的效果。

当你把这个属性添加到容器时，你就是在告诉这个元素，“嘿，哥们儿，这里由你负责！让你的第一代子元素遵循flexbox规则。” 在其中最基本的形式中，这些规则让孩子元素沿着被称作“主轴”的方向排列，默认是X轴(水平方向)，从左到右。

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
