# Project 19: Windows Blue Screen and Unexpected Restart Troubleshooting

## Project Overview

**Ticket ID:** BSOD-001  
**Category:** Windows Desktop Support / System Stability  
**Environment:** Simulated Windows 11 laptop  
**Status:** Stable during the simulated initial observation period  
**Project Type:** IT Support Portfolio Case Study

> **Important:** This is a fictional troubleshooting exercise for learning and portfolio demonstration. No real device was accessed, diagnosed, or modified. No Azure resources were created, started, or modified.

## 1. Problem Description

A user reported that their Windows 11 laptop had restarted unexpectedly twice during the day. On one occasion, the user saw the blue-screen message:

`Your device ran into a problem and needs to restart.`

The user was working on an important document when the incident occurred.

During the simulated investigation:

- Windows started normally after the unexpected restart.
- Reliability Monitor showed a Windows failure around the reported time.
- The user reported that the issue began shortly after a device driver update.
- The technician considered checking protected Windows system files.
- The laptop remained stable during the initial simulated observation period after troubleshooting.

These observations are fictional. The underlying cause was not independently confirmed.

## 2. Troubleshooting Objectives

- Gather the symptoms, timing, and any available stop code.
- Protect important user data.
- Review system stability history and relevant event logs.
- Investigate recent driver changes.
- Check Windows system-file integrity when appropriate.
- Verify system stability and document unresolved uncertainty.

## 3. Troubleshooting Process

### Step 1: Gather Initial Information

Before making changes, ask the user:

1. When did the unexpected restarts begin?
2. Was a blue-screen stop code displayed?
3. Did the user recently install a driver, application, or Windows update?
4. Does Windows start normally now?
5. Was any work lost or corrupted?
6. Are other computers experiencing similar problems?

Record the approximate restart times and the exact error message if available.

**Purpose:** Establish the incident timeline, assess the impact, and identify useful diagnostic clues.

**Safety:** Protect important files and unsaved work where possible. If the computer repeatedly crashes or shows signs of hardware failure, avoid unnecessary repeated restarts and follow the organization's recovery procedures.

### Step 2: Review Reliability Monitor

Reliability Monitor provides a timeline of Windows failures, application crashes, and other stability events.

To open it:

1. Open the Start menu.
2. Search for `View reliability history`.
3. Open the result.
4. Find the date and time of the unexpected restart.
5. Review relevant critical events and technical details.
6. Record any available failure information.

**Simulated finding:** Reliability Monitor shows a Windows failure near the reported restart time.

This establishes a relevant event in the timeline, but it does not independently identify the cause.

### Step 3: Review Event Viewer

Event Viewer provides additional information about system events.

To investigate:

1. Open Event Viewer.
2. Navigate to **Windows Logs → System**.
3. Filter or review events around the restart time.
4. Record relevant event IDs, providers, timestamps, and messages.
5. Compare the events with Reliability Monitor and any available stop-code information.

For example, Event ID 41 from the `Kernel-Power` provider can indicate that Windows restarted without a clean shutdown.

**Important:** Event ID 41 does not, by itself, prove a power-supply, battery, driver, or other specific hardware failure. It is a clue to investigate alongside other evidence.

### Step 4: Investigate Recent Driver Changes

**Simulated clue:** The user reports that the problem began shortly after a device driver update.

Recommended checks:

1. Ask which device or driver was updated.
2. Review the driver version and installation timeline.
3. Check compatibility with the Windows version and device model.
4. Review relevant error messages or crash information.
5. Follow approved procedures to roll back or reinstall the specific driver if evidence supports that action.
6. Retest system stability after the change.

**Safety precautions:**

- Do not remove every driver.
- Do not download drivers from untrusted websites.
- Use manufacturer-approved or organization-approved driver packages.
- Follow change-management procedures for managed computers.

The timing of a driver update is a useful clue, but it does not prove that the driver caused the crash.

### Step 5: Check Protected Windows System Files

If corruption is suspected, System File Checker can check protected Windows system files.

Run the following command in an elevated Command Prompt or terminal, following approved procedures:

```powershell
sfc /scannow
```

Possible results include:

- No integrity violations found.
- Corrupted files found and repaired.
- Corrupted files found, but some could not be repaired.

If SFC cannot repair detected corruption, investigate the reported result and follow approved Windows servicing procedures. DISM may be appropriate in some cases, depending on the findings.

**Important:** SFC does not diagnose every cause of a blue screen. A clean result does not rule out driver, memory, storage, thermal, power, or other hardware and software problems.

No command in this report was executed against a real device.

### Step 6: Investigate Further if Crashes Continue

If unexpected restarts continue, consider the following checks according to the evidence and organizational procedures:

- Review available stop codes and crash-dump files.
- Check recent driver and software changes.
- Run approved hardware diagnostics.
- Investigate memory or storage errors when indicated.
- Check device temperatures and power-related symptoms if relevant.
- Escalate persistent or unexplained crashes to the appropriate support team.

Do not assume a particular hardware component is defective without supporting evidence.

### Step 7: Validate Stability

After the approved troubleshooting steps:

1. Confirm Windows starts normally.
2. Verify the outcome of any repair or driver action.
3. Check whether new failures appear in the relevant logs.
4. Ask the user to confirm that normal work can resume.
5. Monitor for recurrence according to the support team's procedures.
6. Document the result and any remaining uncertainty.

**Simulated outcome:** The laptop starts normally and no further crashes occur during the initial observation period.

This does not establish that the underlying issue is permanently resolved.

## 4. Simulated Findings Summary

| Investigation area | Simulated observation | Next action |
|---|---|---|
| User report | Two unexpected restarts | Gather timeline and impact |
| System stability | Windows failure in Reliability Monitor | Review failure details |
| Event logs | Relevant events need correlation | Examine events around the restart |
| Recent changes | Driver update reported by user | Check driver details and compatibility |
| System integrity | SFC considered as a diagnostic step | Follow approved procedures if appropriate |
| Final validation | No further crashes during initial observation | Document and monitor for recurrence |

These are illustrative scenario details, not actual diagnostic results.

## 5. Root Cause and Resolution

**Confirmed root cause:** Not established in this simulated case.

**Simulated outcome:** The laptop starts normally and remains stable during the initial observation period following troubleshooting.

The reported driver update is a possible lead, not a confirmed cause. Additional diagnostic evidence would be required to determine whether the incident involved a driver, corrupted system files, hardware, power, or another factor.

A professional incident report should distinguish between:

- **Observed symptoms:** What the user experienced.
- **Diagnostic findings:** What the available evidence shows.
- **Actions taken:** What the technician actually performed.
- **Root cause:** The explanation supported by sufficient evidence.
- **Resolution status:** Whether the service has been restored and whether further monitoring is required.

## 6. Escalation Guidelines

Escalate the ticket when:

- Blue screens recur after approved troubleshooting.
- Windows cannot start normally.
- Hardware diagnostics report errors.
- Important data may be at risk.
- Crash-dump analysis or advanced debugging is required.
- The incident affects several devices.
- The cause remains unclear and the problem affects business operations.

Provide the support team with the stop code, timestamps, relevant event details, recent changes, repair results, and steps already performed.

Avoid including confidential user data or sensitive dump-file contents in public documentation.

## 7. Skills Demonstrated

- Windows 11 troubleshooting
- Reliability Monitor
- Event Viewer and system event interpretation
- Basic driver troubleshooting
- Windows system-file integrity checks
- Incident timeline and evidence collection
- Data protection and safe recovery
- Troubleshooting validation
- Escalation and technical documentation

## 8. Lessons Learned

1. Collect evidence before replacing hardware or reinstalling Windows.
2. Reliability Monitor and Event Viewer help establish a timeline, but do not always reveal the root cause.
3. An unexpected-shutdown event is not proof of a specific hardware fault.
4. A recent driver update is a clue that needs investigation, not proof of causation.
5. System File Checker can help investigate protected system-file corruption, but it does not detect every possible cause of a crash.
6. Make controlled changes and retest after each appropriate step.
7. Verify system stability and record any remaining uncertainty.
8. Escalate when the issue requires advanced diagnostics or additional permissions.

## 9. Safety and Scope

This project is a simulated learning exercise.

- No real computer was accessed or modified.
- No real crash logs or dump files were collected.
- No real driver was installed, removed, or rolled back.
- No system repair command was executed on a real device.
- No Azure resources were created, started, or modified.
- All findings and outcomes are illustrative.

## Conclusion

This project demonstrates an evidence-based approach to Windows blue-screen and unexpected-restart troubleshooting. It covers initial assessment, system stability history, event logs, driver investigation, system-file integrity, validation, and escalation.

These skills are relevant to entry-level IT Support Specialist and Service Desk roles, where careful diagnosis and accurate documentation are more valuable than guessing at a root cause.
