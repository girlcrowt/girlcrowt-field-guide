# Lesson 02

# Design Your Lab

## Why this lesson exists

Good engineers do not begin with tools.

They begin with requirements.

Before choosing virtualization software, creating virtual machines or installing an operating system, you need to understand what your Lab must allow you to do.

A Lab designed around unclear assumptions may become too limited, unnecessarily complicated or unsuitable for future Adventures.

This lesson helps you define the environment you actually need before deciding how to build it.

---

## The Question

What must my Lab be able to do in order to support this Field Guide?

---

## Learning Objectives

By the end of this lesson, you should be able to:

- explain the purpose of your learning Lab;
- identify your technical and practical requirements;
- distinguish requirements from possible solutions;
- identify constraints, risks and priorities;
- document a clear requirements profile for your Lab;
- use that profile to evaluate tools in the next lesson.

---

## Understand

Imagine someone asks:

> Which computer should I buy?

There is no useful answer without more information.

The right computer depends on what it must do, what it may cost, which software it must run and how long it should remain useful.

The same applies to your Lab.

A requirement describes what the Lab must accomplish.

A solution describes how that requirement might be fulfilled.

Example:

**Requirement**

> I need to run Windows and Linux systems at the same time.

**Possible solution**

> Use a virtualization platform that supports multiple simultaneous virtual machines.

The requirement should be defined before the solution is selected.

This keeps the decision focused on purpose rather than popularity, habit or advertising.

---

## Practice

Create a new document for your Lab requirements.

Answer the following prompts as specifically as possible.

Do not choose products yet.

Describe what the environment must be able to do.

### 1. Existing Environment

- Which physical computer will host the Lab?
- Which operating system runs on that computer?
- How much Random Access Memory (RAM) is installed?
- How much storage space is currently available?
- Which processor is installed?
- Does the processor support hardware-assisted virtualization?
- Is virtualization enabled in the Unified Extensible Firmware Interface (UEFI) or Basic Input/Output System (BIOS)?
- Which other devices could become part of the Lab later?
- Which existing hardware must not be modified or endangered?

### 2. Intended Use

- Which technologies do you expect to explore during the next twelve months?
- Will the Lab need to run Windows systems?
- Will it need to run Linux systems?
- Will Windows and Linux need to run simultaneously?
- Will you need client and server systems?
- Will you need multiple machines communicating with one another?
- Will you practise networking, Domain Name System (DNS), directory services, databases, automation or cloud integration?
- Will the Lab need access to the internet?
- Will some systems need to remain isolated from the internet?
- Will you need to recreate workplace-like environments?

### 3. Safety and Isolation

- Which experiments could damage your everyday computer if performed directly on it?
- Which personal files or applications must remain protected?
- Must Lab systems be isolated from your home network?
- Must individual Lab systems be isolated from one another?
- How quickly should you be able to undo a failed experiment?
- What should happen if a virtual machine becomes unusable?
- Which parts of the Lab must be recoverable from backup?
- What would an acceptable worst-case failure look like?

### 4. Persistence and Recovery

- Which systems should remain available for future Adventures?
- Which systems may be temporary?
- Which configurations must be documented?
- Will you need snapshots before making risky changes?
- Will snapshots alone be sufficient?
- Which files require an independent backup?
- Where will backups be stored?
- How will you verify that recovery actually works?
- How much rebuilding would be acceptable after a failure?

### 5. Resources and Constraints

- What budget is available?
- Which existing hardware should be reused?
- How much storage can be dedicated to the Lab?
- How much memory can the Lab use without affecting everyday work?
- How much time can be spent maintaining the Lab?
- Are there software licensing restrictions?
- Are there electricity, noise, heat or space constraints?
- Must the Lab remain portable?
- Must it work without purchasing additional hardware?

### 6. Usability and Maintenance

- How easy must it be to create a new test system?
- How quickly should a system be reset or rebuilt?
- How will systems be named?
- How will configurations be documented?
- How will completed work be versioned?
- How will you know which systems are active, archived or disposable?
- How much manual maintenance is acceptable?
- Which recurring tasks should eventually be automated?

### 7. Future Growth

- Which future Adventures are already foreseeable?
- Could the Lab later include dedicated physical hardware?
- Could it later include a hypervisor host such as Proxmox Virtual Environment?
- Could it later connect to Microsoft Azure, Amazon Web Services or another cloud platform?
- Could it later include containers?
- Could it later support monitoring, central authentication or automated deployment?
- Which decisions made today must remain easy to change later?

---

## Prioritize

Classify every requirement using these categories:

### Must Have

Without this requirement, the Lab cannot fulfil its purpose.

### Should Have

This requirement is important, but the Lab could initially operate without it.

### Could Have

This would improve the Lab but is not currently necessary.

### Not Needed Yet

This may become relevant later but does not belong in the first version.

Example:

| Requirement | Priority | Reason |
|---|---|---|
| Run Windows and Linux simultaneously | Must Have | Required for cross-platform Adventures |
| Restore a system after a failed configuration | Must Have | Experiments must be reversible |
| Dedicated physical server | Not Needed Yet | Existing hardware is sufficient for Version 1 |
| Cloud integration | Could Have | Relevant later, but not required for the first Lab |

---

## Define Your Requirements Profile

Summarize your findings.

```markdown
# Lab Requirements Profile

## Purpose

Describe why the Lab exists.

## Existing Environment

Document the available hardware, host operating system and relevant limitations.

## Must-Have Requirements

- 
- 
- 

## Should-Have Requirements

- 
- 
- 

## Could-Have Requirements

- 
- 
- 

## Not Needed Yet

- 
- 
- 

## Risks

- 
- 
- 

## Constraints

- 
- 
- 

## Open Questions

- 
- 
- 
```

Do not remove unresolved questions.

An open question is not a failure.

It identifies where further investigation is required.

---

## Prepare

In the next lesson, you will compare possible tools against this requirements profile.

You will not ask:

> Which virtualization platform is best?

You will ask:

> Which available solution satisfies my requirements with the fewest unacceptable trade-offs?

Keep your requirements profile nearby.

It will become the basis for your technical decisions.

---

## Campfire

Before moving on, reflect on the requirements process.

- Which requirement became visible only after working through the prompts?
- Which assumption did you discover?
- Which requirement is most important to the safety of the Lab?
- Which requirement is most important to future growth?
- Which desired feature is not actually necessary yet?
- Where are you at risk of choosing a tool because it is popular rather than suitable?
- Which questions still require research?
- What would cause you to revise this requirements profile later?

---

## Looking Ahead

You now know what your Lab must accomplish.

The next step is to evaluate the available tools and assemble a toolkit that fits those requirements.
