# Generative Art Agent Skills Repository

A comprehensive collection of skills, capabilities, and techniques for creating generative art using three.js, p5.js, and Sonic Pi. This repository serves as a knowledge base for AI agents and developers working with creative coding frameworks.

## 📚 Documentation Overview

### [Three.js Skills](./docs/threejs-skills.md)
**3D Graphics and WebGL**

Three.js is the leading 3D graphics library for the web, with 2.7 million weekly NPM downloads. It provides a high-level abstraction over WebGL for creating interactive 3D experiences.

**Key Skill Areas:**
- Core Architecture (Scene, Camera, Renderer)
- Geometry Creation (Primitives, Custom, Procedural)
- Materials and Shaders (PBR, Custom GLSL)
- Lighting and Shadows
- Animation Systems (Transform, Skeletal, Keyframe)
- Textures and Asset Loading
- Raycasting and Interaction
- Post-Processing Effects
- Performance Optimization
- VR/AR Integration
- Physics and Particles
- Creative Coding Techniques

**Use Cases:** Web-based 3D games, data visualization, product configurators, architectural walkthroughs, immersive experiences, generative 3D art

---

### [p5.js Skills](./docs/p5js-skills.md)
**Creative Coding and 2D/3D Graphics**

p5.js makes coding accessible for artists, designers, and beginners. Built on Processing's philosophy, it brings creative coding to the web with an emphasis on visual output and interactivity.

**Key Skill Areas:**
- Canvas Drawing (2D Shapes, Curves, Custom Paths)
- Color and Styling
- Typography and Text
- Image and Media (Loading, Manipulation, Pixel Access)
- Video and Camera Integration
- Animation and Transformations
- User Interaction (Mouse, Touch, Keyboard)
- Mathematical Functions (Noise, Random, Vectors)
- Physics Simulation
- Object-Oriented Design
- 3D Graphics (WebGL Mode)
- Audio (Playback, Analysis, Synthesis)
- Data Visualization
- Machine Learning (ml5.js)
- DOM Manipulation

**Use Cases:** Generative art, data visualization, interactive installations, educational tools, visual music, creative sketches, prototyping

---

### [Sonic Pi Skills](./docs/sonic-pi-skills.md)
**Live Coding Music and Sound**

Sonic Pi is a live coding environment for creating music through code. Created by Sam Aaron, it's designed for education, performance, and algorithmic composition with a focus on accessibility and real-time interaction.

**Key Skill Areas:**
- Basic Synthesis (Notes, Synths, Parameters)
- Rhythm and Timing (Loops, BPM, Threading)
- Musical Theory (Scales, Chords, Progressions)
- Sample Playback and Manipulation
- Audio Effects (Reverb, Delay, Filters, Modulation)
- Live Coding Performance
- Control Flow and Algorithms
- MIDI Input/Output
- OSC Communication
- Sound Design (Additive, Subtractive, FM)
- Composition and Arrangement
- Genre-Specific Techniques
- Education and Teaching
- Recording and Export

**Use Cases:** Live coded music performance, algorithmic composition, music education, generative soundscapes, audio-visual installations, club performances (Algorave)

---

## 🎯 Framework Comparison

| Feature | three.js | p5.js | Sonic Pi |
|---------|----------|-------|----------|
| **Primary Domain** | 3D Graphics | 2D/3D Visual Art | Music & Sound |
| **Language** | JavaScript | JavaScript | Ruby |
| **Learning Curve** | Moderate-High | Low-Moderate | Low-Moderate |
| **Real-time Performance** | Yes | Yes | Yes (Live Coding) |
| **Hardware Acceleration** | WebGL | WebGL (optional) | SuperCollider |
| **Best For** | 3D experiences | Visual sketches | Music composition |
| **Community Size** | Very Large | Very Large | Large |
| **Platform** | Web browsers | Web browsers | Desktop (cross-platform) |
| **Education Focus** | Professional | Beginner-friendly | Education-first |

---

## 🚀 Getting Started

### Three.js
```javascript
// Basic scene setup
const scene = new THREE.Scene();
const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
const renderer = new THREE.WebGLRenderer();
renderer.setSize(window.innerWidth, window.innerHeight);
document.body.appendChild(renderer.domElement);

const geometry = new THREE.BoxGeometry();
const material = new THREE.MeshBasicMaterial({ color: 0x00ff00 });
const cube = new THREE.Mesh(geometry, material);
scene.add(cube);

camera.position.z = 5;

function animate() {
    requestAnimationFrame(animate);
    cube.rotation.x += 0.01;
    cube.rotation.y += 0.01;
    renderer.render(scene, camera);
}
animate();
```

**Resources:**
- Official Site: https://threejs.org
- Documentation: https://threejs.org/docs
- Examples: https://threejs.org/examples

---

### p5.js
```javascript
// Basic sketch
function setup() {
    createCanvas(400, 400);
}

function draw() {
    background(220);
    
    // Draw a circle that follows the mouse
    fill(255, 0, 0);
    circle(mouseX, mouseY, 50);
    
    // Animated rotating square
    push();
    translate(width/2, height/2);
    rotate(frameCount * 0.01);
    rectMode(CENTER);
    fill(0, 0, 255);
    square(0, 0, 100);
    pop();
}
```

**Resources:**
- Official Site: https://p5js.org
- Web Editor: https://editor.p5js.org
- Reference: https://p5js.org/reference
- The Coding Train: https://thecodingtrain.com

---

### Sonic Pi
```ruby
# Basic live loop
use_bpm 120

live_loop :drums do
  sample :drum_heavy_kick
  sleep 1
end

live_loop :bass do
  use_synth :tb303
  play :c2, release: 0.5, cutoff: rrand(60, 110)
  sleep 0.5
end

live_loop :melody do
  use_synth :prophet
  play scale(:c4, :minor_pentatonic).choose, release: 0.25
  sleep 0.25
end
```

**Resources:**
- Official Site: https://sonic-pi.net
- GitHub: https://github.com/sonic-pi-net/sonic-pi
- Built-in Tutorial: Included in the application
- Forum: https://in-thread.sonic-pi.net

---

## 🎨 Cross-Framework Integration

### Audio-Visual Combinations

**Sonic Pi + p5.js via OSC**
- Send beat and frequency data from Sonic Pi to p5.js
- Create music-reactive visualizations
- Synchronize visual patterns with audio events

**p5.js + three.js**
- Use p5.js for 2D UI overlays on three.js 3D scenes
- Generate textures in p5.js for three.js materials
- Combine 2D and 3D elements in creative ways

**All Three Together**
- three.js for 3D environment
- p5.js for 2D graphics and data visualization
- Sonic Pi for generative music and audio reactivity
- OSC/WebSockets for real-time communication

---

## 🛠️ Agent Development Guidelines

### For AI Agents Using This Repository

**Skill Selection:**
1. Identify the user's creative goal (3D scene, 2D art, music composition)
2. Select the appropriate framework(s)
3. Reference relevant skill sections for implementation details
4. Combine skills from multiple frameworks when needed

**Code Generation:**
- Use skill documentation as a reference for API usage
- Combine multiple sub-skills for complex effects
- Consider performance implications from optimization sections
- Follow framework-specific best practices

**Error Handling:**
- Reference debugging skills for troubleshooting
- Use helper/visualization skills during development
- Apply performance optimization when needed

**Learning Path:**
- Start with core architecture skills
- Progress to basic creative output
- Add interaction and animation
- Implement advanced techniques
- Optimize for performance

---

## 📖 Skill Categories

### Visual Skills
- Geometry and shape creation
- Color and styling
- Materials and textures
- Lighting and shadows
- Animation and motion
- Effects and post-processing

### Interaction Skills
- Mouse and touch input
- Keyboard control
- Camera navigation
- Object picking and raycasting
- MIDI and OSC communication

### Technical Skills
- Performance optimization
- Memory management
- Asset loading and management
- Audio configuration
- Cross-platform compatibility

### Creative Skills
- Generative algorithms
- Procedural generation
- Algorithmic composition
- Audio-visual synchronization
- Live performance techniques

### Mathematical Skills
- Vector mathematics
- Trigonometry and geometry
- Noise and randomness
- Physics simulation
- Signal processing

---

## 🌟 Use Cases by Domain

### Data Visualization
- **p5.js**: Charts, graphs, interactive data exploration
- **three.js**: 3D data landscapes, network visualization, spatial data
- **Sonic Pi**: Sonification, data-driven music

### Education
- **p5.js**: Teaching programming concepts visually
- **Sonic Pi**: Music theory and computational thinking
- **three.js**: 3D geometry and spatial reasoning

### Art & Installation
- **All frameworks**: Interactive gallery installations
- **p5.js + Sonic Pi**: Audio-visual performances
- **three.js**: Immersive VR/AR experiences

### Game Development
- **three.js**: 3D game engines and prototypes
- **p5.js**: 2D games and mechanics testing
- **Sonic Pi**: Procedural game music

### Live Performance
- **Sonic Pi**: Algorave and live coded music
- **p5.js**: VJ visuals and real-time graphics
- **three.js**: 3D environments for performances

---

## 🤝 Contributing

This repository is designed as a living knowledge base. Contributions are welcome:

- Add new skills and techniques
- Update existing documentation
- Provide code examples
- Share use cases and patterns
- Report errors or outdated information

---

## 📝 License

This documentation is provided as a reference for the generative art community. Individual frameworks have their own licenses:

- **three.js**: MIT License
- **p5.js**: LGPL License  
- **Sonic Pi**: MIT License

---

## 🔗 Additional Resources

### Communities
- **three.js**: [Discourse Forum](https://discourse.threejs.org)
- **p5.js**: [Processing Forum](https://discourse.processing.org/c/p5js)
- **Sonic Pi**: [In-Thread Forum](https://in-thread.sonic-pi.net)

### Learning Platforms
- **The Coding Train** (p5.js, three.js)
- **Three.js Journey** (three.js)
- **Sonic Pi Tutorial** (built-in)
- **OpenProcessing** (p5.js community sketches)

### Related Technologies
- **ml5.js**: Machine learning for creative coding
- **Tone.js**: Advanced web audio framework
- **matter.js**: 2D physics engine
- **SuperCollider**: Audio synthesis platform (Sonic Pi's engine)

---

**Repository maintained for AI agent skill development and generative art creation**

Last Updated: February 2026