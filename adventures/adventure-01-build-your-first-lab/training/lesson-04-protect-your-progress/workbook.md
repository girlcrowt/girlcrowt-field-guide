# Workbook
> **Lesson 04 · Protect Your Progress**

## Purpose

This workbook helps design a recovery strategy before the first Adventure begins.

Rather than assuming nothing will go wrong, the goal is to prepare for failure, recover quickly and continue learning with confidence.

Every recovery decision should be supported by the documented Lab requirements, Toolkit decisions and realistic failure scenarios.

---

# 1. Understanding Recovery

### Why is recovery more important than prevention?

Generally speaking, we don't know what we don't know. And being fairly new to the entire field of IT I know that the things I don't know clearly surpass the things I do know. 

So, in the spirit of **"Break it 'til you get it"** I'd like to be able to accidentally wreck my setup without having to rebuild it from scratch over and over and over again. 

Hence, a **Recovery Strategy** must be determined!

---

### What is the difference between prevention and recovery?

I can only attempt to prevent what I know may need to be prevented. 

With recovery I can make an educated decision about going back to the Last Known GOod Configuration after making an educated decision about restoring a responsibly created backup or snapshot.

---

### What is the difference between confidence and certainty?

Certainty means believing nothing will go wrong.

Confidence means knowing that if something does go wrong, I can recover.

Recovery doesn't create certainty.

It creates confidence.

---

### Why do experienced engineers prepare for failure?

It's inevitable. 

If my time in TV has taught me anything it's this: 

> **Reality writes the most absurd stories.**

My point is, you need to be prepared. Not for the cause but for the result. And results are much easier to evaluate. 

You literally ask: What's the worst that could happen. And then you find ways to prevent it by playing a few rounds of "What if...?".

---

### How does recovery create confidence?

If I know I can simply go back to the **Last Known Good Configuration**, I'm less reserved about experimenting, troubleshooting and exploring system limits.

Mistakes become learning opportunities instead of disasters.

---

### Which engineering principle from this lesson stands out the most?

Recovery strategy: designing backup and recovery procedures—including **RPO (Recovery Point Objective)** and **RTO (Recovery Time Objective)**—before experimentation begins.

---

# 2. Failure Analysis

### Which failures are most likely to occur in your Lab?

- Exceeding available hardware resources, particularly memory, storage or CPU capacity
- Typos while configuring services such as DNS
- Incorrect software or operating system configurations
- Accidentally deleting files, snapshots or virtual machines
- Breaking a system while experimenting with new technologies
- Forgetting to document configuration changes

---

### Which failures would have the greatest impact?

- Failure of the host computer or its storage device
- Loss or corruption of documentation
- Permanent loss of files without a working backup
- Hardware failure requiring replacement of the host system

---

### Which failures are acceptable?

- Virtual machines becoming unusable
- Databases becoming corrupted or unusable
- Failed software installations
- Broken operating system configurations inside virtual machines
- Any failure that can be recovered through snapshots, backups or rebuilding the virtual machine

---

### Which failures are unacceptable?

- Permanent loss of documentation
- Permanent loss of important files stored on the host
- Losing the ability to recover because backups fail or do not exist
- Any failure that directly affects the host system without a recovery path

---

### Which failures can be reversed within minutes?

- Restoring a virtual machine snapshot
- Restoring a database backup
- Rolling back configuration changes
- Recovering files through version control

---

### Which failures would require rebuilding part of the Lab?

- Failure of the host operating system
- Host hardware failure
- Migration to a newer operating system such as Windows Server 2025
- Corruption that cannot be recovered through snapshots or backups

---

### Which failures could permanently destroy data?

- Host storage failure without a working backup
- Hardware failure affecting storage devices
- File corruption that propagates into all available backups
- Accidental deletion of files that were never backed up

---

### Which failures would mainly cost time rather than information?

- Rebuilding a virtual machine from scratch
- Reinstalling an operating system
- Reconfiguring services after failed experiments
- Recreating databases from documented procedures


---

# 3. Scenario Analysis

## Scenario 1 — Accidental VM Deletion

### What happened?

A virtual machine was accidentally deleted while cleaning up old systems or managing virtual machine files.

---

### What was lost?

- The operating system installation
- Installed software
- Configuration changes
- Data stored only inside the virtual machine since the last backup or snapshot

---

### How could it have been prevented?

- Clearly naming and documenting virtual machines
- Separating active and archived virtual machines
- Verifying the selected virtual machine before deletion
- Creating snapshots or backups before major cleanup tasks

---

### How could it have been recovered?

- Restore the most recent backup of the virtual machine
- Restore from a snapshot if available
- Rebuild the virtual machine using the documented installation procedure
- Restore configuration files and data from backups

---

## Scenario 2 — Server No Longer Boots

### What happened?

A configuration change, software installation or system update prevents the server from starting successfully.

---

### What was lost?

- Temporary productivity while troubleshooting
- Unsaved changes made after the last recovery point

The virtual machine itself should still exist.

---

### How could it have been prevented?

- Create a snapshot before major configuration changes
- Test changes incrementally instead of making many at once
- Document important configuration changes
- Verify commands before executing them

---

### How could it have been recovered?

- Revert to the previous snapshot
- Restore the latest backup
- Compare the current configuration with documentation
- Rebuild the virtual machine if recovery is not practical

---

## Scenario 3 — Configuration File Overwritten

### What happened?

An important configuration file was accidentally overwritten or replaced with an incorrect version.

---

### What was lost?

- The working configuration
- Time spent troubleshooting
- Any undocumented changes

---

### How could it have been prevented?

- Keep configuration files under version control where appropriate
- Create backups before editing important files
- Document significant configuration changes
- Edit carefully and verify file paths before saving

---

### How could it have been recovered?

- Restore the previous version from Git
- Restore the file from a backup
- Restore the entire virtual machine snapshot if necessary
- Recreate the configuration using the documentation

---

## Scenario 4 — Host Hardware Failure

### What happened?

The host computer experiences a hardware failure such as a failing SSD, faulty memory or motherboard failure.

---

### What was lost?

Potentially everything stored exclusively on the host:

- Virtual machines
- Snapshots
- Local documentation
- Local backups
- Any files that were never copied elsewhere

---

### How could it have been prevented?

Hardware failure cannot always be prevented.

Its impact can be reduced by:

- Maintaining independent backups
- Using version control
- Keeping multiple backup copies
- Periodically verifying backup integrity

---

### How could it have been recovered?

- Replace or repair the failed hardware
- Reinstall the host operating system
- Reinstall VirtualBox and supporting software
- Restore documentation from GitHub
- Restore virtual machines from backups
- Continue working using the documented recovery procedures

---

## Scenario 5 — Mistake Discovered Days Later

### What happened?

An incorrect configuration or accidental deletion goes unnoticed for several days before causing visible problems.

---

### What was lost?

- Changes made after the mistake occurred
- Potentially several days of work if recovery points are too old

---

### How could it have been prevented?

- Regular testing after major changes
- Frequent commits with meaningful messages
- Frequent backups
- Reviewing configuration changes before moving on to new tasks

---

### How could it have been recovered?

- Restore the most appropriate backup or snapshot
- Recover individual files through version control where possible
- Reapply legitimate changes made after the recovery point
- Update documentation to reduce the likelihood of repeating the mistake

--- 

## Scenario 6 — The Good Backup Is Gone

### What happened?

A configuration mistake or accidental deletion went unnoticed for several days.

During that time, new backups were created automatically, eventually replacing the last backup that still contained the correct data.

The problem was only discovered after the recovery point had already been overwritten.

---

### What was lost?

- The last known good version of the affected files
- Potentially several days of work
- Confidence in the current backup strategy

---

### How could it have been prevented?

- Retaining multiple generations of backups instead of only the latest one
- Using version control for configuration files and documentation
- Testing systems after major configuration changes
- Performing regular reviews to detect problems earlier
- Defining an appropriate backup retention policy based on the expected RPO

---

### How could it have been recovered?

- Restore an older backup if one is still available
- Recover individual files through version control
- Rebuild the affected system using the documented installation and configuration procedures
- Reapply legitimate changes made after the recovered backup
- Review and improve the backup retention strategy to reduce the likelihood of the same situation occurring again

---

# 4. Snapshot Strategy

### Which systems deserve snapshots?

- Virtual machines before major changes
- Databases before structural or data modifications
- DBMS (Database Management System) configuration before significant configuration changes
- Operating system configurations before major updates or role installations

---

### When should snapshots be created?

- Before every major configuration change
- Before installing new software or server roles
- Before operating system updates
- Before database schema changes
- Before experiments that may significantly alter the system

---

### When should snapshots be deleted?

Snapshots should only be deleted once they are no longer needed for recovery and newer recovery points have been validated.

Storage limitations may require older snapshots to be removed, but multiple recovery points should always remain available to reduce the risk of losing the Last Known Good Configuration.

---

### Which risks do snapshots not protect against?

- Host hardware failure
- Storage device failure or corruption
- On-premises disasters (fire, flood, theft, etc.)
- Ransomware affecting the host system
- Accidental deletion of the virtual machine itself
- Long-term data retention requirements

---

### Under which circumstances should snapshots not be relied upon?

- As a replacement for independent backups
- For long-term data retention
- When protecting against host hardware failure
- When disaster recovery is required
- As the only recovery mechanism

---

### Which principle best summarizes the purpose of snapshots?

> **Snapshots are for experiments.**
>
> **Backups are for disasters.**

Snapshots allow me to safely explore, test and learn by providing a quick way to return to a **Last Known Good Configuration** after a mistake.

Backups protect my data and systems against failures that snapshots cannot address, such as hardware failure, corruption or long-term recovery requirements.

---

# 5. Backup Strategy

### Which files require independent backups?

- All Field Guide documentation
- Git repositories
- Scripts and automation
- Database backup files
- Configuration files that required significant effort to create

---

### Which systems require full backups?

- Windows Server VM
- Debian VM
- SQL Server databases
- The host system only after reaching a stable milestone

---

### How frequently should backups occur?

- Documentation: after every study session
- Git repositories: after every meaningful milestone
- Database backups: before major database changes and after completed projects
- Full VM backups: before major system changes and at the end of each Adventure

---

### Where should backups be stored?

- Primary copy on the host computer
- Secondary copy on an external drive
- Tertiary copy in cloud storage

---

### How many backup copies should exist?

I will follow the 3-2-1 Backup Strategy:

- Three copies
- Two different storage media
- One copy stored off-site

---

### How will backup integrity be verified?

- Verify that backup files were created successfully
- Regularly restore selected files
- Periodically restore an entire virtual machine
- Confirm that restored systems boot and function correctly

---

### How often should recovery be tested?

- After introducing a new backup method
- After major infrastructure changes
- At least once every Adventure

---

# 6. Version Control Strategy

### Which documents belong under version control?

- Field Guide lessons
- Lab documentation
- Markdown notes
- Scripts & automation
- Configuration files
- Diagrams created for the Lab

---

### Which files should not be version controlled?

- Personal workbook answers
- Temporary files
- Generated files that can easily be recreated
- Backup files
- Virtual machine disk images

---

### How should commits be organized?

- One logical change per commit
- Small enough to understand easily
- Large enough to represent meaningful progress

---

### What makes a commit meaningful?

A commit should represent the completion of a single task, lesson or milestone that can be understood independently.

---

### Which information should every commit communicate?

- What changed
- Why it changed
- The scope of the change

---

### How should commit messages be written?

- Short summary in the title
- Additional explanation when necessary
- Clear & specific wording
- Written so Future Me understands the purpose without opening the files

---

### When should changes be committed?

- At the completion of a lesson
- At the completion of an Adventure task
- Before major refactoring
- Before experimenting with a different solution
- Before ending a productive work session

---

# 7. Documentation Strategy

### Which recovery procedures should be documented?

- Initial Lab setup
- Virtual machine creation & configuration
- Backup procedures
- Snapshot procedures
- Restore procedures
- Database installation & configuration
- Common troubleshooting steps
- Lessons learned from failures

---

### Which information would Future Me need during an emergency?

- What happened
- What was attempted
- What worked
- What failed
- Which backups &/or snapshots are available
- The exact recovery procedure
- Links to relevant documentation

---

### Which documentation should remain available even if the Lab is unavailable?

- The Field Guide
- Recovery procedures
- Infrastructure overview
- Backup locations
- Installation instructions
- Important credentials & license information 

---

### How should recovery documentation be organized?

- One topic per document
- Clear titles & consistent structure
- Step-by-step recovery procedures
- Links between related documents
- Updated immediately after significant infrastructure changes

---

### When should documentation be updated?

- Immediately after completing a task
- After every successful recovery
- Whenever infrastructure changes
- Whenever a better solution is discovered
- Whenever existing documentation is found to be incomplete or inaccurate

---

### Which principle best summarizes the purpose of documentation?

> **Documentation should be good enough that Future Me can recover without relying on memory.**

In an emergency, memory is unreliable.

Good documentation reduces uncertainty, shortens recovery time and allows problems to be solved methodically instead of from memory.

---

# 8. Recovery Toolkit

| Recovery Method | Protects Against | Cannot Protect Against | Recovery Speed | Best Used For |
|-----------------|------------------|------------------------|----------------|---------------|
| Snapshots | Configuration mistakes, failed updates, software experiments | Host hardware failure, storage corruption, ransomware, long-term retention | Very Fast | Quickly returning to a Last Known Good Configuration during learning and experimentation |
| Backups | Data loss, hardware failure, accidental deletion, disasters | Mistakes made after the latest available recovery point, problems caused by insufficient backup retention | Moderate | Recovering systems and data after major failures or disasters |
| Version Control | Accidental file changes, lost revisions, poor configuration decisions | Hardware failure (without remote repository), VM corruption, binary system recovery | Fast | Tracking changes, comparing revisions and restoring previous versions of files |
| Documentation | Forgotten procedures, uncertainty during recovery, knowledge loss | Hardware failure (unless stored independently), undocumented changes, missing backups | Fast | Guiding recovery, rebuilding systems and preserving engineering knowledge |

---

# 9. Design Decisions

### Which recovery decision gives you the most confidence?

Having a multi-layer recovery strategy that includes snapshots, backups, version control and documentation.

---

### Which recovery process should be tested first?

Restoring a virtual machine from a snapshot.

It is quick, low-risk and provides immediaet confidence that the recovery workflow functions as expected.

---

### Which failure would be most expensive?

The permanent loss of documentation.

Virtual machines and databases can usually be rebuilt, but the lessons learned, design decisions and engineering knowledge accumulated throughout the Adventures would be difficult or impossible to recreate.

---

### Which recovery strategy depends on assumptions that still need validation?

The complete backup strategy.

I still need to validate:

- Backup frequency
- Backup retention
- Cloud storage provider, if applicable
- Restore procedures
- Recovery times
- Backup automation (later)

---

### Which recovery process should remain as simple as possible?

Restoring a working learning environment.

When something breaks, I want to spend my time learning, not rebuilding unnecessary complexity.

Recovery should be reliable, well documented and require as few manual steps as possible.

---

### Which recovery strategy is most likely to evolve during future Adventures?

The backup strategy.

As the Lab grows, new systems, larger datasets and additional services will require changes to backup frequency, storage locations, retention policies and automation.

---

# Notes

A complete backup and recovery strategy can only be determined as I progress through the Field Guide.

Since the Adventures are completed alongside my classes, there is no fixed schedule for when I will work on the Lab. Some weeks may involve significant infrastructure changes, while others may focus entirely on theory.

That's why my recovery strategy is based on milestones, not a calendar. Snapshots, backups and recovery tests should occur before major changes, and after meaningful progress, not simply because a certain amount of time has passed.
