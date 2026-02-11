# Three.js Skills & Capabilities

## Overview

Three.js is the dominant 3D library for the web, with 2.7 million NPM downloads per week. It abstracts WebGL complexity to make 3D content accessible on webpages.

**Official Site:** https://threejs.org  
**Documentation:** https://threejs.org/docs  
**Examples:** https://threejs.org/examples

---

## Core Architecture Skills

### 1. Scene Graph Management

**Skill: Building Scene Hierarchies**
- Create and manage `THREE.Scene()` as root container
- Organize objects in parent-child relationships
- Control visibility, transformations, and inheritance
- Set scene properties (background, fog, environment)

**Sub-skills:**
- Scene graph traversal and manipulation
- Object grouping with `THREE.Group()`
- Hierarchical transformations (position, rotation, scale)
- Layer-based rendering for selective visibility

### 2. Camera Systems

**Skill: Perspective Camera Control**
- Configure `PerspectiveCamera(fov, aspect, near, far)`
- Position and orient cameras in 3D space
- Implement camera movement and animations
- Handle aspect ratio changes and responsive rendering

**Sub-skills:**
- Field of view (FOV) adjustments for zoom effects
- Near/far clipping plane optimization
- Camera look-at targeting
- Viewport frustum calculations

**Skill: Alternative Camera Types**
- Orthographic cameras for isometric/UI views
- Array cameras for multi-viewport rendering
- Stereo cameras for VR experiences
- Cube cameras for environment mapping

### 3. Rendering Pipeline

**Skill: WebGL Renderer Configuration**
- Initialize `WebGLRenderer` with optimal settings
- Configure antialiasing, alpha, and pixel ratio
- Manage render loops and frame timing
- Handle canvas resizing and device pixel density

**Sub-skills:**
- Shadow map configuration and quality settings
- Tone mapping for HDR rendering
- Output encoding (sRGB, linear)
- Performance profiling and optimization
- Multiple render target (MRT) usage

---

## Geometry Skills

### 4. Primitive Geometries

**Skill: Built-in Geometry Creation**
- BoxGeometry, SphereGeometry, CylinderGeometry
- PlaneGeometry, CircleGeometry, RingGeometry
- TorusGeometry, TorusKnotGeometry, ConeGeometry
- IcosahedronGeometry, OctahedronGeometry, TetrahedronGeometry

**Sub-skills:**
- Parameter tuning (segments, radius, detail levels)
- UV mapping understanding for textures
- Geometry merging for performance
- Buffer geometry conversion

### 5. Custom Geometry Construction

**Skill: BufferGeometry Programming**
- Create custom geometries from vertices
- Define vertex attributes (position, normal, UV, color)
- Build indexed vs non-indexed geometry
- Compute vertex normals and tangents

**Sub-skills:**
- Typed array management (Float32Array, Uint16Array)
- Instanced geometry for repeated objects
- Dynamic geometry updates
- Memory-efficient attribute handling
- Morph targets for animations

### 6. Procedural Modeling

**Skill: Parametric Geometry Generation**
- LatheGeometry from 2D profiles
- ExtrudeGeometry from 2D shapes
- TubeGeometry along curves
- ParametricGeometry with custom functions

**Sub-skills:**
- Shape and path construction
- Extrude settings (depth, bevel, steps)
- Curve generation (splines, Bezier, Catmull-Rom)
- Procedural terrain and landscapes

---

## Material Skills

### 7. Standard Materials

**Skill: PBR Material Configuration**
- MeshStandardMaterial (metallic-roughness workflow)
- MeshPhysicalMaterial (advanced PBR)
- Configure albedo, metalness, roughness maps
- Implement clearcoat, sheen, transmission effects

**Sub-skills:**
- Texture map application (diffuse, normal, displacement)
- Material property animation
- Environment mapping and IBL
- Subsurface scattering simulation
- Anisotropic reflections

### 8. Special-Purpose Materials

**Skill: Specialized Material Usage**
- MeshBasicMaterial for unlit surfaces
- MeshLambertMaterial for diffuse-only lighting
- MeshPhongMaterial for specular highlights
- MeshToonMaterial for cel-shading
- MeshNormalMaterial for debugging
- MeshDepthMaterial for depth rendering

**Sub-skills:**
- Wireframe rendering
- Double-sided materials
- Transparency and alpha blending
- Material blending modes
- Vertex colors integration

### 9. Shader Materials

**Skill: Custom Shader Development**
- ShaderMaterial for full GLSL control
- RawShaderMaterial for minimal overhead
- Write vertex and fragment shaders
- Pass uniforms and attributes to shaders

**Sub-skills:**
- GLSL syntax and built-in functions
- Shader debugging techniques
- Uniform value passing and animation
- Texture sampling in shaders
- Screen-space effects
- Noise functions and procedural textures

---

## Lighting Skills

### 10. Light Types and Configuration

**Skill: Scene Lighting Design**
- AmbientLight for global illumination
- DirectionalLight for sun-like lighting
- PointLight for omni-directional sources
- SpotLight for focused beams
- HemisphereLight for sky/ground lighting
- RectAreaLight for area sources

**Sub-skills:**
- Light intensity and color tuning
- Shadow casting configuration
- Light helpers for debugging
- HDR environment lighting
- Light probes for indirect lighting

### 11. Shadow Systems

**Skill: Shadow Map Implementation**
- Enable shadow casting and receiving
- Configure shadow map resolution
- Adjust shadow camera frustum
- Optimize shadow bias and radius

**Sub-skills:**
- PCF (Percentage Closer Filtering) shadows
- VSM (Variance Shadow Maps)
- Cascaded shadow maps for large scenes
- Contact shadows for detail
- Shadow map debugging

---

## Animation Skills

### 12. Object Animation

**Skill: Transform Animation**
- Animate position, rotation, scale over time
- Use requestAnimationFrame for smooth loops
- Implement easing functions
- Synchronize animations with delta time

**Sub-skills:**
- Quaternion-based rotation interpolation
- Curve-based motion paths
- Physics-based animation
- Spring dynamics and damping

### 13. Skeletal Animation

**Skill: Rigged Character Animation**
- Load and configure SkeletonHelper
- Play animation clips from loaded models
- Blend between animation states
- Control animation speed and looping

**Sub-skills:**
- Bone hierarchy management
- Inverse kinematics (IK)
- Animation mixer usage
- Morph target blending
- Animation retargeting

### 14. Animation System

**Skill: Three.js Animation Framework**
- AnimationMixer for managing clips
- AnimationClip creation and editing
- KeyframeTrack for property animation
- AnimationAction for playback control

**Sub-skills:**
- Time scaling and warping
- Cross-fading between clips
- Event triggering during playback
- Custom interpolation modes

---

## Texture & Asset Skills

### 15. Texture Loading and Management

**Skill: Texture Integration**
- TextureLoader for image loading
- Configure texture wrapping (repeat, clamp, mirror)
- Set texture filtering (nearest, linear, mipmap)
- Handle texture transformations (offset, scale, rotation)

**Sub-skills:**
- Loading manager for asset tracking
- Cube texture loading for skyboxes
- Compressed texture formats (KTX2, DDS)
- Video textures for dynamic content
- Canvas textures for procedural/dynamic updates
- Texture atlas management

### 16. Model Loading

**Skill: 3D Model Import**
- GLTFLoader for modern PBR models
- OBJLoader and MTLLoader for legacy formats
- FBXLoader for complex scenes
- ColladaLoader (DAE) support
- DRACOLoader for compressed geometry

**Sub-skills:**
- Model scale and orientation correction
- Material override and customization
- Animation extraction from models
- LOD (Level of Detail) model swapping
- Model traversal and modification

### 17. HDR and Environment Maps

**Skill: Image-Based Lighting**
- Load HDR environment maps (RGBE, EXR)
- Apply environment maps to scenes
- Generate prefiltered mipmaps
- Use PMREMGenerator for IBL

**Sub-skills:**
- Equirectangular to cubemap conversion
- Environment map intensity control
- Background vs environment separation
- Custom BRDF lookup tables

---

## Interaction Skills

### 18. Raycasting and Object Picking

**Skill: 3D Object Interaction**
- Implement mouse/touch raycasting
- Detect object intersections
- Calculate intersection points and faces
- Handle multiple object selection

**Sub-skills:**
- Screen-to-world coordinate conversion
- Recursive raycasting through hierarchies
- Custom intersection algorithms
- Performance optimization for large scenes
- Bounding volume hierarchies (BVH)

### 19. Camera Controls

**Skill: User Camera Navigation**
- OrbitControls for object inspection
- FlyControls for free movement
- FirstPersonControls for FPS navigation
- TrackballControls for unconstrained rotation
- TransformControls for object manipulation

**Sub-skills:**
- Touch gesture support
- Camera constraint systems
- Smooth camera transitions
- Auto-rotation and damping
- Collision detection for camera

---

## Post-Processing Skills

### 20. Effect Composer Setup

**Skill: Post-Processing Pipeline**
- Configure EffectComposer
- Add RenderPass as base layer
- Chain multiple passes sequentially
- Output final result to screen

**Sub-skills:**
- Render target management
- Multi-pass rendering strategies
- Alpha channel preservation
- Resolution scaling for performance

### 21. Built-in Effects

**Skill: Standard Post-Processing Effects**
- Bloom for glow effects
- Depth of field (DOF) for focus
- SSAO (Screen Space Ambient Occlusion)
- Motion blur
- Film grain and vignette
- Color correction (LUT, brightness, contrast)
- Glitch effects
- Outline and edge detection

**Sub-skills:**
- Effect parameter tuning
- Performance optimization
- Selective object effects
- Custom shader passes
- Temporal antialiasing (TAA)

---

## Performance Skills

### 22. Optimization Techniques

**Skill: Performance Profiling**
- Use Stats.js for FPS monitoring
- Browser DevTools performance analysis
- Identify rendering bottlenecks
- Measure draw calls and triangles

**Sub-skills:**
- Geometry instancing for repeated objects
- Level of Detail (LOD) implementation
- Frustum culling optimization
- Occlusion culling strategies
- Texture compression and atlasing
- Shader complexity reduction
- GPU instancing with InstancedMesh

### 23. Memory Management

**Skill: Resource Lifecycle**
- Dispose geometries, materials, textures
- Remove objects from scene graph
- Clear render targets
- Handle WebGL context loss

**Sub-skills:**
- Object pooling for reusable objects
- Lazy loading strategies
- Texture streaming and pagination
- Memory leak detection and prevention

---

## Advanced Rendering Skills

### 24. Custom Render Pipelines

**Skill: Multi-Pass Rendering**
- Render to texture (RTT) techniques
- Deferred rendering setup
- Multiple render targets
- Ping-pong buffer techniques

**Sub-skills:**
- G-buffer construction
- Light accumulation passes
- Screen-space reflections (SSR)
- Volume rendering
- Procedural generation in shaders

### 25. VR and AR Integration

**Skill: Immersive Experiences**
- WebXR integration
- VR camera rig setup
- Controller input handling
- AR hit testing and anchors

**Sub-skills:**
- Stereoscopic rendering
- Gaze-based interaction
- Hand tracking
- Spatial audio integration
- Performance optimization for mobile VR

---

## Particle & Physics Skills

### 26. Particle Systems

**Skill: Point Cloud and Particles**
- Points/PointsMaterial for particle rendering
- Sprite-based particles
- GPU particle systems
- Particle emitters and lifetime management

**Sub-skills:**
- Custom particle shaders
- Texture atlases for particle sprites
- Particle physics simulation
- Instanced particle rendering
- Billboard orientation

### 27. Physics Integration

**Skill: Physics Simulation**
- Integrate Cannon.js or Ammo.js
- Synchronize Three.js objects with physics bodies
- Implement collision detection
- Apply forces and constraints

**Sub-skills:**
- Rigid body dynamics
- Soft body simulation
- Cloth physics
- Ragdoll systems
- Constraint solvers

---

## Utility Skills

### 28. Scene Management

**Skill: Scene Organization**
- Layer-based rendering
- Object naming and tagging
- Scene serialization/deserialization
- Scene cloning and instancing

**Sub-skills:**
- Object3D userData for custom properties
- Scene graph searching and filtering
- Dynamic object addition/removal
- Scene state management

### 29. Math and Utilities

**Skill: 3D Mathematics**
- Vector3 operations
- Matrix4 transformations
- Quaternion rotations
- Euler angle conversions
- Ray, Plane, Box3, Sphere utilities

**Sub-skills:**
- Coordinate system conversions
- Interpolation (lerp, slerp)
- Bounding box calculations
- Frustum geometry
- Projection and unprojection

### 30. Debugging and Visualization

**Skill: Development Tools**
- AxesHelper for coordinate visualization
- GridHelper for spatial reference
- CameraHelper for camera frustum
- DirectionalLightHelper, SpotLightHelper
- SkeletonHelper for bones
- BoxHelper, Box3Helper for bounds

**Sub-skills:**
- Custom helper creation
- Performance monitoring overlays
- Shader debugging techniques
- Console logging for scene inspection

---

## Integration Skills

### 31. Framework Integration

**Skill: Three.js in Modern Frameworks**
- React Three Fiber (R3F) integration
- Vue.js integration
- Svelte integration
- Vanilla JS best practices

**Sub-skills:**
- Component lifecycle management
- State synchronization
- Event handling in frameworks
- SSR considerations
- Hot module replacement

### 32. Build and Deployment

**Skill: Production Optimization**
- Tree-shaking for minimal bundle size
- Code splitting strategies
- Asset optimization and CDN usage
- Progressive loading

**Sub-skills:**
- Webpack/Vite configuration
- Dynamic imports for large scenes
- Service worker caching
- Performance budgeting

---

## Creative Coding Skills

### 33. Generative Art

**Skill: Procedural Content Generation**
- Noise-based geometry modification
- Fractal and recursive structures
- Algorithmic pattern generation
- Particle-based artworks

**Sub-skills:**
- Simplex/Perlin noise implementation
- L-systems for organic forms
- Cellular automata visualization
- Flow field particle systems

### 34. Audio Visualization

**Skill: Music-Reactive Graphics**
- Web Audio API integration
- FFT analysis for frequency data
- Waveform visualization
- Beat detection and sync

**Sub-skills:**
- Real-time audio processing
- Frequency-based material modulation
- Audio-driven animations
- 3D spectrum analyzers

---

## Reference Resources

**Learning Resources:**
- Three.js Journey: https://threejs-journey.com/
- Three.js Manual: https://threejs.org/manual/
- Discover Three.js: https://discoverthreejs.com/

**Community:**
- Three.js Forum: https://discourse.threejs.org/
- GitHub: https://github.com/mrdoob/three.js
- Discord: Official Three.js community

**Key Statistics:**
- 2.7M weekly NPM downloads (2026)
- 270x more popular than competitors
- Active development since 2010
- 100k+ stars on GitHub
