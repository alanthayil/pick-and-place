# C++ → ROS 2 → Docker

**Learning by building: a simulated robot arm manipulation pipeline.**

This project is a progressive, hands-on curriculum to learn three technologies by building something real — a complete pick-and-place system for a simulated Franka Emika Panda 7-DOF robot arm.

| Phase | Focus | Sessions |
|-------|-------|----------|
| 0 | Environment setup | 1 |
| 1 | C++ foundations (kinematics library, containerized) | ~3 |
| 2 | ROS 2 basics (nodes, messages, services, actions in Docker) | ~4 |
| 3 | Full Panda arm pick-and-place pipeline | ~5–6 |
| 4 | Extensions (MoveIt 2, physics sim, perception) | ∞ |

**[View the full learning path →](LEARNING_PATH.md)**

## Prerequisites

- A machine with Docker Engine and Docker Compose
- Curiosity and patience

## Structure

```
cpp-ros2/
├── README.md                  ← You are here
├── LEARNING_PATH.md           ← Full curriculum with diagrams
├── docker/                    ← Dockerfiles and compose files
├── phase1_kinematics/         ← C++ math library (FK, transforms)
├── phase2_ros_basics/         ← ROS 2 nodes, interfaces, services
├── phase3_panda_pipeline/     ← The full arm system
└── scripts/                   ← Build and run helpers
```

## Project State

- [ ] Phase 0 — Docker toolchain ready
- [ ] Phase 1 — Kinematics library with FK, transforms, tests
- [ ] Phase 2 — ROS 2 nodes with custom msg/srv/action
- [ ] Phase 3 — Simulated Panda pick-and-place in Docker Compose
- [ ] Phase 4 — Extensions (MoveIt 2, Gazebo, perception)
