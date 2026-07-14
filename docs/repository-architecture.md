# Repository Architecture

> *Version 1.0*

This document defines how the girlcrowt Field Guide is organized.

Unlike the Learning Architecture, which describes *how learning works*, the Repository Architecture describes *how that learning is represented inside the repository.*

Its purpose is consistency.

Every Adventure should feel familiar.

Every document should have an obvious home.

Every artifact should be easy to find.

---

# Guiding Principles

The repository should reflect the learning journey.

The folder structure exists to support learning, not the other way around.

When a document has more than one responsibility, split it.

Nothing meaningful is ever wasted.

---

# Repository Structure

```text
README.md

docs/
├── learning-architecture.md
├── repository-architecture.md
└── roadmap.md

adventures/
└── adventure-name/
    ├── README.md
    ├── training/
    ├── systems/
    ├── relationships/
    ├── communication/
    ├── trust/
    ├── expression/
    ├── knowledge/
    ├── evaluation/
    ├── build/
    ├── field-notes/
    ├── realizations/
    └── campfire.md

realms/

templates/

resources/
```

The structure may evolve as the Field Guide grows.

Consistency matters more than perfection.

---

# Repository Responsibilities

## README

Introduces the Field Guide.

Answers:

> **What is this?**

---

## docs/

Contains documentation about the Field Guide itself.

Examples:

- Learning Architecture
- Repository Architecture
- Roadmap

---

## adventures/

Contains the Main Adventures.

Each Adventure represents one meaningful mission.

---

## realms/

Contains Realm-specific documentation and Side Adventures.

The Realms are persistent.

The Adventures move through them.

---

## templates/

Contains reusable templates.

Examples:

- Adventure README
- Training Lesson
- Field Notes
- Campfire

---

## resources/

Reference material.

Examples:

- Cheat sheets
- External resources
- Reference diagrams
- Useful assets

---

# Adventure Structure

Every Main Adventure follows the same structure.

```text
Adventure

README
│
├── Training
├── Systems
├── Relationships
├── Communication
├── Trust
├── Expression
├── Knowledge
├── Evaluation
├── Build
├── Field Notes
├── Realizations
└── Campfire
```

The structure remains familiar.

The challenge changes.

---

# Adventure Contract

Every Main Adventure follows the same contract.

The contract creates consistency across the Field Guide while allowing every Adventure to tell a different story.

Consistency creates confidence.

The learner should always know where they are.

The challenge changes.

The structure does not.

---

## Adventure Metadata

Every Adventure begins with a short overview.

It answers:

- Should I start this Adventure?
- What will I build?
- What do I need beforehand?

Metadata includes:

- Difficulty
- Estimated Time
- Primary Realms
- Artifact
- Prerequisites
- Required World State
- World State Added

---

## Brief

Introduces the Adventure.

Answers:

- What are we building?
- Why does it matter?
- What will exist afterwards?
- Who will I become?

---

## Challenge Scenario

Presents the real-world problem.

The learner understands why the Adventure exists before learning how to solve it.

---

## Success Criteria

Defines when the Adventure is complete.

Success should be measurable by evaluating the system rather than evaluating the learner.

---

## Training

Training prepares the learner for the Mission.

Each Training section follows the same rhythm:

- Understand
- Practice
- Prepare

---

## Mission

The practical work of the Adventure.

This is where the learner builds the solution.

---

## Mission Call Sheet

**Objective**

What is the goal of this phase?

---

**Inputs**

What should already exist before starting?

Examples:

- Lab Requirements Profile
- Toolkit Decision Record
- Recovery Strategy

---

**Outputs**

What should exist when this phase is complete?

---

**Estimated Effort**

A rough indication of scope, not a deadline.

---

**Difficulty**

Beginner | Intermediate | Advanced

---

**Primary Realms**

Systems • Trust

---

**Engineering Principles**

Which principles should guide the work?

---

**Success Criteria**

How do I know this phase is complete?

---

**World State Updated**

What permanently changes after this phase?

---

## Build

Every Adventure produces a real artifact.

The artifact becomes part of the persistent world.

---

## Field Notes

The engineering notebook.

Every Field Note should capture:

- Goal
- Approach
- Mistakes
- Fixes
- Observations
- Sources
- Next Time

---

## Realizations

Capture transferable understanding.

Record principles rather than isolated facts.

---

## World Impact

Every Adventure updates the persistent world.

Document:

### Added

What now exists?

### Changed

What became different?

---

## Campfire

Reflection completes the Adventure.

Suggested prompts:

- What surprised me?
- What frustrated me?
- What am I proud of?
- What would Future Me thank me for?
- Where do I see today's lesson appearing elsewhere?

---

# Documentation Philosophy

Documentation is part of the learning process.

It is written for Future Me.

Clear documentation is an act of kindness to the next explorer.

---

# Commit Philosophy

Commits describe meaningful changes.

Prefer:

- Refactor...
- Define...
- Expand...
- Create...

over

- Update stuff
- Changes
- Fix

Every commit should tell part of the Field Guide's story.

---

# Naming Philosophy

Choose names that describe purpose rather than implementation.

Good:

> Build Your First Lab

Poor:

> VirtualBox Exercise

The challenge should outlive the technology.

---

# Design Principles

- Repository follows learning.
- Consistency over cleverness.
- Split responsibilities.
- Documentation is part of the artifact.
- The repository should remain approachable.
- Build the world one Adventure at a time.
- The Field Guide provides orientation without imposing pace.
