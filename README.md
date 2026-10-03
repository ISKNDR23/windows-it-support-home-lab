# Windows IT Support Home Lab

## Overview
This project is a hands-on Windows IT support lab designed to demonstrate practical troubleshooting, system administration, permissions management, network diagnostics, performance analysis, and Windows repair investigation.

The project contains five labs that simulate common entry-level IT Support and Help Desk tasks using Windows built-in tools.

## Project Goals
- Practice common Windows administration tasks
- Apply basic troubleshooting methodology
- Document technical findings clearly
- Demonstrate hands-on IT Support skills
- Build a practical portfolio project for Help Desk and Technical Support roles

## Environment
- Windows 10
- Local user accounts
- Command Prompt
- Computer Management
- Task Manager
- NTFS permissions
- DISM
- SFC
- Windows ISO repair source

## Labs

### Lab 01 - Local User Management
Created and validated a standard local Windows user account.

Tasks included:
- Creating a local user
- Verifying group membership
- Confirming the account did not have administrator privileges
- Testing successful login

[View Lab 01](lab-01-local-user-management/)

---

### Lab 02 - NTFS Permissions
Configured and tested NTFS permissions for a standard user.

Tasks included:
- Creating a dedicated folder
- Assigning Modify, Read, Write, and Execute permissions
- Applying least-privilege access
- Testing file creation and modification using the standard user account

[View Lab 02](lab-02-ntfs-permissions/)

---

### Lab 03 - Network Configuration and Troubleshooting
Used Windows command-line tools to inspect network configuration and verify connectivity.

Tasks included:
- Reviewing IP configuration
- Testing connectivity to an external IP address
- Testing domain name resolution
- Using `nslookup`
- Flushing the DNS resolver cache

[View Lab 03](lab-03-network-configuration/)

---

### Lab 04 - PC Performance Troubleshooting
Investigated Windows performance issues using Task Manager.

Initial findings included:
- High memory utilization
- 100% disk utilization
- Multiple unnecessary startup applications
- High resource usage from browser processes

Actions included:
- Reviewing system resource usage
- Disabling unnecessary startup applications
- Reducing unnecessary running applications
- Comparing performance before and after optimization

[View Lab 04](lab-04-pc-performance-troubleshooting/)

---

### Lab 05 - Windows System File Corruption Diagnosis and Repair Source Analysis
Performed a real troubleshooting investigation after Windows system corruption was detected.

Tasks included:
- Running `sfc /scannow`
- Detecting corrupt Windows system files
- Using DISM `ScanHealth` and `CheckHealth`
- Investigating DISM error `0x800f081f`
- Preparing an external Windows repair source
- Identifying the correct Windows edition and image index
- Verifying system language and architecture
- Comparing the repair source version with the installed Windows version
- Narrowing the unsuccessful repair attempt to repair-source compatibility

[View Lab 05](lab-05-system-file-corruption-diagnosis/)

## Skills Demonstrated
- Windows user account management
- Local Users and Groups
- NTFS permissions
- Least-privilege access control
- Windows file security
- TCP/IP fundamentals
- Network troubleshooting
- DNS diagnostics
- Command-line troubleshooting
- Windows performance analysis
- Task Manager
- Startup optimization
- System File Checker
- DISM diagnostics
- Windows component store analysis
- Repair source validation
- Root cause analysis
- Technical documentation

## Troubleshooting Approach
Throughout the project, a structured troubleshooting process was followed:

1. Identify the issue
2. Gather relevant information
3. Test likely causes
4. Apply an appropriate action
5. Verify the result
6. Document findings

## Project Structure

```text
Windows-IT-Support-Home-Lab/
│
├── lab-01-local-user-management/
│   ├── README.md
│   └── screenshots/
│
├── lab-02-ntfs-permissions/
│   ├── README.md
│   └── screenshots/
│
├── lab-03-network-configuration/
│   ├── README.md
│   └── screenshots/
│
├── lab-04-pc-performance-troubleshooting/
│   ├── README.md
│   └── screenshots/
│
├── lab-05-system-file-corruption-diagnosis/
│   ├── README.md
│   └── screenshots/
│
└── README.md
```

## Key Takeaways
This project strengthened my understanding of practical Windows IT support and troubleshooting.

The labs provided hands-on experience with common tasks such as user administration, permissions, network diagnostics, performance troubleshooting, and Windows system repair analysis.

The project also emphasized the importance of validating results and documenting each troubleshooting step clearly.

## Career Relevance
This project is directly relevant to entry-level roles such as:

- IT Support
- Help Desk
- Technical Support
- Desktop Support
- Service Desk
- IT Support Technician
- IT Support Specialist