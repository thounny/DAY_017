# DAY_017 | Responsive Landing Page Reveal Animation with GSAP

This project is part of my daily code challenge series, **DAY_017**, where I focus on building a **responsive landing page** with **reveal animations** inspired by an element from **Our Revolution**. The inspiration site won **SOTD**, on **Awwwards**.

[Visit the Inspiration Website](https://our-revolution.com/)

---

## Preview

![DAY_017 Preview](./assets/DAY_017_1.gif)

## Inspiration

![Our Revolution](./assets/DAY_017_2.gif)

---

## Project Overview

This project replicates key visual and interactive elements from the award-winning site, incorporating **GSAP animations** for fluid interactions. The page includes staggered text reveals, hover effects, and responsive design principles to ensure the experience is immersive across devices.

---

## Key Features

- **Hero Section Reveal**: The main headline smoothly reveals itself with staggered animations on page load.
- **Hover Effect**: The word "future" starts blurry and becomes clear on hover, adding an extra interactive layer.
- **GSAP Animations**: GSAP is used to animate the images, text, and hover effects, ensuring smooth transitions.

---

## GSAP in Action

**GSAP (GreenSock Animation Platform)** allows developers to create performance-optimized animations. In this project, GSAP controls the entrance of images and text, as well as hover effects.

### Effects Breakdown

- **Staggered Image and Text Reveal**: Images and text elements slide and fade in from off-screen.
- **Clip-path Animation**: Certain elements use `clip-path` to create a "wipe" effect, revealing content smoothly.
- **Hover Interactivity**: The word "future" begins blurred and becomes sharp on hover, offering dynamic user interaction.

### Short Code Snippet

```javascript
const tl = gsap.timeline({ delay: 1 });

tl.to(".img", { y: 0, opacity: 1, duration: 1.5, stagger: 0.05 })
  .to(".loader-imgs", { x: 0, duration: 3 }, "-=2.5")
  .to(".img:not(#loader-logo)", { clipPath: "polygon(0% 0%, 100% 0%)", duration: 1 }, "-=1")
  .to(".nav-item, h1, footer, .item", { y: 0, opacity: 1, stagger: 0.1, duration: 1 }, "-=0.5");
```

### Explanation

1. **Image Reveal**: The `.img` elements slide up from below and fade in simultaneously.
2. **Loader Animation**: The loader images move horizontally from off-screen to their final position.
3. **Clip-path**: The `.img` elements are revealed with a clipping effect, simulating a wipe animation.
4. **Text & Navigation**: Text elements and the footer appear with subtle fade-ins and upward transitions.

---

## How to Run

1. **Clone the repository**:

   ```bash
   git clone https://github.com/thounny/DAY_017.git
   ```

2. **Navigate to the project directory**:

   ```bash
   cd DAY_017
   ```

3. **Open the `index.html` file** in your browser, or use a local development server like **Live Server** in VSCode.

---

## Project Structure

```bash
DAY_017/
│
├── assets/
├── fonts/
│   └── helveticaneue.woff2
├── images/
├── styles.css
├── index.html
└── script.js
```

---

## Features

- **Staggered Text Reveal**: Text elements animate into view on load for a cinematic feel.
- **Hover Blur-to-Clear**: The word "future" starts blurred and transitions to clarity on hover.
- **GSAP-Powered Animations**: Smooth, high-performance animations elevate the user experience.

---

## Technologies Used

- **HTML5**: Document structure and semantics.
- **CSS3**: Layout and styling, including animations and hover effects.
- **JavaScript (ES6)**: For controlling animations and interactions.
- **GSAP (GreenSock Animation Platform)**: For creating performant and fluid animations.

---

## Author

![Logo](./assets/index_dwn.gif)

**Thounny Keo**  
Creative Developer & Designer  
Frontend Development Student | Year Up United

---

![miku](./assets/miku.gif)
