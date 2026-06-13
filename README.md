# ChronoFusion — Digital & Analog Table Watch Website

**Live Fusion Experience:** A sleek, responsive product showcase website that presents a **hybrid table watch** combining classic analog aesthetics with real-time digital intelligence. The page features live analog canvas clock, dynamic digital time display, and a modern product interface — perfect for smartwatch or hybrid device landing pages.

<img width="1880" height="1934" alt="image" src="https://github.com/user-attachments/assets/dbfbcb6e-3b3a-43b9-9e27-50b7a60a1fff" />

---

## Features

- **Dual Watch Visualization**
  - **Analog Clock:** Canvas-based mechanical-style watch face with sweeping second hand, Roman/Arabic hybrid markers, and polished dial design.
  - **Digital Display:** Real-time digital clock (12‑hour with AM/PM), live date (weekday, month, day, year), and a futuristic dark screen.
- **Perfect Synchronization:** Both analog and digital displays derive from your system time — fully synced down to milliseconds.
- **Product Highlights:**
  - Hybrid movement & smart features (wireless charging, app companion, weather sync)
  - Premium materials: sapphire glass, luminous hands, quartz + digital hybrid engine
  - Pricing section & “Notify Me” interactive button (demo interaction)
- **Responsive & Modern Design:**
  - Glass‑morphism cards, gradient hero, smooth hover animations
  - Works on desktop, tablet, and mobile screens
- **Interactive User Feedback:** Click the preorder button for a smooth toast notification.

---

## 🛠️ Tech Stack

| Area          | Technologies                                                                 |
|---------------|------------------------------------------------------------------------------|
| **Frontend**  | HTML5, CSS3 (Flexbox, Grid, backdrop‑filter, animations)                   |
| **Graphics**  | Canvas API (real‑time analog clock rendering)                              |
| **Interactivity** | Vanilla JavaScript (Date API, requestAnimationFrame, setInterval, DOM)  |
| **Icons**     | Font Awesome 6                                                              |
| **Fonts**     | Google Fonts: Inter, Space Grotesk                                         |

---

## Project Structure

```
chronofusion-hybrid-watch/
│
├── index.html          # Main landing page (complete website)
├── README.md           # Project documentation (this file)
└── assets/             (optional) – if you add images or screenshots
    └── preview.png
```

> **Note:** This is a single‑file frontend project. All CSS and JavaScript are embedded within `index.html` for simplicity and easy deployment.

---

## Getting Started

Follow these steps to run the project locally or deploy it.

### 1. Clone the repository

```bash
git clone https://github.com/your-username/chronofusion-hybrid-watch.git
cd chronofusion-hybrid-watch
```

### 2. Open the website

Simply open `index.html` in any modern web browser:

```bash
# On macOS
open index.html

# On Windows
start index.html

# Or double‑click the file
```

Alternatively, use a local development server (e.g., with VS Code Live Server or Python):

```bash
# Python 3
python -m http.server 8000
# Then visit http://localhost:8000
```

### 3. Explore the experience

- Watch the **analog clock** hands move in real time.
- See the **digital display** update every second.
- Hover over cards to see subtle animations.
- Click the **“Notify when available”** button for a demo interaction.

---

## Customization Guide

You can easily adapt this template for your own hybrid watch or smart product.

### Change Color Theme

In the `<style>` section, update the CSS variables / gradients:

```css
/* Example: modify the hero gradient */
h1 {
  background: linear-gradient(135deg, #yourColor1, #yourColor2);
}
```

### Modify Product Specs

Edit the feature lists inside `.feature-list` or `.hybrid-card` elements to reflect your own watch features.

### Update Pricing & Call‑to‑Action

Locate the `.price-cta` block and change the price text or button behavior in the JavaScript `notifyBtn` event listener.

### Replace the Analog Watch Face

The analog clock drawing logic is inside `drawAnalogClock()`. You can customize:
- Hand colors, sizes, and shapes
- Marker styles (tick marks, numerals)
- Dial background and textures

---

## 🌟 Key Code Highlights

### Real‑Time Analog Clock (Canvas)

```javascript
function drawAnalogClock() {
  const now = new Date();
  const seconds = now.getSeconds() + now.getMilliseconds() / 1000;
  const secondAngle = (seconds / 60) * 2 * Math.PI;
  // Draw hands, markers, and numerals...
}
// Continuous smooth animation using requestAnimationFrame
```

### Digital Time & Date

```javascript
function updateDigitalDisplay() {
  const now = new Date();
  const timeString = `${formatHours(now)}:${minutes}:${seconds} ${ampm}`;
  const dateString = now.toLocaleDateString(undefined, { weekday: 'short', ... });
  // Update DOM elements
}
setInterval(updateDigitalDisplay, 1000);
```

---

## 📱 Responsive Behavior

- Uses Flexbox and `flex-wrap` to stack cards on small screens.
- CSS media queries adjust font sizes and container padding for mobile devices.
- Canvas is resolution‑locked (200×200) and remains sharp.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!  
Feel free to fork the repository and submit a pull request.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/amazing-feature`)
3. Commit your Changes (`git commit -m 'Add some amazing feature'`)
4. Push to the Branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` file for more information (you can add a simple MIT license file if desired).  
Basically, you are free to use, modify, and distribute this code for personal or commercial projects.

---

## 🙌 Acknowledgements

- [Font Awesome](https://fontawesome.com/) for crisp icons
- [Google Fonts](https://fonts.google.com/) for typography
- Inspiration from modern hybrid watch designs (Apple Watch, mechanical‑digital fusion concepts)

---

## 📬 Contact

Project Link: [https://github.com/your-username/chronofusion-hybrid-watch](https://github.com/your-username/chronofusion-hybrid-watch)  
Live Demo: [Insert GitHub Pages or Netlify link]

Created with ⏱️ by [Your Name] — enjoy the fusion of tradition and technology!

---

> **Note:** This website is a frontend demonstration. The “Notify Me” button is a UI example and does not store user data. Replace placeholders with actual links and images before publishing.
```
