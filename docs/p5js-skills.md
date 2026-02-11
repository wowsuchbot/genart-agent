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
- Bezier and curve tangent calculations
- Custom shape libraries and templates

---

## Styling Skills

### 4. Color and Fill

**Skill: Color Management**
- `fill(r, g, b, [a])` for shape interiors
- `stroke(r, g, b, [a])` for outlines
- `noFill()` and `noStroke()`
- `background(color)` for canvas clearing
- Color modes: RGB, HSB with `colorMode()`

**Sub-skills:**
- Alpha transparency control
- Color object creation with `color()`
- Color interpolation with `lerpColor()`
- Palette generation and management
- Hex and named color support
- Hue, saturation, brightness manipulation

### 5. Stroke and Style Properties

**Skill: Line Styling**
- `strokeWeight(pixels)` for line thickness
- `strokeCap(mode)` - SQUARE, PROJECT, ROUND
- `strokeJoin(mode)` - MITER, BEVEL, ROUND
- Dashed lines patterns

**Sub-skills:**
- Gradient simulation techniques
- Pattern fills with custom functions
- Texture-based fills

---

## Typography Skills

### 6. Text Rendering

**Skill: Text Display**
- `text(str, x, y, [w, h])` for rendering
- `textSize(pixels)` for font size
- `textFont(font)` for font selection
- `loadFont(path)` for custom fonts
- `textAlign(horizAlign, [vertAlign])`

**Sub-skills:**
- Text metrics: `textWidth()`, `textAscent()`, `textDescent()`
- Text leading (line spacing) with `textLeading()`
- Text bounds calculation
- Dynamic text sizing and wrapping
- Loading web fonts and Google Fonts
- Unicode and emoji support

### 7. Advanced Typography

**Skill: Text Manipulation**
- Character-by-character access
- Text along paths
- Kinetic typography
- Text deformation and effects

**Sub-skills:**
- Font outline extraction
- Text as particles or shapes
- 3D text in WebGL mode
- Responsive text scaling
- Text animation timing

---

## Image & Media Skills

### 8. Image Loading and Display

**Skill: Image Integration**
- `loadImage(path)` in `preload()`
- `image(img, x, y, [w, h])` for display
- `tint(color, [alpha])` for color overlay
- `imageMode()` for positioning

**Sub-skills:**
- Image resizing and scaling
- Image cropping with additional parameters
- Animated GIF support
- Image blending modes
- Copy and paste regions with `copy()`

### 9. Pixel Manipulation

**Skill: Low-Level Image Processing**
- `loadPixels()` and `updatePixels()`
- Direct pixel array access
- `get(x, y)` for pixel color reading
- `set(x, y, color)` for pixel writing

**Sub-skills:**
- Image filters: BLUR, GRAY, THRESHOLD, INVERT, POSTERIZE
- Custom filter algorithms
- Pixel sorting and glitch effects
- Convolution kernels
- Real-time video pixel manipulation
- Edge detection and computer vision

### 10. Video and Camera

**Skill: Video Integration**
- `createCapture(VIDEO)` for webcam
- `createVideo(src)` for video files
- Video playback control: play, pause, loop
- Video pixel access for effects

**Sub-skills:**
- Multiple camera source selection
- Video speed and time control
- Video as texture in WebGL
- Frame differencing for motion detection
- Green screen / chroma key effects

---

## Animation Skills

### 11. Motion and Timing

**Skill: Animation Fundamentals**
- Use `frameCount` for time-based motion
- `millis()` for elapsed time
- Velocity and acceleration patterns
- Easing functions (linear, quadratic, sine)

**Sub-skills:**
- Delta time for frame-rate independence
- Animation looping and cycles
- State machine animation
- Timeline-based sequencing
- Tweening libraries integration

### 12. Transformation System

**Skill: Coordinate Transformations**
- `translate(x, y)` for position offset
- `rotate(angle)` for rotation
- `scale(x, [y])` for sizing
- `push()` and `pop()` for transformation stacks

**Sub-skills:**
- Rotation around custom pivot points
- Nested transformations for hierarchies
- Matrix transformations with `applyMatrix()`
- Isometric and axonometric projections
- Transformation debugging techniques

---

## Interaction Skills

### 13. Mouse and Touch Input

**Skill: User Input Handling**
- `mouseX` and `mouseY` for position
- `pmouseX` and `pmouseY` for previous position
- `mouseIsPressed` for state checking
- `mousePressed()`, `mouseReleased()`, `mouseClicked()` callbacks
- `mouseDragged()` and `mouseMoved()` for motion

**Sub-skills:**
- Mouse button detection with `mouseButton`
- Touch event handling: `touchStarted()`, `touchMoved()`, `touchEnded()`
- Multi-touch with `touches[]` array
- Drawing applications (paint, sketch)
- Gesture recognition
- Mouse velocity calculation

### 14. Keyboard Input

**Skill: Keyboard Interaction**
- `keyPressed()` and `keyReleased()` callbacks
- `key` for character value
- `keyCode` for special keys
- `keyIsPressed` for state

**Sub-skills:**
- Modifier key detection (shift, ctrl, alt)
- Key combination handling
- Text input capture
- Keyboard-controlled animations
- Accessibility considerations

---

## Mathematical Skills

### 15. Math Functions and Utilities

**Skill: Mathematical Operations**
- `map(value, start1, stop1, start2, stop2)` for range conversion
- `constrain(n, low, high)` for clamping
- `lerp(start, stop, amt)` for interpolation
- `dist(x1, y1, x2, y2)` for distance
- `norm(value, start, stop)` for normalization

**Sub-skills:**
- Trigonometric functions: `sin()`, `cos()`, `tan()`, `atan2()`
- Angle conversion: `radians()`, `degrees()`
- Random number generation: `random()`, `randomGaussian()`
- Noise generation: `noise()` (Perlin noise)
- Vector mathematics with `p5.Vector`

### 16. Noise and Randomness

**Skill: Procedural Generation**
- `random([min], [max])` for uniform distribution
- `randomSeed(seed)` for reproducible randomness
- `noise(x, [y], [z])` for smooth noise
- `noiseSeed(seed)` for reproducible noise
- `noiseDetail(lod, falloff)` for noise customization

**Sub-skills:**
- 1D, 2D, 3D noise applications
- Noise-based terrain generation
- Organic motion with noise
- Random distribution strategies
- Probability-weighted selection

---

## Vector Mathematics Skills

### 17. p5.Vector Fundamentals

**Skill: Vector Operations**
- `createVector(x, y, [z])` for creation
- Vector arithmetic: `add()`, `sub()`, `mult()`, `div()`
- `mag()` for magnitude, `normalize()` for unit vectors
- `dot()` and `cross()` products
- `heading()` for angle extraction

**Sub-skills:**
- Vector distance with `dist()`
- Vector interpolation with `lerp()`
- Vector rotation and angle calculation
- Velocity and acceleration vectors
- Force accumulation patterns

### 18. Physics Simulation

**Skill: Motion Physics**
- Implement velocity and acceleration
- Apply forces (gravity, friction, drag)
- Collision detection and response
- Particle systems and emitters

**Sub-skills:**
- Spring forces and oscillation
- Gravitational attraction
- Steering behaviors (seek, flee, arrive)
- Flocking and boids algorithms
- Verlet integration
- Constraint systems

---

## Object-Oriented Skills

### 19. Class-Based Design

**Skill: OOP in p5.js**
- Create custom classes for entities
- Constructor patterns
- Method encapsulation
- Array-based object management

**Sub-skills:**
- Inheritance and polymorphism
- Object pooling for performance
- Factory patterns
- Component-based architecture
- State management in objects

### 20. Particle Systems

**Skill: Particle System Design**
- Particle class creation
- Emitter systems
- Particle lifecycle management
- Force application to particles

**Sub-skills:**
- Different particle behaviors
- Particle attractors and repellers
- Trail and fade effects
- Particle collision systems
- GPU-accelerated particles (WebGL)

---

## 3D Graphics Skills (WebGL Mode)

### 21. 3D Primitives and Modeling

**Skill: 3D Shape Creation**
- `box(size)`, `sphere(radius)`, `cylinder(radius, height)`
- `cone()`, `torus()`, `plane()`
- Custom 3D geometry with vertices
- Model loading with `loadModel()`

**Sub-skills:**
- 3D transformation stacking
- Camera control: `camera()`, `perspective()`, `ortho()`
- `orbitControl()` for mouse camera
- Normal and texture coordinate specification
- OBJ and STL file loading

### 22. 3D Lighting and Materials

**Skill: 3D Scene Lighting**
- `ambientLight(r, g, b)` for global illumination
- `directionalLight(r, g, b, x, y, z)` for sun
- `pointLight(r, g, b, x, y, z)` for omni lights
- `spotLight()` for focused beams
- Material properties: `ambientMaterial()`, `specularMaterial()`, `shininess()`

**Sub-skills:**
- Normal material visualization
- Texture mapping in 3D
- Custom shaders in WebGL mode
- Light positioning strategies
- Multiple light source management

### 23. 3D Textures and Shaders

**Skill: Advanced 3D Rendering**
- `texture(img)` for surface textures
- Normal maps for detail
- Custom GLSL shaders with `createShader()`
- Shader uniforms and attributes

**Sub-skills:**
- UV mapping techniques
- Shader-based effects (distortion, displacement)
- Post-processing in 3D
- Framebuffer objects
- Render to texture techniques

---

## Audio Skills

### 24. Sound Playback

**Skill: p5.sound Library**
- `loadSound(path)` in preload
- `play()`, `pause()`, `stop()` control
- `loop()` and `setLoop()` for repetition
- Volume and pan control
- Playback rate manipulation

**Sub-skills:**
- Sound file format support (MP3, WAV, OGG)
- Multiple simultaneous sounds
- Sound callbacks and events
- Audio sprite techniques
- Spatial audio (3D sound)

### 25. Audio Analysis

**Skill: Sound Visualization**
- `p5.Amplitude` for volume analysis
- `p5.FFT` for frequency analysis
- Waveform visualization
- Spectrum display
- Beat detection

**Sub-skills:**
- Frequency band isolation
- Real-time audio reactive visuals
- Amplitude envelope following
- Peak detection algorithms
- Audio-driven animation parameters

### 26. Sound Synthesis

**Skill: Generative Audio**
- `p5.Oscillator` for tone generation
- Waveform types: sine, triangle, square, sawtooth
- `p5.Envelope` for ADSR
- `p5.Filter` for frequency shaping
- `p5.Reverb` and `p5.Delay` effects

**Sub-skills:**
- Additive synthesis techniques
- FM (Frequency Modulation) synthesis
- Note sequencing and scheduling
- Polyphonic synthesis
- Audio effect chaining

---

## Data & File Skills

### 27. Loading External Data

**Skill: Data Import**
- `loadJSON(path)` for JSON data
- `loadStrings(path)` for text files
- `loadTable(path)` for CSV/TSV
- `loadXML(path)` for XML data
- Data parsing in `preload()`

**Sub-skills:**
- API data fetching
- Error handling for failed loads
- Asynchronous data with callbacks
- Real-time data updates
- Data caching strategies

### 28. Data Visualization

**Skill: Information Graphics**
- Chart creation (bar, line, scatter)
- Data mapping to visual properties
- Statistical visualization
- Network and graph visualization

**Sub-skills:**
- Scale and axis generation
- Legend and label creation
- Interactive data exploration
- Animated data transitions
- Responsive visualizations
- Geographic data (maps)

### 29. Saving and Export

**Skill: Output Generation**
- `save(filename)` for canvas download
- `saveCanvas(filename, extension)` for PNG/JPG
- `saveFrames()` for animation export
- `saveJSON()`, `saveStrings()`, `saveTable()`

**Sub-skills:**
- High-resolution export
- SVG export for vector graphics
- PDF generation for print
- Batch frame export for video
- Data export formats

---

## Advanced Programming Skills

### 30. Custom Libraries and Addons

**Skill: Library Integration**
- Include external p5.js libraries
- p5.sound for audio
- p5.dom for HTML elements (legacy)
- Community libraries (ml5.js, matter.js, toxiclibs)

**Sub-skills:**
- Library compatibility checking
- Version management
- Creating custom p5.js libraries
- Contributing to p5.js ecosystem

### 31. Machine Learning Integration

**Skill: ml5.js Integration**
- Image classification
- Pose detection (PoseNet)
- Object detection
- Style transfer
- Hand tracking

**Sub-skills:**
- Pre-trained model usage
- Real-time prediction
- Training custom models
- Data collection for ML
- Performance optimization for ML

### 32. DOM Manipulation

**Skill: HTML Element Creation**
- `createDiv()`, `createP()`, `createButton()`
- `createSlider()`, `createInput()` for controls
- Element positioning and styling
- CSS class and ID management

**Sub-skills:**
- Event listeners on DOM elements
- Dynamic UI generation
- Form integration
- Responsive layout with p5.js
- Accessibility attributes

---

## Performance Skills

### 33. Optimization Techniques

**Skill: Performance Tuning**
- Minimize calculations in draw loop
- Object pooling and reuse
- Spatial data structures (quadtree, grid)
- Level of detail (LOD) strategies
- Profiling with browser DevTools

**Sub-skills:**
- Drawing optimization (reduce overdraw)
- Texture atlas usage
- Geometry batching
- Off-screen rendering and caching
- WebGL mode for hardware acceleration
- Worker threads for heavy computation

### 34. Memory Management

**Skill: Resource Efficiency**
- Image and media disposal
- Array management strategies
- Avoiding memory leaks
- Garbage collection awareness

**Sub-skills:**
- Lazy loading techniques
- Asset preloading strategies
- Circular reference avoidance
- Object reference cleanup

---

## Creative Coding Patterns

### 35. Generative Art Techniques

**Skill: Algorithmic Art**
- Fractal generation (Mandelbrot, Julia sets)
- L-systems for organic growth
- Cellular automata (Conway's Game of Life)
- Reaction-diffusion patterns
- Flow fields and vector fields

**Sub-skills:**
- Recursive drawing patterns
- Symmetry and tiling
- Randomized composition
- Emergence and complexity
- Color palette generation

### 36. Simulation and Modeling

**Skill: Natural Phenomena**
- Fluid simulation
- Particle flow systems
- Gravity and planetary motion
- Ecosystem modeling
- Agent-based modeling

**Sub-skills:**
- Differential equations
- Numerical integration methods
- Spatial hashing for collisions
- Behavioral AI (steering, flocking)
- Environmental parameters

---

## Project Patterns

### 37. Interactive Installations

**Skill: Installation Development**
- Fullscreen and immersive modes
- Multi-screen synchronization
- Sensor integration (Arduino, etc.)
- Projection mapping alignment
- Kiosk mode deployment

**Sub-skills:**
- Hardware interfacing
- Network communication (WebSockets)
- State persistence
- Idle state and screensaver
- Reset and maintenance modes

### 38. Mobile and Responsive Design

**Skill: Cross-Device Development**
- Touch optimization
- Device orientation handling
- Responsive canvas sizing
- Mobile performance optimization
- Progressive web app (PWA) setup

**Sub-skills:**
- Accelerometer and gyroscope access
- Mobile browser quirks
- Touch gesture libraries
- Viewport meta tags
- Mobile debugging techniques

---

## Community and Resources

### 39. p5.js Ecosystem

**Learning Resources:**
- The Coding Train (Daniel Shiffman): https://thecodingtrain.com/
- p5.js Tutorials: https://p5js.org/learn/
- Nature of Code: https://natureofcode.com/
- Generative Design: http://www.generative-gestaltung.de/2/

**Community:**
- p5.js Forum: https://discourse.processing.org/c/p5js
- GitHub: https://github.com/processing/p5.js
- OpenProcessing: https://openprocessing.org/
- Editor Community Sketches

**Compatible Libraries:**
- ml5.js (Machine Learning)
- matter.js (Physics)
- Tone.js (Advanced Audio)
- dat.GUI (Interface Controls)

### 40. Best Practices

**Skill: Professional Development**
- Code organization and structure
- Commenting and documentation
- Version control with Git
- Accessibility standards
- Cross-browser testing

**Sub-skills:**
- ES6+ JavaScript features
- Module systems (import/export)
- Build tools (webpack, vite)
- Code linting and formatting
- Performance profiling
- Unit testing creative code

---

## Key Differences from Processing

**JavaScript vs Java:**
- Dynamic typing
- Prototype-based OOP
- Browser APIs available
- Asynchronous programming patterns

**Web-Specific Features:**
- DOM integration
- CSS styling
- Web Audio API
- WebGL acceleration
- Mobile touch events
- Web APIs (geolocation, camera, etc.)

**Philosophy:**
- Accessibility and inclusivity
- Beginner-friendly documentation
- Web-native from the ground up
- Active community contributions
