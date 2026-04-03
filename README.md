# Proto-AGI
### Architecture direction and test-build map for the ARC / Lucifer runtime line

> This repository documents the direction being built and tested through the public runtime work, rather than claiming that full AGI already exists.

![Status](https://img.shields.io/badge/status-direction%20%2B%20test%20map-8b5cf6)
![Focus](https://img.shields.io/badge/focus-persistent%20proto--agi%20loop-22d3ee)
![Implementation](https://img.shields.io/badge/implementation-arc--lucifer%20runtime-22c55e)

---

## What this repo is

**Proto-AGI** is the architectural map for a persistent, memory-backed, goal-driven intelligence system.

It describes the operating loop, subsystems, and milestones needed to move from:

- local assistant
- to persistent controller
- to tool-using autonomous runtime
- to a more serious proto-AGI substrate

This repository is the **direction/spec repo**.

The main public build being used to **test and implement this direction** is:

- [arc-lucifer-cleanroom-runtime](https://github.com/GareBear99/arc-lucifer-cleanroom-runtime)

That runtime repo is where the practical work is being hardened:
- memory and archive behavior
- directives and receipts
- validation and verifier patterns
- repair/self-improvement scaffolding
- optional perception / embodiment adapters
- public runtime packaging and operator-facing docs

So the clean way to read this repo is:

- **this repo** = what is being built conceptually
- **arc-lucifer-cleanroom-runtime** = the current public implementation/test vehicle for that direction

---

## Core loop

```text
observe → update world model → choose goal → plan → act → evaluate → learn → repeat
```

That loop is the minimum useful transition from a prompt-response assistant to a system that can pursue work across time.

---

## Why this repo exists

Most assistant projects still stop at:

- prompt in
- response out
- weak memory
- weak continuity
- weak planning
- weak self-evaluation
- weak improvement over time

A proto-AGI path needs a fuller machine shape:

- perception or structured observation
- world-state tracking
- memory with provenance
- goal creation and prioritization
- planning and replanning
- tool execution
- evaluation after action
- learning from outcomes
- persistent runtime continuity

This repo exists to define that shape clearly.

---

## What is being built and tested in the runtime repo

The linked runtime repo is being used to test the practical substrate for this direction.

### Current emphasis
- persistent runtime behavior
- bounded command/action surfaces
- memory + archive discipline
- receipts / provenance
- rollback / replay thinking
- validation and verifier layers
- self-improvement scaffolding
- optional adapters for vision, audio, robotics, and embodiment

### Important framing
The runtime repo is **not** claiming that complete AGI or a living machine already exists.

It is being built as:
- a serious autonomy foundation
- a testbed for the proto-AGI loop
- a place to harden real architecture before stronger cognition and embodiment layers are attached

---

## System layers

## 1. Perception Layer
Handles incoming input and converts it into usable state.

Examples:
- text
- code
- files
- structured data
- future multimodal inputs
- optional vision/audio/robotics adapters

Important:
Perception should be **optional and modular**, not a required dependency for the whole runtime.

---

## 2. World Model
Maintains structured understanding of:

- projects
- tools
- environment state
- active branches
- known facts
- causal relationships
- current task context

This is where the system starts maintaining reality as state instead of only generating replies.

---

## 3. ARC Memory + Receipts
Operational memory system with provenance.

### Memory classes
- **Episodic** — what happened
- **Semantic** — what is true
- **Procedural** — how to do things
- **Strategic** — what tends to work

### Receipt role
Every meaningful action should emit evidence such as:
- cause
- tool used
- inputs
- outputs
- success/failure
- branch/session lineage
- confidence / trust

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
- optional embodied action adapters

---

## 7. Evaluation Layer
After every action, the system should ask:

- did this help the goal?
- what actually happened?
- what failed?
- what should be remembered?

Without this layer, the system does not improve.

---

## 8. Learning Layer
The stack should update itself over time by:

- promoting repeated successful procedures
- adjusting planner/tool weights
- reducing repeated mistakes
- improving future goal execution

This is not “magic self-rewrite.”
It is structured improvement through memory, evaluation, verification, and staged promotion.

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

That is the loop the runtime repo is being shaped to support and test over time.

---

## How this repo relates to arc-lucifer-cleanroom-runtime

| Repo | Role |
|---|---|
| **Proto-AGI** | architectural direction, milestone framing, public map of the intended system |
| **arc-lucifer-cleanroom-runtime** | implementation/testbed for the runtime substrate being built to validate that direction |

### In plain language
This repo says:
- **what the machine should become**

The runtime repo tests:
- **how much of that can be made real cleanly, modularly, and credibly**

---

## Suggested system composition

A practical stack can be assembled from components like:

- **Runtime/controller layer** → interface + routing + tool shell
- **ARC-style core** → memory + receipts + world-state substrate
- **Planner module** → structured goal decomposition
- **Persistent loop daemon** → continuity across time
- **Tool execution layer** → shell / API / file / workflow control
- **Deterministic runtime / branch-aware substrate** → optional reproducibility and replay strength
- **Simulation/world-model sandbox** → optional policy testing and controlled learning
- **Perception / embodiment adapters** → optional vision, audio, robotics, and physical action surfaces

---

## Build order

### Phase 1
- persistent loop daemon
- goal table
- ARC receipt store
- world-state updates

### Phase 2
- planner
- tool wrappers
- evaluation layer

### Phase 3
- learning updates
- strategic memory
- branch-aware execution

### Phase 4
- optional perception adapters
- optional embodiment adapters
- stronger autonomy controls
- simulation-backed world-model modules

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

## Documentation

- [Stack breakdown](docs/STACK.md)
- [Public overview HTML](docs/proto_agi_public_overview.html)
- [Detailed stack HTML](docs/proto_agi_stack.html)
- [SEO / public positioning notes](docs/SEO_NOTES.md)

---

## Related public repos

- [arc-lucifer-cleanroom-runtime](https://github.com/GareBear99/arc-lucifer-cleanroom-runtime)
- [LuciferAI_Local](https://github.com/GareBear99/LuciferAI_Local)
- [ARC-Core](https://github.com/GareBear99/ARC-Core)
- [Proto-Synth Grid Engine](https://github.com/GareBear99/Proto-Synth_Grid_Engine)
- [Seeded Universe Recreation Engine](https://github.com/GareBear99/Seeded-Universe-Recreation-Engine)
- [ARC Turbo OS](https://github.com/GareBear99/ARC-Turbo-OS)
- [Arc-RAR](https://github.com/GareBear99/Arc-RAR)

---

## Public-facing summary

> Proto-AGI starts when a system can pursue goals across time, not just answer prompts.

This repo documents the architecture direction.
The linked ARC/Lucifer cleanroom runtime is the main public repo being built to test and harden that direction in practice.

---

## License

Choose your license and update this section.
