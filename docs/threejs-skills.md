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
- Shadow map configuration
- Tone mapping for HDR rendering
- Color space management (sRGB, Linear)
- Render target usage for off-screen rendering

---

## Geometry Creation Skills

### 4. Primitive Geometries

**Skill: Built-in Geometry Usage**
- `BoxGeometry`, `SphereGeometry`, `CylinderGeometry`
- `PlaneGeometry`, `TorusGeometry`, `ConeGeometry`
- Parameter control (segments, radius, detail levels)
- Geometry transformation and positioning

**Sub-skills:**
- Segment density for performance vs. quality tradeoffs
- UV mapping for textures on primitives
- Geometry merging for batch rendering

### 5. Custom Geometry

**Skill: BufferGeometry Creation**
- Define vertices with `Float32Array`
- Set attributes (position, normal, uv, color)
- Configure vertex indices for face definitions
- Update geometries dynamically

**Sub-skills:**
- Typed array management for performance
- Attribute interleaving
- Vertex normal calculation
- Dynamic buffer updates with `needsUpdate` flag

**Skill: Procedural Generation**
- Parametric geometry creation
- Noise-based terrain generation
- Mathematical surface definitions
- L-system and fractal structures

### 6. Model Loading

**Skill: External Model Import**
- GLTF/GLB loading (recommended format)
- FBX, OBJ, Collada format support
- Draco compression for optimized models
- Animation extraction from imported models

**Sub-skills:**
- Asset pipeline optimization
- Texture and material preservation
- Scene graph extraction
- Progressive loading for large models

---

## Materials & Texture Skills

### 7. Material Systems

**Skill: PBR Materials (Physical-Based Rendering)**
- `MeshStandardMaterial` - Metallic/roughness workflow
- `MeshPhysicalMaterial` - Advanced properties (clearcoat, transmission)
- Configure metalness, roughness, and environment maps
- IBL (Image-Based Lighting) setup

**Sub-skills:**
- Texture map application (albedo, normal, roughness, metallic, AO)
- Environment map configuration
- Material properties for different surface types
- Anisotropy and sheen for fabric rendering

**Skill: Non-Photorealistic Materials**
- `MeshBasicMaterial` - Unlit rendering
- `MeshLambertMaterial` - Diffuse lighting only
- `MeshPhongMaterial` - Specular highlights
- `MeshToonMaterial` - Cel-shading effects

**Skill: Special Materials**
- `ShaderMaterial` - Custom GLSL shaders
- `RawShaderMaterial` - Full control over vertex/fragment shaders
- `PointsMaterial` - Particle system rendering
- `LineMaterial` - Advanced line rendering

### 8. Texture Mapping

**Skill: Texture Loading and Application**
- Load images with `TextureLoader`
- Apply to material properties
- Configure wrapping modes (repeat, clamp, mirror)
- Set filtering (nearest, linear, mipmaps)

**Sub-skills:**
- UV coordinate manipulation
- Texture transformation (offset, repeat, rotation)
- Canvas textures for dynamic content
- Video textures for animated surfaces
- Cube textures for environment mapping

---

## Lighting & Shadow Skills

### 9. Light Types

**Skill: Ambient and Hemisphere Lighting**
- `AmbientLight` - Uniform scene illumination
- `HemisphereLight` - Sky/ground color gradients
- Configure intensity and color
- Use as base lighting layer

**Skill: Directional Lighting**
- `DirectionalLight` - Parallel rays (sun-like)
- Shadow casting configuration
- Shadow camera setup for optimal coverage
- Light helpers for visualization

**Skill: Point and Spot Lights**
- `PointLight` - Omnidirectional light source
- `SpotLight` - Cone-shaped illumination
- Distance falloff and decay
- Shadow mapping for point/spot lights

**Sub-skills:**
- Light intensity and color temperature
- Multiple light source management
- Performance optimization with light limits
- Baked lighting alternatives

### 10. Shadow System

**Skill: Shadow Configuration**
- Enable shadows on renderer, lights, and objects
- Configure shadow map resolution
- Set shadow camera bounds
- Optimize shadow bias and radius

**Sub-skills:**
- Shadow type selection (Basic, PCF, VSM)
- Shadow acne prevention
- Performance vs. quality tradeoffs
- Shadow baking for static scenes

---

## Animation & Interaction Skills

### 11. Animation System

**Skill: Object Transformation Animation**
- Manual animation in render loop
- Tween libraries integration (GSAP, Tween.js)
- Easing functions and timing control
- Transform interpolation

**Skill: Skeletal Animation**
- `AnimationMixer` for complex animations
- `AnimationClip` and `AnimationAction` management
- Blend between animation states
- Animation blending and crossfades

**Sub-skills:**
- Timeline synchronization
- Keyframe animation
- Morph target animation
- Physics-based animation

### 12. User Interaction

**Skill: Camera Controls**
- `OrbitControls` - Rotate around target
- `TrackballControls` - Free rotation
- `FlyControls` - First-person navigation
- `PointerLockControls` - FPS-style control

**Skill: Object Interaction**
- Raycasting for mouse picking
- Hover and click detection
- Drag and drop in 3D space
- Touch gesture support

**Sub-skills:**
- Ray-object intersection testing
- Screen-to-world coordinate conversion
- Multi-touch handling
- VR controller interaction

---

## Shader Programming Skills

### 13. GLSL Fundamentals

**Skill: Custom Vertex Shaders**
- Vertex position transformation
- Normal and UV passing to fragment shader
- Vertex displacement techniques
- Custom attribute handling

**Skill: Custom Fragment Shaders**
- Color calculation and output
- Texture sampling
- Lighting calculations
- Procedural patterns and noise

**Sub-skills:**
- Uniform passing from JavaScript
- Varying interpolation
- Built-in Three.js shader chunks
- ShaderMaterial configuration

### 14. Advanced Shader Techniques

**Skill: Procedural Textures**
- Noise functions (Perlin, Simplex, Worley)
- Mathematical patterns
- Fractal generation
- Domain warping

**Skill: Post-Processing Shaders**
- Bloom and glow effects
- Color grading and correction
- Depth of field
- Motion blur and chromatic aberration

---

## WebGPU Skills (Modern API)

### 15. WebGPU Renderer

**Skill: WebGPU Configuration**
- Initialize `WebGPURenderer`
- Feature detection and fallback
- Render pipeline optimization
- Compute shader integration

**Sub-skills:**
- GPU-driven rendering
- Indirect drawing
- Storage buffers
- Advanced texture formats

---

## Performance Optimization Skills

### 16. Rendering Optimization

**Skill: Draw Call Reduction**
- Geometry merging
- Instanced rendering with `InstancedMesh`
- Level of Detail (LOD) systems
- Frustum culling

**Skill: Memory Management**
- Geometry and texture disposal
- Resource pooling
- Texture atlas generation
- Compressed texture formats

**Sub-skills:**
- GPU memory monitoring
- Lazy loading strategies
- Asset streaming
- Progressive enhancement

### 17. Profiling and Debugging

**Skill: Performance Analysis**
- Stats.js integration for FPS monitoring
- Chrome DevTools GPU profiling
- Draw call counting
- Bottleneck identification

**Sub-skills:**
- Frame time analysis
- GPU vs. CPU bound detection
- Memory leak detection
- Shader compilation monitoring

---

## Advanced Techniques

### 18. Post-Processing

**Skill: EffectComposer Usage**
- Multi-pass rendering setup
- Effect pass chaining
- Render target management
- Custom pass creation

**Sub-skills:**
- Bloom, blur, and glow effects
- SSAO (Screen-Space Ambient Occlusion)
- Outline and edge detection
- Film grain and vignette

### 19. Physics Integration

**Skill: Physics Engine Connection**
- Cannon.js or Ammo.js integration
- Rigid body simulation
- Collision detection
- Constraint systems

**Sub-skills:**
- Physics-driven animation
- Ragdoll physics
- Soft body simulation
- Fluid simulation

### 20. VR/XR Development

**Skill: WebXR Integration**
- VR session initialization
- Controller input handling
- Room-scale tracking
- Hand tracking support

**Sub-skills:**
- Stereoscopic rendering
- Performance optimization for VR (90+ FPS)
- Teleportation and locomotion
- UI in VR space

---

## Learning Resources

### Official
- [Three.js Manual](https://threejs.org/manual/)
- [Three.js Examples](https://threejs.org/examples/)
- [API Documentation](https://threejs.org/docs/)

### Courses
- Three.js Journey by Bruno Simon
- Three.js Fundamentals
- Udemy Three.js courses

### Community
- [Three.js Forum](https://discourse.threejs.org/)
- [Three.js Discord](https://discord.gg/56GBJwAnUS)
- [r/threejs](https://reddit.com/r/threejs)

### Books
- "Learning Three.js" by Jos Dirksen
- "Three.js Cookbook"

---

## Integration Patterns

### With React
- React Three Fiber (R3F) - Declarative Three.js
- Component-based scene composition
- React hooks for animation
- Drei helpers library

### With Vue
- TresJS - Vue Three.js integration
- Composition API patterns
- Reactive 3D scenes

### With Vanilla JS
- Direct Three.js usage
- Custom render loops
- State management patterns
- Module bundling (Vite, Webpack)

---

## Best Practices

1. **Dispose Resources:** Always dispose geometries, materials, and textures when done
2. **Use BufferGeometry:** More efficient than legacy Geometry
3. **Limit Draw Calls:** Merge geometries, use instancing
4. **Optimize Shadows:** Lower resolution, limit shadow-casting objects
5. **Texture Compression:** Use compressed formats (KTX2, Basis)
6. **Responsive Design:** Handle window resizing properly
7. **Progressive Enhancement:** Start simple, add effects gradually
8. **Test Performance:** Profile on target devices early
9. **Use LOD:** Reduce detail for distant objects
10. **Leverage CDNs:** Use CDN versions with tree-shaking for production

---

**Version Reference:** Three.js r170+ (2025-2026)  
**Last Updated:** February 2026