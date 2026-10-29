
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
```

## OpenSSH Troubleshooting and Remote SSH Test

Event Viewer showed a Service Control Manager error:

- Event ID: 7034
- Service: OpenSSH SSH Server
- Message: The OpenSSH SSH Server service terminated unexpectedly.

### Troubleshooting Steps

Checked the SSH service status:

```powershell
Get-Service sshd
```

Reviewed the OpenSSH operational log:

```powershell
Get-WinEvent -LogName "OpenSSH/Operational" -ErrorAction SilentlyContinue |
Select-Object -First 20 TimeCreated, Id, LevelDisplayName, Message
```

The logs showed that `sshd` had terminated earlier but later restarted successfully.

Verified the SSH service configuration:

```powershell
Get-Service sshd | Select-Object Status, Name, StartType
```

Verified that SSH was listening on TCP port 22:

```powershell
netstat -ano | findstr :22
```

Verified the process using the SSH port:

```powershell
Get-Process -Id 2508
```

Tested SSH locally on the Windows Server:

```powershell
ssh localhost
```

The local SSH connection worked successfully.

### Azure Network Security Group Configuration

Created an inbound NSG rule for SSH with:

- Source: My IP address
- Source port: *
- Destination: Any
- Destination port: 22
- Protocol: TCP
- Action: Allow
- Priority: 310
- Rule name: SSH

### Remote SSH Test from macOS

SSH was tested remotely from macOS using:

```bash
ssh Azureadmin@<VM_PUBLIC_IP>
```

The connection succeeded and opened a remote Windows Server shell.

### Result

OpenSSH was confirmed to be functioning correctly both locally and remotely.

The troubleshooting process included:

- Event Viewer analysis
- Service Control Manager Event ID 7034
- OpenSSH operational logs
- Service status verification
- Port 22 verification
- Process ID verification
- Local SSH testing
- Azure NSG configuration
- Remote SSH testing from macOS

This confirmed that the earlier OpenSSH service failure was investigated and that the service was working correctly afterward.

---

## IT Support Troubleshooting Portfolio

In addition to the hands-on Azure Windows Server lab above, this repository contains 20 IT support troubleshooting case studies. These projects demonstrate a structured approach to identifying problems, investigating possible causes, applying appropriate solutions, and documenting results.

**Note:** Projects 01–20 are simulated troubleshooting scenarios created for learning and portfolio purposes. They are not presented as real customer incidents.

### Project Index

| Project | Topic |
|---|---|
| Project 01 | RDP Connectivity Troubleshooting |
| Project 02 | Windows Event Log Troubleshooting |
| Project 03 | Windows Failed Login Investigation |
| Project 04 | Microsoft 365 / Entra ID Sign-in Troubleshooting |
| Project 05 | Intune Device Compliance Troubleshooting |
| Project 06 | Outlook Email Troubleshooting |
| Project 07 | Windows DNS and Network Troubleshooting |
| Project 08 | Windows DHCP and IP Address Troubleshooting |
| Project 09 | Windows Account Lockout Troubleshooting |
| Project 10 | Windows Printer Troubleshooting |
| Project 11 | Windows Software Installation Troubleshooting |
| Project 12 | Windows Slow Computer Troubleshooting |
| Project 13 | Microsoft Teams Audio and Video Troubleshooting |
| Project 14 | OneDrive Sync Troubleshooting |
| Project 15 | Microsoft Teams Meeting and Calendar Troubleshooting |
| Project 16 | Microsoft 365 MFA Troubleshooting |
| Project 17 | Windows VPN Connectivity Troubleshooting |
| Project 18 | Windows Update Troubleshooting |
| Project 19 | Windows Blue Screen and Unexpected Restart Troubleshooting |
| Project 20 | Full Service Desk Incident Simulation |

### Troubleshooting Approach

For each case study, the goal is to follow a structured support workflow:

1. Identify and define the reported problem.
2. Gather relevant information and check the symptoms.
3. Investigate likely causes using appropriate tools.
4. Apply a suitable fix or recommend the next action.
5. Verify whether the issue has been resolved.
6. Document the findings and preventive recommendations.

### Skills Demonstrated

- Windows desktop and Windows Server troubleshooting
- Remote Desktop Protocol (RDP)
- Microsoft 365 and user sign-in support
- Identity, authentication, and MFA concepts
- Basic networking, DNS, DHCP, and VPN troubleshooting
- Intune device compliance concepts
- Outlook, Teams, and OneDrive support
- Windows logs, system maintenance, and incident documentation
- Service Desk communication and structured problem-solving

### Learning Goals

This portfolio supports my development toward entry-level IT Support, Service Desk, Microsoft 365 Support, and Cloud Support roles. It combines practical lab experience with documented troubleshooting exercises.



