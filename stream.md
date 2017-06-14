---
layout: page
title: Stream
chapter: "6.2"
thumb: stream.jpg
---
<div class="demo">
{% include_relative assets/examples/stream.html %}
</div>
This is a bit of a weird example, because it’s not completely realistic, but I really wanted to show you an interesting quirk to `flex-direction`.

Let’s say you have a list of posts that you want to show to the user. If you’ve just retrieved this data from an API, then chances are good that it’s sorted from oldest to most recent. But you can’t just display the posts in this order, because in a Stream (like on Facebook or Twitter), you actually want the most recent posts at the top.

Assuming you didn’t want to just sort the data in JavaScript, you could use `flex-direction: column-reverse` to list the posts vertically, but in the reverse order than they appear in the DOM.

But here’s the weird quirk! If you try to select the text of all of the posts, you’ll see that your selection will enter each post from the opposite direction you expect. I’m sure this has something to do with the fact that the DOM elements themselves haven’t been rearranged (the browser is just drawing them in a different order) — but I’m not sure why browsers don’t account for this.

```css
{% include_relative assets/styles/stream.css %}
```
```html
{% include_relative assets/examples/stream.html %}
```
