# Frontend Mentor - Recipe page solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### Links

- Solution URL: [Add solution URL here](https://github.com/ericraycodes/recipe-page-main)
- Live Site URL: [Add live site URL here](https://ericraycodes.github.io/recipe-page-main)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- Variable Fonts

### What I learned

- I discovered that there is such a thing as a **variable font weight** to a _font family_. It can be styled to a wide range of granular `font-weight` instead of using multiple _static fonts_. I learned to `preload` the _variable font_ with another _static font_ as fallback which helps with performance.

```html
<link
  rel="preload"
  href="./assets/fonts/outfit/Outfit-VariableFont_wght.ttf"
  as="font"
  type="font/ttf"
  crossorigin="anonymous"
/>
<link
  rel="preload"
  href="./assets/fonts/outfit/static/Outfit-Regular.ttf"
  as="font"
  type="font/ttf"
  crossorigin="anonymous"
/>
```
```css
/* "Outfit Variable", "Outfit Static-Regular" as fallback */
@font-face {
  font-family: "Outfit Variable";
  src: url(./assets/fonts/outfit/Outfit-VariableFont_wght.ttf) format("truetype");
  font-weight: 100 900;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: "Outfit Static-Regular";
  src: url(./assets/fonts/outfit/static/Outfit-Regular.ttf) format("truetype");
  font-weight: normal;
  font-style: normal;
  font-display: swap;
}
```
- I have learned to make *pseudo-class* `::before` as a custom list-marker for `<ul>`.
```css
/* THESE GROUP OF RULES IMITATE THE CHALLENGE DESIGN VISUALS
  ON BULLETED LISTS */
ul {
  list-style: none; /* native list marker is removed */
  padding-inline-start: 0.5em;
}
/* pseudo-class ::before acts as custom list-marker */
ul > li::before {
  content: "\2022"; /* code for a bullet marker */
  font-size: 1.2em;
  color: var(--Brown-800);
}
ul > li {
  /* arrange the custom marker and text content */
  display: flex;
  gap: 1.5em;
  align-items: center;
}
.supplementary-content-container li::before {
  color: var(--Rose-800);
}
```

### Continued development

- Continuing to work on _Mobile-first Design_.


### Useful resources

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.


## Author

- Frontend Mentor - [@ericraycodes](https://www.frontendmentor.io/profile/ericraycodes)
- GitHub - [ericraycodes](https://github.com/ericraycodes)
