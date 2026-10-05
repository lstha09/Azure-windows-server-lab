
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

