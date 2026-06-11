# Pick-and-Place Learning Project

## Project Goal

Learn C++, ROS 2, and Docker by building a complete pick-and-place pipeline for a simulated Franka Emika Panda 7-DOF robot arm. This is a **learning-by-building** project — the code is a means to the understanding, not the end goal.

## Working Agreement (Learning Partnership)

The user drives, Claude navigates and explains. This ensures real learning, not passive code generation.

📖 **Start here:** [learning-playbook.md](learning-playbook.md) — a practical guide on how to learn with the AI, including conversation patterns, modes (Explain/Show me/Review), and checkpoint criteria.

### Roles

| User | Claude |
|------|--------|
| Declares intent ("I want to build X") | Asks scaffolding questions first |
| Writes headers, high-level structure, test cases | Fills in boilerplate with explanation |
| Writes CMake targets and Dockerfiles (with guidance) | Fixes syntax, explains *why* each line is needed |
| Asks "why?" on anything | Explains concepts, points to docs |
| Decides when a step is "done" | Reviews for correctness, edge cases, style |

### Modes (user picks)

- **"Explain mode"** — Claude describes what needs to happen and why, user writes the code.
- **"Show me"** — Claude writes it with line-by-line narration.
- **"Review this"** — User writes it, Claude critiques.

### What Claude avoids

- Writing entire files from scratch without explanation (unless explicitly asked)
- Moving on before the user is comfortable with current concepts
- Using "magic" library features without explaining them

### Checkpoint Policy

Before moving to the next step, the user should be able to explain:
1. What each file does and why it exists
2. How the build system (CMake) ties them together
3. What each Docker layer contributes
4. The key C++/ROS 2 concepts introduced in that step

---

## Project Conventions

### Repository Structure
- `docker/` — Dockerfiles and compose files
- `phase1_kinematics/` — C++ math library (FK, transforms)
- `phase2_ros_basics/` — ROS 2 nodes, interfaces, services
- `phase3_panda_pipeline/` — Full arm system
- `scripts/` — Build and run helpers

### Build & Test
- All compilation happens inside Docker containers
- Tests run via `docker compose run --rm test`
- Multi-stage Docker builds: builder stage (full toolchain) → runtime stage (minimal)

### Code Style
- C++17/20, `namespace kinematics`, `#include` guards
- Tests use GTest
- ROS 2 nodes use `rclcpp` with `ament_target_dependencies()`

### Phase State
See README.md for current progress checklist.
