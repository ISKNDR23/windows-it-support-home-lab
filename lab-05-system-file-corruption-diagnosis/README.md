# Lab 05 - Windows System File Corruption Diagnosis and Repair Source Analysis

## Overview
This lab demonstrates a real Windows troubleshooting workflow for diagnosing system file corruption and investigating why automated repair fails.

The goal was to verify system file integrity, determine whether the Windows component store was repairable, and identify why DISM could not complete the repair.

## Objective
Diagnose Windows system file corruption using SFC and DISM, verify the health of the component store, and investigate repair-source compatibility.

## Tools Used
- Windows Command Prompt
- System File Checker (SFC)
- Deployment Image Servicing and Management (DISM)
- Windows 10 ISO
- install.esd

## Troubleshooting Process

### 1. System File Integrity Check
The following command was used:

```cmd
sfc /scannow
```

SFC detected corrupted system files but was unable to repair some of them.

![SFC corruption detected](screenshots/01-sfc-corruption-found.png)

### 2. Initial DISM Repair Attempt
The following command was used:

```cmd
DISM /Online /Cleanup-Image /RestoreHealth
```

The repair failed with:

```text
Error: 0x800f081f
The source files could not be found.
```

![DISM source error](screenshots/02-dism-source-files-not-found.png)

### 3. Component Store Analysis
The component store was analyzed using:

```cmd
DISM /Online /Cleanup-Image /ScanHealth
```

The result confirmed:

```text
The component store is repairable.
```

![ScanHealth result](screenshots/03-dism-scanhealth-repairable.png)

The status was also confirmed using:

```cmd
DISM /Online /Cleanup-Image /CheckHealth
```

![CheckHealth result](screenshots/04-dism-checkhealth-repairable.png)

### 4. External Repair Source Preparation
A Windows 10 ISO was mounted and the repair image file was identified as:

```text
E:\sources\install.esd
```

![Install ESD identified](screenshots/05-install-esd-source-identified.png)

### 5. Edition Verification
The available Windows editions inside the ESD were inspected.

Windows 10 Pro was identified as:

```text
Index: 4
```

The installed Windows edition was also verified as:

```text
Current Edition: Professional
```

![Edition and index check](screenshots/06-windows-edition-and-index-check.png)

### 6. Language Verification
The system language configuration was checked using:

```cmd
DISM /Online /Get-Intl
```

The system was confirmed to use:

```text
Default system UI language: ar-SA
```

![System language check](screenshots/07-system-language-check.png)

### 7. Repair Source Version Analysis
The Windows 10 Pro image inside the ISO was inspected using:

```cmd
DISM /Get-WimInfo /WimFile:E:\sources\install.esd /index:4
```

The repair source was based on an older Windows build than the currently installed operating system.

![Source build analysis](screenshots/08-source-build-mismatch-identified.png)

## Findings
- SFC detected system file corruption.
- The Windows component store was confirmed to be repairable.
- DISM failed with error `0x800f081f`.
- The Windows edition, architecture, and language were verified.
- The external repair source was based on an older Windows build than the installed system.
- The repair-source mismatch was identified as the most likely reason the selected source was unsuitable for the repair.

## Result
The root cause of the unsuccessful repair attempt was narrowed down to repair-source compatibility.

A matching or newer repair source would be required before continuing the repair process.

## Skills Demonstrated
- Windows system troubleshooting
- SFC diagnostics
- DISM diagnostics
- Windows component store analysis
- Error code investigation
- Windows edition verification
- Repair source validation
- Root cause analysis
- Technical documentation