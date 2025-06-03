---
title: GSAP 2.0
date: 2025-04-21
tags:
  - Workshop
  - GSAP
  - basics
  - cursor
  - code-pen
  - animatie
---
wow we are going to learn thing from the cursor, mouse trail, buttons and more
- [this is the course for today](https://github.com/fdnd-task/css-challenges/blob/main/docs/CHALLENGES.md#dinsdag-20-mei)
#   `cursor`
- normally you can make events for the cursor by using `eventListeners`
	- `mouseEnter`
	- `mouseMove`

```js
window.addEventListener('mousemove',(e) => {

})
```
# courses
## [first course](https://codepen.io/Samarafelladina/pen/gbbJyrp)
- [example](https://codepen.io/Sidstumple/pen/vEEPOgr) code
- `x:e.clientx` is used for the coordinates of the mouse. This is the `x` axis
- `stagger`

```js
window.addEventListener('mousemove', (e) => {
  gsap.to('.cursor', {
    x:e.clientX,
    y:e.clientY
  })
})
```
- with this code you can select the cursor and creates and object that follows
- `console.log(e.target)`:

```js 
  if (e.target.nodeName == 'A') {
    gsap.to('.cursor', {
      scale:1,
    })
    
  } else {
    gsap.to('.cursor', {
      scale:0.33
    })
  }
})
```
* with this code you make an event where if the mouse is over an `<a>` element, it will modify the size
```js
  if (e.target.nodeName == 'A' || e.taget.closest('a')) {
```
* here you select the `<a>` element, but also the children inside the `<a>`

## [second course](https://codepen.io/Samarafelladina/pen/NPPVmJw)
- [example](https://codepen.io/Sidstumple/pen/xbbBzbR) code

```js
const header = document.querySelector(".header");
const headerImage = document.querySelector(".header img");


let sizeW = headerImage.offsetWidth;
let sizeH = headerImage.offsetHeight;

if (header && headerImage) {
  header.addEventListener("mousemove", (e) => {

    gsap.to(headerImage, {
      x:e.clientX - sizeW / 2,
      y:e.clientY - sizeH / 2,
    });
  });
}

```

this is the eventual code I came up with. 
1. I had to define the width and height of the image. 
	1. I used `offsetWidth` and `offsetHeight` to define this. 
	2. I had to select this in a new variable
```js 
let sizeW = headerImage.offsetWidth;
let sizeH = headerImage.offsetHeight;
```
I checked this with `console.log(sizeH)`. Which when you check this in the console of the browser, it will return a value.
![[Pasted image 20250520101126.png]]

2. after that, you can create the `gsap` animation
	1. here you create a `gsap` animation and call the event.
	2. `x:e.clientX - sizeW / 2`, you will define the width and takes the width of the image and slice it by 2, which centers it.
```js 
if (header && headerImage) {
  header.addEventListener("mousemove", (e) => {
    gsap.to(headerImage, {
      x:e.clientX - sizeW / 2,
      y:e.clientY - sizeH / 2,
    });
```

## [third course](https://codepen.io/Samarafelladina/pen/RNNmzVe)
[example](https://codepen.io/Sidstumple/pen/pvvYKeo) code
- I need to use [`canvasrenderingcontext2d`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D)