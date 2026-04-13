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

Cheat Sheet

PROJECT: P.U.L.S.E

CREATOR: Pragath (Pragon)

INPUT:
• Prompt
• Drawing
• Code

PROCESS:
• Gemini API → Particle Logic
• JS Runtime Engine

RENDER:
• Three.js + WebGL

OUTPUT:
• Real-time 3D Simulation

FEATURES:
• AI Generation
• Interactive Control
• Code Export

USE:
• Art
• VFX
• Web Development
• Education
