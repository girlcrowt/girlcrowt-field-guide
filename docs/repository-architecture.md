# Repository Architecture

> *Version 1.1*

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
├── build.md
├── learning-architecture.md
├── repository-architecture.md
└── roadmap.md

adventures/
└── adventure-name/
    ├── README.md
    ├── training/
    ├── mission/
    ├── build/
    ├── field-notes/
    ├── realizations/
    ├── campfire.md
    ├── systems/
    ├── relationships/
    ├── communication/
    ├── trust/
    ├── expression/
    ├── knowledge/
    └── evaluation/

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
- Build
- Roadmap

---

## adventures/

Contains the Main Adventures.

Each Adventure represents one meaningful expedition.

---

## realms/

Contains Realm-specific documentation and Side Adventures.

The Realms are persistent.

Adventures move through them.

---

## templates/

Contains reusable templates.

Examples:

- Adventure
- Training Lesson
- Mission Phase
- Field Notes
- Realizations
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
├── Mission
├── Build
├── Field Notes
├── Realizations
├── Campfire
│
├── Systems
├── Relationships
├── Communication
├── Trust
├── Expression
├── Knowledge
└── Evaluation
```

Every Adventure progresses through a consistent sequence.

```text
Challenge
    ↓
Training
    ↓
Mission
    ↓
Build
    ↓
Field Notes
    ↓
Realizations
    ↓
Campfire
```

The Realm folders are different.

They are not stages.

They are persistent perspectives through which every Adventure is explored.

---

# Adventure Contract

Every Main Adventure follows the same contract.

The contract creates consistency across the Field Guide while allowing every Adventure to tell a different story.

Consistency creates confidence.

The learner should always know where they are.

The challenge changes.

The structure does not.

Each stage has one responsibility.

- Training develops understanding.
- Mission creates the artifact.
- Build preserves the artifact.
- Field Notes preserve the journey.
- Realizations preserve transferable wisdom.
- Campfire preserves personal growth.

Every document exists for one reason only.

Clear responsibilities create clear thinking.

---

## Adventure Metadata

Every Adventure begins with a short overview.

It answers:

- Should I start this Adventure?
- What will I build?
- What do I need beforehand?

Metadata includes:

- Difficulty
- Estimated Effort
- Primary Realms
- Artifacts Produced
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

Training develops understanding before implementation begins.

Each lesson follows the same rhythm:

- Understand
- Practice
- Create the Artifact
- Prepare
- Campfire
- Looking Ahead

---

## Mission

The Mission transforms preparation into reality.

Implementation is divided into clearly defined phases.

Each phase follows the same Mission Call Sheet.

---

## Mission Call Sheet

**Objective**

What is the goal of this phase?

---

**Inputs**

What should already exist before starting?

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

Which Realm perspectives are most active during this phase?

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

The Build preserves the completed artifact.

It captures what now exists because the Mission was completed.

The Build is evidence, not process.

---

## Field Notes

Field Notes preserve the journey.

They record:

- context
- actions
- observations
- decisions
- problems
- evidence
- changes
- open questions
- next steps

---

## Realizations

Realizations preserve transferable wisdom.

They capture principles rather than implementation details.

A good Realization remains useful even if the underlying technology changes.

---

## Campfire

Campfire preserves personal growth.

It is not a technical review.

It is a conversation with yourself after the Adventure has ended.

---

## World Impact

Every Adventure changes the world.

Document:

### Added

What now exists?

### Changed

What became different?

Every completed Adventure should leave the world richer than it found it.

---

# Documentation Philosophy

Documentation is part of the learning process.

It is written for Future Me.

Clear documentation is an act of kindness to Future Me.

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
- Every stage answers one question.
- Documentation is part of the artifact.
- The repository should remain approachable.
- Build the world one Adventure at a time.
- The Field Guide provides orientation without imposing pace.
