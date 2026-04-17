# P.U.L.S.E-pragath
P.U.L.S.E is a browser-based platform that generates real-time 3D particle simulations from simple text prompts using Google Gemini API. It renders interactive visuals using Three.js and WebGL, enabling easy creation and export of particle effects.
Project Title:

P.U.L.S.E – AI-Based 3D Particle Simulation System


---

Creator Details

Name: Pragath (Alias: Pragon)
Academic Level: First Year


---

1. Project Overview

P.U.L.S.E is a browser-based system that generates and visualizes real-time 3D particle simulations using artificial intelligence. It enables users to create complex visual effects through simple text prompts without requiring advanced programming knowledge.

The system utilizes Three.js and WebGL for rendering and integrates Google Gemini API to automatically convert user prompts into particle logic.


---

2. Project Description

The AI-Based 3D Particle Simulation System is designed to simplify the creation of visually rich particle effects such as fire, smoke, waves, spirals, and cylindrical formations. Users can describe an effect using natural language, and the system generates the corresponding particle behavior and motion in real time.

The platform supports AI-based generation, manual input, and code-level customization, providing flexibility for both beginners and advanced users. It also allows real-time interaction and export of reusable code.


---

3. Objectives

Simplify particle simulation development

Enable no-code and low-code creation

Provide real-time interactive 3D visualization

Integrate AI for automatic logic generation

Support reusable and exportable code



---

4. Problem Statement

Traditional particle system development requires advanced programming skills, strong mathematical understanding, and significant development time, making it difficult for beginners and inefficient for rapid prototyping.


---

5. Proposed Solution

1. User inputs a prompt / drawing / code


2. Google Gemini API generates particle logic


3. Simulation engine processes behavior


4. Three.js renders output using WebGL


5. User interacts and exports results




---

6. Key Features

AI-based particle generation

Real-time 3D rendering

Interactive controls and adjustments

3D camera navigation

Code-level particle scripting

Export functionality



---

7. Technology Stack

Component	Technology

Frontend	HTML, CSS, JavaScript
3D Engine	Three.js
Rendering	WebGL
AI Integration	Google Gemini API
Backend (Optional)	Node.js



---

8. Modules

Input Module: Captures user prompts, drawings, or code

AI Processing Module: Converts input into particle behavior

Simulation Engine: Handles motion, structure, and physics

Rendering Module: Displays real-time 3D output

Control Module: Enables parameter adjustments

Export Module: Generates reusable code



---

9. Example Implementation (Cylinder Particle System)

// Controls
const r = addControl('r', 'Radius', 50, 300, 120);
const h = addControl('h', 'Height', 100, 600, 300);

// Vertical distribution
const y = (i / count - 0.5) * h;

// Circular angle
const theta = i * 2.399 + time;

// Position on cylinder surface
target.set(
  Math.cos(theta) * r,
  y,
  Math.sin(theta) * r
);

// Color gradient
color.setHSL(i / count, 1, 0.55);

// Label
if (i === 0) setInfo('Cylinder', 'Particle Cylinder Shape');


---

10. Applications

Generative art

Visual effects (VFX)

Game development

Interactive web applications

Educational simulations



---

11. Advantages

Easy to use for beginners

Supports advanced customization

Real-time interaction and feedback

Runs directly in the browser without installation



---

12. Future Enhancements

Voice-based prompt input

Offline AI integration

Advanced physics simulation

VR/AR support

Mobile optimization



---

13. Credits

Inspiration Source: Particles by Casberry

Concept adapted for academic project purposes



---

14. Conclusion

P.U.L.S.E demonstrates how artificial intelligence combined with modern web technologies can simplify complex particle simulations. By transforming simple prompts into dynamic 3D visualizations, the system enables efficient creation, experimentation, and learning for both beginners and developers.


---

user manual # ✦ AI Particle Shape Generator — User Manual

---

## 🧭 1. Introduction

The **AI Particle Shape Generator** is a real-time visual simulation tool that lets you create, animate, and control thousands of particles in 3D space using presets, AI generation, and custom JavaScript logic.

This manual explains how to operate every major part of the system.

---

## 🖥️ 2. Interface Overview

The application is divided into key sections:

### 1. Top Controls

* Shape selector (Sphere, Cube, Torus, etc.)
* Apex Effects dropdown
* Distribution/Grid selector

### 2. Left Panel

* AI Shape Generator
* Theme & Color settings
* Presets

### 3. Center Canvas

* Real-time particle rendering viewport
* Interactive camera (drag to rotate, scroll to zoom)

### 4. Right Panel

* Particle controls
* Runtime editor
* Media inputs
* Effects & physics

---

## ⚙️ 3. Basic Workflow (Quick Start)

1. Select a **Shape Mode** (e.g., Sphere)
2. Choose a **Distribution** (e.g., Golden Spiral)
3. Optionally apply an **Apex Effect**
4. Adjust particle settings (size, count, etc.)
5. Click ▶ **Run**

---

## 🧠 4. AI Shape Generator

### Input Field

Type a shape idea:

* `Galaxy`
* `DNA helix`
* `Black hole`
* `Crystal`

### Buttons

* ✦ **Generate** → Creates shape
* ✕ → Clears input

### Preset Chips

Quick select:

* Galaxy
* DNA
* Klein
* Lorenz
* Supernova

---

## 🧩 5. Shape Modes

Defines the base geometry:

* **Sphere** → Radial distribution
* **Cube** → Box-based structure
* **Torus** → Donut-shaped
* **Pyramid**
* **Double Helix**
* **Möbius Strip**
* **Custom Code** → Fully programmable

---

## 🌐 6. Distribution Systems

Controls how particles are placed:

* **Lat/Lon Grid** → Earth-like mapping
* **Golden Spiral** → Natural uniform spacing
* **Random Shell** → Organic randomness
* **3D Volume Grid** → Dense cube filling
* **Flat Plane** → 2D layouts
* **Custom Logic** → JS-based control

---

## 🌊 7. Apex Effects

Applies dynamic transformations:

* **None** → No distortion
* **Apex Ripples** → Wave deformation
* **Apex Vortex** → Swirling motion
* **Pinch** → Center compression

---

## 🎨 8. Theme & Color System

### Presets

Choose from:

* Cyan Dark
* Emerald
* Crimson
* Ice Blue
* Rose Neon

### Manual Controls

* Primary Accent
* Background
* Text colors
* Borders & glow

Click **Apply & Close** to save.

---

## ✍️ 9. Drawing Pad

* Draw shapes manually
* Convert strokes into particles
* Supports:

  * Brush size
  * Depth
  * Rotation
  * Symmetry

Modes:

* PEN
* Pulsar (animated strokes)

---

## 🔤 10. Word Input

* Type text to generate particle typography
* Adjust font size
* Works best with bold words

---

## 🧬 11. Per-Particle JS Runtime

This is the core engine.

### Execution

Runs **every frame for every particle**

---

### Variables (Read-only)

* `i` → index
* `count` → total particles
* `time` → animation time
* `THREE` → math utilities

---

### Functions (Write-only)

```js
target.set(x, y, z)
color.setHSL(h, s, l)
```

---

### Helpers

```js
addControl(id, label, min, max, default)
setInfo(title, description)
annotate(id, vec3, label)
```

---

### Example: Sphere

```js
const r = addControl('r','Radius',50,300,120);

const phi = Math.acos(1 - 2*(i+0.5)/count);
const theta = i * 2.399 + time;

target.set(
  Math.sin(phi)*Math.cos(theta)*r,
  Math.sin(phi)*Math.sin(theta)*r,
  Math.cos(phi)*r
);

color.setHSL(i/count,1,0.55);
```

---

## 🎛️ 12. Particle Controls

* **PTS** → Number of particles
* **Size** → Particle size
* **Scale** → Overall shape scaling
* **Opacity**
* **Auto-Spin**
* **Turbulence**
* **Lerp Speed** → Smoothness of motion

---

## 🌌 13. Effects & Physics

* Pulse Wave
* Orbit Drift
* Wave Frequency
* Tension
* Force X/Y/Z

Used for motion dynamics.

---

## 📷 14. Media Inputs

### Image

* Upload image
* Use brightness → depth mapping

### Video

* Converts frames into particle animation

### 3D Model

Supports:

* GLB
* OBJ
* PLY
* PDB

---

## 🧍 15. Face Mesh System

* Click **Start Face Cam**
* Captures 468 facial points
* Converts into particle formation

Tip:
Hold still for 2 seconds to auto-save.

---

## 💾 16. Save & Export

* Save formations using name field
* Export configurations
* Reuse saved grids

---

## ▶️ 17. Runtime Controls

* ▶ Run → Start simulation
* ■ Stop → Pause
* Clear → Reset runtime code

Status:

* IDLE
* RUNNING

---

## 🧪 18. Performance Tips

* Keep particles under **10,000**
* Avoid heavy math inside loops
* Use `lerpSpeed` for smoother transitions
* Disable effects if lag occurs

---

## ⚠️ 19. Troubleshooting

### Nothing renders

* Ensure RUN is enabled
* Check particle count > 0

### Lagging

* Reduce particle count
* Disable turbulence

### Code not working

* Verify syntax
* Ensure `target.set()` is used

---

## 🧩 20. Best Practices

* Start simple → then add effects
* Use AI generator for inspiration
* Combine:

  * Shape + Distribution + Runtime
* Save frequently

---

## 📌 21. Keyboard & Interaction

* Drag → Rotate camera
* Scroll → Zoom
* Drag mode → Move particles manually

---

## 🔐 22. API Key Usage

* Paste Gemini/Claude API key
* Stored only in memory
* Not saved externally

---

## 🧠 23. Concept

> Every particle is independent, programmable, and alive in motion.

---

## 📞 24. Support

For improvements or issues:

* Check runtime errors
* Reset settings
* Reapply presets

---

## 📍 End of Manual

---
