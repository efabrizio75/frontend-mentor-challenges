# Frontend Mentor - Meet landing page

This is a solution to the [Meet landing page](https://www.frontendmentor.io/challenges/meet-landing-page-rbTDS6OUR/).

## Table of contents

- [Frontend Mentor - Meet landing page](#frontend-mentor---meet-landing-page)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [Solution screenshot](#solution-screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Questions](#questions)
    - [Author](#author)
  - [Learning Resources](#learning-resources)
    - [Responsive images](#responsive-images)
    - [The `picture` element](#the-picture-element)
    - [Typography](#typography)
    - [Flexbox - Josh Comeau's Interactive Guide to Flexbox](#flexbox---josh-comeaus-interactive-guide-to-flexbox)
      - [Basics](#basics)
      - [Positioning](#positioning)
      - [Growing and Shrinking](#growing-and-shrinking)
      - [Cool things to know](#cool-things-to-know)
    - [Grid by Example](#grid-by-example)
    - [Grid - Josh Comeau's Interactive Guide to Grid](#grid---josh-comeaus-interactive-guide-to-grid)
      - [Grid construction](#grid-construction)
      - [Tracks using `auto-fill`](#tracks-using-auto-fill)
      - [Assigning children](#assigning-children)
      - [Alignment](#alignment)
  - [Acknowledgments](#acknowledgments)

## Overview

In the source code you will find what I consider the bare minimum markup and styles to solve this challenge, with the addition of some landmark roles to comply with Accessibility best practices.

This solution started with a mobile-first approach and it contains responsive adjustment to spacing without modifying font sizes.

### Solution screenshot

![Solution screenshot](./assets/solution_01.png)

### Links

Sandboxes with the solution are available at the following links:

- View it on GitHub Pages: [Live Solution](https://efabrizio75.github.io/frontend-mentor-challenges/newbie/meet-landing-page/

## My process

Final testing includes running axe DevTools extension to check for accessibility issues, with best practices option turned on.

### Built with

- Visual Studio Code
- Semantic HTML5
- CSS3
- Mobile-first workflow
- axe-core 4.10


### What I learned

1. I learned that the wrong choice of initial layout causes issues with responsive design. In my case the biggest problem is around the hero section, with the fact that I utilized `img` elements rather than background images.
2. I learned that it is possible to include multiple images in a single `background-image` property value, by separating them with a comma [MDN Article](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_backgrounds_and_borders/Using_multiple_backgrounds).

### Questions

### Author

- Website - [efabrizio](https://www.efabrizio.com)
- GitHub - [efabrizio75](https://github.com/efabrizio75)
- Frontend Mentor - [@efabrizio75](https://www.frontendmentor.io/profile/efabrizio75)
- LinkedIn - [efabrizio](https://www.linkedin.com/in/efabrizio/)
---
---
## Learning Resources

I utilized the following resources while completing this challenge, but it doesn't mean that I implemented all techniques and approaches.

---

### [Responsive images](https://web.dev/learn/design/responsive-images)

Best ways to serve responsive images:

```css
img {
  max-inline-size: 100%;
  block-size: auto;
  object-fit: contain; // preserve aspect ratio
  aspect-ratio: 2/1; // only if needed with some CMS
}
```

Since `contain` value leaves some space around the sides of the image, try with `cover` and adjust the cropping position:

```css
img {
  max-inline-size: 100%;
  block-size: auto;
  object-fit: cover;
  object-position: top center;
}
```
- Always specify the `width` and `height` of the image, so that the browser knows the aspect ratio, as long as you have the above CSS properties applied.
- Use the `decoding` attribute to specify how the browser should decode the image: `async` (reduce priority) or `sync` (increase priority).
- Use the `srcset` attribute to specify the image to use based on the viewport width:
```html
<img
  src="small-image.png"
  alt="A description of the image."
  width="300"
  height="200"
  srcset="small-image.png 300w,
    medium-image.png 600w,
    large-image.png 1200w"
  sizes="(min-width: 66em) 33vw,
    (min-width: 44em) 50vw,
    100vw"
>
```
- Include presentational images only in CSS (it is for presentational purposes only), via the `background-image` property in conjunction with the `image-set` function of CSS:
```css
element {
  background-image: image-set(
    "small-image.png" 1x,
    "medium-image.png" 2x,
    "large-image.png" 3x
  );
}
```

---

### [The `picture` element](https://web.dev/learn/design/picture-element) 

The `picture` element build upon the `img` element and is used to swap out different images in different conditions. There **must be an `img` element inside the `picture` element**. You have **control** over the image served via the `source` element and the browser will serve the first one that matches the conditions: *wider than 75em will serve the large, wider than 40em will serve the medium, otherwise the small image*
```html
<picture>
  <source srcset="large.png" media="(min-width: 75em)">
  <source srcset="medium.png" media="(min-width: 40em)">
  <img src="small.png" alt="A description of the image." width="300" height="200">
</picture>
```

The `picture` element gives you the possibility to specify alternative: formats, densities, sizes, and croppings.

---

### [Typography](https://web.dev/learn/design/typography)

- Mix `vw` and `rem` units to achieve a responsive typography through the `calc()` function:
  ```css
  html {
    font-size: calc(0.75rem + 1.5vw);
  }
  ```
- Use the `clamp()` function to set a minimum and maximum font size, with the middle value being the `calc()` function from the previous example:
  ```css
  html {
    font-size: clamp(1.25rem, 0.75rem + 1.5vw, 5rem);
  }
  ```
- Use the `ch` unit to set the limit of characters per line:
  ```css
  p {
    max-inline-size: 66ch;
  }
  ```
- Use woff2 format for web fonts (best compression and support) through the the `@font-face` rule.
-  Load the font file via external `link` element utilizing the `crossorigin` attribute all the time (even if you host).
-  Include a `font-display` property with the value of `swap` if you want to stick with your choice after it's loaded.
  ```css
  @font-face {
    font-family: Roboto;
    src: url('/fonts/roboto-regular.woff2') format('woff2');
  }
  body {
    font-family: Roboto, sans-serif;
    font-display: swap;
  }
  ```
---
### Flexbox - [Josh Comeau's Interactive Guide to Flexbox](https://www.joshwcomeau.com/css/interactive-guide-to-flexbox/)

#### Basics

- Flex is one of the 4 layout modes in CSS.
- Flex direction default is `row` and it lays out items along the primary-axis (x, -->), and __content__ mushes from the start.
- Flex cross-axis (y, ↓) is perpendicular to the primary-axis, and by default __items__ stretch to fill the container.

#### Positioning

- `justify-content`: Content is like kebab on a skewer: we can only move it horizontally and decide how much space to give between the meat pieces.
- `align-items`: Aligns items along the cross-axis like a toothpick through a cocktail weiner.

#### Growing and Shrinking

- By default, elements **will shrink** to the minimum along the primary-axis.
- `flex-basis`: by default it acts as `width`, but it becomes `height` if the flex-direction is `column`. It is __pegged__ to the primary-axis.
- However, the `flex-basis` value is a **suggestion** and the browser will decide how much space to give to the items based on the `flex-grow` and `flex-shrink` values of other items.
- `flex-grow`: by default it is `0` (do NOT grow)
- `flex-shrink`: by default it is `1` (shrink!!)
- `flex-grow` controls how the **extra space is distributed** when the items are _smaller than_ the container.
- `flex-shrink` control how **space is removed** when the items are bigger than their container.
- When shrinking, each item shrinks equally. If we want to change the amount of space each item shrinks by, we can use the `flex-shrink` property.
- **IMPORTANT**: `flex-shrink` will not shrink some elements like input fields or long text. Therefore, on the flex children that you need to shrink but may overflow because they contain unbreakable content, set the `min-width` property to `0`.

#### Cool things to know

- The `margin` property value of `auto` will make the element take up as much space as possible, hence in conjunction with flex layout allows we to increase the "empty space" between content on the primary-axis (useful in navigation headers).
- The `flex-wrap` property allows us to wrap items onto multiple lines. It's like adding another skewer of kebabs. The item **DOES NOT SHRINK BELOW THE HYPOTHETICAL SIZE** of the container.
- Play with the [interactive tutorial](https://www.joshwcomeau.com/css/interactive-guide-to-flexbox/#wrapping-14).

---

### [Grid by Example](https://gridbyexample.com/examples/)

Find simple and concise explanations about all features of CSS Grid.

---

### Grid - [Josh Comeau's Interactive Guide to Grid](https://www.joshwcomeau.com/css/interactive-guide-to-grid/)

- By default the grid uses a single column and each child element gets its own row.
- By default the grid container will stretch to fit the height of its children (inside). But if you se the `height` property, then it will divide that value by the number of children.

#### Grid construction

- The `fr` unit is a fraction of the available space: add the value of all tracks specified using `fr` and that is the denominator value: **IT DISTRIBUTES THE EMPTY SPACE** in the grid.
  ```css
  .container {
    display: grid;
    grid-template-columns: 1fr 3fr; //means 1/4 and 3/4
  }
  ```
- The column **WILL NOT SHRINK** below the its content size, even if that means breaking the fractionary proportion.

#### Tracks using `auto-fill`

- Create as many tracks as possible, filling the container as much as possible with items of at least `150px`:
  ```css
  .container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
  }
  ```
- Use `auto-fit` if you want to collapse empty tracks to `0` when there **are not enough** items in the grid container.

#### Assigning children

- By default, the children will be placed in order of appearance, each child getting the next grid cell.
- We can also make children span tracks by using the `grid-column` and `grid-row` properties.
- It's possible to use negative numbers to specify the number of tracks to span: `grid-column: 1 / -1` will span all the columns. <-- especially useful with dynamic number of columns
- Use `grid-area` to specify the name of the area to place the child in:
  ```css
  .parent {
    display: grid;
    grid-template-columns: 2fr 5fr;
    grid-template-rows: auto-fit, 1fr;
    grid-template-areas:
      "header header"
      "sidebar content";
  }
  .child {
    grid-area: header;
  }
  ```

#### Alignment

- On the grid container, with `justify-content` we arrange the compartments of our grid, distributing the space between them.
- On the grid container, instead, with `justify-items` we align the items within their compartments, allowing us to override the default behavior of stretching to fill the compartment.
- __On the individual child__, using `justify-self` we can override the default behavior of stretching to fill the compartment.
- If we want to align stuff along the cross-axis (rows), we use `align-content`, `align-items`, and `align-self`.

## Acknowledgments

Obviously, there wouldn't be this file without the wonderful idea that is Frontendmentor.io. Thank you guys!
