# Project 04: Microsoft 365 and Entra ID Sign-In Troubleshooting

## Project Overview

**Ticket ID:** M365-001  
**Category:** Microsoft 365 / Microsoft Entra ID  
**Difficulty:** Beginner  
**Environment:** Simulated support scenario  
**Status:** Partially resolved; final verification pending  
**Cost:** €0

### Objective

Practise a structured approach to Microsoft 365 sign-in issues, identity verification, Conditional Access, device compliance, application-specific troubleshooting, and ticket documentation.

## 1. Initial Support Ticket

**User report:**

"I can't sign in to Microsoft 365. I enter my work email and password, but the sign-in fails. I need access to Outlook and Teams for work."

**Initial findings in the simulated scenario:**
- The user could sign in the previous day.
- The user is using a browser on a MacBook.
- A colleague can access Microsoft 365 normally.
- The exact cause is initially unknown.

## 2. Troubleshooting Process

### Step 1: Gather information

- Ask for the exact error message.
- Confirm the work account and browser being used.
- Determine which services are affected.
- Check whether other users experience the same problem.
- Never request the user's password or MFA code.

### Step 2: Verify identity and investigate account status

The user reports an incorrect-account-or-password message.

**Action:** Follow the organisation's approved identity-verification and password-reset procedures. If the issue persists, an authorised administrator can investigate account status and relevant sign-in logs.

### Step 3: Investigate the sign-in failure

In the simulated case, an authorised administrator reports that Conditional Access requires a compliant device, but the user's MacBook is not marked compliant.

**Evidence limitation:** The Conditional Access finding is simulated. In a real Microsoft Entra ID investigation, an authorized administrator should verify the sign-in log, including the failure reason, Conditional Access result, applied policy, and device-compliance information.

**Action:** Follow the approved device-compliance process and check the applicable policy. Do not disable security controls to bypass the restriction.

### Step 4: Verify access

After the device-compliance issue is addressed in the simulation:
- The user can open Outlook.
- Teams still displays a sign-in error.

**Next action:** Gather the exact Teams error and timestamp, investigate any application-specific authentication or client issue, and escalate if necessary. Confirm Teams access before closing the ticket.

## 2.1 Example Microsoft Entra ID investigation checks

The following checks describe how an authorized administrator could investigate a Microsoft 365 sign-in failure. They were not performed against a live tenant during this simulation.

**Check sign-in logs:**
1. Open the Microsoft Entra admin center.
2. Navigate to **Identity → Monitoring & health → Sign-in logs**.
3. Filter by the affected user and approximate sign-in time.
4. Review the sign-in status, failure reason, Conditional Access tab, and device information.

**Check Conditional Access:**
1. Open **Protection → Conditional Access → Policies**.
2. Identify the policy applied to the affected sign-in.
3. Review the grant controls and device-compliance requirement.
4. Confirm the policy result in the corresponding sign-in log.

**Important:** Do not change or disable Conditional Access policies simply to restore access. Follow the organization's approved security and device-compliance procedures.

## 3. Root Cause and Resolution

**Identified issue in the simulation:** The initial sign-in was blocked by a Conditional Access policy because the MacBook did not meet the required device-compliance condition.

**Progress:** Outlook access was restored in the simulated scenario after the compliance requirement was addressed.

**Outstanding issue:** Teams access remains unverified and requires further investigation.

**Important:** The original incorrect-password message was not independently confirmed as the root cause. This scenario does not establish whether a separate password or authentication issue existed.

**Validation limitation:** Outlook access restoration is a simulated outcome. Teams access remains unverified, and no live Microsoft 365 account, Conditional Access policy, or device-compliance status was changed or tested.

## 4. Security and Support Best Practices

- Verify identity before account-related changes.
- Never ask users to disclose passwords or MFA codes.
- Use least-privilege access and approved administrative procedures.
- Review sign-in evidence before deciding on a root cause.
- Do not disable Conditional Access or other security controls as a shortcut.
- Record actions, findings, and unresolved issues clearly.
- Close the ticket only after the affected services have been tested.

## 5. Quiz Results

| Question | Answer | Result |
|---|---|---|
| Q1: Initial information gathering | B | Correct |
| Q2: Persistent sign-in failure | C | Correct |
| Q3: Investigate account restrictions | B | Correct |
| Q4: Conditional Access block | C | Correct |
| Q5: Verify application access | C | Correct |

**Score: 5/5 (100%)**

## 6. Skills Practised

- Microsoft 365 sign-in troubleshooting
- Microsoft Entra ID fundamentals
- Conditional Access concepts
- Device-compliance troubleshooting
- Identity verification and account security
- Ticket documentation and escalation
- Service restoration and verification

## 7. Lab Safety and Limitations

This is a simulated learning exercise. No real Microsoft 365 tenant or Entra ID account was accessed, and no real sign-in logs were examined.

**Azure resources created, started, or modified:** None  
**Azure cost:** €0

## Conclusion

This project demonstrates a methodical approach to identity and application-access troubleshooting. The case remains open in the simulation because Teams access has not yet been verified. Further investigation and documented validation would be required before closure.
