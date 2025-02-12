---
title: CSS Animation on element creation
created: 2021-10-19
modified: 2021-10-19
tags: [basics, animation]
level: beginner
version: 2.0.4
authors: [tebe]
credits: []
links: []
layout: layouts/example.html
---

Animating an element via CSS when the element is created is simple.
Just add an animation to a CSS class normally.

## Styles

~~~css
.fancy {
  animation:fade-in 2.0s;
  font-size: 2rem;
}
@keyframes fade-in
{
  from {opacity:0;}
  to {opacity:1;}
}
~~~

## JavaScript

~~~js
const FancyComponent = {
    view: function() {
        return m(".fancy", "Hello world")
    }
}

m.mount(document.body, FancyComponent)
~~~

This example was taken from the official website at <https://mithril.js.org/animation.html#animation-on-element-creation> and slightly modified.
