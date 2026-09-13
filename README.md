# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### Screenshot

![](./preview.jpg)

### Links

- Live Site URL: [https://sarmentotiago.github.io/qr-code-component/](https://sarmentotiago.github.io/qr-code-component/)
- Repository: [https://github.com/SarmentoTiago/qr-code-component](https://github.com/SarmentoTiago/qr-code-component)

## My process

### Built with

- Semantic HTML5 markup
- Flexbox
- Mobile-first workflow
- [Google Fonts](https://fonts.google.com/) (Outfit)

### What I learned

This was my first Frontend Mentor project, and I learned several important concepts hands-on:

**box-sizing: border-box**

Without this property, padding is added on top of the defined width, making the element bigger than expected. I fixed this on the `.card`:

```css
.card {
  box-sizing: border-box;
  width: 320px;
  padding: 16px 16px 40px 16px;
}
```

**Using Figma for exact measurements**

I initially estimated values like `border-radius` and text width just by eyeballing the reference JPG, and got them wrong. Opening the Figma file, I found the real values (`border-radius: 20px` on the card, not 4px like I had guessed; the text block has a width of 256px, different from the image width). This taught me to always check the design source before estimating.

**Relative paths for deployment**

I used absolute paths (`/images/...`) that worked fine on Live Server but broke on GitHub Pages, because the site is hosted inside a subfolder (`username.github.io/repo-name/`). I switched to relative paths (`./images/...`) to fix it.

```html
<img src="./images/image-qr-code.png" alt="QR code for the Frontend Mentor website">
```

**The `<main>` tag and functional alt text**

I learned that `<main>` should wrap the single, primary content of the page, and that the `alt` text for functional images (like a QR code) should describe the image's purpose, not its visual appearance.

### Continued development

For upcoming challenges, I want to learn and apply:

- Media queries for responsive layouts (this challenge didn't require them, since the card layout doesn't change)
- CSS Grid
- More advanced Git practices (branches, more structured commit messages)

### AI Collaboration

I used Claude (by Anthropic) as a mentor/teacher throughout this project, not as a code generator.

- **How I used it**: I asked it to guide me with questions and explanations instead of writing the CSS/HTML for me. It reviewed my code, pointed out what was missing (e.g. the `<main>` tag, `box-sizing`), and taught me the concept behind each fix.
- **What worked well**: catching typos (like `320%` instead of `320px`), and helping me interpret Figma and browser DevTools values when I didn't know what I was looking at.
- **Challenge**: early on, I had trouble getting Live Server to work (VS Code was in "Restricted Mode") and pushing the project to GitHub (typos in Git commands) — Claude helped me debug each error step by step, explaining the reasoning, not just the fix.

## Author

- GitHub - [@SarmentoTiago](https://github.com/SarmentoTiago)
- Frontend Mentor - [@SarmentoTiago](https://www.frontendmentor.io/profile/SarmentoTiago)