+++
title = "Day 8 of 100 Days of CSS"
date = 2023-11-08T09:00:00+05:30
draft = false
tags = ['100DaysOfCSS']
+++

# Day 8 of 100 Days of CSS Challenge

Welcome back to the DevHavok blog! We've reached Day 8 of our incredible journey through the 100 Days of CSS Challenge. Today, we're exploring the seemingly impossible – Metaballs, a fascinating visual effect that you might think is challenging to implement with CSS alone. But with the power of filters, we're making the impossible possible.

## HTML Structure

To create these mesmerizing Metaballs, we've designed an HTML layout with a central frame and multiple circular blobs. The blobs are the key elements that will create the Metaballs effect. Here's the HTML structure:

```html
<div class="frame">
  <div class="center">
		<div class="blob b1"></div>
		<div class="blob b2"></div>
		<div class="blob b3"></div>
		<div class="blob b4"></div>
		<div class="blob b5"></div>
		<div class="blob b6"></div>
		<div class="blob b7"></div>
		<div class="blob b8"></div>
		<div class="blob b9"></div>
		<div class="blob b10"></div>
  </div>
</div>
```

The central frame and the collection of blobs come together to form the Metaballs effect.

## CSS Styles

The magic happens with CSS styles. We've applied filters, transformations, and animations to achieve the Metaballs effect. Let's take a closer look at the CSS:

```css
@import url(https://fonts.googleapis.com/css?family=Open+Sans:700,300);

:root {
  --animation-time: 2s; 
}

.frame {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 400px;
  height: 400px;
  margin-top: -200px;
  margin-left: -200px;
  border-radius: 4px;
	box-shadow: 4px 8px 16px 0 rgba(0,0,0,0.1);
	overflow: hidden;
  background: #fff;
  color: #333;
	font-family: 'Open Sans', Helvetica, sans-serif;
  filter: contrast(35);
}

.center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%,-50%);
  filter: blur(10px);
}

.blob{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%,-50%);
  background: black;
  border-radius: 50%;
	filter: blur(4px);
}

.b1{
  height: 90px;
  width: 90px;
}

.b2{
  height: 70px;
  width: 70px;
  transform-origin: 25px 30px;
  animation:rotate 3s linear infinite;
}

.b3{
  height: 75px;
  width: 75px;
  transform-origin: 40px 50px;
  animation:rotate 5s linear infinite;
}


.b4{
  height: 45px;
  width: 40px;
  transform-origin: 65px 55px;
  animation:rotate 4s linear infinite;
}


.b5{
  height: 28px;
  width: 28px;
  transform-origin: -50px 45px;
  animation:rotate 3.7s linear infinite;
}


.b6{
  height: 30px;
  width: 30px;
  transform-origin: -50px -55px;
  animation:rotate 4.2s linear infinite;
}


.b7{
  height: 25px;
  width: 25px;
  transform-origin: -50px 85px;
  animation:rotate 4.8s linear infinite;
}

.b8{
  height: 32px;
  width: 34px;
  transform-origin: 40px -55px;
  animation:rotate 5s linear infinite;
}

.b9{
  height: 28px;
  width: 28px;
  transform-origin: 53px 69px;
  animation:rotate 5.5s linear infinite;
}

.b10{
  height: 35px;
  width: 35px;
  transform-origin: -40px 48px;
  animation:rotate 7s linear infinite;
}

```

### Keyframes for animations

```css
@keyframes rotate{
  0%{
    transform: translate(-50%,-50%) rotate(0);
  }
  100%{
    transform: translate(-50%,-50%) rotate(360deg);
  }
}
```


In the CSS, we define variables, set up the central frame, center it on the screen, and style the circular blobs. We also include keyframes for the animation that makes the blobs appear to merge and separate, creating the Metaballs effect.

### Result

![Bear Image](https://i.imgur.com/2wJncWh.gif)
The result is a visually stunning Metaballs effect that combines circular blobs, seemingly merging and separating as they move. All of this is achieved with the power of CSS filters and animations.

## Conclusion

Metaballs are a mesmerizing visual effect that adds a touch of magic to web design. At first glance, you might think it's impossible to implement with CSS, but by leveraging filters, we've demonstrated that creativity knows no bounds. With a combination of HTML structure and CSS wizardry, you can bring enchanting effects like Metaballs to your web projects.

Blog Series: [100DaysofCSS](/tags/100daysofcss)

**Stay connected with DevHavok for more exciting content:**
- GitHub: [GitHub](https://github.com/Shaunfurtado/100daysofCSS)
- YouTube: [YouTube](https://www.youtube.com/channel/UC66ahSH1xpBBlaMBP8lNuBg)
- CodePen: [CodePen](https://codepen.io/Shaun-Furtado)
- Blog: [DevHavok](https://devhavok.is-a.dev/)

Join us tomorrow for Day 9 of the "100 Days of CSS" challenge, where we'll continue to explore the captivating world of web design.

Keep coding and stay creative! 🚀

*Stay tuned with [DevHavok](https://devhavok.is-a.dev/) for more exciting content.*
