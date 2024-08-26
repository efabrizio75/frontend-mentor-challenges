# Frontend Mentor - Four card feature section

This is a solution to the [Four card feature section](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK).

## Table pf contents

- [Frontend Mentor - Four card feature section](#frontend-mentor---four-card-feature-section)
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

This solution started with a mobile-first approach and it contains responsive adjustment to spacing without modifying font sizes.

### Solution screenshot

![Solution screenshot](assets/images/solution_1.png)

### Links

Sandboxes with the solution are available at the following links:
- View it on GitHub Pages: [Live Solution](https://efabrizio75.github.io/frontend-mentor-challenges/newbie/four-card-feature-section-master/)

## My process

Final testing includes running axe DevTools extension to check for accessibility issues, with best practices option turned on.

### Built with

- Visual Studio Code
- Semantic HTML5
- CSS3
- Mobile-first workflow
- axe-core 4.10

### Layout

The basic layout of the entire sections containing cards is this:

```html
<div id="feature-section">
  <header>
    <h1 />
    <p />
  </header>
  <section class="cards-wrapper">
    <div class="card">
      <article>
        <h2 />
        <p />
        <img />
      </article>
    </div>
    <div class="card">...</div>
    <div class="card">...</div>
    <div class="card">...</div>
  </section>
</div>
```

### What I learned

1. I learned how to play with `grid` and `flex` layouts in order to achieve the intended result.
1. I favored an accessible approach for the choice of elements to use, and opted for the `article` tag instead of just a `div`.
1. I started using nested rules for the `card` class to avoid repetition.

### Questions

1. I like to keep the attribution section in all my challenges, but I noticed it interferes with the screenshot. What solution would you suggest?

### Author

- Website - [efabrizio](https://www.efabrizio.com)
- GitHub - [efabrizio75](https://github.com/efabrizio75)
- Frontend Mentor - [@efabrizio75](https://www.frontendmentor.io/profile/efabrizio75)
- LinkedIn - [efabrizio](https://www.linkedin.com/in/efabrizio/)

## Acknowledgments

Obviously, there wouldn't be this file without the wonderful idea that is Frontendmentor.io. Thank you guys!
