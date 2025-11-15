# MEGA DEMO SCENE GENERATOR

## Overview

A procedurally generated audiovisual "demo" that creates unique, synchronised chiptune music and retro graphics from a single seed value. Each seed produces a completely different but reproducible demo with millions of possible variations.

## Features

- **Seeded Generation**: Every demo is deterministically generated from a seed number
- **Configurable Duration**: Create demos from 30 seconds to unlimited length
- **Automatic Recording**: Exports video as a WebM video file with synchronised audio
- **Music Theory Engine**: Generates musical compositions using scales, chord progressions, and rhythm patterns
- **Multiple Visual Scenes**: Matrix rain, tunnels, plasma, fractals, particles, and more
- **100% Browser-Based**: No installation required, runs entirely in a web browser

## Requirements

- Modern web browser (Chrome, Firefox, Edge, Safari)
- JavaScript enabled
- Free space for video recording

## Quick Start

1. Open the HTML file in a browser
2. Click "GENERATE DEMO" to create a random demo
3. The demo will automatically record and download when complete

## URL Parameters

Control the demo with URL parameters:

```
?seed=12345&duration=300
```

### Parameters:
- **seed**: Integer (0-2147483647) - Determines all random generation. Same seed = same demo
- **duration**: Integer (seconds) - Length of the demo. Default: 300 (5 minutes)

### Example URLs:
```
demo.html?seed=42&duration=180   # 3-minute demo with seed 42
demo.html?seed=1337&duration=600 # 10-minute epic with seed 1337
demo.html?seed=999&duration=120  # Quick 2-minute demo
demo.html                        # Random seed, 5-minute default
```

## Music Generation

Each seed generates unique music with:
- **BPM**: 120-160 beats per minute
- **Key**: Random selection from all 12 keys
- **Scale**: Major, Minor, Dorian, Phrygian, Lydian, Mixolydian, Pentatonic, Blues, etc.
- **Structure**: Intro → Buildup → Drop → Breakdown → Bridge → Outro
- **Instruments**: 3 pulse waves, triangle bass, drums (kick, snare, hi-hat)

Most of it will sound completely insane. Nice.

## Visual Scenes

The generator randomly selects from 12 scene types:

- **Matrix**: Digital rain effect
- **Tunnel**: Rotating perspective tunnel
- **Plasma**: Animated plasma effect
- **Starfield**: 3D star movement
- **Fractals**: Recursive geometric patterns
- **Particles**: Particle system explosions
- **Geometry**: Rotating polygons
- **Waves**: Sine wave distortions
- **Spiral**: Colourful spiral patterns
- **Glitch**: Digital corruption effects
- **Fire**: Flame simulation
- **Electric**: Lightning bolts

## Output

At the end of the song, the demo automatically saves as a WebM video file:

- **Filename**: `demoscene_seed{SEED}_{TIMESTAMP}.webm`
- **Video**: 30 FPS, 8 Mbps bitrate
- **Audio**: Stereo, 48kHz
- **Format**: VP9/VP8 codec with Opus audio

## Technical Details

Amazing all the terrible things you can do with tech these days.

### Technologies Used:
- **Tone.js**: Web Audio synthesis and sequencing
- **Canvas API**: 2D graphics rendering
- **MediaRecorder API**: Video capture
- **Mulberry32**: Seeded random number generator
