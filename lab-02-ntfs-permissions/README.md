# Lab 02 - NTFS Permissions

## Overview
This lab demonstrates how to configure and verify NTFS permissions for a standard Windows user account.

The goal was to allow `support.user` to read, modify, and create files inside a dedicated folder without granting Full Control.

## Objective
Configure NTFS permissions for `support.user` and verify that the assigned permissions work correctly.

## Tools Used
- Windows
- File Explorer
- NTFS Security Permissions
- Local User Account

## Tasks Performed
1. Created a dedicated folder named `IT-Support-Lab`.
2. Reviewed the existing folder security permissions.
3. Added the `support.user` account to the folder permissions.
4. Granted the following permissions:
   - Modify
   - Read & execute
   - List folder contents
   - Read
   - Write
5. Verified that Full Control was not granted.
6. Logged in using the `support.user` account.
7. Accessed the folder and created a new file.
8. Modified an existing text file and saved the changes successfully.
9. Confirmed that the changes were visible from the main user account.

## Screenshots

### 1. Folder created
![Folder created](screenshots/01-folder-created.png)

### 2. Security permissions before modification
![Security before](screenshots/02-security-before.png)

### 3. Permissions assigned to support.user
![Support user permissions](screenshots/03-support-user-permissions.png)

### 4. Permission test successful
![Permission test](screenshots/04-permission-test-success.png)

### 5. Modify permission verified
![Modify permission verified](screenshots/05-modify-permission-verified.png)

## Result
The `support.user` account successfully accessed the folder, created files, and modified existing files using the assigned NTFS permissions without receiving Full Control.

## Skills Demonstrated
- NTFS permissions
- Windows file security
- User access control
- Least privilege
- Permission testing
- IT support troubleshooting