# Elementor White Gradient Overlay CSS

This repo contains a simple CSS snippet to create a white-to-transparent gradient overlay in Elementor. It helps improve text visibility over background images, perfect for hero sections, call-to-actions, or landing pages.

## 🌈 Effect Preview

![Gradient Preview](screenshot.png)

## ✨ How It Works

This CSS adds a white gradient to the left side of an Elementor section and ensures all content appears clearly above it.

## 💻 CSS Code

```css
/* White gradient fade from left to transparent */
selector::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to right, white 40%, rgba(255, 255, 255, 0) 80%);
  z-index: 0;
  pointer-events: none;
}

/* Ensure all section content stays on top */
selector > .elementor-container {
  position: relative;
  z-index: 1;
}
