+++
title = "Day-2 of 100 Days of CSS"
date = 2023-11-02T18:08:23+05:30
draft = false
tags = ['100DaysOfCSS' ]
+++
## Day 2 of 100 Days of CSS Challenge: Creating an Impressive Menu Icon

Welcome back to **DevHavok**, your go-to destination for all things web development and design! Today, we're diving into Day 2 of our 100 Days of CSS Challenge, where we'll be creating a visually appealing and impressive menu icon. This seemingly simple yet animated design element is a staple on almost every website nowadays and can make a remarkable difference when it comes to user experience.

### The Basics of Creating a Menu Icon

To create an impressive menu icon, we'll need some fundamental knowledge of HTML and CSS. If you're new to web development, don't worry - this challenge is designed to be beginner-friendly!

#### HTML Structure

We'll start by setting up the HTML structure. Here's a basic example:

```html
<div class="frame">
  <div class="center">
    <button class="bars">
      <div class="bar bar-1"></div>
      <div class="bar bar-2"></div>
      <div class="bar bar-3"></div>
    </button>
  </div>
</div>
```

#### CSS Styling

Now, let's add some CSS to style our menu icon:

```css
.frame {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 400px;
  height: 400px;
  margin-top: -200px;
  margin-left: -200px;
  border-radius: 2px;
  box-shadow: 4px 8px 16px 0 rgba(0, 0, 0, 0.1);
  overflow: hidden;
  background: #3faf;
  color: #fff;
  font-family: "Open Sans", Helvetica, sans-serif;
  -webkit-font-smoothening: antialiased;
  -moz-osx-font-smoothening: grayscale;
}

.center{
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.bars{
  border: none;
  outline: none;
  cursor: pointer;
  background: transparent;
  position: relative;
  width: 80px;
  height: 55px;
}

.bar{
  width: 100%;
  height: 8px;
  box_shadow: 0 0 10px #777;
  position: absolute;
  left: 0;
  background: #fff;
  border-radius: 6px;
}

.bar-1 {
  z-index: 5;
  top: 0;
}
.bar-2 {
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  margin: auto;
}

.bar-3 {
  bottom: 0;
}
.open > .bar-1{
  animation: 0.75s bar-1-open ease forwards;
}
.open > .bar-2{
  animation: 0.75s bar-2-open ease forwards;
}
.open > .bar-3{
  animation: 0.75s bar-3-open ease forwards;
}

.closed > .bar-1{
  animation: 0.75s bar-1-open ease reverse forwards;
}
.closed > .bar-2{
  animation: 0.75s bar-2-open ease reverse forwards;
}
.closed > .bar-3{
  animation: 0.75s bar-3-open ease reverse forwards;
}

@keyframes bar-1-open {
  0%{
    top:0;
    transform: none;
  }
  40%{
    top: calc(50% - 4px);
    transform: none;
  }
  60%{
    top: calc(50% - 4px);
    transform: none;
  }
  100%{
    top: 23px;
    transform: rotate(135deg);
  }  
}

@keyframes bar-2-open{
  from{
    transform: scale(1);
    opacity: 1;
  }
  
  to {
    transform: scale(0);
    opacity:0;
  }
}

@keyframes bar-3-open{
  0%{
    top:0;
    transform: none;
  }
  40%{
    top: calc(50% - 4px);
    transform: none;
  }
  60%{
    top: calc(50% - 4px);
    transform: none;
  }
  100%{
    top: 23px;
    transform: rotate(45deg);
  }
}

```

#### Adding Animation

To make our menu icon impressive, let's add a simple animation:

```javascript
const button = document.querySelector(".bars");

button.addEventListener("click", () => {
	const wasOpen = button.classList.contains("open");

	button.classList.remove("open");
	button.classList.remove("closed");

	requestAnimationFrame(() => {
		wasOpen ? button.classList.add("closed") : button.classList.add("open");
	});
});

```
#### Result

![Bear Image](https://i.imgur.com/nbk22gS.png)
In this code, we've added a hover effect to our menu icon bars. When a user hovers over them, they'll expand slightly, creating a visually appealing animation.

### Final Thoughts

And there you have it - a simple yet impressively animated menu icon for your website! While this is just the tip of the iceberg when it comes to CSS and web development, it's a fantastic starting point for your 100 Days of CSS Challenge.

Remember, the key to mastering CSS is practice. Experiment with different designs and animations to create the perfect menu icon that suits your website's style and functionality.



**Also watch the YouTube Video of this challenge: [Day-2](https://youtu.be/hdsGiJQrgvg)**.

**You can also follow the playlist: **\
Videos : [100DaysofCSS](https://youtube.com/playlist?list=PLm38KaFgtrqkGMSAe6wb2sUv-DlRtUGHl&si=JVk-slBUreu6A2Cx)

Blog Series : [100DaysofCSS](/tags/100daysofcss/)

**Follow me on other platforms for more content:**
- GitHub: [GitHub](https://github.com/Shaunfurtado/100daysofCSS)
- YouTube: [YouTube](https://www.youtube.com/channel/UC66ahSH1xpBBlaMBP8lNuBg)
- CodePen: [CodePen](https://codepen.io/Shaun-Furtado)
- Blog: [BearBlog](https://devhavok.bearblog.dev/)


Stay tuned for my daily updates in the "100 Days of CSS" challenge as I explore and create new and exciting designs.

Happy coding, and see you on Day 3! 🚀

*Keep up with the [DevHavok](https://devhavok.bearblog.dev/) for more content.*