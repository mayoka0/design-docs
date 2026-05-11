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

## World Building
**NEON SURGE** takes place within the "Data Stream"—a high-velocity conduit for a rogue superintelligence known as *The Architect*. Players assume the role of a **Siphon Agent**, a specialized digital entity tasked with infiltrating the Stream to retrieve fragmented data packets. The obstacles encountered are not random; they are **Correction Protocols** deployed by *The Architect* to purge unauthorized agents. Survival is temporary; the goal is to extract as much data (Score) as possible before the inevitable "Connection Lost" event.

## Technical Spec: 10-Agent Architecture
The development and runtime of NEON SURGE are managed by a modular 10-agent system:
1.  **Core Engine Agent**: Manages the Three.js scene, camera, and the primary rendering loop.
2.  **Game Logic Agent**: Orchestrates state transitions, game-over conditions, and speed scaling logic.
3.  **Input System Agent**: Processes keyboard and touch events, translating them into player movement commands.
4.  **Physics System Agent**: Handles collision detection algorithms and spatial mathematics for the cylindrical tunnel.
5.  **Player Entity Agent**: Controls the ship's visual representation, animations, and movement constraints.
6.  **Obstacle Entity Agent**: Manages the procedural spawning, pooling, and recycling of geometric obstacles.
7.  **Audio System Agent**: Drives the procedural synthwave audio engine and synchronizes sound effects with gameplay.
8.  **UI System Agent**: Manages the DOM-based HUD, score tracking, and the "Reboot" interface.
9.  **Build Config Agent**: Oversees the CI/CD pipeline, dependency management, and production assembly.
10. **Design Docs Agent**: Curates the architectural vision, lore expansion, and technical documentation.

## Asset Registry
Every object in the Data Stream is a geometric primitive mapped to a specific gameplay function:
- **BoxGeometry (Static Block)**: Solid barriers that represent "Corrupted Data Sectors." They must be avoided at all costs.
- **TorusGeometry (Data Ring)**: "Optimization Loops" that reward precise navigation. Passing through them provides a visual speed-blur effect.
- **IcosahedronGeometry (Rotating Hazard)**: "Viral Fragments" that rotate unpredictably, requiring split-second timing to bypass.
- **CylinderGeometry (The Tunnel)**: The physical boundary of the Data Stream, glowing with wireframe energy.
- **SphereGeometry (Data Packets)**: Planned collectible items for future progression systems.
