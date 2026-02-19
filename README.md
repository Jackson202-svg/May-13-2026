# ⏳ Countdown to May 13, 2026

![HTML5](https://img.shields.io/badge/HTML-5-orange?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS-3-blue?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow?logo=javascript&logoColor=black)
![Responsive](https://img.shields.io/badge/Responsive-Yes-brightgreen)
![Status](https://img.shields.io/badge/Status-Production--Ready-success)
![License](https://img.shields.io/badge/License-MIT-green)

A fully responsive countdown website built using **HTML**, **CSS**, and **Vanilla JavaScript** that tracks the time remaining until **May 13, 2026**.

The countdown updates live every second and displays:

- Months remaining  
- Weeks remaining  
- Days remaining  
- Hours remaining  
- Minutes remaining  
- Seconds remaining  

---

## 📌 Overview

**Countdown to May 13, 2026** is a lightweight, production-ready web application that calculates the exact time remaining until a specific target date.

The project uses:

- `index.html` → Structure  
- `style.css` → Styling and responsiveness  
- `script.js` → Countdown logic and time calculations  

The application recalculates the time difference every second and updates the page dynamically without refreshing.

---

## 🚀 Features

- ✅ Real-time countdown (updates every second)
- ✅ Displays months, weeks, days, hours, minutes, seconds
- ✅ Fully responsive design (mobile, tablet, desktop)
- ✅ Clean and modern UI
- ✅ Lightweight (no external libraries)
- ✅ GitHub Pages ready
- ✅ Easy to customize

---

## 🌐 Live Demo (GitHub Pages)

After deployment, your site will be available at:

https://jackson202-svg.github.io/May-13-2026/

```
https://YOUR-USERNAME.github.io/countdown-to-may-13-2026/
```

Example:

```
https://john-doe.github.io/countdown-to-may-13-2026/
```

---

# 🧠 How the Countdown Works

## 1️⃣ Defining the Target Date

Inside `script.js`:

```javascript
const targetDate = new Date("May 13, 2026 00:00:00").getTime();
```

- `Date()` creates the date object.
- `.getTime()` converts it to milliseconds.
- This allows accurate time comparison.

---

## 2️⃣ Getting the Current Time

```javascript
const now = new Date().getTime();
```

This retrieves the current time in milliseconds every second.

---

## 3️⃣ Calculating the Time Difference

```javascript
const distance = targetDate - now;
```

- If `distance > 0` → countdown continues.
- If `distance <= 0` → countdown stops.

---

## 4️⃣ Converting Milliseconds into Time Units

```javascript
const second = 1000;
const minute = second * 60;
const hour = minute * 60;
const day = hour * 24;
const week = day * 7;
const month = day * 30.44; // Average month
```

Then calculating values:

```javascript
const months = Math.floor(distance / month);
const weeks = Math.floor((distance % month) / week);
const days = Math.floor((distance % week) / day);
const hours = Math.floor((distance % day) / hour);
const minutes = Math.floor((distance % hour) / minute);
const seconds = Math.floor((distance % minute) / second);
```

---

## 5️⃣ Updating Every Second

```javascript
setInterval(function () {
   // countdown logic here
}, 1000);
```

`setInterval()` runs the function every 1000 milliseconds (1 second).

---

## 6️⃣ Updating the DOM Dynamically

```javascript
document.getElementById("months").innerText = months;
document.getElementById("weeks").innerText = weeks;
document.getElementById("days").innerText = days;
document.getElementById("hours").innerText = hours;
document.getElementById("minutes").innerText = minutes;
document.getElementById("seconds").innerText = seconds;
```

This updates the HTML elements in real time without reloading the page.

---

# 🎨 How style.css Works

The `style.css` file controls:

## Layout
- Flexbox or Grid for alignment
- Centered countdown display
- Clean spacing and structure

## Responsiveness
- Media queries for mobile devices
- Flexible sizing
- Scalable fonts

Example:

```css
@media (max-width: 768px) {
  .countdown {
    flex-direction: column;
  }
}
```

## Visual Design
- Background colors or gradients
- Typography styling
- Shadows and smooth transitions
- Card-style countdown blocks

---

# 🏗 How index.html Connects Everything

The `index.html` file:

1. Creates the countdown layout.
2. Assigns unique IDs for each time unit.
3. Links CSS and JavaScript.

Example:

```html
<link rel="stylesheet" href="style.css">
<script src="script.js"></script>
```

Countdown containers:

```html
<div id="months"></div>
<div id="weeks"></div>
<div id="days"></div>
<div id="hours"></div>
<div id="minutes"></div>
<div id="seconds"></div>
```

---

# 📁 Project Structure

```
countdown-to-may-13-2026/
│
├── index.html
├── style.css
├── script.js
└── README.md
```

---

# 🛠 Installation

1. Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/countdown-to-may-13-2026.git
```

2. Open the folder.
3. Open `index.html` in your browser.

No dependencies required.

---

# 🔧 Customizing the Target Date

Open `script.js` and modify:

```javascript
const targetDate = new Date("May 13, 2026 00:00:00").getTime();
```

Change it to any future date:

```javascript
const targetDate = new Date("December 25, 2026 00:00:00").getTime();
```

Save and refresh.

---

# 🌍 Deploying to GitHub Pages

1. Push the repository to GitHub.
2. Go to **Repository Settings**
3. Click **Pages**
4. Select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **Save**

Your site will go live shortly.

---

# 🛑 When the Countdown Reaches Zero

When `distance <= 0`:

- The interval is cleared.
- Countdown stops.
- A message can be displayed:

```javascript
document.getElementById("countdown").innerHTML = "🎉 The Day Has Arrived!";
```

This prevents negative values.

---

# ⚡ Performance

- No external libraries
- Efficient calculations
- Updates once per second
- Minimal DOM updates
- Fully client-side

Fast and optimized for all modern browsers.

---

# 🔮 Future Improvements

- Dark mode toggle
- Progress bar
- Timezone selection
- Animation effects
- Sound notification
- Convert to PWA

---

# 📄 License

This project is licensed under the **MIT License**.

You are free to use, modify, and distribute this project with attribution.

---

# 👤 Author

Created by **imel imel**

Built with HTML, CSS, and Vanilla JavaScript.

---

## ⭐ Support

If you found this project helpful:

- Star the repository  
- Fork it  
- Share it  

Happy coding! 🚀
