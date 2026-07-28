# Workbook

> **Lesson 02 · Design Your Lab**

---

# Purpose

This workbook helps define what my Lab must accomplish before I decide how to build it. By identifying requirements, constraints and priorities first, I can make informed technical decisions in the lessons that follow.

---

# 1. Existing Environment
 

### Which physical computer will host the Lab? What are the specifications?

| Specification | **MacBook Pro (Primary Candidate)** | **Lenovo Legion (Alternative Candidate)** |
|----------------|--------------------------------------|-------------------------------------------|
| Processor | Apple M3 (8 cores) | Intel Core i7 |
| Memory (RAM) | 8 GB | 16 GB |
| Storage | 877 GB available | 2 TB HDD + 512 GB SSD |
| Host Operating System | macOS 26.5 | Windows 10 |
| Architecture | ARM (Apple Silicon) | x86-64 |
| Hardware-Assisted Virtualization | Supported | Supported* |
| Virtualization Enabled | To be verified | To be verified |
| Firmware | Apple Silicon firmware (UEFI-based) | UEFI/BIOS (to be verified) |
| Portability | High | Moderate |
| Current Status | Daily-use computer | Available as secondary machine |
| Additional Hardware | Several spare laptops and an older desktop PC may later be repurposed for experiments or spare parts. | — |
| Hardware to Protect | Primary everyday computer. Must remain stable and reliable throughout the project. | Secondary machine. May be repurposed if required. |

**Note**

The Lab will initially be hosted on the **MacBook Pro**. It's my primary computer, offers sufficient processing power and available storage for the first version of the Lab, and provides the most convenient day-to-day development environment. Its limited memory (8 GB RAM) is a known constraint and will be evaluated as the Lab grows. The Lenovo Legion remains a viable alternative should additional computing resources become necessary.

\* The Lenovo Legion's processor is expected to support hardware-assisted virtualization. The current firmware configuration (UEFI/BIOS) and virtualization settings should be verified before the system is considered for use as a Lab host.


---

# 2. Intended Use
 

### Which technologies do you expect to explore during the next twelve months?

The Lab should support a broad range of technologies that reflect both my current curriculum as a trainee in System Integration and my own learning goals.

| Technology Area | Examples |
|-----------------|----------|
| Operating Systems | Windows 11, Windows Server, Linux distributions (primarily Ubuntu and Debian) |
| Virtualization | Virtual machines, snapshots, virtual networking |
| Networking | TCP/IP, Domain Name System (DNS), Dynamic Host Configuration Protocol (DHCP), routing, switching, Virtual Local Area Networks (VLANs), firewall concepts |
| Directory Services | Active Directory Domain Services (AD DS), Group Policy, mixed Windows/Linux environments |
| Databases | Microsoft SQL Server, MySQL, PostgreSQL |
| Database Languages | Structured Query Language (SQL), database administration |
| Cloud | Microsoft Azure and hybrid environments |
| Development Tools | Visual Studio Code, Git, GitHub, PowerShell, Bash |
| System Administration | Windows administration, Linux administration, file services, user management |
| Automation & Scripting | PowerShell, Bash, Python (where appropriate) |
| Embedded Systems | Single-board computers, microcontrollers, embedded Linux, hardware interfaces and prototype devices |
| Open-Source Software | Various open-source server and administration tools as required throughout the Adventures |

---

### Which requirements must be considered when designing the Lab?

| Requirement | Decision |
|-------------|----------|
| **Support Windows systems** | Yes. |
| **Support Linux systems** | Yes. |
| **Run Windows and Linux simultaneously** | Yes. The Lab should support this as it grows. The available hardware will determine when this becomes practical. |
| **Include client and server systems** | Yes. |
| **Support communication between multiple machines** | Yes. |
| **Support networking, Domain Name System (DNS), directory services, databases, automation and cloud integration** | Yes. |
| **Provide internet access** | Yes. Internet connectivity will be required for software installation, updates, cloud services and general administration. |
| **Allow isolated systems** | Yes. Some systems should remain isolated from the internet when required for testing, security or specific learning scenarios. |
| **Recreate workplace-like environments** | Yes, where practical. The goal is to simulate realistic small-scale enterprise environments suitable for learning and experimentation. |


---

# 3. Safety and Isolation

### Which experiments could damage your everyday computer if performed directly on it?

- Installing or modifying operating systems
- allocating excessive system resources to virtual machines
- misconfiguring storage
- experimenting with networking
- accidentally deleting or overwriting files
- installing unstable or potentially harmful software

The Lab should isolate these risks from the host system.

---

### Which personal files or applications must remain protected?

All of them.

My everyday computer remains my primary work and personal device. No experiment performed inside the Lab should put personal files, applications or system stability at risk.

---

### Must Lab systems be isolated from your home network?

Yes, where appropriate.

Experiments should not interfere with other devices on my home network. The host computer should primarily manage the Lab, while experimentation takes place inside virtual machines.

---

### Must individual Lab systems be isolated from one another?

Yes, when required.

Individual systems should be isolated or connected depending on the learning objective. The Lab should support both isolated experiments and realistic multi-machine environments.

---

### How quickly should you be able to undo a failed experiment?

Ideally within minutes by restoring a virtual machine snapshot.

However, whenever practical, I want to investigate failures before restoring them. Troubleshooting is an essential system administration skill and an important part of the learning process.

---

### What should happen if a virtual machine becomes unusable?

The cause of the failure should be investigated first. If recovery is no longer practical, the virtual machine should be restored from the most appropriate snapshot or backup.

---

### Which parts of the Lab must be recoverable from backup?

All significant milestones and stable working configurations should be recoverable from backup.

---

### What would an acceptable worst-case failure look like?

A virtual machine becomes unrecoverable, but no personal data is lost and the environment can be restored from snapshots or backups with minimal effort.


---

# 4. Persistence and Recovery

### Which systems should remain available for future Adventures?

Base virtual machines and stable milestone environments that can serve as reusable starting points for future Adventures.

---

### Which systems may be temporary?

Experimental virtual machines, temporary network configurations and proof-of-concept environments may be discarded once they have served their learning purpose.

---

### Which configurations must be documented?

All significant configurations, changes and design decisions should be documented so that the Lab can be reproduced, understood and maintained in the future.

---

### Will you need snapshots before making risky changes?

Obviously.

Snapshots should be created before making significant configuration changes or performing potentially destructive experiments.

---

### Will snapshots alone be sufficient?

Nope.

Snapshots provide fast rollback during experimentation, but they aer not a replacement for backups. Important milestones and completed Adventures should also be backed up independently on storage separate from the host, such as an external drive.

---

### Which files require an independent backup?

- Virtual machines
- databases
- documentation
- scripts
- other important project files
  
---

### Where will backups be stored?

- Host (temporary)
- External drive (primary backup location)
- Cloud storage (optional secondary backup where appropriate)

---

### How will you verify that recovery actually works?

Recovery procedures should be tested before they are relied upon. Both Windows and Linux systems should be restored successfully at least once to verify that the recovery strategy works as intended.

---

### How much rebuilding would be acceptable after a failure?

At most, the work completed since the last successful backup. Frequent backups reduce the amount of rebuilding required after a failure.

---

# 5. Resources and Constraints

### What budget is available?

The Lab should be as cost-effective as possible. However, I am willing to invest approximately **€100–150 per month** when necessary. This budget may also include books and other learning resources.

The budget should prioritize reusable hardware, books and learning resources over convenience purchases.

---

### Which existing hardware should be reused?

Existing hardware should be evaluated before purchasing new equipment.

The available hardware currently includes:

- MacBook Pro (primary Lab host)
- Lenovo Legion (secondary host and gaming laptop)
- Several older laptops
- An older desktop PC

Older systems may be repurposed, upgraded or dismantled for parts where appropriate.

---

### How much storage can be dedicated to the Lab?

Storage is not expected to be a major limitation.

- **MacBook Pro:** Approximately **750–800 GB** can be dedicated to the Lab if required.
- **Lenovo Legion:** Approximately **500 GB** can be allocated while still leaving sufficient space for personal use.

---

### How much memory can the Lab use without affecting everyday work?

The Lab should leave sufficient memory available for normal work on the host system.

The MacBook Pro currently has **8 GB of RAM**, which already relies on memory compression and swap during everyday use. As a result, only lightweight virtual machines should be run simultaneously on the MacBook. Larger multi-machine environments may require using the Lenovo Legion or another host in the future.

---

### How much time can be spent maintaining the Lab?

Approximately **30 minutes per week**.

The Lab should be designed to require minimal ongoing administration so that most available time can be spent learning, experimenting and completing Adventures rather than maintaining infrastructure.

---

### Are there software licensing restrictions?

No significant restrictions are expected.

Educational software and licenses provided through the academy should be used whenever available.

---

### Are there electricity, noise, heat or space constraints?

No.

The Lab will be operated from a dedicated home office, so these factors are not expected to limit the design.

---

### Must the Lab remain portable?

Ideally, yes.

The Lab should remain portable enough to continue development using the primary laptop or to relocate the environment if required.

---

### Must it work without purchasing additional hardware?

Ideally, yes.

Existing hardware should be used wherever practical. Additional hardware should only be purchased when it clearly enables new learning opportunities or removes a significant limitation.

---

# 6. Usability and Maintenance

### How easy must it be to create a new test system?

Creating a new test system should be as straightforward and well documented as reasonably possible.

I'm willing to invest additional time when doing so helps me understand the underlying technology rather than simply automating the process.

---

### How quickly should a system be reset or rebuilt?

Resetting a system should ideally take only a few minutes.

Rebuilding a system from scratch may take longer if it contributes to learning or validates that the documentation is complete and accurate.

---

### How will systems be named?

Systems should follow a consistent naming convention that is meaningful to me while avoiding personal information or publicly identifying details.

---

### How will configurations be documented?

Configurations, changes and design decisions should be documented using plain text files. Git and GitHub may later be used for version control and long-term documentation.

---

### How will completed work be versioned?

I first need to learn more about version control before making an informed decision.

Until then, the documentation should remain flexible enough to accommodate a future versioning strategy.

---

### How will you know which systems are active, archived or disposable?

Labels, directory structure and documentation should clearly indicate whether a system is active, archived or intended to be disposable.

---

### How much manual maintenance is acceptable?

Approximately **30 minutes per week**.

The Lab should require only minimal routine maintenance so that the majority of time can be spent learning and experimenting.

---

### Which recurring tasks should eventually be automated?

Recurring tasks that do not contribute directly to learning should eventually be automated, including:

- Regular backups
- Snapshot reminders
- Documentation reminders
- Resource monitoring (CPU, memory and storage usage)
- System health reports
- Routine software updates when appropriate

Tasks should only be automated once I understand the underlying manual process. No shortcuts! 

---

# 7. Future Growth

### Which future Adventures are already foreseeable?

The Lab should be capable of supporting future Adventures in areas such as:

- Windows Server
- Linux Administration
- Networking
- Active Directory Domain Services (AD DS)
- Databases & DBMS
- Cloud Computing (Microsoft Azure)
- Automation & Scripting
- Cybersecurity
- Embedded Systems & Raspberry Pi
- Additional technologies introduced throughout my retraining

The first planned Adventure is:

- **Adventure 01 – Build Your First Lab**

---

### Could the Lab later include dedicated physical hardware?

Absolutely.

The Lab should remain flexible enough to incorporate dedicated physical hardware in the future. Ideally, existing hardware can be repurposed to build a dedicated workstation or small server. These systems should be remotely accessible and manageable from my primary computer.

---

### Could it later include a hypervisor host such as Proxmox Virtual Environment?

Yes.

The Lab should remain flexible enough to migrate to a dedicated hypervisor host, such as Proxmox Virtual Environment, if future requirements justify doing so.

---

### Could the Lab later connect to Microsoft Azure, Amazon Web Services or another cloud platform?

Yes. 

This will become relevant as my understanding of cloud technologies grows throughout the Adventures.

---

### Could it later include containers?

Yes, once I have gained a better understanding of them.

---

### Could it later support monitoring, central authentication or automated deployment?

Yes.

But: Changes should never be automated without first ensuring that an appropriate backup or recovery point exists.

---

### Which decisions made today must remain easy to change later?

As many decisions as possible should remain reversible.

The Lab should evolve over time, allowing technologies, architectures and workflows to be replaced when better solutions become available. Stable systems should not be changed without good reason, but no decision made today should unnecessarily limit future growth.
