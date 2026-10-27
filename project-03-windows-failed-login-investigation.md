# Project 3: Windows Failed Login Investigation

## Ticket SEC-001 — Repeated Failed Remote Desktop Logins (Simulated)

**Project type:** IT Support / Windows Security Troubleshooting  
**Difficulty:** Beginner  
**Environment:** Simulated Windows Server Security Event Log investigation  
**Status:** Training exercise completed  
**Azure cost:** €0  
**Live environment changes:** None

> **Important:** This is a fictional training scenario. All event records, account details, timestamps, and IP addresses are simulated. No real security incident was investigated, and no live Windows Server was accessed or changed.

## 1. Project Overview

This project demonstrates a structured approach to investigating failed Windows sign-in attempts using Windows Security event logs.

The objectives were to:

- Understand Windows Security Event IDs 4625 and 4624.
- Interpret failed-logon status and substatus codes.
- Distinguish suspicious activity from confirmed compromise.
- Identify when a security incident should be escalated.
- Document investigation findings in a support ticket.
- Follow safe incident-response practices.

## 2. Incident Description

A fictional user reported a sign-in concern involving a Windows Server account.

The simulated Security log contained two failed Remote Desktop logon attempts followed by a successful logon for the same account and source address.

The user subsequently stated that they did not recognize the successful login.

**Ticket ID:** SEC-001  
**Affected account:** `LAB\labuser1`  
**Simulated service:** Remote Desktop  
**Priority:** Requires prompt security assessment under the organization's incident-response policy.

## 3. Simulated Security Event Evidence

| Time | Event ID | Description |
|---|---|---|
| 10:31 | 4625 | Failed Remote Desktop logon |
| 10:32 | 4625 | Failed Remote Desktop logon |
| 10:35 | 4624 | Successful Remote Desktop logon |

The fictional events used the same source IP address, `192.0.2.45`, and the same account, `LAB\labuser1`.

The address belongs to a range reserved for documentation and examples. It is not evidence of an actual user's location.

### Relevant Windows Event IDs

- **4625 — Failed logon:** Records an unsuccessful sign-in attempt.
- **4624 — Successful logon:** Records a successful sign-in.
- **4740 — User account locked out:** Can be relevant when investigating account lockouts in applicable Windows domain environments.

A successful logon following failed attempts does not establish whether the activity was legitimate or malicious.

## 4. Investigating the Failed Logon

The simulated Event ID 4625 details included:

- **Logon type:** 10 — RemoteInteractive, commonly associated with Remote Desktop.
- **Status:** `0xC000006D` — General logon failure.
- **Substatus:** `0xC000006A` — Commonly indicates an incorrect password.

### Interpretation

The substatus suggests that the password supplied during the failed attempt was incorrect.

Possible explanations include:

- The user mistyped their password.
- A saved credential was outdated.
- Someone attempted to access the account without authorization.

The event alone does not establish which explanation is correct.

## 5. Troubleshooting Workflow

### Step 1: Review the relevant Security events

Identify failed and successful logons, their timestamps, the affected account, logon type, and available source-address information.

### Step 2: Examine the failure details

Review the status and substatus codes in the failed-logon event. Use the event details to narrow down possible causes without assuming a definitive root cause.

### Step 3: Correlate related events

Compare the failed and successful logons. Review relevant surrounding events and additional available evidence to determine whether the activity is consistent with expected use.

### Step 4: Verify the activity

Contact the user or authorized administrator through the approved process.

In this simulation, the user stated that they did not recognize the successful login.

### Step 5: Escalate the suspected incident

Because the successful logon was unrecognized, escalate promptly to the authorized security team under the organization's incident-response policy.

Preserve relevant evidence and follow authorized instructions for any containment actions. Do not make unauthorized account changes or disable security controls.

### Step 6: Document the investigation

Record the relevant event IDs, timestamps, account details, observations, user statement, actions taken, and escalation reference where available.

Keep the ticket factual and avoid describing a suspected compromise as confirmed until the evidence supports that conclusion.

## 6. Resolution and Final Status

**Simulated outcome:** The case was escalated to the security team, which acknowledged receipt and continued its investigation.

The exercise did not establish a confirmed root cause or prove that the account had been compromised.

The appropriate support outcome is to document the escalation and follow the organization's ticket-handling procedure. The ticket should not be marked as a confirmed security resolution while the investigation remains open.

## 7. Security and Operational Best Practices

- Never ask a user to send their password.
- Never store passwords in support tickets.
- Do not delete or alter security logs to remove errors.
- Preserve relevant evidence according to organizational policy.
- Avoid assuming that every failed logon indicates an attack.
- Do not assume that a successful logon means the account is safe.
- Escalate suspected compromises promptly.
- Apply account restrictions or other containment measures only through authorized procedures.
- Protect log data and user information according to applicable policies.

## 8. Skills Practised

This exercise covered:

- Windows Security Event Viewer concepts.
- Failed-logon investigation.
- Event ID 4625 and Event ID 4624 interpretation.
- Logon type identification.
- Windows authentication status and substatus codes.
- Basic security incident triage.
- Evidence preservation and escalation.
- Support-ticket documentation.

## 9. Budget and Environment Safety

This project was completed as a documentation-only simulation using fictional evidence.

- No Azure resources were created.
- No Azure resources were started.
- No Azure resources were modified.
- No live Windows Server was accessed or changed.
- No real security incident was investigated.
- **Azure resource cost for this exercise: €0.**

## 10. Project Conclusion

This project demonstrates a basic, structured approach to Windows failed-login investigations.

The main lesson is to gather and correlate evidence, verify suspicious activity, escalate appropriately, and document the outcome accurately.

These skills are relevant to entry-level IT support, service desk, Windows support, and junior security operations workflows.
