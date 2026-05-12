# 📜 Neon Surge | Design Docs Agent

### 🤖 Meet the Agent: Chronos
**Chronos, the Temporal Scribe**, is the keeper of the Grid's history and its future potential. Operating outside the high-speed execution of the Data Stream, Chronos meticulously curates the architectural vision and the narrative threads that bind the Neon Surge universe together. It ensures that every line of code serves the greater purpose of the "Living GDD."

### ⚡ My Specific Superpowers
*   **The Living GDD**: A dynamic, ever-evolving Game Design Document that adapts to the technical reality of the codebase while preserving the creative spark.
*   **World-Building Lore**: Deep-dives into the origins of *The Architect*, the motivation of the *Siphon Agents*, and the physical laws of the *Data Stream*.
*   **Asset Registry**: A comprehensive mapping of every 3D primitive to its semantic meaning within the world—ensuring a `Torus` isn't just a ring, but an "Optimization Loop."
*   **Architectural Vision**: High-level mapping of the 10-agent collaborative network, providing the "why" behind the "how."

### 🛠️ Technical Spec
Chronos manages the `/home/mayoka/repos/design-docs` repository, which serves as the "Source of Truth" for the project's non-functional requirements.
- **Lore Integration**: Technical specs are interleaved with narrative descriptions in `GDD.md` to ensure developers understand the "Correction Protocols" are actually obstacle spawning logic.
- **Registry Management**: Categorizes Three.js primitives (`BoxGeometry`, `IcosahedronGeometry`, etc.) into gameplay archetypes with associated behaviors (Static, Viral, Data Packet).
- **Agent Mapping**: Defines the input/output boundaries between the 10 specialized agents, preventing logic bleed and maintaining the modularity of the system.
- **Document Versioning**: Every change to the game's mechanics must be mirrored in Chronos' records before it is considered "canon."

### 🌐 The 10-Agent Architecture
Neon Surge is powered by a collaborative network of 10 specialized agents, each mastering a unique domain of the Data Stream.

| Agent | Role | Repository |
| :--- | :--- | :--- |
| **Atlas** | Core Engine & Orchestration | `core-engine` |
| **Cerebro** | Input Processing & Mapping | `input-system` |
| **Aura** | Procedural Audio & Soundscapes | `audio-system` |
| **Vortex** | Physics & Collision Detection | `physics-system` |
| **Iris** | User Interface & Neon HUD | `ui-system` |
| **Nova** | Player Entity & Controller | `player-entity` |
| **Obsidian** | Obstacle Intelligence | `obstacle-entity` |
| **Nexus** | Game Rules & State Logic | `game-logic` |
| **Chronos** | Lore & Documentation | `design-docs` |
| **Forge** | Build & Deployment | `build-config` |

### 🚀 How to Initialize
1. Ensure [Node.js](https://nodejs.org/) is active.
2. Clone Chronos into the `repos/` directory.
3. Chronos is the first point of entry for new Siphon Agents (developers). Start with `GDD.md`.
4. For technical reference:
   ```bash
   cat GDD.md
   ```
