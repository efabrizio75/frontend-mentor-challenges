# Frontend Mentor - Blog preview card

This is a solution to the [Blog preview card](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS).

## Table pf contents

- [Frontend Mentor - Blog preview card](#frontend-mentor---blog-preview-card)
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
- View it on GitHub Pages: [Live Solution](https://efabrizio75.github.io/frontend-mentor-challenges/newbie/blog-preview-card-main/index.html)

## My process

Final testing includes running axe DevTools extension to check for accessibility issues, with best practices option turned on.

### Built with

- Visual Studio Code
- Semantic HTML5
- CSS3
- Mobile-first workflow
- axe-core 4.10

### Layout

The basic layout in which the product card component is rendered is this:

```html
<div id="blog-entry-preview">
  <div class="container">
    <img class="visual" ... />
    <ul class="tags">
      <li class="extra-small">...</li>
    </ul>
    <p class="timestamp extra-small">Published <time>21 Dec 2023</time></p>
    <h1>
    <p class="blurb small">
    <div class="authors">
      <p class="author-bio small"><img class="avatar" .../>
    </div>
  </div>
</div>
```

### What I learned

1. I learned how to use viewport width unit (vw) to adjust the font size of the content in a responsive way, thus avoiding the need for media queries.
2. I learned that using an image element in the source html is better than using a `background-image` property in the css because it allows it plays better with the text nearby.

### Questions

1. What other options are there to create responsive font sizes without media queries?

### Author

- Website - [efabrizio](https://www.efabrizio.com)
- GitHub - [efabrizio75](https://github.com/efabrizio75)
- Frontend Mentor - [@efabrizio75](https://www.frontendmentor.io/profile/efabrizio75)
- LinkedIn - [efabrizio](https://www.linkedin.com/in/efabrizio/)

## Acknowledgments

Obviously, there wouldn't be this file without the wonderful idea that is Frontendmentor.io. Thank you guys!
