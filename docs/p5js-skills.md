# p5.js Skills & Capabilities

## Overview

p5.js is a JavaScript library for creative coding that makes coding accessible for artists, designers, educators, and beginners. Built on Processing's philosophy of "sketching with code," it brings the power of Processing to the web.

**Official Site:** https://p5js.org  
**Reference:** https://p5js.org/reference/  
**Web Editor:** https://editor.p5js.org  
**Examples:** https://p5js.org/examples/

---

## Core Drawing Skills

### 1. Canvas and Setup

**Skill: Sketch Initialization**
- `createCanvas(width, height)` for drawing surface
- `setup()` function runs once at start
- `draw()` function loops continuously
- Control frame rate with `frameRate(fps)`

**Sub-skills:**
- Canvas sizing and responsive design
- WebGL mode with `createCanvas(w, h, WEBGL)`
- Multiple canvas creation and management
- Pixel density handling for retina displays
- `noLoop()` and `loop()` for animation control
- `redraw()` for manual frame rendering

### 2. Basic Shapes

**Skill: 2D Primitive Drawing**
- `ellipse(x, y, w, h)` and `circle(x, y, d)`
- `rect(x, y, w, h)` and `square(x, y, s)`
- `triangle(x1, y1, x2, y2, x3, y3)`
- `line(x1, y1, x2, y2)`
- `point(x, y)`
- `arc(x, y, w, h, start, stop)`
- `quad()` for quadrilaterals

**Sub-skills:**
- `rectMode()` and `ellipseMode()` for anchor points
- Corner rounding with optional parameters
- Arc modes: OPEN, CHORD, PIE
- Shape alignment and positioning strategies

### 3. Custom Shapes and Curves

**Skill: Vertex-Based Drawing**
- `beginShape()` and `endShape(CLOSE)`
- `vertex(x, y)` for polygon points
- `curveVertex()` for smooth curves
- `bezierVertex()` for Bezier curves
- `quadraticVertex()` for quadratic curves

**Sub-skills:**
- Shape modes: POINTS, LINES, TRIANGLES, TRIANGLE_FAN, QUADS
- Contour creation with `beginContour()` and `endContour()`
- Curve tightness control
- Bezier and curve tangent calculations

**Skill: Curve Drawing**
- `bezier()` for cubic Bezier curves
- `curve()` for Catmull-Rom splines
- Control point manipulation
- `bezierPoint()` and `curvePoint()` for point calculation along curves

---

## Styling Skills

### 4. Color Management

**Skill: Color Creation and Application**
- `fill()` for shape fill color
- `stroke()` for outline color
- `background()` for canvas background
- `color()` for color object creation

**Sub-skills:**
- RGB, HSB, HSL color modes with `colorMode()`
- Alpha transparency
- `noFill()` and `noStroke()` for style removal
- Color interpolation with `lerpColor()`
- Color extraction with `red()`, `green()`, `blue()`, `hue()`, `saturation()`, `brightness()`

**Skill: Advanced Color Techniques**
- Gradient creation with vertex colors
- Color palette generation
- Complementary and analogous color schemes
- Color blending modes with `blendMode()`

### 5. Stroke and Fill Properties

**Skill: Line Styling**
- `strokeWeight()` for line thickness
- `strokeCap()` for line endings (ROUND, SQUARE, PROJECT)
- `strokeJoin()` for corner styles (MITER, BEVEL, ROUND)
- Dashed lines (not built-in, requires custom implementation)

---

## Typography Skills

### 6. Text Rendering

**Skill: Basic Text Drawing**
- `text(str, x, y)` for text display
- `textSize()` for font size
- `textFont()` for font selection
- `loadFont()` for custom font loading

**Sub-skills:**
- Text alignment with `textAlign()` (LEFT, CENTER, RIGHT, TOP, BOTTOM)
- Text leading (line spacing) with `textLeading()`
- Text styling with `textStyle()` (NORMAL, ITALIC, BOLD)
- Text bounds calculation with `textWidth()` and `textAscent()/textDescent()`
- Multi-line text handling

**Skill: Advanced Typography**
- Dynamic text sizing and wrapping
- Text on paths
- Animated typography
- Text as texture in WebGL mode

---

## Image & Media Skills

### 7. Image Manipulation

**Skill: Image Loading and Display**
- `loadImage()` for image loading (in preload())
- `image(img, x, y, w, h)` for display
- `imageMode()` for positioning
- Image caching and optimization

**Skill: Pixel Manipulation**
- `loadPixels()` and `updatePixels()` for pixel array access
- `get()` and `set()` for individual pixel operations
- `pixels[]` array manipulation
- Image filtering with `filter()` (BLUR, GRAY, INVERT, THRESHOLD, etc.)

**Sub-skills:**
- Custom image filters
- Pixel-level effects (glitch, mosaic, pixelation)
- Color mapping and remapping
- Image blending and compositing

### 8. Video Integration

**Skill: Video Playback**
- `createVideo()` for video element creation
- `createCapture()` for webcam access
- Video control (play, pause, loop, speed)
- Video as texture in WebGL

**Sub-skills:**
- Frame-by-frame video analysis
- Real-time video effects
- Video export (with external libraries)
- Multiple video sources

---

## Animation & Transformation Skills

### 9. Coordinate Transformations

**Skill: 2D Transformations**
- `translate(x, y)` for position offset
- `rotate(angle)` for rotation
- `scale(x, y)` for scaling
- `shearX()` and `shearY()` for skewing

**Sub-skills:**
- `push()` and `pop()` for transformation state management
- Transformation matrix understanding
- Nested transformations
- `applyMatrix()` for custom transformations
- `resetMatrix()` for matrix reset

### 10. Animation Techniques

**Skill: Frame-Based Animation**
- `frameCount` for frame tracking
- `deltaTime` for time-based animation
- Easing functions (linear, quadratic, cubic, etc.)
- Animation loops and cycles

**Sub-skills:**
- Oscillation with `sin()` and `cos()`
- Smooth interpolation with `lerp()`
- Noise-based animation with `noise()`
- Spring physics simulation
- Particle systems

---

## Interaction Skills

### 11. Mouse Interaction

**Skill: Mouse Input Handling**
- `mouseX` and `mouseY` for position
- `pmouseX` and `pmouseY` for previous position
- `mousePressed()`, `mouseReleased()`, `mouseClicked()` callbacks
- `mouseDragged()` and `mouseMoved()` for movement
- `mouseWheel()` for scroll events

**Sub-skills:**
- Drawing applications
- Hover detection
- Drag and drop
- Mouse velocity calculation
- Click vs. drag differentiation

### 12. Keyboard Interaction

**Skill: Keyboard Input**
- `keyPressed()`, `keyReleased()`, `keyTyped()` callbacks
- `key` and `keyCode` variables
- Modifier key detection (shift, ctrl, alt)
- Text input handling

**Sub-skills:**
- Keyboard-controlled animation
- Text input fields
- Keyboard shortcuts
- Game controls

### 13. Touch Interaction

**Skill: Touch Event Handling**
- `touchStarted()`, `touchMoved()`, `touchEnded()` callbacks
- `touches[]` array for multi-touch
- Touch vs. mouse input abstraction
- Gesture recognition (pinch, swipe, rotate)

---

## Mathematical Skills

### 14. Vector Mathematics

**Skill: p5.Vector Usage**
- Create vectors with `createVector(x, y, z)`
- Vector arithmetic (add, sub, mult, div)
- Vector operations (mag, normalize, limit, setMag)
- Dot product and cross product

**Sub-skills:**
- Physics simulation with vectors
- Velocity and acceleration
- Vector field visualization
- Steering behaviors

### 15. Noise and Randomness

**Skill: Random Number Generation**
- `random()` for uniform distribution
- `randomGaussian()` for normal distribution
- `randomSeed()` for reproducible randomness
- `noise()` for Perlin noise

**Sub-skills:**
- Noise-based terrain generation
- `noiseSeed()` for reproducible noise
- `noiseDetail()` for octave control
- Flow fields with noise
- Random walk algorithms

### 16. Mathematical Utilities

**Skill: Math Helper Functions**
- `map()` for value remapping
- `constrain()` for value clamping
- `lerp()` for linear interpolation
- `dist()` for distance calculation
- `abs()`, `sq()`, `sqrt()`, `pow()`, etc.

**Sub-skills:**
- Trigonometric functions (`sin()`, `cos()`, `tan()`, `atan2()`)
- Angle conversion (`radians()`, `degrees()`)
- Normalization and scaling
- Modulo operations for wrapping

---

## Object-Oriented Patterns

### 17. Class-Based Design

**Skill: Custom Classes**
- ES6 class syntax in p5.js
- Constructor and methods
- Object arrays for multiple instances
- Encapsulation of behavior

**Sub-skills:**
- Particle class design
- Object pooling for performance
- Inheritance and polymorphism
- Static methods and properties

**Skill: Design Patterns**
- Factory pattern for object creation
- Observer pattern for events
- State machines for animation states
- Component-based architecture

---

## 3D Graphics Skills (WebGL Mode)

### 18. 3D Primitives and Camera

**Skill: 3D Shape Creation**
- `box()`, `sphere()`, `cylinder()`, `cone()`, `torus()`
- `plane()` for flat surfaces
- Custom 3D shapes with `beginShape(TRIANGLES)`
- 3D transformations (translate, rotate, scale in 3D)

**Skill: 3D Camera Control**
- `camera()` for custom camera positioning
- `perspective()` and `ortho()` for projection
- `orbitControl()` for interactive camera
- Camera movement and animation

**Sub-skills:**
- 3D coordinate system understanding
- Camera frustum configuration
- First-person and third-person views
- Camera easing and smooth movement

### 19. Lighting and Materials

**Skill: 3D Lighting**
- `ambientLight()` for overall illumination
- `directionalLight()` for sun-like lighting
- `pointLight()` for local light sources
- `spotLight()` for focused illumination

**Skill: Material Properties**
- `ambientMaterial()` for ambient reflection
- `specularMaterial()` for shiny surfaces
- `normalMaterial()` for debugging normals
- `texture()` for surface textures

**Sub-skills:**
- `shininess()` for specular control
- Multiple light sources
- Light color and intensity
- Material-light interaction

### 20. 3D Model Loading

**Skill: External Model Import**
- `loadModel()` for OBJ/STL files
- `model()` for display
- Model transformation and animation
- Texture mapping on imported models

---

## Audio Skills (p5.sound Library)

### 21. Audio Playback

**Skill: Sound File Management**
- `loadSound()` for audio loading
- `play()`, `pause()`, `stop()` for control
- `loop()` for continuous playback
- Volume and pan control

**Sub-skills:**
- Playback rate manipulation
- `jump()` for seeking
- Audio sprite techniques
- Multiple sound playback

### 22. Audio Analysis

**Skill: Audio Visualization**
- `Amplitude` for volume analysis
- `FFT` for frequency analysis
- `Waveform` for time-domain visualization
- Beat detection

**Sub-skills:**
- Spectrum visualization
- Audio-reactive graphics
- Peak detection
- Frequency band analysis

### 23. Audio Synthesis

**Skill: Oscillator Synthesis**
- `Oscillator` for tone generation
- Waveform types (sine, triangle, square, sawtooth)
- Frequency and amplitude control
- Envelope application

**Skill: Advanced Synthesis**
- `PolySynth` for polyphonic synthesis
- `Noise` generators (white, pink, brown)
- `Envelope` for ADSR control
- Audio effects (reverb, delay, filter)

---

## Data & File Operations

### 24. Data Loading

**Skill: External Data Import**
- `loadJSON()` for JSON data
- `loadStrings()` for text files
- `loadTable()` for CSV data
- `loadXML()` for XML data

**Sub-skills:**
- Data parsing and processing
- API integration with `loadJSON(url)`
- Data visualization
- Real-time data updates

### 25. Data Export

**Skill: Saving Output**
- `save()` and `saveCanvas()` for image export
- `saveFrames()` for animation frames
- `saveJSON()`, `saveTable()` for data export
- `saveStrings()` for text export

**Sub-skills:**
- High-resolution image export
- Animation rendering
- Data logging
- Custom file formats

---

## Performance Optimization

### 26. Rendering Optimization

**Skill: Performance Techniques**
- `noSmooth()` to disable anti-aliasing
- Shape batching with `beginShape()`/`endShape()`
- Reduce `draw()` loop complexity
- Conditional rendering based on visibility

**Sub-skills:**
- Object pooling
- Spatial partitioning (quadtree, grid)
- Level of detail (LOD)
- Off-screen rendering with `createGraphics()`

### 27. Memory Management

**Skill: Resource Management**
- Remove unused objects from arrays
- `remove()` for p5.Element cleanup
- Image and sound disposal
- Clear buffers when not needed

---

## Generative Art Techniques

### 28. Algorithmic Design

**Skill: Generative Patterns**
- Grid-based compositions
- Recursive patterns
- L-systems for organic growth
- Cellular automata (Game of Life, etc.)

**Skill: Randomized Layouts**
- Poisson disc sampling for distribution
- Voronoi diagrams
- Delaunay triangulation
- Random tiling and tesselation

### 29. Particle Systems

**Skill: Particle Simulation**
- Particle class with physics
- Emitter systems
- Forces and fields
- Collision detection

**Sub-skills:**
- Flocking behaviors (boids)
- Spring systems
- Attractor/repeller forces
- Particle trails and decay

### 30. Fractal Generation

**Skill: Fractal Drawing**
- Recursive functions for fractals
- Mandelbrot and Julia sets
- Iterated function systems (IFS)
- Fractal trees and plants

---

## DOM Manipulation

### 31. HTML Integration

**Skill: DOM Element Creation**
- `createButton()`, `createSlider()`, `createInput()`
- `createDiv()`, `createP()`, `createImg()`
- `createSelect()` for dropdowns
- Element positioning with `.position()`

**Skill: Event Handling**
- `.mousePressed()` for element clicks
- `.input()` for real-time input changes
- `.changed()` for value changes
- Custom event listeners

**Sub-skills:**
- Dynamic UI generation
- CSS styling with `.style()`
- Element parent-child relationships with `.parent()`
- Element removal with `.remove()`

---

## Advanced Integration

### 32. Library Extensions

**Skill: Third-Party Libraries**
- ml5.js for machine learning
- Matter.js for physics
- Tone.js for advanced audio
- p5.scribble for hand-drawn aesthetics

**Sub-skills:**
- Library import and initialization
- Cross-library integration
- Custom library creation
- Performance considerations with multiple libraries

---

## Learning Resources

### Official Resources
- [p5.js Reference](https://p5js.org/reference/)
- [p5.js Examples](https://p5js.org/examples/)
- [p5.js Tutorials](https://p5js.org/learn/)
- [p5.js Web Editor](https://editor.p5js.org/)

### Community Learning
- [The Coding Train](https://thecodingtrain.com/) - Daniel Shiffman's video tutorials
- [OpenProcessing](https://openprocessing.org/) - Community sketches
- [p5.js Forum](https://discourse.processing.org/c/p5js/10)

### Books
- "The Nature of Code" by Daniel Shiffman
- "Getting Started with p5.js" by Lauren McCarthy et al.
- "Generative Design" by Benedikt Gross et al.

### Courses
- Kadenze p5.js courses
- Creative Coding on YouTube
- University courses using p5.js

---

## Best Practices

1. **Use preload() for assets:** Load images, fonts, and sounds before setup()
2. **Organize with functions:** Break complex sketches into manageable functions
3. **Comment your code:** Creative coding benefits from clear documentation
4. **Optimize for performance:** Profile and optimize slow sections
5. **Responsive design:** Use `windowWidth`/`windowHeight` for responsive canvases
6. **Version control:** Use Git for sketch versioning
7. **Cross-browser testing:** Test on multiple browsers and devices
8. **Accessibility:** Consider color contrast and alternative text
9. **Start simple:** Build complexity incrementally
10. **Learn from examples:** Study and remix community sketches

---

## Common Patterns

### Sketch Template
```javascript
function setup() {
  createCanvas(400, 400);
  // Initialization
}

function draw() {
  background(220);
  // Animation loop
}
```

### Particle System Pattern
```javascript
let particles = [];

function setup() {
  createCanvas(600, 400);
  for (let i = 0; i < 100; i++) {
    particles.push(new Particle());
  }
}

function draw() {
  background(0, 10); // Trail effect
  for (let p of particles) {
    p.update();
    p.show();
  }
}

class Particle {
  constructor() {
    this.pos = createVector(random(width), random(height));
    this.vel = p5.Vector.random2D();
  }
  
  update() {
    this.pos.add(this.vel);
  }
  
  show() {
    circle(this.pos.x, this.pos.y, 5);
  }
}
```

---

**Version Reference:** p5.js 1.9+ (2025-2026)  
**Last Updated:** February 2026