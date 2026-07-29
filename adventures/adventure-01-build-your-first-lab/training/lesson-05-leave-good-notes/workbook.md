# Workbook
> **Lesson 05 · Leave Good Notes**

## Purpose

This workbook helps establish a documentation strategy before the first Adventure begins.

Rather than documenting everything, the goal is to preserve understanding, explain decisions and create a reliable source of knowledge that Future Me can build upon.

Every documentation decision should support future Adventures, reduce repeated work and make recovery, troubleshooting and learning easier.

---

# 1. Understanding Documentation

### Why is documentation an essential part of engineering?

Documentation preserves decisions, configurations and procedures that would otherwise be lost. It supports troubleshooting, reproducibility and collaboration, making it an integral part of engineering rather than an optional task completed afterwards.

---

### What is the difference between documenting actions and documenting understanding?

**Documenting actions** records what was done so a system can be recreated, maintained or troubleshooted.

**Documenting understanding** explains why decisions were made so Future Me understands the reasoning rather than simply repeating the steps.

---

### Which information is most important to preserve for Future Me, and why?

Design decisions, assumptions, configurations and troubleshooting steps are the most valuable because they explain not only how a system was built, but also why it was built that way. This reduces repeated mistakes, makes recreating the environment easier and provides a reliable reference when memory fades.

---

### Which engineering principle from this lesson stands out the most?

**Document the why, not only the what.**

Actions can often be reproduced, but understanding the reasoning behind them prevents repeating the same investigations and allows Future Me to build upon existing knowledge instead of starting from scratch.

---

# 2. Documentation Strategy

### Which types of information deserve documentation?

Any information that would be difficult to recreate or remember should be documented. This includes system specifications, configurations, design decisions, tool selection (including advantages and limitations), backup locations, troubleshooting procedures and significant changes to the environment.

---

### Which information is usually unnecessary?

Information that does not contribute to understanding, recreating or maintaining a system should generally not be documented. This includes repetitive information, temporary notes, duplicate content and personal reflections such as Campfire entries.

---

### Which decisions are most likely to be forgotten?

The reasoning behind technical decisions, configuration details, troubleshooting approaches and the root causes of solved problems are often forgotten long before the outcome itself.

---

### Which mistakes are worth documenting?

Any mistake that teaches an important lesson or could reasonably happen again should be documented. This is especially true for mistakes that affect system stability, security, recovery or future troubleshooting.

---

### Which assumptions should always be recorded?

The expected outcome, design assumptions, constraints and success criteria should always be documented. Recording assumptions makes it easier to evaluate whether an Adventure achieved its intended goal.

---

### Which documentation would be the most difficult to recreate?

Complete system setups, infrastructure configurations, troubleshooting histories and engineering decisions would be the most difficult to recreate because they are built over time through many small decisions and experiments.

---

# 3. Documentation Principles

### Which principles should guide every document?

Every document should have a clear purpose. If it doesn't help me understand, recreate, maintain or troubleshoot a system, it probably doesn't need to exist.

---

### When should documentation be updated?

Whenever reality changes. This includes major configuration changes, completed troubleshooting, infrastructure changes and improved procedures.

---

### What should documentation never become?

A knowledge dump, cluttered, outdated or difficult to navigate. It should remain structured, readable and useful to both Future Me and anyone else working with the system.

---

### How much detail is enough?

There should be enough information to understand the reasoning behind the work and to recreate the setup without relying on memory.

---

### Which writing habit should become automatic?

Capture important information while working instead of relying on memory afterwards. Whether using a text file or a physical notebook: record decisions, configurations and troubleshooting steps as they happen.

---

### Which principle best summarizes your documentation philosophy?

**Invest now, reap the benefits later.**

Good documentation requires effort in the present, but saves significant amounts of time during troubleshooting, maintenance and future Adventures.

---

# 4. Documentation Guide

### What is the purpose of your documentation and who is it written for?

The primary purpose is to make systems easy to recreate, understand and troubleshoot without relying on memory.

Documentation should be understandable to anyone with a similar technical background, but it is primarily written for Future Me.

---

### How should documentation be named and organized?

Use consistent, descriptive names that reflect the content or purpose of the document. Follow established naming conventions for virtual machines, databases, projects and files while avoiding publicly identifiable information.

Group documentation by Adventure and keep related files together. Organize documents logically and include dates only where they provide useful context.

---

### Which writing standards should every document follow?

**As little as possible, as much as needed.**

Documentation should be concise, structured and focused on understanding rather than unnecessary detail.

---

### How should documentation be maintained?

Use Git for version control whenever possible. Great opportunity to get familiar with it. 

For standalone files that are not tracked by Git, include a date or version number in the filename when appropriate. Review documentation whenever it no longer reflects reality or when a better structure would improve usability.

---

### Which aspects of your documentation system are most likely to evolve?

Folder structures, templates, naming conventions and documentation workflows will likely improve as the Field Guide grows. Any changes should make the documentation easier to maintain, navigate and understand without sacrificing useful information.

---

# 5. Documentation Toolkit

| Documentation Type | Purpose | Audience | Update Frequency | Example |
|--------------------|---------|----------|------------------|----------|
| Adventure Documentation | Record the complete engineering process of an Adventure | Future Me | During and after every Adventure | Adventure 01 |
| Field Guide | Explain engineering concepts, principles and learning objectives | Future Me | When lessons are completed or improved | Lesson 05 |
| Workbook | Capture personal decisions, reflections and engineering reasoning | Future Me | During each lesson | Lesson 05 Workbook |
| Troubleshooting Log | Record problems, root causes and solutions | Future Me | After resolving an issue | DNS troubleshooting |
| Configuration Documentation | Preserve system configurations and design decisions | Future Me | After major changes | Windows Server VM configuration |
| Backup & Recovery Documentation | Document backup locations, recovery procedures and testing | Future Me | Whenever the recovery strategy changes | Recovery Strategy |
| README | Provide a quick overview of a project or repository | Anyone | Whenever the project changes significantly | Repository README |

---

# 6. Design Decisions

### Which document will become the single source of truth?

The current Adventure's documentation and the Field Guide together.

The Field Guide defines engineering principles, standards and best practices, while the Adventure documentation records how those principles were applied. Together they provide the authoritative reference for future work.

---

### Which documentation decision gives you the most confidence?

Writing documentation alongside the work instead of afterwards.

Capturing decisions while they are fresh reduces forgotten details, improves accuracy and makes troubleshooting and recreating systems significantly easier.

---

### Which documentation should remain as simple as possible?

READMEs and project overviews.

They should provide enough context for readers to understand the purpose of a project without overwhelming them with technical details.

---

### Which documentation deserves the greatest amount of detail?

Adventure documentation.

It records the complete engineering process, including requirements, design decisions, implementation, troubleshooting, recovery and lessons learned. It should contain enough information to recreate the Adventure from scratch.

---

### Which documentation practice is most likely to evolve during future Adventures?

Templates, folder structures and documentation workflows.

As the number of Adventures grows, the documentation system should continue to evolve to remain consistent, maintainable and easy to navigate.


---

# Notes

Thoughts on **"As little as possible, as much as needed."**:

Yes, the lessons are a bit overkill for now. But I'd rather spend a little more time on the framework now so I can fully concentrate on the actual Adventures later. 

I expect less theory and more practice in the future. 

