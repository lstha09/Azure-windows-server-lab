# Project 05: Microsoft Intune Device Compliance Troubleshooting

## Project Overview

**Ticket ID:** INTUNE-001  
**Category:** Microsoft Intune / Endpoint Management  
**Difficulty:** Beginner  
**Environment:** Simulated support scenario  
**Status:** Resolved in simulation  
**Cost:** €0

## 1. Initial Support Ticket

**User report:**

"My company laptop is marked as non-compliant, and I cannot access some company resources. The laptop appears to work normally."

**Initial findings:**
- Device operating system: Windows 11
- User can sign in to Windows.
- Some company resources are blocked.
- The exact compliance failure is initially unknown.

## 2. Troubleshooting Process

### Step 1: Gather information

- Ask for the exact error message.
- Identify the affected device and blocked resources.
- Determine whether other users or devices are affected.
- Check the device's compliance details using authorised support procedures.

### Step 2: Identify the security requirement

In the simulation, the user reports that Windows real-time protection is turned off.

**Action:** Follow approved troubleshooting procedures to check and restore real-time protection.

### Step 3: Investigate the continued compliance failure

After protection is restored, the device still shows Non-compliant.

**Action:** Check the latest compliance details, device sync or check-in status, and any other failing requirements.

### Step 4: Resolve the Windows version requirement

The simulated compliance details show that the device does not meet the minimum Windows version required by company policy.

**Action:** Follow the approved Windows update process. Do not bypass compliance requirements without appropriate authorisation.

**Evidence limitation:** The real-time protection and Windows version findings are simulated. In a real Intune investigation, an authorized administrator should review the device's compliance details, applicable compliance policy, last check-in time, and reported failure reasons before deciding on corrective action.

### Step 5: Verify the result

In the simulation:
- The user installs the required Windows update.
- The device syncs with Intune again.
- The compliance status changes to Compliant.
- The user confirms that company resources are accessible again.

  ## 2.1 Example Microsoft Intune investigation checks

The following steps demonstrate how an authorized support technician could investigate a non-compliant device. They were not performed against a live Intune tenant during this simulation.

**Review device compliance:**
1. Open the Microsoft Intune admin center.
2. Navigate to **Devices → All devices**.
3. Find the affected device.
4. Review its compliance status and last check-in time.
5. Open the device's compliance details and identify the failing requirement.

**Check Windows security status:**
1. On an authorized Windows device, open Windows Security.
2. Select **Virus & threat protection**.
3. Review the real-time protection status.
4. Follow approved procedures if protection is disabled.

**Check Windows version:**

Run this command on an authorized Windows device:

```powershell
Get-ComputerInfo | Select-Object WindowsProductName, WindowsVersion, OsBuildNumber
```

**Important:** A device sync requests updated communication with Intune, but it does not automatically fix a failing compliance requirement. Verify the reported compliance result after synchronization.

## 3. Root Cause and Resolution

**Identified compliance issues in the simulation:**
1. Real-time protection was turned off.
2. The device did not meet the organisation's minimum Windows version requirement.

**Resolution:** Restore real-time protection, update Windows through the approved process, sync the device, and verify compliance and access.

**Ticket status:** Resolved in simulation after the user confirmed access was restored.

**Validation limitation:** The compliance restoration and successful access described above are simulated outcomes. No live Windows device was updated, no Intune synchronization was performed, and no actual company resource access was tested.

## 4. Security and Support Best Practices

- Gather evidence before changing settings.
- Follow approved procedures for security settings and updates.
- Never bypass compliance policies simply because a user is in a hurry.
- Use authorised access and least-privilege permissions.
- Confirm the latest compliance status after syncing.
- Record findings, actions, and user confirmation before closing a ticket.

## 5. Quiz Results

| Question | Answer | Result |
|---|---|---|
| Q1: Initial investigation | B | Correct |
| Q2: Real-time protection | C | Correct |
| Q3: Continued non-compliance | B | Correct |
| Q4: Policy bypass request | C | Correct |
| Q5: Ticket closure | B | Correct |

**Score: 5/5 (100%)**

## 6. Skills Practised

- Microsoft Intune device compliance fundamentals
- Windows security settings
- Windows update troubleshooting
- Device sync and compliance reevaluation
- Security policy awareness
- Help-desk ticket documentation
- Resolution verification and escalation

## 7. Lab Safety and Limitations

This project is a simulated learning exercise. No real Intune tenant or managed device was accessed, and no live compliance settings were changed.

**Azure resources created, started, or modified:** None  
**Azure cost:** €0

## Conclusion

This project demonstrates a structured approach to endpoint compliance troubleshooting: identify the failing requirement, apply an approved fix, verify the compliance result, and confirm that the user can access the required resources before closing the ticket.
