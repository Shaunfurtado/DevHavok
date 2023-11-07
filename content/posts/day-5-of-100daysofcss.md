+++
title = "Day-5 of 100 Days of CSS"
date = 2023-11-05T18:08:23+05:30
draft = false
tags = ['100DaysOfCSS' ]
+++
# Day 5 of 100 Days of CSS Challenge

Welcome back to the DevHavok blog! We're on Day 5 of our adventurous journey through the 100 Days of CSS Challenge. Today, we are diving into the world of statistics. In a world filled with numbers and data, it's essential to be able to interpret them correctly. Beautiful statistics not only help us comprehend data but also make it visually captivating.

## HTML Structure

To bring our beautiful statistics to life, we've created a structured HTML layout:

```html
<div class="frame">
  <div class="center">
    <div class="card">
      <header class="header">
        <div class="title-container">
          <h1 class="title">Weekly Report</h1>
          <h2 class="date">01.Feb - 07.Feb</h2>
        </div>
        <div class="revenue-container">
          <span class="revenue-heading">Revenue</span>
          <span class="revenue-total">$3621.79</span>
        </div>
      </header>
      <div class="graph-container">
        <div class="legend">
          <span class="red">Views</span>
          <span class="blue">Purchases</span>
        </div>
        <div class="graph">
          <!-- Graph lines and data go here -->
        </div>
        <div class="days">
          <!-- Days of the week -->
        </div>
      </div>
    </div>
  </div>
</div>
```

Our HTML structure consists of a "frame" container, which is the main frame of our statistic report. Inside, there's a "card" that holds the entire report. The card is divided into sections, including a header, graph container, and days of the week.

## CSS Styles

To make our statistics visually appealing, we've applied carefully crafted CSS styles:

```css
@import url(https://fonts.googleapis.com/css?family=Open+Sans:600,400);

* {
  box-sizing: border-box;
}
:root {
  --red: #FA7373;
  --blue: #7BA2FF;
}

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
  background: #22C7C1;
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

/* Styles for the report card */
.card {
  width: 280px;
  height: 220px;
  background-color: #fff;
  display: flex;
  flex-direction: column;
  border-radius: 3px;
  box-shadow: 10px 10px 15px 0 rgba(0, 0, 0, 0.2);
  overflow: hidden;
}

.header {
  width: 100%;
  height: 60px;
  background-color: #F1BA64;
  display: flex;
  justify-content: space between;
  padding: 15px;
  color: white;
}

/* Styles for the title and date section */
.title-container {
  width: 60%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.title {
  font-size: 14px;
  text-transform: uppercase;
  margin: 0;
  letter-spacing: .02rem;
}

date {
  font-size: 11px;
  margin: 0;
  font-weight: 400;
  margin-top: 2px;
}

/* Styles for the revenue section */
.revenue-container {
  width: 40%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: right;
}

revenue-heading {
  display: block;
  font-size: 11px;
  font-weight: 400;
}

revenue-total {
  font-size: 14px;
  font-weight: 600;
  margin-top: 2px;
}

/* Styles for the graph container */
.graph-container {
  padding: 15px 12px;
}

/* Styles for the legend section */
.legend {
  display: flex;
  justify-content: flex-end;
  color: #606060;
}

/* Styles for legend entries */
.legend .red,
.legend .blue {
  font-size: 9px;
}

.legend .red {
  position: relative;
  line-height: 1;
}

.legend .red:before {
  content: "";
  width: 11px;
  border-radius: 1px;
  position: absolute;
  top: 40%;
  left: -20px;
  border-top: 3px solid var(--red);
}

.legend .blue {
  margin-left: 40px;
  position: relative;
}

.legend .blue:before {
  content: "";
  width: 11px;
  border-radius: 1px;
  position: absolute;
  top: 40%;
  left: -20px;
  border-top: 3px solid var(--blue);
}

/* Styles for the graph section */
.graph {
  width: 100%;
  position: relative;
}

/* Styles for the graph lines */
.line {
  background: #F2F2F2;
  width: 100%;
  height: 1px;
}

.line-1 {
  margin-top: 15px;
}

.line-2 {
  margin-top: 40px;
}

.line-3 {
  margin-top: 40px;
}

.graph svg {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

/* Styles for the graph lines */
polyline {
  fill: none;
  stroke-width: 2;
  stroke-linecap: round;
}

.red polyline {
  stroke: var(--red);
}

.blue polyline {
  stroke: var(--blue);
}

/* Styles for data points */
.point {
  cursor: pointer;
  position: absolute;
  width: 6px;
  height: 6px;
  border-radius: 50%;
  z-index: 2;
  
  &:hover .tooltip {
    visibility: visible;
    opacity: 1;
    transform: translate(-50%, 0);
  }
}

.red .point {
  background: var(--red);
}

.red .point-1 {
  left: 7px;
  top: 43px;
}

.red .point-2 {
  left: 47px;
  top: 9px;
}

.red .point-3 {
  left: 87px;
  top: 20px;
}

.red .point-4 {
  left: 127px;
  top: 9px;
}

.red .point-5 {
  left: 167px;
  top: 36px;
}

.red .point-6 {
  left: 207px;
  top: 45px;
}

.red .point-7 {
  left: 247px;
  top: 17px;
}

.blue .point {
  background: var(--blue);
}

.blue .point-1 {
  left: 7px;
  top: 58px;
}

.blue .point-2 {
  left: 47px;
  top: 47px;
}

.blue .point-3 {
  left: 87px;
  top: 62px;
}

.blue .point-4 {
  left: 127px

```

These CSS styles help us create a visually pleasing statistic report with a professional and modern look.

### Result

![Bear Image](https://i.imgur.com/6oVEhCf.png)


## Conclusion

In a world filled with numbers and data, the ability to present statistics beautifully is a valuable skill. Our Day 5 project in the 100 Days of CSS Challenge showcases a Weekly Report with elegant design elements, including a graph, legend, and days of the week. With the right combination of HTML structure and CSS styles, you can transform dry data into captivating and informative statistics.


Blog Series : [100DaysofCSS](/tags/100daysofcss)

**Follow me on other platforms for more content:**
- GitHub: [GitHub](https://github.com/Shaunfurtado/100daysofCSS)
- YouTube: [YouTube](https://www.youtube.com/channel/UC66ahSH1xpBBlaMBP8lNuBg)
- CodePen: [CodePen](https://codepen.io/Shaun-Furtado)
- Blog: [DevHavok](https://devhavok.is-a.dev/)


Stay tuned for my daily updates in the "100 Days of CSS" challenge as I explore and create new and exciting designs.

Happy coding, and see you on Day 5! 🚀

*Keep up with the [DevHavok](https://devhavok.is-a.dev/) for more content.*