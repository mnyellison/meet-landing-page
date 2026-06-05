# Frontend Mentor - Meet landing page solution

This is a solution to the [Meet landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/meet-landing-page-rbTDS6OUR). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./assets/screenshot.jpg)

### Links

- Solution URL: [Repository URL](https://github.com/mnyellison/meet-landing-page)
- Live Site URL: [Live deployment URL](https://meet-landing-page-sigma-blue.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS Custom Properties (Variables)
- Flexbox
- CSS Grid (with defensive minmax columns)
- Mobile-first workflow
- Clean Architecture (7-1 inspired modular CSS structure)
- Advanced UX & Accessibility (a11y) practices

### What I learned

During this project, I advanced my frontend skills by tackling layout constraints, CSS specificity bugs, and code architecture. Here are the key takeaways:

1. **Defensive CSS Grid:** I learned that standard fractional columns (`1fr`) have an implicit minimum width of `auto`. When viewport space is tight, this can crush centered text elements. I resolved this by applying explicit `minmax(0, 1fr)` boundaries on the flanking layout columns, protecting the central content structure.

2. **CSS Specificity Overrides:** Ran into a debugging scenario where component class styles were ignored because of stronger compound selectors (`.parent img`) inherited from tablet media queries. I fixed this by using exact selector paths to boost specificity cleanly:

```css
.hero-images .img-desktop-left,
.hero-images .img-desktop-right {
  min-width: auto;
  max-width: 394px;
}
```

3. **Modular Folder Structure:** Transitioned from a single monolithic stylesheet to a production-grade modular structure, splitting files logically into base/, components/, and layouts/ directories using native CSS `@import` rules.

### Continued development

For my future projects, I intend to focus on:

- Deeper integration of comprehensive web accessibility guidelines (WCAG).
- Enhancing my fluency with advanced responsive layouts using fluid typography techniques (`clamp()`).
- Automating CSS optimization workflows.

### AI Collaboration

I collaborated with Gemini as an AI pair-programmer during this project.

- **How I used it:** We used the AI assistant for complex debugging sessions (inspecting DevTools behaviors when layout boundaries collapsed), brainstorming optimal desktop alignment techniques, and mapping out a modular CSS file architecture.
- **What worked well:** The AI was highly effective at diagnosing CSS specificity clashes and explaining the underlying math of why layout components were getting crushed on specific viewports. It also helped translate high-level software design patterns into vanilla CSS modules.

## Author

- Frontend Mentor - [@mnyellison](https://www.frontendmentor.io/profile/mnyellison)
- GitHub - [Nyellison Matheus](https://github.com/mnyellison)
