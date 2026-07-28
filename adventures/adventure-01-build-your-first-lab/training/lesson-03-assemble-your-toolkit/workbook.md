# Workbook
> **Lesson 03 · Assemble Your Toolkit**

## Purpose

This workbook helps evaluate potential tools before they become part of the Lab. Rather than searching for the "best" software, the goal is to choose tools that best satisfy the documented Lab requirements established in Lesson 02. Every decision should be supported by evidence, documented trade-offs and future flexibility.

---

# 1. Requirements Review

### Which requirements from Lesson 02 influence your tool choices the most?

- Limited hardware resources, particularly the available memory (8 GB RAM on the primary host)
- Compatibility with both Windows and Linux environments
- Support for future growth without requiring major redesigns
- The ability to experiment safely without risking the host system
- Minimal ongoing maintenance
- Low overall cost through the use of existing hardware and educational software

---

### Which requirements are essential?

The selected tools must...

- Be compatible with the available hardware.
- Support Windows and Linux virtual machines.
- Provide sufficient stability for learning.
- Support snapshots, backups or other recovery mechanisms.
- Scale to future Adventures where possible.
- Be cost-effective or available through educational licensing.

---

### Which requirements are desirable but optional?

- Running multiple virtual machines simultaneously
- Easy migration to future platforms such as Proxmox
- Integration with cloud platforms
- Built-in automation features
- Cross-platform compatibility
- Strong community support and learning resources

---

### Which requirements introduce technical constraints?

- Limited available memory on the primary host
- Available CPU and storage resources
- Compatibility with Apple Silicon where applicable
- Software licensing requirements
- The need to balance Lab performance with everyday use of the host computer

---

### Which requirements are likely to influence future Adventures?

- Hardware limitations
- Future scalability
- Compatibility with emerging technologies
- Recovery and backup capabilities
- Maintainability
- Flexibility to replace individual tools without redesigning the entire Lab

---

# 2. Virtualization Platform

### Which virtualization platforms are being considered?

| Platform | Intended Host |
|----------|---------------|
| Oracle VirtualBox | MacBook Pro |
| Microsoft Hyper-V | Lenovo Legion (subject to Windows edition compatibility) |

Both platforms have already been used during my retraining.

---

### Which requirements does each platform satisfy?

#### Oracle VirtualBox

- Compatible with my current MacBook Pro setup
- Supports Windows and Linux virtual machines
- Allows snapshots for safe experimentation
- Familiar from class
- Free to use
- Suitable for the current Adventure

#### Microsoft Hyper-V

- Integrated into supported editions of Windows
- Supports Windows and Linux virtual machines
- Suitable for future Windows-based Labs
- Familiar from class

---

### Which requirements does each platform not satisfy?

#### Oracle VirtualBox

- Limited by the available hardware resources of the MacBook Pro
- May not provide enterprise-level virtualization features

#### Microsoft Hyper-V

- Requires a compatible Windows edition
- Cannot be used on macOS
- May require upgrading the Lenovo Legion before it becomes a practical option

---

### What advantages does each platform provide?

#### Oracle VirtualBox

- Easy to learn
- Cross-platform
- Widely used for education
- Low barrier to entry

#### Microsoft Hyper-V

- Built into supported Windows editions
- Strong integration with Windows
- Valuable experience for future system administration work

---

### What disadvantages does each platform introduce?

#### Oracle VirtualBox

- Lower performance than some bare-metal hypervisors
- Dependent on host hardware limitations

#### Microsoft Hyper-V

- Windows edition restrictions
- Less flexible for a mixed operating system environment

---

### How difficult is each platform to learn?

Both platforms were intuitive to use during class.

I currently find VirtualBox slightly more user-friendly.

---

### How well does each platform support future Adventures?

Both platforms should support future Adventures involving Windows and Linux.

If future requirements change, additional virtualization platforms may be evaluated against the documented Lab requirements.

---

### Which risks should be considered?

- Limited hardware resources on the MacBook Pro
- Windows edition compatibility for Hyper-V on the Lenovo Legion
- Future hardware requirements may exceed the capabilities of the current hosts

---

### Which platform best fits the current Lab?

**Current choice:** Oracle VirtualBox on my MacBook Pro

VirtualBox satisfies the current Lab requirements while remaining compatible with my existing hardware and learning objectives.

Hyper-V remains a possible future option for my Lenovo Legion if the required Windows edition becomes available.

---

### Under which circumstances would this decision be reconsidered?

- Hardware limitations significantly affect performance
- New learning objectives introduce requirements that the current platform cannot satisfy
- The Lab outgrows desktop virtualization
- A dedicated virtualization host becomes justified by the documented requirements
- Hyper-V becomes fully supported on my Lenovo Legion and better satisfies the Lab requirements
- Another virtualization platform better satisfies the documented Lab requirements
  
---

# 3. Operating Systems

### Which operating systems should the Lab support?

- Windows Server 2022
- Debian Server 
- Windows 11 (Client)
- Debian Desktop

---

### Which operating systems are required immediately?

- Windows Server 2022
- Debian Server

---

### Which operating systems can be introduced later?

- Additional Linux distributions
- Windows client operating systems
- Debian Desktop
- Additional server operating systems as future Adventures require

---

### Which distributions or editions are being considered?

#### Virtual Machines

- Windows Server 2022
- Debian 13 "Trixie"

#### Hosts

- macOS (current MacBook Pro)
- Windows 10 Home (current Lenovo Legion)

---

### Why were they chosen?

- Available through my retraining
- Already used in class
- Windows Server 2022 and Windows Server 2025 are both used during my retraining, allowing me to gain experience with both versions
- Windows Server 2022 currently provides the better balance of stability and maturity for a personal home Lab
- Stable and well documented
- Large community support
- Compatible with the documented Lab requirements
- Representative of technologies commonly encountered in enterprise environments

---

### What alternatives exist?

- Windows Server 2025
- Additional Linux distributions such as Ubuntu Server

These alternatives satisfy many of the documented requirements but are not currently necessary for the planned Adventures.

---

### Which trade-offs are being accepted?

By choosing **Windows Server 2022**:

**Advantages**

- Stable and mature platform
- Well tested across the IT industry
- Matches part of the environment used during my retraining
- Extensive documentation and community resources
- Lower likelihood of encountering early-adopter issues

**Accepted trade-offs**

- Shorter remaining support lifecycle than Windows Server 2025 (ends October 2026)
- Does not include every feature introduced in Windows Server 2025
- A future migration to a newer version may become appropriate as the Lab evolves

---

### Why not always use the newest operating system?

In class I learnedL: The newest version is not automatically the best choice.

For learning system administration, stability, documentation, compatibility with course material and community support are often more valuable than newly introduced features.

Newer operating systems can be evaluated once the documented Lab requirements justify their adoption.

---

# 4. Documentation and Knowledge Management

### Which documentation tools are being considered?

- Plain text editor
- Git
- GitHub

---

### Which requirements do they satisfy?

#### Plain text editor

- Low complexity
- Portable
- Future-proof
- Works offline
- Human-readable
- Easy to back up

#### Git

- Version history
- Change tracking
- Safe experimentation
- Rollback capabilities
- Professional workflow

#### GitHub

- Remote backup
- Collaboration
- Public portfolio
- Off-site storage

---

### How portable are the notes?

#### Plain text editor

- Highly portable
- Can be opened by virtually any operating system
- Independent of any specific software

#### Git / GitHub

- Portability will be evaluated during a future Adventure once I have gained more practical experience using both tools

---

### How easily can documentation be backed up?

#### Plain text editor

- Simple to copy using standard file backups
- Easy to synchronize across storage locations

#### Git / GitHub

- Backup workflows will be explored during a future Adventure

---

### How well do they support long-term maintenance?

#### Plain text editor

- Open and widely supported file format
- Software-independent
- Readable for many years without requiring a specific application

#### Git / GitHub

- Designed for long-term version management
- Preserve documentation history
- Support collaboration and continuous development

---

### Which documentation tool should become the primary system?

Plain text files, because they are simple, portable, future-proof and independent of any particular application.

Additional tools should enhance the documentation rather than replace it.

---

### Why use plain text instead of a more advanced documentation tool?

Plain text is software-independent, portable, easy to back up and unlikely to become obsolete.

It allows me to focus on documenting knowledge rather than learning another application. More advanced tools can always be introduced later if they satisfy new requirements.

---

### Under which circumstances would this decision be reconsidered?

- Collaboration becomes necessary
- Public repositories become part of the project
- Version history becomes increasingly important
- The documented Lab requirements justify a more advanced documentation workflow

---

# 5. Version Control

### Which version control systems are being considered?

- Git because it is widely adopted throughout the software and IT industry and therefore a valuable technology to learn
- At least one centralized version control system during a future Adventure
- Potentially another distributed version control system for comparison

---

### Why is version control needed?

- Track changes to files over time
- Restore previous versions when necessary
- Support safe experimentation
- Enable collaboration on shared projects

---

### Which requirements does it satisfy?

- Traceability
- Recoverability
- Collaboration
- Long-term maintenance
- Safe experimentation

---

### How difficult is it to learn?

The underlying concepts appear logical, but I expect the practical workflows and advanced features to require time and practice.

---

### Which hosting platforms are being considered?

- GitHub because it is widely used throughout the software and IT industry
- Alternative hosting platforms during future Adventures
- Potentially self-hosted solutions if future requirements justify them

---

### Which solution best fits the Lab?

- Git
- GitHub

Both satisfy the current Lab requirements while providing valuable experience with professional tools. Also, I'm already here. ;)

---

### Which trade-offs are being accepted?

- A steeper learning curve than simpler alternatives
- Learning new workflows before becoming fully productive
- Dependence on a third-party hosting platform for remote repositories

---

### Why learn Git before exploring alternatives?

Git is widely used throughout the software and IT industry and provides a strong foundation for understanding version control concepts.

Once I understand Git well, I will be better equipped to evaluate alternative version control systems based on their requirements, strengths and trade-offs rather than learning several systems simultaneously.

---

### Under which circumstances would this decision be reconsidered?

- The documented Lab requirements change
- Collaboration requirements change
- Privacy or hosting requirements change
- Self-hosting becomes desirable
- Another version control solution better satisfies the documented Lab requirements

---

# 6. Supporting Tools

### Which additional tools are currently required?

#### Documentation

- Plain text editor
- Draw.io

#### Development & Administration

- Terminal applications
- Database clients
- Remote access tools

#### Learning Resources

- Books
- Microsoft Learn
- Official vendor documentation
- Trusted community resources
- AI assistant

#### Maintenance

- Backup tools
- Monitoring tools

---

### Which requirements does each tool satisfy?

| Tool | Primary Requirements Satisfied |
|------|--------------------------------|
| Plain text editor | Documentation, portability, long-term maintenance |
| Draw.io | Visual documentation, system design, communication |
| Terminal applications | System administration, automation, troubleshooting |
| Database clients | Database administration, SQL experimentation, learning |
| Remote access tools | Remote administration, flexibility |
| Backup tools | Recoverability, data protection |
| Monitoring tools | System health, troubleshooting, maintenance |
| Books | Structured learning, reference material |
| Microsoft Learn | Official documentation, guided learning |
| Official vendor documentation | Accurate technical reference, best practices |
| Trusted community resources | Alternative perspectives, practical experience, additional explanations |
| AI assistant | Interactive learning, lab design, quizzes, exam simulations, critical discussion, brainstorming, explanation of concepts |

---

### Which tools are essential?

- Plain text editor
- Draw.io
- Terminal applications
- Database clients
- Backup tools
- Books
- Microsoft Learn
- Official vendor documentation
- AI assistant

---

### Which tools are optional?

- Remote access tools
- Monitoring tools
- Trusted community resources beyond official documentation

---

### Which tools can wait until later Adventures?

- Advanced monitoring solutions
- Remote administration tools
- More specialized database clients
- Additional diagramming or documentation software
- Any supporting tool that is not currently required by the documented Lab requirements

### How should AI be used responsibly?

- To deepen understanding rather than replace it
- To create labs, quizzes and realistic scenarios
- To review and challenge my own solutions
- To explain concepts from different perspectives
- To support creativity and brainstorming
  
---

# 7. Lab Toolkit 

| Category | Selected Tool | Why this Tool? | Main Trade-off | Revisit When |
|----------|---------------|----------------|----------------|--------------|
| Virtualization | Oracle VirtualBox | Compatible with my current hardware, familiar from class, supports the current Lab requirements | Limited by host hardware and lacks some enterprise virtualization features | Hardware limitations affect performance or another virtualization platform better satisfies the documented Lab requirements |
| Operating System | Windows Server 2022 | Stable, mature, well documented and representative of enterprise environments while matching part of my retraining | Does not include every feature introduced in Windows Server 2025 | New requirements justify migrating to a newer server operating system |
| Linux Distribution | Debian 13 "Trixie" | Stable, widely used, well documented and already familiar from class | Less exposure to other Linux distributions | Future Adventures require another distribution or a comparison becomes beneficial |
| Documentation | Plain text (Markdown) | Simple, portable, future-proof, software-independent and easy to back up | Lacks some advanced features offered by dedicated documentation platforms | The documented Lab requirements justify a more advanced documentation workflow |
| Version Control | Git | Widely adopted throughout the software and IT industry and provides a strong foundation for learning version control | Steeper learning curve than simpler alternatives | Another version control system better satisfies the documented Lab requirements |
| Repository Hosting | GitHub | Widely used, supports collaboration, remote backup and public portfolio projects | Dependence on a third-party hosting platform | Privacy, collaboration or hosting requirements change |
| Diagramming | Draw.io | Easy to use, platform-independent and well suited for documenting systems and architectures | Fewer advanced features than some commercial alternatives | Future documentation requirements justify another diagramming tool |
| Learning Resources | Books, Microsoft Learn, Official Documentation, Trusted Community Resources, AI Assistant | Provide complementary perspectives for building understanding, developing practical skills and supporting long-term learning | Requires evaluating information from multiple sources and investing time in continuous learning | Better resources become available or future Adventures introduce new learning requirements |

---

# 8. Design Decisions

### Which decision are you most confident about?

Using plain text (Markdown) as the primary documentation format.

It satisfies the documented Lab requirements while remaining simple, portable, software-independent and future-proof.

---

### Which decision required the greatest compromise?

Choosing tools based on the current Lab requirements rather than future possibilities.

This means favouring mature, stable and familiar technologies over newer or more feature-rich alternatives until the documented requirements justify a change.

---

### Which tool best supports future growth?

Git.

Learning Git establishes a strong foundation for version control concepts that remain valuable regardless of future hosting platforms or development workflows.

---

### Which decision should remain easy to change later?

Implementation decisions should remain flexible.

Virtualization platforms, operating systems, hosting platforms and supporting tools should all be replaceable if future requirements justify doing so.

The engineering principles documented throughout the Field Guide should remain significantly more stable than the individual tools used to implement them.

---

### Which assumptions still need to be validated?

- Whether Hyper-V is practical on the Lenovo Legion
- Whether VirtualBox continues to satisfy future Adventures
- Whether Git and GitHub fit my preferred workflow
- Which Linux distributions become most valuable for future Adventures
- Which supporting tools prove to be essential over time

---

# Notes

I'm getting really excited about finally building the Lab.

But as a very wise lecturer of mine once said (roughly):

> "Basics first. Playing around later."

And even though I am a tad bit impatient and would enjoy simply taking the plunge, I do have to admit that it's good advice.

A solid foundation makes every future Adventure easier, and all that. ;)
