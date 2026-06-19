# Frontend Mentor - Four card feature section solution

This is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

![](./screenshot.jpg)

### Links

- Solution URL: [My Solution](https://github.com/Omar-525/four-card-feature-section-master)
- Live Site URL: [View Live Site](https://omar-525.github.io/four-card-feature-section-master/)

## My process

### Built with

- Semantic HTML5 markup
- CSS Custom Properties
- CSS Grid
- Flexbox
- Mobile-first response adaptation using Media Queries

### What I learned

During this project, I strengthened my understanding of CSS Grid, specifically how to span rows and columns to achieve an asymmetric multi-column layout for the card section, and how to reset them properly for smaller screens.

Here is the Grid layout implementation from my stylesheet:

```css
.cards {
  width: 100%;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
  margin-top: 10vh;
  align-items: center;
}

.cards .supervisor {
  grid-column: 1 / 2;
  grid-row: 1 / 3;
  border-top-color: var(--Cyan);
}

.cards .team-builder {
  grid-column: 2 / 3;
  grid-row: 1 / 2;
  border-top-color: var(--Red);
}
```

I also configured responsive rules within media queries to force a single-column layout on smaller viewports:

```css
@media (max-width: 375px) {
  .cards {
    grid-template-columns: 1fr !important;
    gap: 24px;
  }

  .cards .supervisor,
  .cards .calculator {
    grid-row: span 1 !important;
    grid-column: 1 !important;
    order: 0;
  }
}
```

### Continued development

In future projects, I intend to focus on:
- Refactoring layout strategies to write cleaner CSS without relying on `!important` declarations within media queries.
- Exploring `grid-template-areas` as an alternative approach to managing asymmetric card grids more intuitively.
- Enhancing font fallback mechanisms and cross-browser rendering reliability for custom local typefaces.

## Author

- Frontend Mentor - [@Omar-525](https://www.frontendmentor.io/profile/Omar-525)
