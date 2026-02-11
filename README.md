# Generative Art Agent Skills Repository

A comprehensive collection of skills, capabilities, and techniques for creating generative art using three.js, p5.js, and SuperSonic. This repository serves as a knowledge base for AI agents and developers working with creative coding frameworks.

## 📚 Documentation Overview

### [Three.js Skills](./docs/threejs-skills.md)
**3D Graphics and WebGL**

Three.js is the leading 3D graphics library for the web, with 2.7 million weekly NPM downloads. It provides a high-level abstraction over WebGL, making 3D content accessible.

**Key Capabilities:**
- Scene graph management and 3D object hierarchies
- Camera systems (Perspective, Orthographic)
- Lighting (Ambient, Directional, Point, Spot, Hemisphere)
- Materials and textures
- Geometries (primitives, custom, imported models)
- Animation systems
- Post-processing effects
- WebGPU support (production-ready as of 2025)
- VR/XR integration

**Skill Categories:**
- Core Architecture (Scene, Camera, Renderer, Mesh)
- Geometry Creation (Primitives, Custom, BufferGeometry)
- Materials & Textures
- Lighting & Shadows
- Animation & Interaction
- Custom Shaders (GLSL)
- WebGPU Rendering
- Performance Optimization
- Advanced Techniques (Instancing, Post-processing, Physics)

---

### [p5.js Skills](./docs/p5js-skills.md)
**Creative Coding and 2D/3D Graphics**

p5.js is a JavaScript library that makes coding accessible for artists, designers, and beginners. Built on Processing's philosophy of "sketching with code."

**Key Capabilities:**
- 2D drawing primitives and shapes
- 3D graphics with WebGL mode
- Image processing and manipulation
- Typography and text rendering
- Audio visualization and synthesis (p5.sound)
- Webcam and video integration
- Mouse, keyboard, and touch interaction
- DOM manipulation
- Data visualization
- Machine learning integration (ml5.js)

**Skill Categories:**
- Core Drawing (Canvas, Shapes, Curves)
- Styling (Color, Stroke, Fill)
- Typography
- Image & Media (Images, Video, Pixels)
- Animation & Transformations
- Interaction (Mouse, Keyboard, Touch)
- Mathematics (Vectors, Noise, Randomness)
- Object-Oriented Patterns
- 3D Graphics (WebGL mode)
- Audio (Playback, Analysis, Synthesis)
- Data & File Operations
- Performance Optimization
- Generative Art Techniques

---

### [SuperSonic Skills](./docs/supersonic-skills.md)
**Professional Web Audio Synthesis**

SuperSonic brings SuperCollider's scsynth audio engine to web browsers via WebAssembly and AudioWorklet. Created by Sam Aaron (Sonic Pi creator), it provides professional-grade synthesis with zero installation.

**Key Technology:**
- AudioWorklet for high-priority audio thread
- WebAssembly (scsynth compiled to WASM)
- OSC (Open Sound Control) API
- Zero configuration via CDN
- Optional SharedArrayBuffer mode for ultra-low latency

**Key Capabilities:**
- Real-time audio synthesis
- Sample playback and manipulation
- Pre-built synth definitions from Sonic Pi
- Custom synth definition support
- Sample-accurate timing with OSC bundles
- Effects processing (reverb, delay, filters)
- Performance monitoring and optimization
- Browser-native with no plugins required

**Skill Categories:**
- Initialization & Setup
- Synth Definition Management
- Triggering & Controlling Synths
- Sample Playback
- Timing & Sequencing
- Effects & Processing
- Performance Monitoring
- Musical Theory Integration
- Browser Integration
- Advanced Techniques (Generative, Live Coding)

---

## 🎯 Purpose

This repository serves as a comprehensive skill library for AI agents and developers creating generative art. Each framework documentation includes:

- **Detailed skill breakdowns** - Organized by capability area
- **Code examples** - Practical patterns and recipes
- **Sub-skills** - Granular technique descriptions
- **Learning resources** - Official docs, tutorials, community links
- **Integration patterns** - How to combine frameworks
- **Best practices** - Performance, optimization, and professional development

---

## 🚀 Getting Started

### Three.js
```bash
npm install three
```
```javascript
import * as THREE from 'three';
// Create scene, camera, renderer...
```

### p5.js
```html
<script src="https://cdn.jsdelivr.net/npm/p5@1.9.0/lib/p5.js"></script>
```
```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}
```

### SuperSonic
```javascript
import {SuperSonic} from 'https://unpkg.com/supersonic-scsynth@latest';

const sonic = new SuperSonic();
await sonic.init();
await sonic.loadSynthDef('sonic-pi-beep');

sonic.send('/s_new', 'sonic-pi-beep', -1, 0, 0, 'note', 60);
```

---

## 📦 Framework Comparison

| Framework | Primary Use | Rendering | Audio | Learning Curve | Best For |
|-----------|-------------|-----------|-------|----------------|----------|
| **Three.js** | 3D Graphics | WebGL/WebGPU | Basic (Web Audio) | Medium | 3D scenes, games, XR experiences |
| **p5.js** | Creative Coding | Canvas/WebGL | p5.sound library | Low | Sketches, 2D art, education, prototyping |
| **SuperSonic** | Audio Synthesis | N/A | Professional scsynth | Medium | Music, sound design, audio-visual sync |

---

## 🔗 Integration Examples

### Three.js + SuperSonic
3D visuals synchronized with professional audio synthesis:
```javascript
// Audio triggers 3D animations
sonic.send('/s_new', 'sonic-pi-beep', -1, 0, 0, 'note', note);
cube.scale.set(1.5, 1.5, 1.5); // Visual feedback
```

### p5.js + SuperSonic
Creative coding with powerful audio:
```javascript
function mousePressed() {
  const note = map(mouseX, 0, width, 48, 84);
  sonic.send('/s_new', 'sonic-pi-prophet', -1, 0, 0, 'note', note);
}
```

### Three.js + p5.js
Combine 3D rendering with p5's ease-of-use:
```javascript
// Use p5 for UI/2D overlays, Three.js for 3D content
```

---

## 📚 Resources

### Official Documentation
- [Three.js](https://threejs.org/docs)
- [p5.js Reference](https://p5js.org/reference/)
- [SuperSonic GitHub](https://github.com/samaaron/supersonic)

### Learning Paths
- **Three.js:** Three.js Journey, Three.js Fundamentals
- **p5.js:** The Coding Train, p5.js Tutorials, Nature of Code
- **SuperSonic:** Sonic Pi Tutorial, SuperCollider docs, OSC specification

### Community
- Three.js Discord & Forum
- p5.js Forum & OpenProcessing
- Sonic Pi Community & SuperCollider Forum

---

## 🤝 Contributing

This is a living knowledge base. Contributions are welcome:

1. Fork the repository
2. Add new skills, examples, or corrections
3. Update documentation with latest framework features
4. Submit pull requests

---

## 📄 License

Documentation: MIT License

**Framework Licenses:**
- Three.js: MIT
- p5.js: LGPL 2.1
- SuperSonic: MIT (client) / GPL-3.0 (core engine)

---

## 🎨 Built for AI Agents

This repository is specifically designed to help AI agents understand and leverage generative art frameworks. The structured skill breakdowns enable:

- **Capability discovery** - What's possible with each framework
- **Code generation** - Detailed examples and patterns
- **Decision making** - When to use which framework
- **Integration strategies** - Combining frameworks effectively

---

**Last Updated:** February 2026  
**Maintainer:** AI Agent Knowledge Base Project