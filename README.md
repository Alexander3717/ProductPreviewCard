# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![](./screenshot.png)

### Links

- Solution URL: [View solution on Frontend Mentor](https://your-solution-url.com)
- Live Site URL: [View live site](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- SASS features
- Flexbox
- Mobile-first workflow

### What I learned

I wanted to organize my code better so I read up on how to work with modules (or partials) in SASS. 

This is the file structure I chose: `main.scss` for the main styling and then the partials, each with a specific purpose: `_variables.scss` for variables and text presets,`_reset.scss` for CSS reset rules and `_functions.scss` for helper functions. 

I then grouped these three in another partial, `_setup.scss`, using the `@forward` rule:
```scss
// sass/_setup.scss

@forward "variables";
@forward "reset";
@forward "functions";
```
That made `_setup.scss` an entrypoint file, allowing `main.scss` to access all the other partials with just one line of code:
```scss
// sass/main.scss

@use "setup" as *; // imports variables, CSS reset and helper functions

// main styling starts here
```
I think from now on I will be using this (or similar) file structure, especially as I start working on bigger projects where separation of concerns is crucial.

### Useful resources

- [@use rule documentation](https://www.example.com)
- [@forward rule documentation](https://sass-lang.com/documentation/at-rules/forward/)

## Author

Frontend Mentor - [@Alexander3717](https://www.frontendmentor.io/profile/Alexander3717)
