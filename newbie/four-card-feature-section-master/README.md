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

It's worth mentioning that I also included structured data about [the recipe in JSON+LD format](https://developers.google.com/search/docs/appearance/structured-data/recipe). This is a way to provide search engines with more information about the content of the page, and it's a good practice to include it in the HTML of the page.

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
<div id="recipe-page">
  <img class="recipe-image" ... />
  <div class="wrapper">
    <h1 />
    <p />
    <section class="preparation-time">
      <h2 />
      <ul >
    </section>
    <h2 />
    <ul class="ingredients-list"/>
    <section class="instructions">
      <h2 />
      <ol class="instructions-steps"/>
    </section>
    <section class="nutrition">
      <h2 />
      <p />
      <table />
    </section>
  </div>
</div>
```

### What I learned

1. I learned how to tackle image sizing issues, in particular the consequences of specifying the `width` and `height` attributes for an `img` element.
1. I pursued the "idea" of training more the eye for details, and discovered that the bulltet icons were styled differently; so I decided to apply the color but not to replace the default disc character.
1. I pursed the "idea" of researching more appropriate tag elements, and opted for the `section` tag: I used it to wrap the various "sections" of the recipe.
1. Additionally I researched the `Recipe` type on Schema.org and implemented it in the HTML using Google's recommended approach.
1. I also learned that it's better to specify the spacing by modifying properties directly in rules, rather than creating a singular class with a specific spacing because this latter approach does not work when using @media queries.

### Questions


### Author

- Website - [efabrizio](https://www.efabrizio.com)
- GitHub - [efabrizio75](https://github.com/efabrizio75)
- Frontend Mentor - [@efabrizio75](https://www.frontendmentor.io/profile/efabrizio75)
- LinkedIn - [efabrizio](https://www.linkedin.com/in/efabrizio/)

## Acknowledgments

Obviously, there wouldn't be this file without the wonderful idea that is Frontendmentor.io. Thank you guys!
