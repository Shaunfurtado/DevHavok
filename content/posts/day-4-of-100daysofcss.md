+++
title = "Day-4 of 100 Days of CSS"
date = 2023-11-04T18:08:23+05:30
draft = false
tags = ['100DaysOfCSS' ]
+++
## Day 4 of 100 Days of CSS Challenge: The Loading

Welcome back to the DevHavok blog! We're on Day 4 of our exciting journey through the 100 Days of CSS Challenge. Today, we'll be creating a loading animation that's not just any loading animation – it's a calming loading animation. Because let's face it, the best websites are the ones that load seamlessly and quickly. However, for those moments when we do need a loading indicator, it should be soothing and pleasant.

## HTML Structure

Let's start by examining the HTML structure of our calming loading animation:

```html
<div class="frame">
  <div class="center">
    <div class="circle1">
      <div class="circle2">
        <div class="circle3">
        </div>
      </div>
    </div>
  </div>
</div>
```


## CSS Styles

Now, let's dive into the CSS styles that bring our calming loading animation to life:

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
  border-radius: 2px;
  box-shadow: 4px 8px 16px 0 rgba(0,0,0,0.1);
  overflow: hidden;
  background: #FF8584;
  color: #333;
  font-family: 'Open Sans', Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

In this section of the CSS, we define the styles for the frame and the central loading animation container. The "frame" class sets the position, size, background color, and fonts. The "center" class represents the main animated element, and it's styled to be centered within the frame.

```css
.circle1 {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background: #aaf;
  box-shadow: 6px 6px 14px rgba(0, 0, 0, 0.4);
  animation: CircleOne 6s infinite ease;
}

.circle2 {
  width: 70px;
  height: 70px;
  border-radius: 50%;
  background: #aaf;
  position: absolute;
  top: 15px;
  left: 15px;
  box-shadow: 6px 6px 14px rgba(0, 0, 0, 0.4);
  animation: CircleTwo 6s infinite ease;
}

.circle3 {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: #aaf;
  position: absolute;
  top: 15px;
  left: 15px;
  box-shadow: 6px 6px 14px rgba(0, 0, 0, 0.4);
  animation: CircleThree 6s infinite ease;
}
```

In this part of the CSS, we define the styles for the three concentric circles that make up our loading animation. Each circle has its own size, position, and animation. The animation is what gives these circles their soothing, pulsating effect.

## Keyframes and Animations

The heart of our calming loading animation lies in the keyframes and animations:

```css
@keyframes CircleOne {
  0% {
    transform: scale(0);
  }
  20% {
    transform: scale(1);
  }
  80% {
    transform: scale(1);
  }
  100% {
    transform: scale(0);
  }
}

@keyframes CircleTwo {
  0% {
    transform: scale(0);
  }
  20% {
    transform: scale(0);
  }
  40% {
    transform: scale(1);
  }
  70% {
    transform: scale(1);
  }
  90%, 100% {
    transform: scale(0);
  }
}

@keyframes CircleThree {
  0% {
    transform: scale(0);
  }
  40% {
    transform: scale(0);
  }
  50% {
    transform: scale(1);
  }
  60% {
    transform: scale(1);
  }
  80%, 100% {
    transform: scale(0);
  }
}
```

These keyframes control the scaling and appearance of each circle at different points in the animation, creating a gentle loading sequence.


### Result

![Bear Image](https://i.imgur.com/frmVfSz.gif)


## Conclusion

Day 4 of our 100 Days of CSS Challenge has brought us a calming loading animation. While the best websites are those that load quickly and smoothly, sometimes we need loading indicators. In those moments, a soothing loading animation like the one we've created can enhance the user experience and leave a positive impression.



Blog Series : [100DaysofCSS](/tags/100daysofcss)

**Follow me on other platforms for more content:**
- GitHub: [GitHub](https://github.com/Shaunfurtado/100daysofCSS)
- YouTube: [YouTube](https://www.youtube.com/channel/UC66ahSH1xpBBlaMBP8lNuBg)
- CodePen: [CodePen](https://codepen.io/Shaun-Furtado)
- Blog: [DevHavok](https://devhavok.is-a.dev/)


Stay tuned for my daily updates in the "100 Days of CSS" challenge as I explore and create new and exciting designs.

Happy coding, and see you on Day 5! 🚀

*Keep up with the [DevHavok](https://devhavok.is-a.dev/) for more content.*