# Frontend Mentor - FAQ accordion card solution

This is a solution to the [FAQ accordion card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/faq-accordion-card-XlyjD0Oam). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- See hover states for all interactive elements on the page
- Hide/Show the answer to a question when the question is clicked

### Screenshot

![](./screenshot.jpg)

### Links

- Solution Code: This repo, check out the code!
- Live Site URL: [View project live](https://xyeres.github.io/faq-accordion-card-main/)

## My process
I approach projects like this with an critical eye for detail because it's the small things that affect the user most. I don't want any of my UI's to feel janky or unreliable so I spend a lot of time honing the look and feel. 

At one point I had the design looking great across desktop and various mobile devices, except Safari on iOS was giving me a terrible bug that has to do with applying `flexbox` to a `<section>` tag. It just didn't look quite right so I spent a number of hours debugging and testing until I had figured out the issue. I think I uncovered a Safari rendering bug in the process! I was able to fix the issue and get the design looking perfect on iOS.

### Built with

- Semantic HTML5 markup
- Mobile-first workflow
- SCSS mixins, variables and partials for oragnized, reuseable SASS
- Flexbox

### What I learned

I took a mobile first approach in laying out this design. I wanted to also incorporate SCSS as I haven't had a chance to use it much in prior projects.
I also wanted to play around with SVG filters and animations so I went ahead and added some movement to the page.

One thing I was really happy with was the HTML5 implementation of `<details>` and `<summary>`, using these tags I was able to get the acordian opening and closing *without any javascript*
Here's an example:
```html
<details>
  <summary>How many team members can I invite?</summary>
  <p>
    You can invite up to 2 additional users on the Free plan. There is no limit on
    team members for the Premium plan.
  </p>
</details>
```
I thought this was a nifty way to modify my animtion without having to repeat code
Mixins with params are awesome.
```css
@mixin shadow($throw: 32px) {
  filter: drop-shadow(0px $throw rgba(240, 240, 252, .8))
}

@keyframes hero-mobile-animation {
  from {
    @include shadow;
    transform: translateY(0px);
  }

  50% {
    @include shadow(12px);
    transform: translateY(10px);
  }

  to {
    @include shadow;
    transform: translateY(0px);
  }
}
```
No JavaScript was used for this project, I'm happy about that because HTML5 is awesome :)
```js
JavaScript? null
```

### Continued development

I will continue to dive in SCSS after this project. I solidified a lot of my understanding around mobile-first layouts and incorporated some pixel-perfect responsive design. I'm excited to continue this in future projects.

### Useful resources
I found a ton of good articles while working on this project. Here are a few you may want to check out if you want to learn more about SVGs, HTML5 'acordians' and more cool stuff used in this project.
- [MDN doc on the HTML5 details 'acordian' tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details) - This helped me a ton! This is how you complete this challenge without javascript
- [Adding shadows to SVGs](https://css-tricks.com/adding-shadows-to-svg-icons-with-css-and-svg-filters/#:~:text=Shadows%20with%20CSS%20filters%20The%20trick%20to%20applying,with%202px%20of%20blur%2C%20and%20is%2040%25%20black.) - Taught me a lot about adding shadows and filters to SVGs
- [Clipping and masking in CSS](https://getflywheel.com/layout/css-svg-clipping-and-masking-techniques/) - This was helpful to get that look where the box is coming off the page. 
- [Clippy clip-path maker](https://bennettfeely.com/clippy/) - Super helpful for quickly making clipping masks on the fly.
- [CSS Annimations Spec](https://drafts.csswg.org/css-animations/#animation-timing-function) - This is the official spec for CSS animations, helpful!

## Author

- Website - [Michael Carr](https://www.linkedin.com/in/mxcarr/)
- Frontend Mentor - [@xyeres](https://www.frontendmentor.io/profile/xyeres)
- Twitter - [@xyeres](https://www.twitter.com/xyeres)
