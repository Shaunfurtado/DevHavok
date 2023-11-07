+++
title = "Day-1 of 100 Days of CSS"
date = 2023-11-01T18:08:23+05:30
draft = false
tags = ['100DaysOfCSS' ]
+++

# My First Day of the 100 Days of CSS Challenge

Today marks the beginning of my "100 Days of CSS" challenge, and I'm excited to share my journey with you. In this series, I'll be updating my progress every day, showcasing the CSS code I've created, and providing explanations to help you understand the magic behind each design.

## Day 1: Creating the Framework

For my very first day, I decided to start with a simple but visually striking design. I'm going to build a frame that will eventually display the number of days I've completed in this challenge.

### The HTML Structure

First, let's take a look at the HTML structure I used:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>100 Days of CSS</title>
    <link rel="stylesheet" href="style.css" />
    <link rel="stylesheet" href="script.js" />
  </head>
  <body>
    <div class="frame">
      <div class="center">
        <div class="number">
          <div class="one-one"></div>
          <div class="one-two"></div>
          <div class="zero-one"></div>
          <div class="zero-two"></div>
        </div>
        <span class="big">Days</span>
        <span class="small">CSS Challenge</span>
      </div>
    </div>
  </body>
</html>
```

Here, I've set up the basic HTML structure with the necessary elements. We have a frame, a center container, and various numbered and text elements.

### The CSS Styles

Now, let's delve into the CSS code responsible for the visual styling:

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
  box-shadow: 1px 2px 10px 0px rgba(0,0,0,0.3);
  background: #43389F;
  background: -webkit-linear-gradient(bottom left, #43389F 0%, #4ec6ca 100%);
  background: -moz-linear-gradient(bottom left, #43389F 0%, #4ec6ca 100%);
  background: -o-linear-gradient(bottom left, #43389F 0%, #4ec6ca 100%);
  background: linear-gradient(to top right, #43389F 0%, #4ec6ca 100%); 
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#43389F', endColorstr='#4ec6ca',GradientType=1 ); 
  font-family: 'Courier New', 'Courier', sans-serif;
  color: #fff;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.center {
  position: absolute;
  top: 50.8%;
  left: 50.5%;
  transform: translate(-50%,-50%);
}

.number {
  position: relative;
  height: 100px;
  width: 200px;

  .one-one {
    position: absolute;
    z-index: 1;
    top: 0;
    left: -16px;
    height: 40px;
    width: 20px;
    background: #fff;
    border-radius: 3px;
    transform: rotate(50deg);
    box-shadow: 0 0 13px 0 rgba(0,0,0,0.8);
  }

  .one-two {
    position: absolute;
    z-index: 10;
    top: 0;
    left: 0px;
    height: 100px;
    width: 24px;
    background: #fff;
    border-radius: 3px;
    box-shadow: 0 0 13px 0 rgba(0,0,0,0.8);
  }

  .zero-one, 
  .zero-two {
    position: absolute;
    z-index: 8;
    top: 0;
    left: 17px;
    box-sizing: border-box;
    height: 100px;
    width: 100px;
    border-radius: 50%;
    border: 24px solid #fff;
    box-shadow: 0 0 13px 0 rgba(0,0,0,0.8);
  }

  .zero-two {
    z-index: 6;
    left: 100px;
  }
}

.big {
  position: relative;
  z-index: 20;
  display: block;
  font-size: 82px;
  line-height: 60px;
  text-transform: uppercase;
  font-weight: 800;
  margin-top: 6px;
}

.small {
  position: relative;
  z-index: 20;
  display: block; 
  font-size: 23px;
  line-height: 20px;
  text-transform: uppercase;
  font-weight: 700;
  letter-spacing: .04em;
}
```
### Result
![Bear Image](https://imgur.com/ddVLyE7.jpg=300x200)

This CSS code outlines the styles for each component of the web page, from the frame to the individual number shapes and text elements.

In this Day 1 design, I've focused on creating a visually appealing frame with the number "100" inside it. Each part of the number is created with CSS, and the text elements are styled to complement the design.


Blog Series : [100DaysofCSS](/tags/100daysofcss)

**Follow me on other platforms for more content:**
- GitHub: [GitHub](https://github.com/Shaunfurtado/100daysofCSS)
- YouTube: [YouTube](https://www.youtube.com/channel/UC66ahSH1xpBBlaMBP8lNuBg)
- CodePen: [CodePen](https://codepen.io/Shaun-Furtado)
- Blog: [DevHavok](https://devhavok.is-a.dev/)


Stay tuned for my daily updates in the "100 Days of CSS" challenge as I explore and create new and exciting designs. Happy coding! 🚀💻

Happy coding, and see you on Day 2! 🚀

*Keep up with the [DevHavok](https://devhavok.is-a.dev/) for more content.*