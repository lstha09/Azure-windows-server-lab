# Project 1: Azure RDP Connectivity Troubleshooting

## 1. Project Overview

**Project name:** Azure RDP Connectivity Troubleshooting  
**Role:** Junior Azure Cloud Support / IT Support  
**Technology:** Microsoft Azure, Windows Server, Remote Desktop Protocol (RDP), Network Security Groups (NSGs), Windows Firewall  
**Budget:** €0 per month  
**Project type:** Simulated troubleshooting exercise — no Azure resources deployed.

### Objective

The goal of this project is to understand how to troubleshoot Remote Desktop Protocol (RDP) connectivity issues when a user cannot connect to a Windows Server virtual machine in Microsoft Azure.

This project demonstrates a structured troubleshooting approach, basic Azure networking knowledge, security awareness, and cost control.

## 2. Initial Situation

The Azure virtual machine list is currently empty, and the original lab virtual machine is not available for testing.

Therefore, this project documents a simulated support incident rather than a confirmed live connection failure.

**Scenario:** A user reports that they cannot connect to a Windows Server virtual machine using Remote Desktop.

## 3. Support Ticket

**Ticket ID:** AZ-RDP-001  
**Issue:** Unable to connect to an Azure Windows Server VM using RDP  
**Impact:** The user cannot access the server remotely.  
**Priority:** To be assessed according to business impact and urgency.

### Possible causes

- The virtual machine is stopped or deallocated.
- The public IP address is missing or has changed.
- The Network Security Group (NSG) blocks inbound TCP port 3389.
- Windows Firewall blocks Remote Desktop connections.
- The Remote Desktop Services service is not running.
- The user's network blocks RDP traffic.
- The user is using an incorrect username or password.
- The hostname or IP address is incorrect.

## 4. Troubleshooting Procedure

### Step 1: Check the virtual machine status

In the Azure portal:

1. Open the Azure portal at https://portal.azure.com.
2. Search for **Virtual machines**.
3. Select the relevant virtual machine, if one exists.
4. Check its status.
5. Confirm whether the VM is running.

**Expected result:** The VM is running and available for connection.

**If the VM is stopped:** Investigate why before starting it. Starting a VM may incur charges, so check the expected cost first.

### Step 2: Verify the public IP address

1. Open the virtual machine's Overview page.
2. Check whether a public IP address is assigned.
3. Confirm that the IP address matches the address being used by the RDP client.

**Expected result:** The correct, current IP address is available.

**Possible resolution:** Correct the RDP destination if the IP address has changed.

### Step 3: Test TCP port 3389

From a Windows computer with PowerShell, run:

```powershell
Test-NetConnection -ComputerName <PUBLIC_IP> -Port 3389
```

Replace `<PUBLIC_IP>` with the actual public IP address.

**How to interpret the result:**

- `TcpTestSucceeded : True` — the TCP connection to port 3389 succeeded.
- `TcpTestSucceeded : False` — the connection failed; investigate network rules, firewall settings, VM status, and RDP service availability.

This test has not been executed against a live VM in this project. Results must be recorded only after an actual test.

### Step 4: Check the Network Security Group (NSG)

In the Azure portal:

1. Open the VM's Networking settings.
2. Locate the associated Network Security Group.
3. Review the inbound security rules.
4. Check whether TCP port 3389 is allowed from the intended source IP address.
5. Check whether another rule blocks the connection.

**Expected result:** An appropriate rule permits RDP from an authorized source.

**Security note:** Do not expose port 3389 to the entire internet (`Any` or `0.0.0.0/0`). Prefer restricted source IP addresses, VPN connectivity, or a more secure access method where available.

### Step 5: Check Windows Firewall and Remote Desktop Services

If authorized access to the server is available through a secure alternative method, run these PowerShell commands on the Windows Server.

Check the Remote Desktop Services status:

```powershell
Get-Service TermService
```

Check the Windows Firewall Remote Desktop rules:

```powershell
Get-NetFirewallRule -DisplayGroup "Remote Desktop"
```

**Expected result:** The Remote Desktop Services service is running, and the relevant firewall rules are enabled as appropriate.

Do not disable Windows Firewall as a troubleshooting shortcut. Investigate and correct only the specific rule or service issue identified.

### Step 6: Check the client network and credentials

- Verify that the correct server IP address or hostname is being used.
- Check whether the current Wi-Fi or network blocks outbound RDP traffic.
- Confirm the correct username and password.
- If permitted, test from another trusted network.
- Record the exact error message shown by the RDP client.

**Expected result:** The destination, network path, and credentials are verified.

## 5. Root Cause and Resolution

**Confirmed root cause:** Not yet determined.

**Resolution status:** Pending live testing.

Because the original VM is not currently available, no specific root cause or successful repair is claimed.

When a live test becomes possible, record:

- The observed symptom.
- The checks performed.
- The actual command output or Azure configuration evidence.
- The confirmed root cause.
- The corrective action taken.
- The result of the final connection test.

## 6. Security and Cost Control

Security practices followed in this project:

- Avoid opening RDP to the entire internet.
- Restrict remote access to authorized sources.
- Do not share passwords or other credentials in screenshots or GitHub.
- Do not disable security controls without a justified reason.
- Record actual findings instead of inventing test results.

Cost-control practices:

- No Azure resources have been deployed for this exercise.
- No VM has been started for this project.
- The troubleshooting report is stored in GitHub.
- Any future live test must be preceded by a review of the expected Azure charges.

## 7. Skills Demonstrated

- Azure virtual machine troubleshooting
- Basic Azure networking concepts
- Network Security Group (NSG) rule inspection
- TCP port connectivity testing
- Windows Server administration fundamentals
- PowerShell troubleshooting commands
- Remote Desktop connectivity troubleshooting
- Security-conscious problem solving
- Technical documentation and support-ticket writing
- Cloud cost awareness

## 8. Evidence and Screenshots

Screenshots can be added after completing relevant checks.

Suggested evidence:

1. Azure Virtual Machines page showing the current lab status.
2. Example `Test-NetConnection` output from an actual test.
3. NSG inbound rule configuration, with sensitive information hidden.
4. PowerShell service-status output, if a server becomes available.
5. Final troubleshooting notes and resolution.

**Important:** Label any example or simulated output clearly. Do not present simulated results as evidence from a real Azure environment.

## 9. Project Summary

This project documents a structured approach to troubleshooting Azure RDP connectivity issues. It covers VM status, public IP addresses, NSG rules, TCP port testing, Windows Firewall, Remote Desktop Services, client networking, and credentials.

The exercise also demonstrates security best practices and awareness of Azure costs. The next step is to perform the checks against an available lab VM when this can be done safely within the €0 monthly budget.

**Overall project status:** The Azure RDP troubleshooting procedures and NSG scenarios have been documented as simulations. The original Azure VM is not currently available for live validation. The simulated tickets demonstrate proposed troubleshooting and resolution workflows; they do not represent a verified repair of a live Azure environment.


## 10. Client-Side Connectivity Test Results

### Test 1: TCP port 3389 to example.com

**Command:**

```bash
nc -vz -G 5 example.com 3389
```

**Result:** Connection timed out.

**Interpretation:** The TCP connection to port 3389 was not established. This does not confirm an Azure problem because example.com is not the Azure VM.

### Test 2: TCP port 443 to example.com

**Command:**

```bash
nc -vz -G 5 example.com 443
```

**Result:** Connection timed out.

**Interpretation:** The TCP connection test did not succeed. The reason was not established by this test alone.

### Test 3: HTTPS request from Terminal

**Command:**

```bash
curl -I --connect-timeout 5 --max-time 10 https://example.com
```

**Result:** `HTTP/2 200`

**Interpretation:** Terminal successfully received an HTTP response over HTTPS.

### Current Conclusion

HTTPS connectivity from Terminal is working. The earlier TCP port test failures do not establish a general internet outage or an Azure configuration fault.

The next stage is to review the simulated Azure-side troubleshooting steps, including VM status, public IP address, Network Security Group rules, and Windows Remote Desktop settings.

**Cost:** No Azure resources created; no Azure VM charges incurred for these tests.

## 11. Azure NSG Troubleshooting Simulation

### Support Ticket AZ-RDP-002

**Issue:** A user cannot connect to a Windows Server VM using Remote Desktop Protocol (RDP).

**Affected port:** TCP 3389

**Simulated finding:** An inbound deny rule at priority 100 matches the RDP connection, while an allow rule at priority 200 permits TCP 3389 from an authorized source IP address.

### Root Cause

The matching deny rule has a higher priority than the allow rule. Azure evaluates the deny rule first and blocks the connection.

This finding is based on a simulated configuration, not a live Azure investigation.

### Proposed Resolution

In the simulated scenario, change the allow rule's priority from 200 to 50 while retaining the restriction to the authorized source IP address.

This allows the matching, authorized RDP traffic to be evaluated by the allow rule before the conflicting deny rule.

Before applying a real change, verify all relevant rule conditions, including source, destination, protocol, port, direction, and any NSG rules attached to the subnet or network interface.

### Security Considerations

Do not allow inbound TCP 3389 from `0.0.0.0/0` as a general troubleshooting fix. This exposes RDP to connection attempts from any IPv4 address.

Prefer restricted source IP addresses, VPN connectivity, or a more secure remote-access method where appropriate.

### Validation Plan

After an authorized change in a real environment:

1. Confirm the effective network security rules.
2. Test TCP connectivity to port 3389.
3. Attempt an RDP connection from the authorized source.
4. Record the actual result and any remaining errors.

No live validation was performed for this simulation.

### Cost and Resource Status

No Azure resources were created or modified. The exercise used a hypothetical NSG configuration and incurred no Azure resource charges.

## 12. NSG Rule Evaluation Exercise

### Objective

Practise identifying the matching Azure Network Security Group rule for inbound RDP traffic.

### Simulated Rules

| Priority | Source | Destination port | Action |
|---:|---|---:|---|
| 50 | 203.0.113.10 | 3389 | Allow |
| 100 | Any | 3389 | Deny |
| 65000 | Any | Any | Deny |

### Results

**Test 1:** Source `203.0.113.10`, TCP port 3389.

Result: Allowed by priority 50 because the source matches the specific allow rule.

**Test 2:** Source `198.51.100.25`, TCP port 3389.

Result: Denied by priority 100 because the source does not match the specific allow rule and matches the general deny rule.

**Security decision:** Restrict RDP access to authorized source IP addresses or an approved private-access method.

### Key Learning

Azure NSG rules are evaluated by priority, with lower numbers evaluated first. The first matching rule determines the outcome for the connection at that NSG.

In a real incident, inspect all relevant rule conditions and any NSGs attached to the subnet and network interface.

**Exercise status:** Completed as a simulation. No live Azure rules were changed.

**Cost:** No Azure resources were created or modified; no Azure resource charges were incurred for this exercise.

## 13. Ticket AZ-RDP-003 — End-to-End RDP Troubleshooting (Simulated)

### Project type
Documentation-only troubleshooting simulation. No live Azure resources were created, started, or modified.

### Incident description
A user could not connect to a Windows Server virtual machine through Remote Desktop Protocol (RDP). The initial symptom was a connection timeout.

### Troubleshooting process

1. **Check the VM and network configuration.** In the simulated evidence, the VM was running and had a public IP address.
2. **Verify the source IP address.** The user's public IP had changed after switching Wi-Fi networks, so it no longer matched the NSG allow rule.
3. **Propose a secure NSG fix.** Update the approved source-IP restriction only after verifying the current IP and obtaining authorization. Never expose RDP to all public IP addresses.
4. **Check effective network rules and routing.** Review the NSGs associated with the network interface and subnet, as applicable, along with the network path.
5. **Check Windows Server.** Verify Remote Desktop settings, Windows Firewall rules, Remote Desktop Services, and the RDP listener.
6. **Investigate authentication.** If TCP connectivity succeeds but login fails, verify the username format, account status, and credentials.
7. **Check authorization.** If the user lacks Remote Desktop sign-in permission, request approval and grant only the required access.
8. **Validate the resolution.** Retest TCP connectivity and RDP login. Close the ticket only after successful validation.

### Simulated findings
The exercise used hypothetical evidence to practise identifying a source-IP mismatch, a disabled Windows Firewall rule, and missing Remote Desktop sign-in permission. These were assumed findings for the exercise, not a confirmed diagnosis of a real Azure VM.

### Security considerations
- Follow the principle of least privilege.
- Keep RDP access restricted to authorized source IPs or an appropriate private-access solution.
- Do not disable the entire Windows Firewall.
- Do not grant administrator privileges unless required and approved.
- Never include passwords, secrets, or sensitive connection details in GitHub documentation.

### Final outcome
**Simulated status:** Resolved after the proposed network, firewall, and authorization fixes were applied and the final connection tests succeeded.

**Cost control:** No Azure resources were created, started, or modified during this exercise. No Azure resource charges were incurred by the simulation.
