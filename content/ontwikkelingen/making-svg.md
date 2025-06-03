---
title: making a `svg` animation using `gsap`
date: 2025-04-21
tags:
  - Ik-doe-het-zelf
  - GSAP
  - svg
  - animatie
---
hii! I wanted to know how to make an `gsap` svg animation for a footer I want to create for my portfolio.

![[Pasted image 20250520210513.png]]
i made this svg and want to make an animation where he follows the mouse

```html 
<svg class="Layer_1" xmlns="http://www.w3.org/2000/svg" version="1.1" viewBox="0 0 160 160">
  <defs>
    <style>
      .st0 {
        fill: #fff;
      }
    </style>
  </defs>

  <!-- Left Eye -->
  <g class="Left_x5F_Eye">
    <path class="st0" d="M67.5,80c0,13.79-11.21,25-25,25s-25-11.21-25-25,11.21-25,25-25,25,11.21,25,25Z" />
    <path d="M42.5,48c-17.67,0-32,14.33-32,32s14.33,32,32,32,32-14.33,32-32-14.33-32-32-32ZM42.5,105c-13.79,0-25-11.21-25-25s11.21-25,25-25,25,11.21,25,25-11.21,25-25,25Z" />
  </g>
  <g class="Left_x5F_pupil">
    <circle cx="42.5" cy="80" r="16" />
  </g>

  <!-- Right Eye -->
  <g class="Right_x5F_Eye">
    <path class="st0" d="M142.5,80c0,13.79-11.21,25-25,25s-25-11.21-25-25,11.21-25,25-25,25,11.21,25,25Z" />
    <path d="M117.5,48c-17.67,0-32,14.33-32,32s14.33,32,32,32,32-14.33,32-32-14.33-32-32-32ZM117.5,105c-13.79,0-25-11.21-25-25s11.21-25,25-25,25,11.21,25,25-11.21,25-25,25Z" />
  </g>
  <g class="Right_x5F_Pupil">
    <circle cx="117.5" cy="80" r="16" />
  </g>
</svg>
```

this is the `svg`
```js
eyeLeft = document.querySelectorAll('.Left_x5F_pupil');
eyeRight = document.querySelectorAll('.Right_x5F_pupil');
```

Here I am selecting the right section of the eye. These are the pupils. I want them to follow the cursor. 

```js
window.addEventListener('mousemove', (e) => {
	const Y = e.clientY;
	const X = e.clientX;
	});
});
```
Here I am creating an event for the mouse
