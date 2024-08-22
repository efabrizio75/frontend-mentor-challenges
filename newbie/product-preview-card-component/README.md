# Frontend Mentor - Product preview card component

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa).

## Table pf contents

- [Frontend Mentor - Product preview card component](#frontend-mentor---product-preview-card-component)
  - [Table pf contents](#table-pf-contents)
  - [Overview](#overview)
    - [Solution screenshot](#solution-screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [Layout](#layout)
    - [What I learned](#what-i-learned)
    - [Questions](#questions)
    - [Author](#author)
  - [Acknowledgments](#acknowledgments)

## Overview

In the source code you will find what I consider the bare minimum markup and styles to solve this challenge, with the addition of some landmark roles to comply with Accessibility best practices.

### Solution screenshot

![Solution screenshot](images/solution_1.png)

### Links

Sandboxes with the solution are available at the following links:
- View it on GitHub Pages: [Live Solution](https://efabrizio75.github.io/frontend-mentor-challenges/newbie/product-preview-card-component/index.html)
- View it on Codepen: [Live Solution](https://codepen.io/Emanuele-Fabrizio/pen/QWXmzqy)

## My process

Final testing includes running axe DevTools exntesion to check for accessibility issues, with best practices option turned on.

### Built with

- Visual Studio Code
- Semantic HTML5
- CSS3
- Mobile-first workflow
- axe-core 4.6.3

### Layout

The basic layout in which the product card component is rendered is this:

```html
<div id="product-card">
  <picture>
    <source media="(min-width: 650px)" srcset...>
    <img class="product-image" src=... />
  </picture>
  <div class="product-details">
    <span class="category">
    <h1 class="name">
    <p class="description">
    <span class="price">
    <span class="price original">
    <button class="cart add" value="Add to Cart">
  </div>
</div>
```

### What I learned

1. How to use the `picture` element to serve different images for different screen sizes.
2. How to flow the content of the page differently with flexbox.

### Questions

1. Has anyone tried a different approach for loading the different images?

### Author

- Website - [efabrizio](https://www.efabrizio.com)
- GitHub - [efabrizio75](https://github.com/efabrizio75)
- Frontend Mentor - [@efabrizio75](https://www.frontendmentor.io/profile/efabrizio75)
- LinkedIn - [efabrizio](https://www.linkedin.com/in/efabrizio/)

## Acknowledgments

Obviously, there wouldn't be this file without the wonderful idea that is Frontendmentor.io. Thank you guys!