# Game Design Document: NEON SURGE

## Overview
**NEON SURGE** is a fast-paced, 3D infinite runner built with Three.js. Players navigate a sleek, glowing craft through a procedural neon tunnel, dodging geometric obstacles while the speed increases indefinitely.

## Core Loop
1. **Pilot:** Control a craft in a 3D cylindrical space.
2. **Evade:** Dodge obstacles (Cubes, Rings, Icosahedrons) spawned procedurally.
3. **Survive:** Maintain speed as the game accelerates.
4. **Repeat:** Each run aims to surpass the previous high score.

## Controls
- **WASD or Arrow Keys:** Move the craft Up, Down, Left, and Right.
- **R (Reboot):** Restart the game after a collision.
- **Constraints:** Movement is restricted to the inner radius of the tunnel.

## Visual Style
- **Synthwave Aesthetic:** A dark void illuminated by vibrant neon wireframes.
- **Procedural Geometry:** No external assets; all objects are generated from Three.js primitives.
- **Dynamic Lighting:** A point light follows the player, casting a glow on passing obstacles.
- **Fog:** Exponential fog is used to create depth and a sense of mystery in the infinite tunnel.

## Progression
- **Linear Acceleration:** Speed increases continuously at a rate of 0.0001 per frame.
- **Scoring:** Points are awarded for every obstacle successfully passed.
- **Visual Feedback:** The score and current speed multiplier are displayed in a real-time HUD.

## Technical Implementation
- **Framework:** Three.js
- **Build Tool:** Vite
- **Assets:** 100% Code-based (BoxGeometry, TorusGeometry, CylinderGeometry, etc.)
