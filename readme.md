# 🎧 Audira Headphone - Premium Interactive Website

A stunning, modern e-commerce website for Audira premium headphones featuring smooth scroll animations, immersive product showcases, and an engaging user experience powered by GSAP animations.

---

## 📋 Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Installation & Setup](#installation--setup)
- [How to Use](#how-to-use)
- [File Descriptions](#file-descriptions)
- [Animation Details](#animation-details)
- [Customization Guide](#customization-guide)
- [Author](#author)

---

## ✨ Features

### 🎯 Core Features

- **Smooth Scroll Animation**: Fluid scrolling experience using GSAP ScrollSmoother
- **Product Showcase**: Dynamic headphone positioning and rotation during scroll
- **Responsive Design**: Optimized for all screen sizes (mobile, tablet, desktop)
- **Interactive Elements**: Hover effects, buttons, and call-to-action components
- **Video Integration**: Embedded video content in product sections
- **Text Animations**: Character-level split text animations with stagger effects
- **Performance Optimized**: Efficient animations with proper rendering optimization

### 🎨 Design Highlights

- Modern, clean UI with premium aesthetic
- Warm color palette (beige, brown, orange)
- Professional typography using Google Fonts
- Multiple product variants with pricing
- Social media integration in footer
- Responsive navigation header

---

## 📁 Project Structure

```
Audira-Headphone-Website/
├── index.html           # Main HTML file with all sections
├── style.css            # All styling and responsive design
├── main.js              # GSAP animations and scroll effects
├── images/
│   ├── logo.png         # Brand logo
│   ├── brown.png        # Brown headphone image
│   ├── green.png        # Green headphone variant
│   ├── black.png        # Black headphone variant
│   ├── img1.jpeg        # Gallery image 1
│   ├── img2.jpeg        # Gallery image 2
│   ├── img3.jpeg        # Gallery image 3
│   ├── img4.jpg         # Full-width section image
│   ├── video.mp4        # Product video
│   ├── fb.png           # Facebook icon
│   ├── insta.png        # Instagram icon
│   └── brown.png        # Additional variant
└── README.md            # This file
```

---

## 🛠️ Technologies Used

### Frontend Framework & Libraries

| Technology            | Version | Purpose                                |
| --------------------- | ------- | -------------------------------------- |
| **HTML5**             | Latest  | Semantic markup and structure          |
| **CSS3**              | Latest  | Styling, layout, and responsive design |
| **JavaScript (ES6+)** | Modern  | Interactive functionality              |
| **GSAP**              | v3.13.0 | Advanced animations                    |
| **ScrollTrigger**     | v3.13.0 | Scroll-based animations                |
| **ScrollSmoother**    | v3.13.0 | Smooth scrolling effect                |
| **SplitText**         | v3.13.0 | Text animation capabilities            |
| **Google Fonts**      | Latest  | Typography (DM Sans, Outfit)           |

### Development Tools

- Code Editor (VS Code recommended)
- Browser DevTools for debugging
- Live Server for local development

---

## 📦 Installation & Setup

### Step 1: Clone or Download the Project

```bash
# Using Git
[git clone https://github.com/yourusername/audira-headphone.git](https://github.com/NeelPatel5150/Audira-Scrolling-Animation.git)
cd audira-headphone

# OR manually download and extract the ZIP file
```

### Step 2: Project Dependencies

This project uses **CDN links** for libraries, so **NO npm installation required**!

All dependencies are loaded via CDN:

- GSAP library (3.13.0)
- ScrollTrigger plugin
- ScrollSmoother plugin
- SplitText plugin
- Google Fonts

---

## 🎮 How to Use

### Basic Navigation

1. **Header Navigation**

   - Click the "Buy Now" button in header
   - Logo on the left is your brand identifier

2. **Scrolling Experience**

   - Smooth scroll enabled by default
   - Headphone image moves and rotates as you scroll
   - Content appears with staggered animations

3. **Product Sections**

   - Section 1: Hero with tagline "Modern Harmony"
   - Section 2: "True Clarity" with features and CTA
   - Section 3: "Masterbeat" with video and description
   - Section 4: Product gallery with images
   - Section 5: "Top Picks" with pricing
   - Section 6: "Pure Escape" closing section

4. **Interactive Elements**
   - Hover over buttons for interaction
   - Click "Buy Now" buttons (currently links to #)
   - Footer social links for additional engagement

---

## 📄 File Descriptions

### index.html

**Purpose**: Main HTML structure and content

**Key Sections**:

- `<header>`: Navigation with logo and CTA button
- `#smooth-wrapper` & `#smooth-content`: Scroll smoother containers (required)
- `#main`: Primary content container with absolute-positioned headphone image
- `#section1-6`: Individual content sections with animations
- `<footer>`: Brand footer with social links

**CDN Libraries Included**:

```html
<!-- GSAP & Plugins -->
<script src="https://cdn.jsdelivr.net/npm/gsap@3.13.0/dist/gsap.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/gsap@3.13.0/dist/ScrollTrigger.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/gsap@3.13.0/dist/ScrollSmoother.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/gsap@3.13.0/dist/SplitText.min.js"></script>
```

### style.css

**Purpose**: Complete styling for the entire website

**CSS Variables Defined**:

```css
--bg-color: #F5ECE4           /* Light beige background */
--primary-color: #734425      /* Brown for headings */
--secondary-color: #C26819    /* Orange for buttons */
--black: #2E2E2E              /* Dark text color */
--heading-font: "Outfit"      /* Bold heading font */
```

**Key Classes**:

- `.w-full`: Full-width responsive container
- `.heading`: Large, uppercase section headings
- `.btn`: Styled button elements
- `.radius`: Rounded corners (10px)
- `.content-wrapper`: Content container
- `.feature-box`: Feature showcase box
- `.product`: Product card
- `.feature-box`, `.radius`: Utility classes

**Responsive Breakpoints**:

- Mobile first approach
- Desktop optimization for screens > 991px

### main.js

**Purpose**: All animations and scroll interactions

**Key Functions**:

1. **ScrollSmoother Initialization**

   ```javascript
   ScrollSmoother.create({
     wrapper: '#smooth-wrapper',
     content: '#smooth-content',
     smooth: 4,
     effects: true,
   });
   ```

   - Enables smooth scrolling
   - `smooth: 4` controls smoothness level
   - `effects: true` enables data-speed and data-lag

2. **Headphone Animation Sequences**

   - **Section 2**: Moves headphone 85vh down, 18vw right, scales to 32vw, rotates 90°
   - **Section 3**: Moves to 218vh, scales to 35vw, rotates 35°
   - **Section 4**: Moves to 308vh, scales to 42vw, no rotation
   - **Section 5a**: Moves based on screen height, scales to 28vw
   - **Section 5b**: Final position at 32vh or 419vh, scales to 300px

3. **Content Animations**

   - Section 2 content fades in from 140% offset
   - Section 3 heading slides in
   - Section 4 images animate width and opacity
   - Section 6 content slides up with duration

4. **Text Split Animation**

   ```javascript
   let split = SplitText.create('#section1 .heading', {
     type: 'chars, words, lines',
   });
   ```

   - Characters split and animated individually
   - Random rotation and position
   - Staggered timing for effect

5. **Screen Height Detection**
   ```javascript
   let isShortHeight = window.screen.height < 1050;
   ```
   - Adjusts animations for short screens
   - Prevents overflow and improves UX

---

## 🎬 Animation Details

### How Scroll Animations Work

#### 1. ScrollTrigger Setup

```javascript
scrollTrigger: {
  trigger: '#section2',      // Element that triggers animation
  start: 'top bottom',       // When animation starts
  end: 'center center',      // When animation ends
  scrub: true,               // Links animation to scrollbar
}
```

**Trigger Point Explanations**:

- `'top bottom'`: Top of trigger element meets bottom of viewport
- `'center center'`: Center of element meets center of viewport
- `'bottom bottom'`: Bottom of element meets bottom of viewport

#### 2. Headphone Animation Journey

The headphone undergoes a 5-phase journey:

| Phase | Trigger    | Position       | Size  | Rotation |
| ----- | ---------- | -------------- | ----- | -------- |
| 1     | Section 2  | 85vh Y, 18vw X | 32vw  | 90°      |
| 2     | Section 3  | 218vh Y        | 35vw  | 35°      |
| 3     | Section 4  | 308vh Y        | 42vw  | 0°       |
| 4     | Section 5a | Responsive Y   | 28vw  | 0°       |
| 5     | Section 5b | End Y          | 300px | 0°       |

#### 3. Text Animation (Hero Section)

```javascript
gsap.from(split.chars, {
  yPercent: () => gsap.utils.random(-100, 100), // Random Y offset
  rotation: () => gsap.utils.random(-30, 30), // Random rotation
  autoAlpha: 0, // Start invisible
  ease: 'back.out(1.5)', // Bounce effect
  stagger: { amount: 0.5, from: 'random' }, // Randomized timing
  duration: 1.5,
});
```

### Animation Easing Functions

- `'power1.inOut'`: Smooth, natural acceleration/deceleration
- `'back.out(1.5)'`: Bouncy overshoot effect
- `'ease'` key: Controls animation smoothness

---

## 🎨 Customization Guide

### Change Colors

Edit `style.css` variables:

```css
:root {
  --bg-color: #f5ece4; /* Change background */
  --primary-color: #734425; /* Change heading color */
  --secondary-color: #c26819; /* Change button color */
  --black: #2e2e2e; /* Change text color */
}
```

### Modify Animation Speed

**Scroll Smoothness** (main.js):

```javascript
ScrollSmoother.create({
  smooth: 4, // 1 = fast, 10 = very slow (adjust as needed)
});
```

**Scroll Trigger Scrub** (main.js):

```javascript
scrub: true,  // Change to 1, 2, 3 for different smoothness
```

- `true`: Immediate sync with scroll
- `1-3`: Delay in seconds (smoother effect)

**Headphone Animation Duration** (main.js):

```javascript
duration: 1.5,  // Change for faster/slower animations
```

### Adjust Hero Text Animation

Edit the SplitText animation:

```javascript
gsap.from(split.chars, {
  duration: 1.5, // Slower = higher value
  stagger: { amount: 0.5 }, // Higher = more staggered timing
});
```

### Change Product Prices

Edit `index.html` section 5:

```html
<div class="price">₹4,499</div>
<!-- Change price here -->
```

### Update Content Text

Simply edit text in corresponding sections in `index.html`:

- Section 1: Hero heading
- Section 2-6: Any paragraph or heading text

### Add New Sections

1. Add HTML structure in `index.html`
2. Add CSS styling in `style.css`
3. Create corresponding animation in `main.js`:
   ```javascript
   gsap.to('#newsection', {
     scrollTrigger: {
       trigger: '#newsection',
       start: 'top bottom',
       end: 'center center',
       scrub: true,
     },
     // Your animation properties
   });
   ```

### Responsive Breakpoint Adjustment

Edit in `main.js`:

```javascript
let isShortHeight = window.screen.height < 1050; // Change threshold
```

Change breakpoint in `main.js`:

```javascript
ScrollTrigger.matchMedia({
  '(min-width: 991px)': function () {
    // Desktop animations
  },
  // Add mobile animations here if needed
});
```

---

## 👨‍💻 Author

Created as a modern e-commerce showcase for Audira Premium Headphones.

**Last Updated**: January 2026

---

## 🎯 Next Steps

1. ✅ Set up local development environment
2. ✅ Customize colors and content for your brand
3. ✅ Replace placeholder images with your products
4. ✅ Update pricing and product information
5. ✅ Link CTA buttons to real purchase pages
6. ✅ Deploy to chosen hosting platform
7. ✅ Set up Google Analytics
8. ✅ Optimize for SEO

---

**Enjoy building with Audira! 🎧✨**
