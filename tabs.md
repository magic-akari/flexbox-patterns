---
layout: page
title: Tabs
chapter: "1.2"
thumb: tabs.jpg
---
<div class="demo">
{% include_relative assets/examples/tabs.html %}
</div>
简单地使用 `display: flex` 就可以实现多种功能。 这些选项卡(tabs)的排列方式和 Stepper Input 实例中一摸一样。

```css
{% include_relative assets/styles/tabs.css %}
```

```html
{% include_relative assets/styles/tabs.css %}
```
<script>
bindButtonToggle('tabs','tab','is-tab-selected')
</script>
