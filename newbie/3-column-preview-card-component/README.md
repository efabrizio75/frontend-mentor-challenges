# Frontend Mentor - 3-column Preview Card component solution

This is a solution to the [3-column Preview Card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-/hub).

## Table of contents

- [Frontend Mentor - 3-column Preview Card component solution](#frontend-mentor---3-column-preview-card-component-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [Solution Screenshot](#solution-screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [Layout](#layout)
    - [What I learned](#what-i-learned)
    - [Questions](#questions)
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)

## Overview

In the source code you will find what I consider the bare minimum markup and styles that I came up with to solve the challenge, with the addition of some landmark roles to comply with Accessibility best practices.

### Solution Screenshot

![Solution screenshot](./solution_1.png)

### Links

Sandboxes with the solution are available at the following links:

- View it on Repl.it: [Live solution](https://fem3-column-card-component.emanuelef75.repl.co)

## My process

Final testing includes running axe DevTools extension to check for accessibility issues, with best practices option turned on.

### Built with

- Visual Studio Code
- Semantic HTML5
- CSS3
- Mobile-first workflow
- axe-core 4.6.3

### Layout

The basic layout in which the Results summary component code is rendered follows this markup:

```html
<div id="preview-cards">
  <section class="card">
    <img src="..." alt="...">
    <h2 class="type">
    <p role="definition">
    <button class="details">
  </section>
</div>
```

### What I learned

1. After much thinking, I decided to apply the rounded corners using the CSS pseudo classes. Therefore, for the stacked cards version, I styled with the top border-radius of the first-child, and the bottom border-radius of the last-child. These selectors work also for the side-by-side version of the component.
2. Using a section tag without a heading in it causes a warning by the W3C validator. Hence, I implemented the type of car as an header level 2 instead of a paragraph.

### Questions

1. Has anyone tried to use an anchor tag rather than a button for the "Learn More" link? I believe it is more semantic to use an anchor tag, but I found it very hard to implement the color changes.
2. I noticed that the color palette given in the style-guide.md for this challenge has low contrast ratio: is it worth it modifying it in order to comply with WCAG 2.1 AA?

## Author

- Frontend Mentor - [@efabrizio75](https://www.frontendmentor.io/profile/efabrizio75)
- LinkedIn - [efabrizio](https://www.linkedin.com/in/efabrizio/)
- Vercel space - [Work in progress](https://vercel-tmpl-react.vercel.app/)
- Netlify space - [Work in Progress](https://factotum-jammming.netlify.app/)

## Acknowledgments

Obviously, there wouldn't be this file without the wonderful idea that is Frontendmentor.io. Thank you guys!
