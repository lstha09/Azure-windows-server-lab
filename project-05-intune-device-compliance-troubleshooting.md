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

### Step 5: Verify the result

In the simulation:
- The user installs the required Windows update.
- The device syncs with Intune again.
- The compliance status changes to Compliant.
- The user confirms that company resources are accessible again.

## 3. Root Cause and Resolution

**Identified compliance issues in the simulation:**
1. Real-time protection was turned off.
2. The device did not meet the organisation's minimum Windows version requirement.

**Resolution:** Restore real-time protection, update Windows through the approved process, sync the device, and verify compliance and access.

**Ticket status:** Resolved in simulation after the user confirmed access was restored.

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
