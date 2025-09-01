# CIA SYBAU? 🌌✨

> An interactive cosmic particle experience featuring galaxy animations, heart particles, and dynamic text effects.

![CIA Demo](https://img.shields.io/badge/Status-Live-brightgreen)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Three.js](https://img.shields.io/badge/Three.js-000000?logo=three.js&logoColor=white)

## 🚀 Features

### 🌌 **Galaxy System**
- **80,000+ particles** on desktop, 40,000+ on mobile
- **5-branch spiral galaxy** with realistic physics
- **Dynamic camera movement** following mouse interaction
- **Responsive particle density** based on screen size
- **Color gradient transitions** from center to outer edges

### 💖 **Love Particle System**
- **Heart-shaped particle paths** with mathematical precision
- **32 particle trails** creating flowing heart animations
- **Adaptive sizing** for different screen resolutions
- **Smooth particle following** with realistic physics
- **Glowing effects** with HSL color transitions

### 🎯 **Interactive CIA Text**
- **Particle-based text rendering** with "C I A" spacing
- **Mouse interaction effects** with explosion animations
- **Touch support** for mobile devices
- **Dynamic particle dispersion** on click/touch
- **Floating background particles** for ambient effects
- **Customizable parameters** via exposed API

### ✨ **Visual Effects**
- **Custom cursor trails** with fade animations
- **Multi-layer canvas system** with proper z-indexing
- **Blend modes** for enhanced visual appeal
- **Responsive design** across all device sizes
- **High DPI support** for crisp rendering

## 🛠️ Technical Stack

- **HTML5 Canvas** - Multi-layer rendering system
- **Three.js r128** - 3D galaxy animations
- **Vanilla JavaScript** - Core particle systems
- **CSS3** - Responsive styling and effects
- **WebGL** - Hardware-accelerated rendering

## 📱 Browser Support

| Browser | Desktop | Mobile |
|---------|---------|--------|
| Chrome  | ✅ | ✅ |
| Firefox | ✅ | ✅ |
| Safari  | ✅ | ✅ |
| Edge    | ✅ | ✅ |

## 🎮 Interactions

### Desktop
- **Mouse Movement** - Galaxy camera follows cursor
- **Click** - Explode CIA particles
- **Hover** - Interactive particle displacement

### Mobile
- **Touch** - Trigger particle explosions
- **Swipe** - Create particle trails
- **Responsive** - Optimized particle counts

## ⚡ Performance

### Optimizations
- **Adaptive particle counts** based on device capabilities
- **Efficient canvas clearing** with minimal overdraw
- **RequestAnimationFrame** for smooth 60fps animations
- **Memory management** for particle lifecycle
- **Device pixel ratio** handling for crisp rendering

### System Requirements
- **Minimum**: Modern browser with WebGL support
- **Recommended**: Dedicated GPU for optimal performance
- **Mobile**: iOS 12+ / Android 8+

## 🔧 Configuration

The CIA text system exposes several configuration methods:

```javascript
const ciaSystem = initCIA();

// Adjust transparency
ciaSystem.setClearAlpha(0.1);

// Modify glow intensity
ciaSystem.setGlow(20);

// Change letter spacing
ciaSystem.setLetterGapRatio(0.5);

// Toggle particle density
ciaSystem.setDensity(true);


📁 Project Structure

cia-sybau/
├── index.html          # Main application file
├── README.md          # Project documentation
└── assets/            # (Optional) Additional resources
    ├── screenshots/   # Demo images
    └── docs/         # Extended documentation


🚀 Quick Start
1. **Clone the repository**
```bash
git clone https://github.com/yourusername/cia-sybau.git
cd cia-sybau
```

2. **Open in browser**
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve .

# Or simply open index.html in your browser
```

3. **Experience the magic** ✨


🎨 Customization

Galaxy Parameters

const parameters = {
    count: 80000,           // Particle count
    size: 0.02,            // Particle size
    radius: 3.5,           // Galaxy radius
    branches: 5,           // Spiral arms
    spin: 4,               // Rotation factor
    randomness: 8,         // Particle scatter
    insideColor: '#ff6030', // Center color
    outsideColor: '#1a73e8' // Edge color
};


Heart System Config

const heartConfig = {
    numHearts: 32,         // Particle trails
    heartSize: 180,        // Heart dimensions
    trailLength: 32,       // Trail particles
    animationSpeed: 0.7    // Movement speed
};


🐛 Known Issues
• **High particle counts** may impact performance on older devices
• **Mobile Safari** may require user interaction to start animations
• **Firefox** might show slight rendering differences in blend modes


🤝 Contributing
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


🙏 Acknowledgments
• **Three.js** community for excellent 3D library
• **Canvas API** for powerful 2D rendering capabilities
• **WebGL** for hardware acceleration support
• **Mathematical formulas** for heart curve generation


📊 Stats

![GitHub stars](https://img.shields.io/github/stars/yourusername/cia-sybau?style=social)
![GitHub forks](https://img.shields.io/github/forks/yourusername/cia-sybau?style=social)
![GitHub issues](https://img.shields.io/github/issues/yourusername/cia-sybau)
![GitHub license](https://img.shields.io/github/license/yourusername/cia-sybau)


⸻


<div align="center">
  <strong>Made with ❤️ and lots of ☕</strong>
  <br>
  <sub>Built for the cosmos, optimized for Earth 🌍</sub>
</div>
```
