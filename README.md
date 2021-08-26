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

![](design/desktop-design.jpg)

### Links

- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Javascript

### What I learned

```js

//gets all elements with the accordian class
var accordions = document.getElementsByClassName("accordion");

//loops through each accordian. if clicked, toggles the 'is-open' class.
for (var i = 0; i < accordions.length; i++) {
  accordions[i].onclick = function() {
    this.classList.toggle('is-open');

    //gets the accordian content.
    var content = this.nextElementSibling;
    if (content.style.maxHeight) {
      //if the accordian has a height, you know the content is open. We can then close it by setting the height to 0 again.
      content.style.maxHeight = null;
    } else {
      // accordion is currently closed, so open it. We change the height from zero to the scroll height. 
      content.style.maxHeight = content.scrollHeight + "px";
    }
  }
}
```

### Continued development

I want to continue studying how I can use javascript to build cool, interactive websites.

### Useful resources

- [Build an Accordian Menu - DevMarketer](https://youtu.be/VTdSW57--yM) - Incredibly straightfoward tutorial on how to build a simple accordian without any dependancies.

## Author

- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/sophiestrausberg)
- Instagram [@sophiestrausberg](https://www.instagram.com/sophiestrausberg)
