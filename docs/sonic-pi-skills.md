# Sonic Pi Skills & Capabilities

## Overview

Sonic Pi is a live coding environment for creating music and sound through code. Created by Sam Aaron (@samaaron), it's designed to make programming music accessible and fun, with a focus on education and live performance.

**Official Site:** https://sonic-pi.net/  
**GitHub:** https://github.com/sonic-pi-net/sonic-pi  
**Tutorial:** https://sonic-pi.net/tutorial.html  
**Community:** https://in-thread.sonic-pi.net/

---

## Core Sound Skills

### 1. Basic Synthesis

**Skill: Playing Notes and Synths**
- `play 60` for MIDI note playback
- `play :C4` for note name notation
- `sleep 1` for timing and rhythm
- `use_synth :name` to select synth engine
- Note number, name, and frequency conversion

**Sub-skills:**
- Octave manipulation (`:C3`, `:C4`, `:C5`)
- Enharmonic equivalents (`:Cs` = `:Db`)
- Chord notation: `play chord(:C, :major)`
- Microtonal tuning and frequency mode
- Rest notation with `sleep` only

### 2. Synth Engine Selection

**Skill: Built-in Synthesizers**
- `:beep` - Simple sine wave
- `:saw` - Sawtooth wave
- `:prophet` - Rich analog-style synth
- `:tb303` - Classic acid bass
- `:dsaw` - Detuned saw
- `:fm` - FM synthesis
- `:mod_saw`, `:mod_pulse`, `:mod_tri` - Modulated waves
- `:piano`, `:guitar` - Sampled instruments

**Sub-skills:**
- Synth parameter exploration
- Waveform characteristic understanding
- Timbral selection for genres
- Custom synth design (advanced)
- Synth engine performance characteristics

### 3. Synth Parameters

**Skill: Sound Shaping**
- `amp:` for amplitude/volume (0.0 to 1.0+)
- `pan:` for stereo positioning (-1 to 1)
- `attack:`, `decay:`, `sustain:`, `release:` for ADSR envelope
- `cutoff:` for filter frequency
- `res:` for filter resonance
- `slide:` for parameter automation

**Sub-skills:**
- Envelope shape design
- Filter sweep techniques
- Amplitude modulation
- Detune and stereo width
- Parameter randomization
- Real-time parameter control

---

## Rhythm and Timing Skills

### 4. Temporal Control

**Skill: Timing and Tempo**
- `sleep duration` for pauses
- `use_bpm 120` to set tempo
- Fractional sleep values (0.5, 0.25)
- `at` for precise timing within threads
- `time_warp` for tempo manipulation

**Sub-skills:**
- Beat subdivision (whole, half, quarter, eighth notes)
- Triplet and swing feel
- Polyrhythmic patterns
- Tempo ramping and acceleration
- Metric modulation
- Syncopation techniques

### 5. Live Loops

**Skill: Loop-Based Composition**
- `live_loop :name do ... end` for repeating patterns
- Multiple concurrent live loops
- Loop synchronization with `sync`
- Loop stopping and starting
- `tick` for step sequencing

**Sub-skills:**
- Loop naming conventions
- Cue-based synchronization
- Loop tempo independence
- Conditional loop execution
- Loop state management
- Cross-loop communication

### 6. Threading and Concurrency

**Skill: Parallel Execution**
- `in_thread do ... end` for parallel code
- Thread naming and management
- Thread synchronization
- `cue` and `sync` for messaging
- Thread-safe patterns

**Sub-skills:**
- Multiple simultaneous melodies
- Background processes
- Event-driven composition
- Thread pooling patterns
- Deadlock avoidance

---

## Musical Theory Skills

### 7. Scales and Modes

**Skill: Scale-Based Composition**
- `scale(:C, :major)` for scale generation
- Major, minor, pentatonic, blues scales
- Modes: dorian, phrygian, lydian, mixolydian, aeolian, locrian
- Exotic scales: harmonic_minor, melodic_minor, whole_tone
- Custom scale definition

**Sub-skills:**
- Scale degree selection
- Modal interchange
- Scale transposition
- Chromatic alterations
- Scale pattern generation
- Pitch class set theory

### 8. Chord Progressions

**Skill: Harmonic Structures**
- `chord(:C, :major)` for chord generation
- Chord types: major, minor, dim, aug, sus2, sus4
- Extended chords: maj7, min7, dom7, 9, 11, 13
- Chord inversions
- Custom chord voicings

**Sub-skills:**
- Common progressions (I-IV-V, ii-V-I)
- Voice leading
- Chord substitution
- Harmonic rhythm
- Jazz reharmonization
- Chord arpeggiation

### 9. Melody and Rhythm Patterns

**Skill: Musical Phrasing**
- Melodic contour design
- Motif development and variation
- Call and response patterns
- Sequence and repetition
- Rhythmic patterns (rings, spreads)

**Sub-skills:**
- Interval relationships
- Melodic ornamentation
- Phrase structure (AABA, verse-chorus)
- Theme and variation
- Counterpoint basics
- Rhythmic displacement

---

## Sample Skills

### 10. Sample Playback

**Skill: Playing Audio Samples**
- `sample :loop_amen` for built-in samples
- `sample "path/to/file.wav"` for custom samples
- Sample rate and pitch control
- Start and finish point selection
- Reverse playback with `rpitch`

**Sub-skills:**
- Sample library exploration
- Sample slicing and chopping
- Time-stretching techniques
- Pitch shifting without time change
- Sample layering
- One-shot vs loop samples

### 11. Sample Manipulation

**Skill: Sample Processing**
- `rate:` for pitch and speed change
- `onset:` for transient selection
- `beat_stretch:` for tempo matching
- `slice:` for sample chopping
- Envelope application to samples

**Sub-skills:**
- Granular sample techniques
- Stutter and glitch effects
- Sample reverse effects
- Sample filtering and effects
- Sample normalization
- Sample attack trimming

### 12. Custom Sample Loading

**Skill: External Audio Integration**
- Load WAV, AIFF, FLAC files
- Sample path management
- Sample preloading for performance
- Sample pack organization
- Multi-sample mapping

**Sub-skills:**
- Sample library curation
- Drag-and-drop sample import
- Sample metadata handling
- Memory management for large samples
- Sample format conversion awareness

---

## Effects Skills

### 13. Built-in Effects

**Skill: Effect Processing**
- `with_fx :reverb` for spatial effects
- `with_fx :echo` for delay/echo
- `with_fx :distortion` for saturation
- `with_fx :slicer` for rhythmic gating
- `with_fx :wobble` for dubstep bass
- Effect chaining and nesting

**Sub-skills:**
- Effect parameter control
- Pre and post-effect placement
- Effect automation
- Parallel effect processing
- Effect removal and bypassing
- Custom effect chains

### 14. Filter Effects

**Skill: Frequency Filtering**
- `:lpf` (low-pass filter)
- `:hpf` (high-pass filter)
- `:bpf` (band-pass filter)
- `:rbpf` (resonant band-pass)
- `:normaliser` for dynamics

**Sub-skills:**
- Filter cutoff automation
- Resonance/Q control
- Filter envelope modulation
- Multi-band filtering
- Spectral processing concepts
- Filter self-oscillation

### 15. Modulation Effects

**Skill: Time-Based Effects**
- `:flanger` for jet plane sweeps
- `:phaser` for phase shifting
- `:chorus` for width and thickness
- `:tremolo` for amplitude modulation
- `:vibrato` for pitch modulation
- `:ping_pong` for stereo delay

**Sub-skills:**
- LFO rate and depth control
- Modulation waveform selection
- Stereo width manipulation
- Feedback control
- Mix (wet/dry) balancing
- Modulation routing

---

## Live Coding Skills

### 16. Real-Time Modification

**Skill: Live Performance**
- Modify loops while running
- Hot-swapping synths and parameters
- Gradual parameter morphing
- On-the-fly loop addition/removal
- Performance error recovery

**Sub-skills:**
- Code organization for live editing
- Visual feedback interpretation
- Muscle memory for common patterns
- Improvisation strategies
- Version control during performance
- Audience engagement techniques

### 17. Control Flow

**Skill: Conditional Logic**
- `if`/`else` for branching
- `one_in(n)` for probability
- `choose` for random selection
- `pick` for weighted randomness
- Conditional sample triggering

**Sub-skills:**
- Algorithmic composition
- Generative music patterns
- State machines for composition
- Markov chain implementation
- Euclidean rhythm generation
- Cellular automata for music

### 18. Data Structures

**Skill: Musical Data Management**
- Arrays/lists for note sequences
- Rings for cyclic patterns
- Hashes for parameter sets
- `tick` and rings for sequencing
- `spread` for euclidean rhythms

**Sub-skills:**
- Pattern rotation and manipulation
- List comprehension
- Data-driven composition
- Pattern transformation functions
- Sequence generation algorithms
- Lookup tables for scales/chords

---

## Advanced Programming Skills

### 19. Functions and Abstraction

**Skill: Code Reusability**
- `define :function_name` for custom functions
- Parameter passing
- Return values
- Function composition
- Procedural generation

**Sub-skills:**
- Musical phrase functions
- Effect wrapper functions
- Algorithmic generators
- Recursive patterns
- Lambda functions
- Higher-order functions

### 20. Randomness and Probability

**Skill: Controlled Chaos**
- `rrand(min, max)` for random ranges
- `rrand_i(min, max)` for integers
- `rand` for 0.0 to 1.0
- `shuffle` for list randomization
- `use_random_seed` for reproducibility

**Sub-skills:**
- Gaussian distribution with `rrand_gaussian`
- Weighted probability selection
- Pseudo-random sequences
- Deterministic randomness
- Controlled variation
- Stochastic composition

### 21. Time and Sync

**Skill: Temporal Coordination**
- `current_time` for absolute timing
- `cue` to send timing events
- `sync` to wait for events
- `time_warp` for tempo changes
- `at` for scheduled execution

**Sub-skills:**
- Beat-accurate triggering
- Multi-loop synchronization
- Polymetric composition
- Phase-aligned loops
- Scheduled pattern changes
- Metronome implementation

---

## MIDI Skills

### 22. MIDI Input

**Skill: MIDI Controller Integration**
- `sync "/midi:*"` for MIDI events
- Note on/off detection
- Control change (CC) handling
- Velocity sensitivity
- MIDI channel filtering

**Sub-skills:**
- Keyboard input for note triggering
- Pad controller mapping
- Knob/fader parameter control
- MIDI learn patterns
- Multi-controller setup
- MIDI clock synchronization

### 23. MIDI Output

**Skill: External Device Control**
- `midi_note_on` and `midi_note_off`
- Control external synthesizers
- MIDI CC transmission
- Program change messages
- SysEx for device-specific control

**Sub-skills:**
- DAW synchronization
- Hardware synth sequencing
- Multi-device orchestration
- MIDI routing strategies
- Latency compensation
- MIDI timing precision

---

## OSC (Open Sound Control) Skills

### 24. OSC Communication

**Skill: Network Control**
- `use_osc` to enable OSC
- `osc` to send OSC messages
- `sync` to receive OSC data
- TouchOSC and mobile control
- Max/MSP and Pure Data integration

**Sub-skills:**
- OSC message formatting
- Address pattern matching
- Multi-parameter messages
- Bidirectional communication
- Network configuration
- Wireless controller setup

### 25. External Application Integration

**Skill: Cross-Platform Connectivity**
- Control visuals (Processing, p5.js, TouchDesigner)
- Lighting control (DMX via OSC)
- Game engine integration (Unity, Unreal)
- Browser-based interfaces
- Smartphone control apps

**Sub-skills:**
- Protocol design
- Message routing
- Latency management
- State synchronization
- Error handling
- Network debugging

---

## Sound Design Skills

### 26. Additive Synthesis

**Skill: Harmonic Construction**
- Layer multiple sine waves
- Harmonic series understanding
- Partial tuning and detuning
- Spectral envelope shaping
- Formant synthesis

**Sub-skills:**
- Harmonic vs inharmonic timbres
- Beating and interference patterns
- Spectral morphing
- Bell and metallic sounds
- Organ-like timbres

### 27. Subtractive Synthesis

**Skill: Filter-Based Sound Design**
- Rich waveform starting point
- Filter cutoff and resonance
- Envelope-controlled filtering
- Multi-stage filtering
- Self-oscillating filters

**Sub-skills:**
- Classic analog synth sounds
- Bass synthesis (808, 303 style)
- Lead synthesis
- Pad synthesis
- Filter sweep automation

### 28. FM Synthesis

**Skill: Frequency Modulation**
- Carrier and modulator configuration
- Modulation index control
- Harmonic and inharmonic timbres
- DX7-style programming
- Complex timbral evolution

**Sub-skills:**
- Bell and mallet sounds
- Electric piano timbres
- Brass-like sounds
- Digital artifacts and aliasing
- Multi-operator FM

---

## Composition Skills

### 29. Song Structure

**Skill: Arrangement and Form**
- Intro, verse, chorus, bridge sections
- Build-up and breakdown techniques
- Transition and fill patterns
- Dynamic variation across sections
- Song-length composition

**Sub-skills:**
- Section triggering and cueing
- Arrangement timeline management
- Energy level control
- Tension and release
- Thematic development
- Structural variation

### 30. Genre-Specific Techniques

**Skill: Style Emulation**
- Electronic dance music patterns
- Hip-hop beat construction
- Ambient soundscapes
- Chiptune/8-bit aesthetics
- Glitch and IDM techniques
- Classical composition approaches

**Sub-skills:**
- Drum pattern programming
- Bass line construction
- Synth lead design
- Atmospheric pad creation
- Genre-appropriate sample selection
- Tempo and swing for genres

### 31. Layering and Orchestration

**Skill: Texture Building**
- Multiple synth layers
- Frequency range allocation
- Stereo field placement
- Rhythmic interplay
- Timbral contrast

**Sub-skills:**
- Low-end management (bass, kick)
- Mid-range clarity
- High-frequency detail
- Counter-melodies
- Call and response between parts
- Sparse vs dense arrangements

---

## Performance Skills

### 32. Live Coding Performance

**Skill: Stage Presence**
- Projected code as visual element
- Explaining code to audience
- Building tracks from silence
- Error recovery strategies
- Performance energy and pacing

**Sub-skills:**
- Keyboard shortcuts and speed
- Code commenting for readability
- Visual organization of code
- Improvisation techniques
- Audience interaction
- Set list preparation

### 33. Algorave and Club Performance

**Skill: Dance Music Context**
- Beatmatching and tempo control
- Energy level management
- Crowd reading and response
- Long-form mixing
- Collaboration with VJs

**Sub-skills:**
- Four-on-the-floor patterns
- Breakbeat programming
- Drop and build techniques
- Bassline variation
- Filter sweeps for transitions
- Loop and pattern evolution

---

## Education Skills

### 34. Teaching with Sonic Pi

**Skill: Educational Application**
- Age-appropriate lesson plans
- Progressive skill building
- Error message interpretation
- Debugging strategies
- Creative project design

**Sub-skills:**
- Classroom management with code
- Connecting music theory to code
- Gamification of learning
- Assessment strategies
- Differentiated instruction
- Cross-curricular connections

### 35. Code Literacy

**Skill: Programming Fundamentals**
- Variables and data types
- Loops and iteration
- Conditionals and logic
- Functions and modularity
- Debugging and testing

**Sub-skills:**
- Computational thinking
- Problem decomposition
- Pattern recognition
- Algorithmic design
- Code optimization
- Documentation practices

---

## Technical Skills

### 36. Audio Configuration

**Skill: System Setup**
- Audio interface selection
- Sample rate configuration
- Buffer size for latency
- Output routing
- Multi-channel audio

**Sub-skills:**
- Latency troubleshooting
- Audio driver optimization (ASIO, CoreAudio)
- Recording setup
- Monitoring configuration
- External effects routing
- Audio feedback prevention

### 37. Recording and Export

**Skill: Output Capture**
- Built-in recording function
- Multi-track recording strategies
- Export for DAW integration
- Stem export for mixing
- Live performance recording

**Sub-skills:**
- File format selection
- Recording level setting
- Post-processing workflow
- Backup strategies
- Session documentation
- Archival best practices

### 38. Optimization and Performance

**Skill: Resource Management**
- CPU usage monitoring
- Polyphony management
- Effect efficiency
- Sample memory usage
- Loop complexity control

**Sub-skills:**
- Code profiling
- Simplification techniques
- Precomputation strategies
- Effect chain optimization
- Sample rate considerations
- Real-time constraint awareness

---

## Community and Ecosystem

### 39. Sonic Pi Community

**Learning Resources:**
- Built-in tutorial (excellent starting point)
- Sonic Pi forum: https://in-thread.sonic-pi.net/
- YouTube tutorials (Sam Aaron's live streams)
- "Code Music with Sonic Pi" book by Sam Aaron
- Sonic Pi teacher resources

**Community Platforms:**
- GitHub repository for contributions
- Twitter #SonicPi hashtag
- Algorave community
- Toplap (live coding organization)
- Educational networks (Code Club, Raspberry Pi Foundation)

**Related Projects:**
- TidalCycles (Haskell-based live coding)
- SuperCollider (advanced audio synthesis)
- Overtone (Clojure music environment)
- FoxDot (Python live coding)
- Hydra (live coding visuals)

### 40. Contributing and Extending

**Skill: Ecosystem Participation**
- Bug reporting on GitHub
- Feature requests and discussion
- Sample pack creation and sharing
- Tutorial writing
- Educational resource development

**Sub-skills:**
- Ruby understanding (Sonic Pi's base language)
- SuperCollider synthesis knowledge
- Open source contribution practices
- Documentation writing
- Community engagement
- Translation contributions

---

## Key Features and Philosophy

**Accessibility:**
- Free and open source
- Cross-platform (Windows, Mac, Linux, Raspberry Pi)
- Designed for beginners and education
- Powerful enough for professionals
- Visual and audio feedback

**Live Coding:**
- Code is the performance
- Mistakes are part of the process
- Transparency and improvisation
- Community-driven practice
- Algorithmic and generative music

**Educational Focus:**
- Computing and music literacy
- Creative expression through code
- STEAM education integration
- Inclusive and accessible design
- Scaffolded learning progression

**Technical Foundation:**
- Built on Ruby (simple syntax)
- SuperCollider for audio engine
- Qt for user interface
- Real-time audio processing
- Multi-threaded execution model

---

## Supersonic (Project Context)

**Note:** The samaaron/supersonic project mentioned in the research appears to be an early or experimental version. The primary, actively maintained project is **Sonic Pi** at https://github.com/sonic-pi-net/sonic-pi

For current development and the most up-to-date information, refer to the main Sonic Pi repository and community resources listed above.
