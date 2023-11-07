+++
title = "Day-3 of 100 Days of CSS"
date = 2023-11-03T18:08:23+05:30
draft = false
tags = ['100DaysOfCSS' ]
+++
## Day 3 of 100 Days of CSS Challenge: Creating The Pyramide

In our journey of 100 Days of CSS, today we are going to create a fun and visually appealing CSS animation project: "The Pyramide" While it's not as challenging as constructing the real pyramids in Egypt, it still offers an interesting shadow animation that can be both captivating and educational. This project demonstrates the power of CSS to create eye-catching animations with just a few lines of code.

## HTML Structure

Let's start by examining the HTML structure of our project:

```html
<div class="frame">
    <div class="center">
        <div class="main">
            <div class="sand"></div>
            <div class="pyramid-left"></div>
            <div class="pyramid-right"></div>
            <div class="sun"></div>
            <div class="shadow"></div>
        </div>
    </div>
</div>
```

Our project is contained within a div with the class "frame." Inside the frame, there's a div with the class "center," which is the central animated element. Within "center," we have another div with the class "main" that contains the elements of our pyramid, the sand, sun, and the shadow.

## CSS Styles

Now, let's explore the CSS styles that make this project come to life:

```css
@import url(https://fonts.googleapis.com/css?family=Open+Sans:700,300);

.frame {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 400px;
  height: 400px;
  margin-top: -200px;
  margin-left: -200px;
  border-radius:3px;
  box-shadow: 4px 8px 16px 0 rgba(0,0,0,0.1);
  overflow: hidden;
  background: #4c5747;
  color: #335;
  font-family: 'Open Sans',Helvetica,sans-serif;
  -webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
}

.center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%,-50%);
  width: 60%;
  height: 60%;
  border-radius: 50%;
  background-color: rgb(2, 230, 255);
  opacity: 0;
  animation: main 6s linear infinite;
}

.main {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  position: relative;
  overflow: hidden;
}
```

In this part of the CSS, we define the styles for the frame and the central animation container. The "frame" class sets the position, size, background color, and fonts. The "center" class is the main animated element, and it's circular in shape, with a changing background color.

```css
.sand {
  background-color: sandybrown;
  width: 100%;
  height: 100px;
  top: 150px;
  position: absolute;
}

.pyramid-left {
  background-color: antiquewhite;
  width: 120px;
  height: 70px;
  position: absolute;
  top: 81px;
  left: 40px;
  clip-path: polygon(0% 0%, 100% 0%, 30% 100%);
  transform: scaleY(-1) scaleX(-1);
  animation: pyramid-left 6s linear infinite;
}

.pyramid-right {
  background-color: rgb(210, 222, 195);
  width: 80px;
  height: 70px;
  position: absolute;
  top: 81px;
  left: 124px;
  clip-path: polygon(0% 0%, 60% 0%, 100% 100%);
  transform: scaleY(-1) scaleX(-1);
  animation: pyramid-right 6s linear infinite;
}
```

In this section, we define the styles for the sand and the left and right sides of the pyramid. These elements have varying sizes and colors, and the pyramid sides use the `clip-path` property to create the pyramid shape. They also have animations to change their colors.

```css
.sun {
  background-color: rgb(266, 150, 0);
  width: 30px;
  height: 30px;
  border-radius: 50%;;
  position: absolute;
  top: 120px;
  left: -50px;
  transform-origin: 170px 70px;
  animation: sun 6s linear infinite;
}

.shadow {
  background-color: rgb(116, 117, 109);
  width: 200px;
  height: 50px;
  position: absolute;
  top: 150px;
  left: 20px;
  clip-path: polygon(10% 0%, 92% 0%, 100% 0%);
  animation: shadow 6s linear infinite;
}
```

Lastly, we style the sun and the shadow. The sun is a yellow circle that moves in an oscillating pattern, while the shadow is a rectangular shape with a changing clip-path to create the illusion of a moving shadow.

## Keyframes and Animations

This project relies heavily on keyframes and animations to achieve its dynamic effects. Here are the keyframes for the sun, pyramid sides, shadow, and the central element:
```css
@keyframes sun {
  0% {
    transform: rotate(0deg);
  }

  25% {
    transform: rotate(50deg);
  }

  50% {
    transform: rotate(50deg);
  }

  75% {
    transform: rotate(120deg);
  }

  100% {
    transform: rotate(200deg);
  }
}

@keyframes pyramid-left {
  0% {
    background-color: antiquewhite;
  }

  25% {
    background-color: antiquewhite;
  }

  50% {
    background-color: antiquewhite;
  }

  75% {
    background-color: rgb(230, 212, 195);
  }

  100% {
    background-color: antiquewhite;
  }
}

@keyframes pyramid-right {
  0% {
    background-color: rgb(230, 212, 185);
  }

  25% {
    background-color: antiquewhite;
  }

  50% {
    background-color: antiquewhite;
  }

  75% {
    background-color: antiquewhite;
  }

  100% {
    background-color: rgb(230, 212, 185);
  }
}

@keyframes shadow {
  0% {
    clip-path: polygon(10% 0%, 92% 0%, 100% 0%);
  }

  25% {
    clip-path: polygon(10% 0%, 92% 0%, 100% 100%);
  }

  50% {
    clip-path: polygon(10% 0%, 92% 0%, 100% 100%);
  }

  80% {
    clip-path: polygon(10% 0%, 92% 0%, 0% 100%);
  }

  90% {
    clip-path: polygon(10% 0%, 92% 0%, 0% 0%);
  }
}

@keyframes main {
  0% {
    opacity: 0;
  }

  25% {
    opacity: 1;
  }

  50% {
    opacity: 1;
  }

  75% {
    opacity: 1;
  }

  100% {
    opacity: 0;
  }
}
```
These animations work together to create the mesmerizing Pyramid animation.


### Result

![Bear Image](https://i.imgur.com/rPPq3Bw.png)


## Conclusion

Day 3 of our 100 Days of CSS challenge brings us the Pyramid animation project. While it may not be as challenging as constructing the real pyramids, it demonstrates the power of CSS to create captivating and dynamic visuals with relatively simple code.


Blog Series : [100DaysofCSS](/tags/100daysofcss)

**Follow me on other platforms for more content:**
- GitHub: [GitHub](https://github.com/Shaunfurtado/100daysofCSS)
- YouTube: [YouTube](https://www.youtube.com/channel/UC66ahSH1xpBBlaMBP8lNuBg)
- CodePen: [CodePen](https://codepen.io/Shaun-Furtado)
- Blog: [DevHavok](https://devhavok.is-a.dev/)


Stay tuned for my daily updates in the "100 Days of CSS" challenge as I explore and create new and exciting designs.

Happy coding, and see you on Day 4! 🚀

*Keep up with the [DevHavok](https://devhavok.is-a.dev/) for more content.*