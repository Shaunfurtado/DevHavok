+++
title = "Day-6 of 100 Days of CSS"
date = 2023-11-06T18:08:23+05:30
draft = false
tags = ['100DaysOfCSS' ]
+++
# Day 6 of 100 Days of CSS Challenge

Welcome back to the DevHavok blog! We're on Day 6 of our adventurous journey through the 100 Days of CSS Challenge. In today's challenge, we'll be creating a stylish profile card using HTML and CSS. Whether you're a seasoned developer or just starting your coding journey, this challenge is a great way to hone your CSS skills and create an impressive profile card.

## HTML Structure
Let's start by looking at the HTML structure that forms the foundation of our profile card:

```html
<div class="frame">
	<div class="center">
		<div class="outer-grid">
			<div class="profile">
				<div class="avatar">
					<svg class="circles">
						<circle class="circle circle-inner" r="37.5" cx="41" cy="41" />
						<circle class="circle circle-outer" r="40.5" cx="41" cy="41" />
					</svg>
					<img class="image" src="https://100dayscss.com/codepen/jessica-potter.jpg" alt="avatar">
				</div>
				<div class="name">DevHavok
</div>
				<div class="job-title">Artist
</div>
				<div class="buttons">
					<button type="button">Follow</button>
					<button type="button">Message</button>
				</div>
			</div>
			<div class="column">
				<div class="card">
					<div class="card-title">109</div>
					<div class="card-desc">Posts</div>
				</div>
				<div class="card">
					<div class="card-title">1344</div>
					<div class="card-desc">Likes</div>
				</div>
				<div class="card">
					<div class="card-title">8,756</div>
					<div class="card-desc">Followers</div>
				</div>
			</div>
		</div>
	</div>
</div>
```

In this structure, we have a `.frame` that acts as the main container, which holds the profile card. The card itself is contained within the `.center` and `.outer-grid` elements. Inside the profile card, we have the user's avatar, name, job title, and action buttons. Below the profile card, we have a column of cards representing various statistics.

## CSS Styling
Now, let's take a look at the CSS styles used to create this beautiful profile card:

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
  background: linear-gradient(55deg, rgba(225,0,0,0.2) , rgba(0,0,160,0.8));
  color: #526150;
	font-family: 'Open Sans', Helvetica, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
}

.center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%,-50%);
	height: 299px;
	width: 320px;
	box-shadow: 10px 10px 15px 0 rgba(0, 0, 0, 0.3);
	background-color: #1b1b1b;
	border-radius: 3px;
}

.outer-grid {
	display: grid;
	grid-template-columns: 1fr 35%;
	height: 100%;
	border-radius: inherit;
}

.profile {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
}

.avatar {
	width: 82px;
	height: 82px;
	position: relative;
	display: flex;
	align-items: center;
	justify-content: center;
}

.circles {
	position: absolute;
	width: inherit;
	height: inherit;
}

.circle {
	fill: transparent;
	stroke-width: 1px;
	stroke: white;
}

.circle-inner {
	clip-path: inset(-1px -1px -1px 15%);
	transform-origin: 50% 50%;
	transition: transform 1.5s ease-in-out;
}

.circles:hover .circle-inner {
	transform: rotate(360deg)
}

.circle-outer {
	clip-path: inset(-1px 15% -1px -1px);
	transform-origin: 50% 50%;
	transition: transform 1.5s ease-in-out;
}

.circles:hover .circle-outer {
	transform: rotate(-360deg)
}

.image {
	display: block;
	border-radius: 50%;
	width: 70px;
}

.name {
	font-size: 15px;
	font-weight: 600;
	margin-top: 20px;
	color: white;
}

.job-title {
	font-size: 11px;
	line-height: 15px;
	color: white;
}

.buttons {
	display: flex;
	flex-direction: column;
	gap: 10px;
	margin-top: 33px;
}

button {
	border: 1px solid white;;
	border-radius: 15px;
	width: 120px;
	height: 30px;
	background-color: inherit;
	color: inherit;
	font-size: 12px;
	font-weight: 600;
	transition: background-color .5s, color .5s;
}

button:hover {
	background-color: #686450;
	color: white;
}

.column {
	display: grid;
	grid-gap: 1px;
	border-radius: inherit;
}

.card {
	display: flex;
	flex-direction: column;
	align-items: center;
	border-radius: inherit;
	background-color: #B5E2DF;
	cursor: pointer;
	transition: background-color .5s;
}

.card:hover {
	background-color: #B7BAA2;
}

.card-title {
	padding-top: 30px;
	font-size: 18px;
	font-weight: 600;
}

.card-desc {
	font-size: 11px;
}

```

The CSS code defines various styles for each component of the profile card, ensuring that it looks visually appealing and well-structured.

### Result

![Bear Image](https://i.imgur.com/oyU8hvc.png)

## Final Thoughts
Creating a profile card is a great way to practice your CSS skills, and this challenge provides a creative and stylish design. You can use this as a starting point and customize it to match your own profile or website. Remember, the key to mastering CSS is practice and experimentation, so don't hesitate to make changes and explore new ideas.

If you've been following along with the 100 Days of CSS Challenge, congratulations on completing Day 6! Keep up the good work, and stay tuned for more exciting CSS challenges in the days to come. Don't forget to share your creations on Codepen and #100DaysOfCSS to connect with fellow developers and showcase your progress.

Blog Series : [100DaysofCSS](/tags/100daysofcss)

**Follow me on other platforms for more content:**
- GitHub: [GitHub](https://github.com/Shaunfurtado/100daysofCSS)
- YouTube: [YouTube](https://www.youtube.com/channel/UC66ahSH1xpBBlaMBP8lNuBg)
- CodePen: [CodePen](https://codepen.io/Shaun-Furtado)
- Blog: [DevHavok](https://devhavok.is-a.dev/)


Stay tuned for my daily updates in the "100 Days of CSS" challenge as I explore and create new and exciting designs.

Happy coding, and see you on Day 5! 🚀

*Keep up with the [DevHavok](https://devhavok.is-a.dev/) for more content.*