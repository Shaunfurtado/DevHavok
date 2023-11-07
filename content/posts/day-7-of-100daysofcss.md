+++
title = "Day 7 of 100 Days of CSS"
date = 2023-11-07T09:00:00+05:30
draft = false
tags = ['100DaysOfCSS']
+++

# Day 7 of 100 Days of CSS Challenge

Welcome back to the DevHavok blog! We've reached Day 7 of our exciting journey through the 100 Days of CSS Challenge. Today, we're diving into the heart of user interface design - notifications, search, and menus. These are the three cornerstones of any application, and we're bringing them together in the smallest possible space.

## HTML Structure

To achieve this, we've created an HTML layout that perfectly blends these crucial elements:

```html
<div class="frame">
  <div class="panel">
    <div class="header">
      <div class="menu-icon">
        <div class="dash-top"></div>
        <div class="dash-bottom"></div>
        <div class="circle"></div>
      </div>
      <span class="title">Notifications</span>
      <input type="text" class="search-input" placeholder="Search...">
      <div class="fa fa-search search-icon"></div>
    </div>
    <div class="notifications clearfix">
      <div class="line"></div>
      <div class="notification">
        <div class="circle"></div>
        <span class="time">9:24 AM</span>
        <p><b>Jhon Walker</b> posted a photo on your wall</p>
      </div>
    </div>
  </div>
  <div class="menu">
    <ul>
      <li><span class="fa fa-dashboard"></span>Dashboard</li>
      <li><span class="fa fa-user"></span>Profile</li>
      <li><span class="fa fa-bell"></span>Notification</li>
      <li><span class="fa fa-comments"></span>Message</li>
      <li><span class="fa fa-gear"></span>Setting</li>
    </ul>
  </div>
</div>
```

This HTML structure brings together notifications, a search bar, and a menu icon, making efficient use of space.

## CSS Styles

We've carefully crafted CSS styles to make the layout visually appealing and user-friendly:

```css
@import url(https://fonts.googleapis.com/css?family=Open+Sans:600,400);
.frame {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 400px;
  height: 400px;
  margin-top: -200px;
  margin-left: -200px;
  border-radius: 2px;
  box-shadow: 1px 2px 10px 0px rgba(0, 0, 0, 0.3);
  background: #264057;
  color: #666666;
  font-family: "Open Sans", Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  overflow: hidden;
}

.panel {
  position: absolute;
  z-index: 2;
  height: 300px;
  width: 300px;
  top: 50px;
  left: 50px;
  background: #fff;
  border-radius: 3px;
  overflow: hidden;
  box-shadow: 10px 10px 15px 0 rgba(0, 0, 0, 0.3);
  transition: all 0.5s ease-in-out;
}
.panel.show-menu {
  transform: translate3d(150px, 0, 0);
}
.panel .header {
  height: 60px;
  width: 100%;
  background: #5F98CD;
}
.panel .header .menu-icon {
  position: absolute;
  width: 29px;
  height: 15px;
  top: 23px;
  left: 20px;
  cursor: pointer;
}
.panel .header .menu-icon:hover .dash-top,
.panel .header .menu-icon:hover .dash-bottom,
.panel .header .menu-icon:hover .circle {
  background: #fff;
}
.panel .header .menu-icon .dash-top, .panel .header .menu-icon .dash-bottom {
  position: absolute;
  width: 20px;
  height: 3px;
  top: 0;
  left: 0;
  background: #B2DAFF;
  border-radius: 3px;
  transition: all 0.2s ease-in-out;
}
.panel .header .menu-icon .dash-bottom {
  width: 29px;
  top: auto;
  bottom: 0;
}
.panel .header .menu-icon .circle {
  position: absolute;
  height: 7px;
  width: 7px;
  border-radius: 4px;
  top: -2px;
  right: 0;
  background: #B2DAFF;
  transition: all 0.2s ease-in-out;
}
.panel .header .title {
  display: block;
  text-align: center;
  line-height: 60px;
  color: #fff;
  font-weight: 600;
  font-size: 15px;
}
.panel .header .search-input {
  box-sizing: border-box;
  position: absolute;
  top: 13px;
  right: 55px;
  width: 230px;
  height: 34px;
  border-radius: 17px;
  border: none;
  background: #fff;
  padding: 0 17px;
  color: #666;
  font-size: 13px;
  opacity: 0;
  transition: all 0.3s ease-in-out;
  transform: translateX(15px);
  pointer-events: none;
}
.panel .header .search-input:focus {
  outline: none;
}
.panel .header .search-input.active {
  transform: translateX(0);
  opacity: 1;
  pointer-events: all;
}
.panel .header .search-icon {
  position: absolute;
  z-index: 2;
  font-size: 21px;
  color: #B2DAFF;
  top: 18px;
  right: 20px;
  transition: all 0.3s ease;
  cursor: pointer;
}
.panel .header .search-icon:hover {
  color: #fff;
}
.panel .notifications {
  position: relative;
  height: 100%;
  overflow: hidden;
}
.panel .notifications .line {
  position: absolute;
  top: 0;
  left: 27px;
  bottom: 0;
  width: 3px;
  background: #EBEBEB;
}
.panel .notifications .notification {
  position: relative;
  z-index: 2;
  margin: 25px 20px 25px 43px;
}
.panel .notifications .notification:nth-child(2) {
  -webkit-animation: here-am-i 0.5s ease-out 0.4s;
          animation: here-am-i 0.5s ease-out 0.4s;
  -webkit-animation-fill-mode: both;
          animation-fill-mode: both;
}
.panel .notifications .notification:nth-child(3) {
  -webkit-animation: here-am-i 0.5s ease-out 0.6s;
          animation: here-am-i 0.5s ease-out 0.6s;
  -webkit-animation-fill-mode: both;
          animation-fill-mode: both;
}
.panel .notifications .notification:nth-child(4) {
  -webkit-animation: here-am-i 0.5s ease-out 0.8s;
          animation: here-am-i 0.5s ease-out 0.8s;
  -webkit-animation-fill-mode: both;
          animation-fill-mode: both;
}
.panel .notifications .notification:hover {
  color: #5F98CD;
  cursor: pointer;
}
.panel .notifications .notification .circle {
  box-sizing: border-box;
  position: absolute;
  height: 11px;
  width: 11px;
  background: #fff;
  border: 2px solid #5F98CD;
  box-shadow: 0 0 0 3px #fff;
  border-radius: 6px;
  top: 0;
  left: -20px;
}
.panel .notifications .notification .time {
  display: block;
  font-size: 13px;
  line-height: 11px;
  margin-bottom: 2px;
}
.panel .notifications .notification p {
  font-size: 15px;
  line-height: 20px;
  margin: 0;
}
.panel .notifications .notification p b {
  font-weight: 600;
}

.menu {
  position: absolute;
  width: 170px;
  height: 270px;
  top: 65px;
  left: 50px;
  background: #43627d;
  border-radius: 3px;
  transition: all 0.5s ease-in-out;
  transform: translate3d(20px, 0, 0);
}
.menu.active {
  box-shadow: 5px 5px 8px rgba(0, 0, 0, 0.3);
  transform: translate3d(0, 0, 0);
}
.menu ul {
  margin: 0;
  padding: 10px 0;
}
.menu li {
  color: #93B2CD;
  margin: 0;
  padding: 18px 17px;
  list-style: none;
  font-size: 14px;
  line-height: 14px;
  cursor: pointer;
  transition: all 0.5s ease-in-out;
}
.menu li:hover {
  color: #fff;
  background: #385269;
}
.menu li span {
  display: block;
  float: left;
  margin-right: 8px;
  margin-top: -1px;
}
.menu li .fa-gear, .menu li .fa-user, .menu li .fa-bell {
  margin-top: 0;
}

@-webkit-keyframes here-am-i {
  from {
    transform: translate3d(0, 50px, 0);
    opacity: 0;
  }
  to {
    trnsform: translate3d(0, 0, 0);
    opacity: 1;
  }
}

@keyframes here-am-i {
  from {
    transform: translate3d(0, 50px, 0);
    opacity: 0;
  }
  to {
    trnsform: translate3d(0, 0, 0);
    opacity: 1;
  }
}
```

These styles define the appearance and behavior of the elements in our compact UI.

## JavaScript Interaction

For added interactivity, we've implemented JavaScript functionality to handle the search and menu toggling:

```javascript
const searchIcon = document.querySelector('.search-icon');
const searchInput = document.querySelector('.search-input');
const menuIcon = document.querySelector('.menu-icon');
const panel = document.querySelector('.panel');
const menu = document.querySelector('.menu');

searchIcon.addEventListener('click', function(){
	searchInput.classList.toggle('active');
});

menuIcon.addEventListener('click', function(){
	panel.classList.toggle('show-menu');
	menu.classList.toggle('active');
})
```

These JavaScript interactions enable users to toggle the search bar and menu with ease.

### Result

![Bear Image](https://i.imgur.com/5xFv7bu.png=300x200)

As a result of this design, you have a compact yet functional user interface that combines notifications, search, and a menu icon in the smallest possible space.

## Conclusion

In today's fast-paced digital world, the efficient use of screen space is vital for creating user-friendly applications. Combining notifications, search, and menus in a compact UI demonstrates the power of thoughtful design and functionality. With HTML, CSS, and a touch of JavaScript, you can provide users with a seamless and enjoyable experience.

Blog Series: [100DaysofCSS](/tags/100daysofcss)

**Stay connected with DevHavok for more exciting content:**
- GitHub: [GitHub](https://github.com/Shaunfurtado/100daysofCSS)
- YouTube: [YouTube](https://www.youtube.com/channel/UC66ahSH1xpBBlaMBP8lNuBg)
- CodePen: [CodePen](https://codepen.io/Shaun-Furtado)
- Blog: [DevHavok](https://devhavok.is-a.dev/)

Join us tomorrow for Day 8 of the "100 Days of CSS" challenge, where we'll continue exploring the fascinating world of web design.

Keep coding and stay creative! 🚀

*Stay tuned with [DevHavok](https://devhavok.is-a.dev/) for more exciting content.*
