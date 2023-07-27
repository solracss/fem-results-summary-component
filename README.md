# Frontend Mentor - [Results summary component.](https://www.frontendmentor.io/challenges/results-summary-component-CE_K6s0maV)

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### The challenge

Build out the project to the designs provided.
Your users should be able to:

- View the optimal layout for the page depending on their device's screen size
- See a hover state on desktop for the Sign-Up call-to-action

### Screenshot

<details>

<summary>Click to open</summary>

![Desktop]()
![Mobile]()

</details>

### Links

- Live Site URL: [Live](https://solracss.github.io/fem-results-summary-component/)

## My process

### Built with

<div >
	<img width="30" src="https://user-images.githubusercontent.com/25181517/192108891-d86b6220-e232-423a-bf5f-90903e6887c3.png" alt="Visual Studio Code" title="Visual Studio Code"/>
	<img width="30" src="https://user-images.githubusercontent.com/25181517/192158954-f88b5814-d510-4564-b285-dff7d6400dad.png" alt="HTML" title="HTML"/>
	<img width="30" src="https://user-images.githubusercontent.com/25181517/192158956-48192682-23d5-4bfc-9dfb-6511ade346bc.png" alt="Sass" title="Sass"/>
	<img width="30" src="https://user-images.githubusercontent.com/25181517/183898674-75a4a1b1-f960-4ea9-abcb-637170a00a75.png" alt="CSS" title="CSS"/>
</div>

### Notes

This time I opted to define all my `font size` as custom variable in `typography` sass file.

### What I learned

1. Importing variable font from assets:

```css
@font-face {
	font-family: "Hanken Grotesk";
	font-weight: 500 800;
	src: url("../assets/fonts/HankenGrotesk.woff2") format("woff2-variations");
}
```

2. Using `gap` and `data-attributes` instead of margins if having same distance between multiple elements in container:

```html
<div class="result-section grid-flow" data-spacing="large">...</div>
```

```css
.grid-flow {
	display: grid;
}

.grid-flow[data-spacing="large"] {
	gap: 1.5rem;
}
```

3. Learned about `stacking context` when dealing with how to apply transition for button gradient on hover.

- create new stacking context on button
- move pseudoelement with gradient to z -1 and opacity 0
- change opacity to 1 on hover
- [working solution on my codepen](https://codepen.io/solracss/pen/BaGqOjj)

### Useful links

[Font converter ttf to woff2](https://everythingfonts.com/ttf-to-woff2)

[What variable fonts are](https://www.youtube.com/watch?v=0fVymQ7SZw0)

[Stacking context, z-index](https://vanseodesign.com/css/css-stack-z-index/)
