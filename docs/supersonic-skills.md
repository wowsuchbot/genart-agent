# SuperSonic Skills & Capabilities

## Overview

SuperSonic is a groundbreaking project by Sam Aaron that brings **SuperCollider's scsynth audio synthesis engine to the web browser**. It runs as a Web AudioWorklet, providing professional-grade audio synthesis capabilities with zero installation required.

**Official Site:** https://sonic-pi.net/supersonic/  
**GitHub Repository:** https://github.com/samaaron/supersonic  
**Live Demo:** https://sonic-pi.net/supersonic/demo.html  
**Latest Version:** v0.31.0 (January 21, 2026)

### Key Technology

- **AudioWorklet** - Dedicated high-priority audio thread for optimal performance
- **WebAssembly (WASM)** - scsynth's original C++ code compiled for browsers
- **OSC API** - Full Open Sound Control messaging protocol access
- **Zero Configuration** - Works directly from CDNs with no installation
- **Optional SAB Mode** - SharedArrayBuffer mode for lower latency (requires COOP/COEP headers)

---

## Core Synthesis Skills

### 1. Initialization and Setup

**Skill: Basic SuperSonic Initialization**

```javascript
import {SuperSonic} from 'https://unpkg.com/supersonic-scsynth@latest';

// Basic setup
const sonic = new SuperSonic();
await sonic.init();

// With custom configuration
const sonic = new SuperSonic({
  baseURL: 'https://unpkg.com/supersonic-scsynth@latest',
  useSAB: true // Enable SharedArrayBuffer mode for lower latency
});
await sonic.init();
```

**Sub-skills:**
- Importing from CDN (unpkg, jsDelivr)
- Configuring base URL for assets
- Enabling/disabling SAB mode based on CORS headers
- Handling async initialization
- Error handling for browser compatibility

---

**Skill: Loading Audio Context**

```javascript
// SuperSonic handles AudioContext internally
// No manual AudioContext setup required
await sonic.init();
// Audio context is created and managed automatically
```

**Sub-skills:**
- Understanding AudioWorklet architecture
- CORS header requirements for SAB mode:
  - `Cross-Origin-Opener-Policy: same-origin`
  - `Cross-Origin-Embedder-Policy: require-corp`
- Browser compatibility detection
- Fallback strategies for unsupported browsers

---

### 2. Synth Definition Management

**Skill: Loading Pre-built Synth Definitions**

```javascript
// Load individual synth from Sonic Pi collection
await sonic.loadSynthDef('sonic-pi-beep');
await sonic.loadSynthDef('sonic-pi-prophet');
await sonic.loadSynthDef('sonic-pi-tb303');

// Load multiple synths
await Promise.all([
  sonic.loadSynthDef('sonic-pi-beep'),
  sonic.loadSynthDef('sonic-pi-dsaw'),
  sonic.loadSynthDef('sonic-pi-fm')
]);
```

**Available Sonic Pi Synths:**
- **sonic-pi-beep** - Simple sine wave
- **sonic-pi-saw** - Sawtooth wave
- **sonic-pi-dsaw** - Detuned sawtooth (fat sound)
- **sonic-pi-fm** - FM synthesis
- **sonic-pi-mod_fm** - Modulated FM
- **sonic-pi-tb303** - Classic acid bassline
- **sonic-pi-supersaw** - Rich detuned sawtooth
- **sonic-pi-hoover** - Rave hoover sound
- **sonic-pi-prophet** - Analog-style synth
- **sonic-pi-zawa** - Aggressive sawtooth
- **sonic-pi-dark_ambience** - Atmospheric pad
- **sonic-pi-growl** - Dubstep wobble bass
- **sonic-pi-hollow** - Hollow resonant tone
- **sonic-pi-pluck** - Plucked string
- **sonic-pi-piano** - Piano sample
- **sonic-pi-kalimba** - Kalimba sound
- **sonic-pi-chipbass** - Chiptune bass
- **sonic-pi-pulse** - Pulse wave
- **sonic-pi-square** - Square wave
- **sonic-pi-tri** - Triangle wave
- **sonic-pi-dtri** - Detuned triangle
- **sonic-pi-blade** - Metallic lead
- **sonic-pi-bnoise** - Brown noise
- **sonic-pi-cnoise** - Clip noise
- **sonic-pi-gnoise** - Gray noise
- **sonic-pi-pnoise** - Pink noise
- **sonic-pi-noise** - White noise

**Sub-skills:**
- Understanding synth families (leads, basses, pads, noise)
- Synth selection for musical context
- Preloading synths for performance
- Managing synth definition memory

---

**Skill: Custom Synth Definition Loading**

```javascript
// Load custom SynthDef from URL or file
await sonic.loadSynthDef('my-custom-synth', '/path/to/synthdef.scsyndef');

// Or provide SynthDef binary data directly
const synthDefData = new Uint8Array([...]);
await sonic.loadSynthDefFromData('my-synth', synthDefData);
```

**Sub-skills:**
- Creating SynthDefs in SuperCollider
- Compiling SynthDefs to .scsyndef format
- Converting SynthDefs for web deployment
- Parameter naming conventions
- Testing custom synths

---

### 3. Triggering and Controlling Synths

**Skill: Basic Synth Triggering**

```javascript
// Trigger a synth with OSC message
// Format: /s_new synthName nodeID addAction targetID ...params

// Simple trigger (auto-assigns node ID)
sonic.send('/s_new', 'sonic-pi-beep', -1, 0, 0, 'note', 60);

// With multiple parameters
sonic.send('/s_new', 'sonic-pi-prophet', -1, 0, 0,
  'note', 72,
  'amp', 0.5,
  'attack', 0.1,
  'release', 1.0,
  'cutoff', 80
);
```

**Common Synth Parameters:**
- **note** - MIDI note number (60 = Middle C)
- **amp** - Amplitude (0.0 to 1.0)
- **pan** - Stereo pan (-1 = left, 0 = center, 1 = right)
- **attack** - Envelope attack time (seconds)
- **decay** - Envelope decay time
- **sustain** - Sustain level (0.0 to 1.0)
- **release** - Release time (seconds)
- **cutoff** - Filter cutoff frequency (0-130 MIDI note range)
- **res** - Filter resonance (0.0 to 1.0)

**Sub-skills:**
- Node ID management (-1 for auto-assignment)
- Add action codes (0=head, 1=tail, 2=before, 3=after)
- Parameter name-value pairing
- Understanding OSC message format

---

**Skill: Synth Control and Modification**

```javascript
// Store node ID for later control
const nodeID = 1000;
sonic.send('/s_new', 'sonic-pi-prophet', nodeID, 0, 0, 'note', 60);

// Modify synth parameters while playing
sonic.send('/n_set', nodeID, 'cutoff', 100);
sonic.send('/n_set', nodeID, 'amp', 0.8, 'res', 0.5);

// Free (stop) a synth
sonic.send('/n_free', nodeID);

// Free all synths
sonic.send('/g_freeAll', 0);
```

**Sub-skills:**
- Real-time parameter modulation
- Multi-parameter updates
- Node lifecycle management
- Group control for multiple synths

---

### 4. Sample Playback

**Skill: Loading and Playing Samples**

```javascript
// Load a sample buffer
await sonic.loadSample('kick', '/audio/kick.wav');
await sonic.loadSample('snare', '/audio/snare.wav');

// Play sample with built-in sample player synth
sonic.send('/s_new', 'sonic-pi-sampler', -1, 0, 0,
  'buf', sonic.getSampleBufferID('kick'),
  'rate', 1.0,
  'amp', 0.8
);
```

**Sample Parameters:**
- **buf** - Buffer number containing sample
- **rate** - Playback rate (1.0 = normal, 2.0 = double speed/octave up)
- **start** - Start position (0.0 to 1.0)
- **finish** - End position (0.0 to 1.0)
- **amp** - Amplitude
- **pan** - Stereo position
- **attack**, **sustain**, **release** - Envelope

**Sub-skills:**
- Audio file format support (WAV, MP3, OGG)
- Buffer management and memory
- Sample rate conversion
- Pitch shifting via playback rate
- Reversing samples (negative rate)
- Sample slicing and chopping

---

### 5. Timing and Sequencing

**Skill: Precise Timing with OSC Bundles**

```javascript
// Schedule messages for future execution
// OSC bundles provide sample-accurate timing

const now = sonic.getOSCTime();
const beat = 0.5; // seconds per beat

// Schedule a sequence
sonic.sendBundle(now, [
  ['/s_new', 'sonic-pi-beep', -1, 0, 0, 'note', 60]
]);

sonic.sendBundle(now + beat, [
  ['/s_new', 'sonic-pi-beep', -1, 0, 0, 'note', 64]
]);

sonic.sendBundle(now + beat * 2, [
  ['/s_new', 'sonic-pi-beep', -1, 0, 0, 'note', 67]
]);
```

**Sub-skills:**
- OSC time format understanding
- Latency compensation
- Clock synchronization
- Lookahead scheduling
- Tempo and beat calculation

---

**Skill: Pattern Sequencing**

```javascript
// Simple step sequencer
const pattern = [60, 64, 67, 72];
const tempo = 120; // BPM
const beatDuration = 60 / tempo;

let step = 0;
setInterval(() => {
  const note = pattern[step % pattern.length];
  sonic.send('/s_new', 'sonic-pi-beep', -1, 0, 0, 'note', note);
  step++;
}, beatDuration * 1000);
```

**Sub-skills:**
- Rhythmic pattern programming
- Tempo calculation (BPM to seconds)
- Step sequencer implementation
- Euclidean rhythms
- Polyrhythmic patterns

---

### 6. Effects and Processing

**Skill: Built-in Effects**

SuperSonic supports SuperCollider's built-in effects via SynthDefs:

```javascript
// Load effect SynthDefs
await sonic.loadSynthDef('sonic-pi-reverb');
await sonic.loadSynthDef('sonic-pi-echo');
await sonic.loadSynthDef('sonic-pi-distortion');

// Create effect on a bus
const fxBus = 100;
sonic.send('/s_new', 'sonic-pi-reverb', 2000, 1, 0,
  'in_bus', fxBus,
  'room', 0.8,
  'damp', 0.5
);

// Route synth output to effect bus
sonic.send('/s_new', 'sonic-pi-beep', -1, 0, 0,
  'note', 60,
  'out_bus', fxBus
);
```

**Common Effects:**
- **sonic-pi-reverb** - Reverb (room, damp parameters)
- **sonic-pi-echo** - Delay/echo (delay time, feedback)
- **sonic-pi-distortion** - Distortion (drive, tone)
- **sonic-pi-wobble** - LFO filter modulation
- **sonic-pi-slicer** - Amplitude gating/slicing
- **sonic-pi-bitcrusher** - Bit reduction and sample rate reduction
- **sonic-pi-flanger** - Flanging effect
- **sonic-pi-phaser** - Phasing effect
- **sonic-pi-ping_pong** - Ping-pong delay
- **sonic-pi-compressor** - Dynamic range compression

**Sub-skills:**
- Audio bus routing
- Effect chains
- Send/return configurations
- Parallel processing
- Effect parameter automation

---

### 7. Advanced OSC Control

**Skill: Group Management**

```javascript
// Create a group for organizing synths
const groupID = 100;
sonic.send('/g_new', groupID, 0, 0);

// Add synths to the group
sonic.send('/s_new', 'sonic-pi-prophet', -1, 0, groupID, 'note', 60);
sonic.send('/s_new', 'sonic-pi-prophet', -1, 0, groupID, 'note', 64);

// Control all synths in group
sonic.send('/n_set', groupID, 'cutoff', 90);

// Free entire group
sonic.send('/n_free', groupID);
```

**Sub-skills:**
- Hierarchical node organization
- Group-based mixing
- Mass parameter control
- Parallel node operations

---

**Skill: Bus Routing**

```javascript
// Audio buses for routing
const reverbBus = 20;
const delayBus = 21;

// Create effect chain
sonic.send('/s_new', 'sonic-pi-reverb', 3000, 1, 0, 'in_bus', reverbBus);
sonic.send('/s_new', 'sonic-pi-echo', 3001, 1, 0, 'in_bus', delayBus);

// Route synth through effects
sonic.send('/s_new', 'sonic-pi-prophet', -1, 0, 0,
  'note', 60,
  'out_bus', reverbBus
);
```

**Sub-skills:**
- Bus numbering conventions
- Signal flow design
- Aux send/return
- Multi-bus routing

---

### 8. Performance Monitoring

**Skill: Server Status Monitoring**

```javascript
// Query server status
sonic.send('/status');

// Listen for status responses (requires OSC listener setup)
sonic.on('status', (data) => {
  console.log('CPU Usage:', data.avgCPU);
  console.log('Peak CPU:', data.peakCPU);
  console.log('Synth Count:', data.numSynths);
});
```

**Sub-skills:**
- CPU usage monitoring
- Voice count tracking
- Performance optimization
- Resource limit awareness

---

## Musical Theory Integration

### 9. Note and Frequency Conversion

**Skill: MIDI to Frequency**

```javascript
// MIDI note to frequency conversion
function midiToFreq(note) {
  return 440 * Math.pow(2, (note - 69) / 12);
}

// Use with 'freq' parameter instead of 'note'
sonic.send('/s_new', 'sonic-pi-prophet', -1, 0, 0,
  'freq', midiToFreq(60) // 261.63 Hz (Middle C)
);
```

**Sub-skills:**
- MIDI note number system (C4 = 60)
- Frequency calculation
- Tuning systems (12-TET, just intonation)
- Microtonal music support

---

**Skill: Scale and Chord Generation**

```javascript
// Define musical scales
const scales = {
  major: [0, 2, 4, 5, 7, 9, 11],
  minor: [0, 2, 3, 5, 7, 8, 10],
  pentatonic: [0, 2, 4, 7, 9],
  blues: [0, 3, 5, 6, 7, 10]
};

// Generate scale from root note
function getScale(root, scaleName) {
  return scales[scaleName].map(interval => root + interval);
}

// Play major scale from C (MIDI 60)
const cMajor = getScale(60, 'major');
cMajor.forEach((note, i) => {
  setTimeout(() => {
    sonic.send('/s_new', 'sonic-pi-beep', -1, 0, 0, 'note', note);
  }, i * 200);
});
```

**Sub-skills:**
- Scale theory and intervals
- Chord construction (triads, 7ths, extensions)
- Arpeggio generation
- Harmonic progression

---

### 10. Rhythm and Timing

**Skill: Rhythm Patterns**

```javascript
// Euclidean rhythm generator
function euclideanRhythm(steps, pulses) {
  const pattern = Array(steps).fill(false);
  const bucket = Array(steps).fill(0);
  
  for (let i = 0; i < steps; i++) {
    bucket[i] += pulses;
    if (bucket[i] >= steps) {
      bucket[i] -= steps;
      pattern[i] = true;
    }
  }
  return pattern;
}

// Generate and play 16-step pattern with 5 hits
const rhythm = euclideanRhythm(16, 5);
let step = 0;

setInterval(() => {
  if (rhythm[step]) {
    sonic.send('/s_new', 'sonic-pi-beep', -1, 0, 0, 'note', 60);
  }
  step = (step + 1) % rhythm.length;
}, 125); // 120 BPM sixteenth notes
```

**Sub-skills:**
- Euclidean rhythm algorithm
- Polyrhythms and cross-rhythms
- Swing and groove quantization
- Metric modulation

---

## Browser Integration

### 11. User Interaction

**Skill: Mouse/Touch Control**

```javascript
// Map mouse position to synth parameters
document.addEventListener('mousemove', (e) => {
  const x = e.clientX / window.innerWidth;
  const y = e.clientY / window.innerHeight;
  
  const note = Math.floor(x * 48) + 36; // Map to note range
  const cutoff = Math.floor(y * 100) + 30; // Map to cutoff range
  
  sonic.send('/s_new', 'sonic-pi-prophet', -1, 0, 0,
    'note', note,
    'cutoff', cutoff,
    'release', 0.1
  );
});
```

**Sub-skills:**
- Event listener integration
- Parameter mapping and scaling
- Touch gesture interpretation
- Multi-touch polyphony

---

**Skill: Keyboard Musical Interface**

```javascript
// QWERTY keyboard as piano
const keyMap = {
  'a': 60, 'w': 61, 's': 62, 'e': 63, 'd': 64,
  'f': 65, 't': 66, 'g': 67, 'y': 68, 'h': 69,
  'u': 70, 'j': 71, 'k': 72
};

const activeNodes = {};

document.addEventListener('keydown', (e) => {
  if (keyMap[e.key] && !activeNodes[e.key]) {
    const nodeID = Math.floor(Math.random() * 10000);
    activeNodes[e.key] = nodeID;
    
    sonic.send('/s_new', 'sonic-pi-prophet', nodeID, 0, 0,
      'note', keyMap[e.key],
      'release', 0.5
    );
  }
});

document.addEventListener('keyup', (e) => {
  if (activeNodes[e.key]) {
    sonic.send('/n_set', activeNodes[e.key], 'gate', 0);
    delete activeNodes[e.key];
  }
});
```

**Sub-skills:**
- Keyboard mapping strategies
- Note-on/note-off handling
- Sustain pedal emulation
- Velocity sensitivity emulation

---

### 12. Visual Synchronization

**Skill: Audio-Visual Sync**

```javascript
// Sync visuals with audio events
function playNoteWithVisual(note) {
  // Trigger sound
  sonic.send('/s_new', 'sonic-pi-beep', -1, 0, 0, 'note', note);
  
  // Trigger visual (example with canvas)
  const canvas = document.getElementById('canvas');
  const ctx = canvas.getContext('2d');
  
  ctx.fillStyle = `hsl(${note * 3}, 70%, 50%)`;
  ctx.fillRect(
    Math.random() * canvas.width,
    Math.random() * canvas.height,
    50, 50
  );
}
```

**Sub-skills:**
- Canvas/WebGL integration
- SVG animation sync
- Three.js/p5.js integration
- Timing synchronization strategies

---

## Advanced Techniques

### 13. Generative Music

**Skill: Algorithmic Composition**

```javascript
// Markov chain melody generator
const transitions = {
  60: [62, 64, 65],
  62: [60, 64, 67],
  64: [62, 65, 69],
  65: [64, 67, 60],
  67: [65, 69, 62],
  69: [67, 72, 64],
  72: [69, 67, 60]
};

let currentNote = 60;

function playNextNote() {
  sonic.send('/s_new', 'sonic-pi-prophet', -1, 0, 0,
    'note', currentNote,
    'release', 0.3
  );
  
  // Choose next note from transitions
  const nextNotes = transitions[currentNote];
  currentNote = nextNotes[Math.floor(Math.random() * nextNotes.length)];
  
  // Schedule next note
  setTimeout(playNextNote, 200 + Math.random() * 200);
}

playNextNote();
```

**Sub-skills:**
- Markov chains for melody
- L-systems for structure
- Cellular automata for rhythm
- Genetic algorithms for evolution
- Chaos theory and strange attractors

---

### 14. Live Coding

**Skill: Dynamic Code Evaluation**

```javascript
// Live coding environment
const codeInput = document.getElementById('code');
const runButton = document.getElementById('run');

runButton.addEventListener('click', () => {
  const code = codeInput.value;
  try {
    // Evaluate user code with sonic in scope
    const func = new Function('sonic', code);
    func(sonic);
  } catch (error) {
    console.error('Code error:', error);
  }
});
```

**Sub-skills:**
- Safe code evaluation
- REPL interface design
- Error handling and debugging
- Hot-reloading patterns
- Code snippet library

---

### 15. Recording and Export

**Skill: Audio Recording**

```javascript
// Record SuperSonic output (requires MediaRecorder API)
const stream = sonic.getAudioContext().destination.stream;
const mediaRecorder = new MediaRecorder(stream);
const chunks = [];

mediaRecorder.ondataavailable = (e) => chunks.push(e.data);

mediaRecorder.onstop = () => {
  const blob = new Blob(chunks, { type: 'audio/webm' });
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url;
  a.download = 'recording.webm';
  a.click();
};

// Start recording
mediaRecorder.start();

// ... play music ...

// Stop recording
mediaRecorder.stop();
```

**Sub-skills:**
- MediaRecorder API usage
- Audio format selection
- Real-time recording
- Offline rendering (requires custom implementation)

---

## Performance Best Practices

1. **Preload SynthDefs:** Load all required synths before performance
2. **Reuse Node IDs:** Track and free nodes to prevent memory leaks
3. **Use OSC Bundles:** For sample-accurate timing
4. **Limit Voice Count:** Monitor active synth count
5. **Use Groups:** For efficient mass control
6. **Bus Routing:** Minimize audio buses for better performance
7. **SAB Mode:** Enable for lowest latency (with proper CORS headers)
8. **Buffer Management:** Dispose unused sample buffers
9. **CPU Monitoring:** Watch server status for performance issues
10. **Graceful Degradation:** Reduce complexity if CPU usage is high

---

## Learning Resources

### Official Documentation
- [SuperSonic GitHub](https://github.com/samaaron/supersonic)
- [SuperSonic Demo](https://sonic-pi.net/supersonic/demo.html)
- [OSC Specification](http://opensoundcontrol.org/spec-1_0)

### Related Projects
- [Sonic Pi](https://sonic-pi.net/) - Live coding music environment
- [SuperCollider](https://supercollider.github.io/) - Original audio synthesis platform
- [SuperCollider Server Guide](https://doc.sccode.org/Guides/ServerGuide.html)

### Community
- [Sonic Pi Forum](https://in-thread.sonic-pi.net/)
- [SuperCollider Forums](https://scsynth.org/)
- [Live Coding Community](https://toplap.org/)

---

## Integration Examples

### With Three.js
```javascript
// Audio-reactive 3D visuals
sonic.send('/s_new', 'sonic-pi-beep', -1, 0, 0, 'note', note);
cube.scale.set(1.5, 1.5, 1.5); // Visual feedback
```

### With p5.js
```javascript
// Creative coding with audio
function mousePressed() {
  const note = map(mouseX, 0, width, 48, 84);
  sonic.send('/s_new', 'sonic-pi-prophet', -1, 0, 0, 'note', note);
}
```

### With Web MIDI
```javascript
// MIDI controller input
navigator.requestMIDIAccess().then((midiAccess) => {
  const inputs = midiAccess.inputs.values();
  for (let input of inputs) {
    input.onmidimessage = (msg) => {
      if (msg.data[0] === 144) { // Note on
        sonic.send('/s_new', 'sonic-pi-prophet', -1, 0, 0,
          'note', msg.data[1],
          'amp', msg.data[2] / 127
        );
      }
    };
  }
});
```

---

## Troubleshooting

### Common Issues

**Issue: No sound output**
- Check browser AudioContext permissions (requires user interaction)
- Verify SynthDef is loaded before use
- Check console for errors

**Issue: High latency**
- Enable SAB mode with proper CORS headers
- Reduce number of active synths
- Check CPU usage

**Issue: Clicks/pops in audio**
- Increase buffer size (SAB mode)
- Reduce CPU load
- Check for timing issues in scheduling

---

**Version Reference:** SuperSonic v0.31.0  
**Last Updated:** February 2026