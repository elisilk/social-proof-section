# Frontend Mentor - Social proof section solution

This is a solution to the [Social proof section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-proof-section-6e0qTv_bA). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the section depending on their device's screen size

### Screenshot

|  Mobile designed at 375px:   |  Desktop designed at 1440px:  |
| :--------------------------: | :---------------------------: |
| ![](./screenshot-mobile.png) | ![](./screenshot-desktop.png) |

### Links

- Solution URL: [https://github.com/elisilk/social-proof-section](https://github.com/elisilk/social-proof-section)
- Live Site URL: [https://elisilk.github.io/social-proof-section/](https://elisilk.github.io/social-proof-section/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

I'm definitely proud of how I implemented the cascade effect of both the ratings and the testimonials. I set up a grid layout and then utilized Kevin Pennekamp's [nth-child CSS trick](https://crinkles.dev/writing/a-nth-child-css-trick/). Here is the CSS for the ratings:

```css
.ratings-list {
  --cascade: 48px;
  grid-template-columns: var(--cascade) var(--cascade) 1fr var(--cascade) var(--cascade);
  grid-template-rows: 1fr 1fr 1fr;
  row-gap: 14px;
  column-gap: 0;
}

.rating:nth-of-type(1) {
  --index: 1;
}

.rating:nth-of-type(2) {
  --index: 2;
}

.rating:nth-of-type(3) {
  --index: 3;
}

.rating {
  grid-row-start: var(--index);
  grid-column-start: var(--index);
  grid-column-end: calc(var(--index) + 3);
}
```

### Continued development

Not sure what I want to work on next. I think I did a good job with font sizing, font-weights, and letter spacing in this challenge, so that is improving for me. And I also think I leveraged both flex and grid in appropriate and elegant ways.

I definitely need to spent more time on accessibility, so will focus on improving that in a revision of this solution.

### Useful resources

- Love these two CSS nth-child tricks:
  - [A nth-child CSS trick](https://crinkles.dev/writing/a-nth-child-css-trick/)
  - [Use the child-element count in CSS](https://crinkles.dev/writing/use-the-child-element-count-in-css/)
- Accessibility:
  - [10 fundamental web accessibility tips for front-end developers](https://www.frontendmentor.io/articles/10-fundamental-web-accessibility-tips-for-frontend-developers-rUurADGxCt)
  - [Main landmark should not be contained in another landmark](https://dequeuniversity.com/rules/axe/4.6/landmark-main-is-top-level?application=axeAPI)
  - [MDN - Accessibility — Make the web usable by everyone](https://developer.mozilla.org/en-US/docs/Learn/Accessibility)
  - [MDN - HTML: A good basis for accessibility](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/HTML)
  - [What are Intelligent Guided Tests](https://www.youtube.com/watch?v=AtsX0dPCG_4&ab_channel=DequeSystems)
  - [axe-core](https://www.npmjs.com/package/axe-core)
  - [html-validator](https://www.npmjs.com/package/html-validator)
  - [Nu Html Checker](https://validator.w3.org/nu/)
- [CSS Tricks: Expanding Beyond a Parent div](https://www.modusagency.com/blog/css-tricks-expanding-beyond-a-parent-div/)

## Author

- Website - [Eli Silk](https://github.com/elisilk)
- Frontend Mentor - [@elisilk](https://www.frontendmentor.io/profile/elisilk)

## Acknowledgments

- [Kevin Pennekamp](https://crinkles.dev/)
