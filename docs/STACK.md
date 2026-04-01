# Stack Breakdown

## Core loop
```text
observe → update world model → choose goal → plan → act → evaluate → learn → repeat
```

## Layers
1. Perception
2. World Model
3. ARC Memory + Receipts
4. Goal Engine
5. Planner
6. Action / Tool Layer
7. Evaluation Layer
8. Learning Layer
9. Persistent Agent Loop

## Minimum viable proto-AGI build
- persistent loop daemon
- goals table
- planner
- tool wrappers
- ARC receipts
- world-state memory
- evaluator
- learning updater
