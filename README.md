
# Azure Windows Server Lab

## Project Overview

This project demonstrates a hands-on Microsoft Azure Windows Server lab created for IT Support and Cloud Support practice.

The goal was to deploy a Windows Server virtual machine in Azure, connect to it remotely, configure local users, troubleshoot Remote Desktop access, configure Windows Firewall, create a shared folder, and test user permissions.

## Technologies Used

- Microsoft Azure
- Windows Server 2025
- Azure Virtual Machines
- Remote Desktop Protocol (RDP)
- Windows App for macOS
- PowerShell
- Windows Defender Firewall
- SMB File Sharing
- NTFS Permissions

## Lab Environment

- Azure Virtual Machine
- Windows Server 2025
- B-series VM
- macOS used as the client computer
- RDP used for remote administration

## Tasks Completed

### 1. Azure Virtual Machine Deployment

Created a Windows Server 2025 virtual machine in Microsoft Azure.

Selected a low-cost B-series VM size to reduce Azure credit usage.

### 2. Remote Desktop Connection

Configured RDP access and connected to the Windows Server VM from macOS using Microsoft Windows App.

Verified that TCP port 3389 was allowed through the Azure Network Security Group.

### 3. Local User Administration

Created local user accounts:

- labuser1
- labuser2

Verified the accounts using PowerShell.

Example command:

```powershell
Get-LocalUser
