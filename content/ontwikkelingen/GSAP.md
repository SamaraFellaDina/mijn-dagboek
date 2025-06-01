* [hier](https://codepen.io/shooft/pen/KKYbBMa) een aantal voorbeelden van Sanne hoe hij GSAP gebruikt
	* Hij maakt gebruik van `drawingsvg`  waarbij er een animatie word getekend
![[Pasted image 20250513101255.png]]
* [hier](https://gsap.com/docs/v3/Eases/) kan je gemakkelijk een library vinden over easing. 

# Oefenen
Ik heb van Sanne een aantal oefeningen gevolgd over GSAP

* ik heb [hier](https://codepen.io/Samarafelladina/pen/ByyvPwZ?editors=1010) aan gewerkt
* en aan [deze](https://codepen.io/Samarafelladina/pen/ZYYVjXq?editors=0010)

# `GSAP` docs
[There are four types of tweens:](https://gsap.com/resources/get-started#creating-an-animation)

`gsap.to()` - This is the most common type of tween. A `.to()` tween will start at the element's current state and **animate "to" the values defined in the tween.**

`gsap.from()` - Like a backwards `.to()` where it **animates "from" the values defined in the tween**and ends at the element's current state.

`gsap.fromTo()` - **You define _both_ the starting _and_ ending values.**

`gsap.set()` **Immediately sets properties** (no animation). It's essentially a zero-duration `.to()`tween.