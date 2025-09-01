# LoveCina 🌌💖

> An interactive cosmic love experience featuring galaxy animations, heart particles, and dynamic CIA text effects.

![LoveCina Demo](https://img.shields.io/badge/Status-Live-brightgreen)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Three.js](https://img.shields.io/badge/Three.js-000000?logo=three.js&logoColor=white)

## 🌟 Live Demo

**[Experience LoveCina →](https://renzmc.github.io/LoveCina/)**

## 🚀 Features

### 🌌 **Spiral Galaxy System**
- **80,000+ particles** on desktop, 40,000+ on mobile
- **5-branch spiral galaxy** with realistic physics simulation
- **Mouse-responsive camera** with smooth orbital movement
- **Adaptive particle density** optimized for device performance
- **Multi-color gradients** from white center to blue edges

### 💖 **Heart Particle Animation**
- **Mathematical heart curve** using parametric equations
- **32 particle trails** with leader-follower dynamics
- **Continuous animation loop** with smooth transitions
- **Glowing particle effects** with HSL color system
- **Screen blend mode** for enhanced visual appeal

### 🎯 **Interactive CIA Text System**
- **Particle-based text rendering** with proper "C I A" letter spacing
- **Mouse interaction physics** with configurable force fields
- **Explosion effects** on click/touch with 26-particle bursts
- **Return-to-origin animation** with spring physics
- **Floating ambient particles** for background atmosphere
- **High-DPI rendering** with device pixel ratio support

### ✨ **Visual Enhancement Effects**
- **Custom cursor trails** with fade and scale animations
- **Multi-layer canvas architecture** with proper z-index layering
- **Screen blend modes** for particle interaction
- **Responsive typography** with clamp() CSS functions
- **Performance-optimized rendering** with requestAnimationFrame

## 🛠️ Technical Implementation

### Core Technologies
- **HTML5 Canvas API** - Multi-layer 2D rendering
- **Three.js r128** - WebGL-based 3D galaxy system
- **Vanilla JavaScript ES6+** - Core particle physics
- **CSS3 Grid & Flexbox** - Responsive layout system
- **WebGL Shaders** - Hardware-accelerated rendering

### Architecture

┌─ Galaxy Layer (z-index: 3) ─ Three.js WebGL
├─ Heart Layer (z-index: 4) ── Canvas 2D + Blend Mode
├─ CIA Text Layer (z-index: 3) ─ Canvas 2D + Interaction
└─ Cursor Trails (z-index: 10) ─ DOM Elements


## 📱 Device Compatibility

| Platform | Desktop | Tablet | Mobile |
|----------|---------|--------|--------|
| **Chrome** | ✅ 60fps | ✅ 45fps | ✅ 30fps |
| **Firefox** | ✅ 60fps | ✅ 40fps | ✅ 25fps |
| **Safari** | ✅ 60fps | ✅ 50fps | ✅ 30fps |
| **Edge** | ✅ 60fps | ✅ 45fps | ✅ 30fps |

### Performance Scaling
- **Desktop (>768px)**: 80,000 galaxy particles, 3px sampling
- **Mobile (≤768px)**: 40,000 galaxy particles, 4px sampling
- **Auto DPR detection**: Scales rendering for Retina displays

## 🎮 User Interactions

### Desktop Controls
- **Mouse Movement** → Galaxy camera orbital tracking
- **Left Click** → CIA particle explosion + text dispersion
- **Mouse Hover** → Particle displacement field (140px radius)
- **Cursor Trail** → Automatic cyan particle trail generation

### Mobile/Touch Controls
- **Touch Move** → Particle trail creation + camera movement
- **Tap** → Explosion effect + particle burst animation
- **Swipe** → Continuous trail generation
- **Multi-touch** → Enhanced particle interaction

## ⚙️ Configuration API

The CIA text system exposes runtime configuration methods:

```javascript
// Initialize and get control handle
const ciaControls = initCIA();

// Adjust canvas clearing transparency (0.0 - 1.0)
ciaControls.setClearAlpha(0.08);

// Modify particle glow intensity (0 - 50)
ciaControls.setGlow(14);

// Change letter spacing ratio (0.1 - 1.0)
ciaControls.setLetterGapRatio(0.42);

// Toggle high-density particle mode
ciaControls.setDensity(true); // 2px sampling vs 4px


Galaxy Parameters

const galaxyConfig = {
    count: 80000,              // Total particles
    size: 0.02,               // Particle size multiplier
    radius: 3.5,              // Galaxy radius units
    branches: 5,              // Spiral arm count
    spin: 4,                  // Rotation intensity
    randomness: 8,            // Particle scatter factor
    randomnessPower: 5,       // Scatter distribution curve
    insideColor: '#ff6030',   // Center color (orange)
    outsideColor: '#1a73e8',  // Edge color (blue)
    centerColor: '#ffffff'    // Core color (white)
};


Heart Animation Config

const heartConfig = {
    numHearts: 32,            // Particle trail count
    heartScale: 180,          // Heart size (desktop)
    heartScaleMobile: 120,    // Heart size (mobile)
    trailLength: 32,          // Particles per trail
    friction: 0.7,            // Movement damping
    targetThreshold: 10,      // Path switching distance
    colorRange: {
        hue: [280, 360],      // Purple to magenta
        saturation: [60, 100], // Color intensity
        brightness: [40, 100]  // Luminosity range
    }
};


🚀 Quick Setup

1. Clone Repository

git clone https://github.com/RenzMc/LoveCina.git
cd LoveCina


2. Local Development

# Using Python 3
python -m http.server 8000

# Using Node.js
npx serve .

# Using PHP
php -S localhost:8000

# Then open: http://localhost:8000


3. GitHub Pages Deployment

The project is automatically deployed via GitHub Pages at:
**https://renzmc.github.io/LoveCina/**


📁 Project Structure

LoveCina/
├── index.html              # Main application (single file)
├── README.md              # This documentation
└── .github/
    └── workflows/
        └── pages.yml      # GitHub Pages deployment


🔧 Code Architecture

Canvas Layer Management

// Layer 1: Galaxy (WebGL) - z-index: 3
const galaxyCanvas = document.querySelector('canvas.webgl');

// Layer 2: Hearts (2D Canvas) - z-index: 4
const heartCanvas = document.getElementById('c');

// Layer 3: CIA Text (2D Canvas) - z-index: 3
const textCanvas = document.getElementById('cia-canvas');


Particle Physics Implementation

// Mouse force field calculation
const dx = (mouse.x - particle.x);
const dy = (mouse.y - particle.y);
const distance = Math.hypot(dx, dy) || 0.0001;

if (distance < CONFIG.mouseRadius) {
    const force = (CONFIG.mouseRadius - distance) / CONFIG.mouseRadius;
    particle.vx -= (dx / distance) * force * CONFIG.mouseForce;
    particle.vy -= (dy / distance) * force * CONFIG.mouseForce;
}

// Spring return force
particle.vx += (particle.originX - particle.x) * CONFIG.returnForce;
particle.vy += (particle.originY - particle.y) * CONFIG.returnForce;

// Apply damping
particle.vx *= CONFIG.damping;
particle.vy *= CONFIG.damping;


🎨 Visual Customization

Color Schemes

// Galaxy colors
insideColor: '#ff6030'    // Orange center
outsideColor: '#1a73e8'   // Blue edges
centerColor: '#ffffff'    // White core

// Heart particles
hue: i/numHearts * 80 + 280  // Purple to magenta gradient

// CIA text particles
hue: 190 + Math.random() * 40  // Cyan to blue range


Responsive Breakpoints

/* Desktop */
@media (min-width: 769px) {
    font-size: clamp(1em, 4vw, 3em);
}

/* Tablet */
@media (max-width: 768px) {
    font-size: clamp(0.8em, 5vw, 2em);
}

/* Mobile */
@media (max-width: 480px) {
    font-size: clamp(0.6em, 6vw, 1.5em);
}


🐛 Known Limitations
• **Performance**: High particle counts may cause frame drops on older devices
• **Mobile Safari**: Requires user interaction to start WebGL context
• **Firefox**: Minor blend mode rendering differences
• **Memory**: Extended usage may require page refresh on low-memory devices


🤝 Contributing
1. **Fork** the repository
2. **Create** feature branch: `git checkout -b feature/amazing-feature`
3. **Commit** changes: `git commit -m 'Add amazing feature'`
4. **Push** to branch: `git push origin feature/amazing-feature`
5. **Open** Pull Request with detailed description


Development Guidelines
• Maintain 60fps performance target
• Test on mobile devices
• Follow existing code style
• Add comments for complex physics calculations


📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.


🙏 Acknowledgments
• **Three.js Community** - Excellent 3D graphics library
• **MDN Web Docs** - Canvas API documentation
• **Mathematical Curves** - Heart equation implementation
• **WebGL Fundamentals** - Shader optimization techniques


📊 Repository Stats

![GitHub Stars](https://img.shields.io/github/stars/RenzMc/LoveCina?style=social)
![GitHub Forks](https://img.shields.io/github/forks/RenzMc/LoveCina?style=social)
![GitHub Issues](https://img.shields.io/github/issues/RenzMc/LoveCina)
![GitHub License](https://img.shields.io/github/license/RenzMc/LoveCina)
![Last Commit](https://img.shields.io/github/last-commit/RenzMc/LoveCina)


⸻


<div align="center">
  <strong>Made with 💖 and cosmic ✨ energy</strong>
  <br>
  <sub>Where love meets technology in the digital cosmos 🌌</sub>
</div>
```
