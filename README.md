# Proto-AGI Stack
### Persistent, Goal-Driven Intelligence Architecture

> A practical architecture for moving from a local assistant/controller toward a persistent, memory-backed, tool-using proto-AGI loop.

![Status](https://img.shields.io/badge/status-architecture%20spec%20%2B%20active%20implementation-8b5cf6)
![Focus](https://img.shields.io/badge/focus-proto--agi%20stack-22d3ee)
![Runtime](https://img.shields.io/badge/runtime-persistent%20agent%20loop-22c55e)

---

## Overview

This project defines a **public-facing proto-AGI architecture** built around a persistent operating loop:

```text
observe → update world model → choose goal → plan → act → evaluate → learn → repeat
```

The stack is designed to connect:

- a **local assistant/controller**
- an **ARC-style memory + receipt system**
- a **goal engine**
- a **planner**
- a **tool/action layer**
- a **learning + evaluation loop**
- a **persistent runtime**
- and optional **simulation / deterministic runtime modules**

The goal is not to make inflated AGI claims.  
The goal is to define the shortest real path from a capable assistant stack to a serious **proto-AGI system**.

### Current implementation path

This repository is the **architecture/spec repo** for that direction.

The main public implementation and testing vehicle for this architecture is:

- **arc-lucifer-cleanroom-runtime**: https://github.com/GareBear99/arc-lucifer-cleanroom-runtime

That runtime repo is being used to test and harden the practical substrate for this stack, including:

- persistent directives and runtime flow
- memory, archive, and receipt behavior
- validation and verifier surfaces
- self-improvement / repair scaffolding
- optional adapter contracts for future perception / robotics layers

So this repo defines **what is being built**, while the cleanroom runtime repo is where the architecture is being turned into a real working substrate and testbed.

---

## Why this exists

Most “AI assistant” systems are still:

- prompt-response driven
- session-fragile
- weak at long-horizon planning
- weak at memory
- weak at self-evaluation
- weak at improvement over time

A proto-AGI stack needs more than model calls. It needs a **system**.

---

## Full Stack

## 1. Perception Layer
Handles incoming input and converts it into usable state.

Includes:
- text understanding
- code understanding
- structured data parsing
- file inspection
- future multimodal inputs

**Implementation note:** perception should remain **optional and modular**. The base runtime should not require cameras, robotics, audio, or multimodal dependencies unless those adapters are explicitly enabled.

---

## 2. World Model
Maintains structured understanding of:

- projects
- tools
- environment state
- active branches
- known facts
- causal relationships

This is where the system stops being a chatbot and starts maintaining an internal representation of reality.

---

## 3. ARC Memory + Receipts
Operational memory system with provenance.

### Memory classes
- **Episodic** — what happened
- **Semantic** — what is true
- **Procedural** — how to do things
- **Strategic** — what tends to work

### Receipt role
Every action should emit:
- cause
- tool used
- inputs
- outputs
- success/failure
- branch/session lineage
- confidence / trust

**Implementation note:** the current runtime work is explicitly moving toward stronger archive behavior, branch-aware lineage, and receipt-backed runtime memory as the real substrate for future autonomous loops.

---

## 4. Goal Engine
Creates and tracks active goals.

A real proto-AGI system needs:
- goal creation
- priority scoring
- decomposition into subgoals
- completion criteria
- conflict resolution

---

## 5. Planner
Turns goals into executable graphs.

Planner responsibilities:
- decompose goals
- estimate step cost
- estimate success likelihood
- choose tool path
- branch when useful
- revise plans after failure

**Implementation note:** in the runtime direction, the model core should act as a **planner/executive over structured state**, not as a raw low-level control loop.

---

## 6. Action / Tool Layer
The system must act, not just answer.

Examples:
- shell commands
- scripts
- file operations
- build pipelines
- package/export flows
- API calls
- wrapped external tools

---

## 7. Evaluation Layer
After every action, the system should ask:

- did this help the goal?
- what actually happened?
- what failed?
- what should be remembered?

Without this, the system does not improve.

---

## 8. Learning Layer
The stack should update itself over time by:

- promoting repeated successful procedures
- adjusting planner/tool weights
- reducing repeated mistakes
- improving future goal execution

This is not “magic self-rewrite.”  
It is structured improvement through memory and evaluation.

**Implementation note:** learning should be promoted through verified candidate policies, receipts, replay, and bounded improvement paths rather than uncontrolled self-modification.

---

## 9. Persistent Agent Loop
The defining runtime layer.

```text
while alive:
  observe()
  update_world_model()
  select_goal()
  plan_steps()
  execute_next_action()
  evaluate_result()
  write_receipt()
  update_memory()
  repeat()
```

This is the transition from:
- assistant
to:
- operating intelligence

---

## Suggested System Composition

A practical stack can be assembled from components like:

- **Local assistant/controller** → interface + routing + tool shell
- **ARC-style core** → memory + receipts + world-state substrate
- **Planner module** → structured goal decomposition
- **Persistent loop daemon** → continuity across time
- **Tool execution layer** → shell / API / file / workflow control
- **Deterministic runtime / turbo execution layer** → optional performance substrate
- **Simulation/world-model sandbox** → optional policy testing + controlled learning
- **Optional perception / embodiment adapters** → attachable vision, audio, robotics, or desktop-control layers when enabled

---

## Where deterministic runtimes and Turbo OS fit

Deterministic execution, branch-aware runtimes, and resolved-output jumping can strengthen the stack by making it:

- more reproducible
- more inspectable
- more efficient
- better at branch comparisons
- better at session continuity

These systems are **substrates**, not the intelligence itself.

---

## Where simulation fits

Simulation should be treated as:

- a world-model module
- a policy sandbox
- a branch testing environment
- an environment for controlled learning

It should **not** be mistaken for AGI by itself.

---

## Build Order

### Phase 1
- persistent loop daemon
- goal table
- ARC receipt store
- world-state updates
- runtime validation spine

### Phase 2
- planner
- tool wrappers
- evaluation layer
- receipt-driven memory updates

### Phase 3
- learning updates
- strategic memory
- branch-aware execution
- repair / self-improvement scaffolding

### Phase 4
- deterministic runtime integration
- simulation-backed world-model modules
- optional perception / robotics adapters
- stronger autonomy controls

---

## What counts as a real proto-AGI milestone?

The system can:

1. accept a high-level goal  
2. break it into subgoals  
3. choose tools  
4. execute across multiple steps  
5. detect failure  
6. revise its plan  
7. remember what worked  
8. improve future runs  

without requiring full manual steering at every step.

---

## Repository Links

Public repos associated with this direction:

- **arc-lucifer-cleanroom-runtime**: https://github.com/GareBear99/arc-lucifer-cleanroom-runtime
- **LuciferAI_Local**: https://github.com/GareBear99/LuciferAI_Local
- **ARC-Core**: https://github.com/GareBear99/ARC-Core
- **Proto-Synth Grid Engine**: https://github.com/GareBear99/Proto-Synth_Grid_Engine
- **Seeded Universe Recreation Engine**: https://github.com/GareBear99/Seeded-Universe-Recreation-Engine
- **ARC Turbo OS**: https://github.com/GareBear99/ARC-Turbo-OS
- **Arc-RAR**: https://github.com/GareBear99/Arc-RAR

---

## Documentation

- [Public HTML architecture overview](docs/proto_agi_stack_public_overview.html)
- [Stack breakdown](docs/STACK.md)
- [SEO / public positioning notes](docs/SEO_NOTES.md)

---

## SEO / Discovery Terms

Relevant terms for discoverability:

- proto agi architecture
- persistent agent loop
- local ai controller
- agent memory system
- ARC receipts
- goal-driven ai runtime
- planner + tool use architecture
- deterministic runtime for agents
- branch-aware execution
- local ai operating intelligence

---

## Public-facing summary

> Proto-AGI starts when a system can pursue goals across time, not just answer prompts.

This project documents a persistent, memory-backed, goal-driven intelligence architecture that combines world modeling, planning, action, evaluation, and learning into one operating loop.

**arc-lucifer-cleanroom-runtime** is the main public implementation repo currently being used to test and harden the runtime substrate for this direction.

---

## License

Choose your license and update this section.
