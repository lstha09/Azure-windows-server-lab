# Project 17: Windows VPN Connectivity Troubleshooting

## Project Overview

**Ticket ID:** VPN-001  
**Category:** Windows Networking / Remote Access  
**Environment:** Simulated Windows 11 remote-work environment  
**Status:** Resolved in the simulated scenario  
**Project Type:** IT Support Portfolio Case Study

> **Important:** This is a fictional troubleshooting exercise for learning and portfolio demonstration. No real company VPN, user account, internal server, or Azure resource was accessed, created, started, or modified.

## 1. Problem Description

A remote employee using a Windows 11 laptop reported that the internet was working, but the company VPN would not connect. The employee needed the VPN to access internal company files.

During the simulated investigation, the following symptoms were reported:

- The laptop could access the internet.
- The VPN client displayed an authentication error.
- After the simulated authentication issue was addressed, the client reported that it could not reach the VPN server.
- After the simulated VPN connection succeeded, the user could not access the internal file server.

The symptoms suggested that more than one troubleshooting area might need investigation.

## 2. Troubleshooting Objectives

- Identify the stage at which the VPN connection failed.
- Distinguish authentication problems from connectivity problems.
- Check VPN configuration and server reachability.
- Investigate internal DNS, network settings, and access permissions.
- Validate the result and document the incident.
- Follow security policies and escalate when necessary.

## 3. Troubleshooting Process

### Step 1: Gather Information

The technician should first ask the user for:

- The exact VPN error message.
- Whether normal internet access works.
- When the issue started and whether anything changed recently.
- Whether other employees are experiencing the same problem.
- The VPN client name and version, if relevant.
- Whether the user can access other approved company resources.

**Purpose:** Gather evidence before changing configuration or reinstalling software.

### Step 2: Investigate Authentication

**Simulated symptom:** The VPN client displays `Authentication failed`.

Recommended checks:

1. Verify the user's identity according to company procedures.
2. Check the account status using authorized IT tools.
3. Confirm the correct sign-in method and whether the password or authentication requirements have changed.
4. Check whether multi-factor authentication (MFA) is required and functioning.
5. Follow the approved account-recovery or escalation procedure if necessary.

**Security precautions:**

- Never ask the user to disclose their password or MFA code.
- Never disable MFA for all users to resolve an individual issue.
- Do not change account security settings without authorization.

### Step 3: Check VPN Server Connectivity

**Simulated symptom:** The VPN client displays `Unable to reach VPN server`.

Recommended checks:

1. Verify the VPN server address against the organization's approved configuration.
2. Review the VPN client's connection settings.
3. Check network reachability using approved diagnostic tools.
4. Check whether the VPN service or server has a reported outage.
5. Review relevant firewall, DNS, routing, or network restrictions with the responsible team.

A basic Windows connectivity test, when appropriate for the actual environment, is:

```powershell
Test-NetConnection vpn.company.example -Port 443
```

**Important:** Replace `vpn.company.example` with the organization's actual approved VPN hostname and use the port required by its VPN configuration. Port 443 is only an example; not every VPN uses it.

Interpretation:

- `TcpTestSucceeded : True` indicates that the TCP connection to the specified host and port succeeded.
- `TcpTestSucceeded : False` indicates that the TCP connection failed, but does not by itself establish the cause.

This test is relevant only when the VPN uses TCP on the specified port. Other VPN protocols require different diagnostic methods.

### Step 4: Investigate Internal Resource Access

**Simulated symptom:** The VPN connects, but the user cannot access the company file server.

Recommended checks:

1. Confirm that the VPN connection remains active.
2. Verify the internal file server hostname and approved access path.
3. Check internal DNS resolution.
4. Review the VPN-assigned IP address, DNS servers, routes, and other relevant network settings.
5. Confirm that the user has permission to access the requested resource.
6. Escalate routing, firewall, server-side, or access-control issues to the responsible team.

Example Windows commands:

```powershell
ipconfig /all
nslookup fileserver.company.example
```

**Command purpose:**

- `ipconfig /all` displays network adapter configuration, including IP addresses, DNS servers, and DHCP information.
- `nslookup` queries DNS to check whether a hostname resolves.

Use the organization's real internal hostname only in an authorized environment. The example hostname above is fictional.

**Important:** Successful DNS resolution does not prove that the file server is reachable or that the user has permission to access it.

### Step 5: Validate the Resolution

In this simulated scenario, the VPN eventually connects and the user confirms access to the internal file server.

A technician should validate that:

- The VPN connects without the original error.
- The required internal resource opens successfully.
- Authentication and MFA continue to work as required.
- No security control was bypassed.
- The user confirms the service has been restored.

The exact underlying root cause is **not independently confirmed** in this exercise. The scenario illustrates a troubleshooting sequence, not evidence of a real diagnosis.

## 4. Simulated Findings

| Area | Simulated observation | Next action |
|---|---|---|
| Internet | Internet access works | Continue with VPN-specific checks |
| Authentication | Authentication error reported | Verify account and sign-in requirements |
| VPN connectivity | VPN server reachability error reported | Check approved configuration and network path |
| Internal resources | File server unavailable after VPN connects | Check DNS, routes, network settings, and permissions |
| Final validation | User confirms VPN and file-server access | Document the outcome |

These observations are fictional scenario details, not actual diagnostic results.

## 5. Root Cause and Resolution

**Root cause:** Not independently confirmed in the simulated case.

**Simulated resolution:** The authentication and connectivity stages were investigated, the connection was restored within the scenario, and the user confirmed access to the internal file server.

In a real support ticket, record only the cause supported by the available evidence. If the cause remains uncertain, document the observed symptoms, verified findings, actions taken, and any remaining uncertainty.

## 6. Escalation Guidelines

Escalate to the appropriate team when:

- Multiple users report the same VPN failure.
- The VPN server appears unavailable.
- Routing, firewall, or network infrastructure changes are required.
- Account or MFA recovery requires additional authorization.
- The VPN connects but internal resources remain inaccessible.
- The issue cannot be resolved within the technician's permissions.

Include the error message, timestamps, relevant test results, scope of impact, and steps already performed. Never include passwords, MFA codes, or other secrets in the ticket.

## 7. Skills Demonstrated

- Windows 11 troubleshooting
- VPN and remote-access fundamentals
- Authentication and MFA security
- Basic TCP connectivity testing
- DNS troubleshooting
- IP configuration and routing fundamentals
- Access-permission checks
- Incident documentation and escalation
- User communication and service validation

## 8. Lessons Learned

1. A working internet connection does not guarantee VPN connectivity.
2. Authentication failure and server reachability failure are different symptoms.
3. A successful VPN connection does not guarantee access to every internal resource.
4. DNS, routing, and permissions should be investigated systematically.
5. Diagnostic results must be interpreted within the relevant VPN configuration.
6. Protecting credentials and following authorization policies are essential.
7. The technician should validate service restoration and document any uncertainty before closing the ticket.

## 9. Safety and Scope

This portfolio project is a simulated learning exercise.

- No real company network or VPN was accessed.
- No real user credentials or accounts were used.
- No production firewall or network configuration was changed.
- No Azure resources were created, started, or modified.
- All reported symptoms and outcomes are illustrative.

## Conclusion

This project demonstrates a structured approach to Windows VPN troubleshooting, from gathering initial symptoms through authentication, server connectivity, internal resource access, validation, and documentation.

It is suitable as a simulated case study for an entry-level IT Support Specialist or Service Desk portfolio.
