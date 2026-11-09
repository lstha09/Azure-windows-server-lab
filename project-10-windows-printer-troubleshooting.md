# Project 10 — Windows Printer Troubleshooting

**Ticket ID:** PRN-001  
**Category:** End-user support / Printing  
**Environment:** Windows 11 and a shared office printer  
**Difficulty:** Beginner  
**Status:** Simulated troubleshooting exercise

## 1. Incident Summary

An employee reported that their Windows 11 computer could not print documents to the office printer. Other employees could print successfully using the same printer.

The initial evidence suggested that the issue might be specific to the affected user's computer, print queue, driver, or printer configuration. The actual cause was not confirmed.

**Important:** This is a simulated support case for learning and portfolio demonstration. It is not a record of a real incident.

## 2. Symptoms

- The affected user could not print documents.
- Other employees could print to the same office printer.
- The user reported a print queue error.
- A document remained stuck in the print queue.
- Clearing the affected user's stuck job did not immediately resolve the issue.
- The investigation then considered the Print Spooler service, driver, port, and connection settings.

## 3. Troubleshooting Procedure

### Step 1 — Gather information

Ask the user:
- Which printer are you trying to use?
- What exact error message appears?
- Does the problem affect every document or only one?
- When did the problem start?
- Can another user print successfully?

Confirm the printer selection and connection before making changes.

### Step 2 — Check the print queue

Open the printer queue in Windows Settings or through the printer's queue window.

Check for:
- Stuck print jobs
- Paused printing
- Error messages
- Jobs waiting indefinitely

Before cancelling a job, confirm with the user if the document is important. Follow the organization's approved procedure.

### Step 3 — Check the Print Spooler

The Windows Print Spooler manages print jobs.

Using authorized troubleshooting tools, check whether the service is running. If a restart is necessary, follow company procedures and consider the effect on other users' print jobs.

Do not make service changes without appropriate authorization.

## 3.1 Example PowerShell printer troubleshooting commands

The following commands demonstrate how an authorized support technician could investigate printer issues on a Windows device. They were not executed during this simulation.

**List installed printers:**

```powershell
Get-Printer
```

**Check the Print Spooler service:**

```powershell
Get-Service -Name Spooler
```

**Check the printer queue and job status:**

```powershell
Get-PrintJob -PrinterName "Office Printer"
```

Note: Replace `"Office Printer"` with the actual printer name.

**Check installed printer drivers:**

```powershell
Get-PrinterDriver
```

**Check printer port configuration:**

```powershell
Get-PrinterPort
```

**Important:** These commands are for Windows devices, not macOS. They are examples for investigation and do not automatically fix printing problems. Restarting the Print Spooler or changing printer settings requires appropriate authorization and may affect other users.

### Step 4 — Verify the printer configuration

If the queue is clear and the service is running, check:
- The installed printer driver and whether it is appropriate for the printer.
- The configured printer port.
- The printer's connection and availability.
- Whether the settings match the organization's approved configuration.

Avoid reinstalling drivers or changing ports until you have gathered sufficient evidence.

**Evidence limitation:** The symptoms and possible causes are fictional examples. In a real investigation, an authorized technician should review the printer queue, Print Spooler service status, driver details, printer port, and relevant error messages before identifying the root cause.

### Step 5 — Test the result

After an approved correction:
1. Ask the user to submit a small test document.
2. Confirm that the job leaves the queue.
3. Verify that the document prints successfully.
4. Ask the user to confirm normal printing has resumed.
5. Record the checks, actions, and results.

If printing still fails, document the evidence and escalate to the appropriate desktop support, print-server, or network team.

## 4. Root Cause

**Not confirmed.**

The exercise identifies possible causes but does not establish which one actually caused the simulated failure. A professional ticket should not claim that the issue is fixed until testing confirms the result.

## 5. Resolution and Validation

No real printer was accessed or changed during this exercise.

In a real support case, the ticket would remain open or be escalated until:
- The cause was identified or adequately investigated.
- An approved corrective action was completed.
- A successful test print was verified.
- The user confirmed that the service was restored.

  **Validation limitation:** No live printer was accessed, no print job was cleared, no Print Spooler service was restarted, and no test document was printed during this simulation. The resolution and validation steps describe the procedure that would be followed in a real support case.

## 6. Security and Good Practice

- Use approved drivers and configuration settings.
- Obtain authorization before changing services or drivers.
- Avoid cancelling other users' print jobs.
- Do not disable security controls to troubleshoot printing.
- Record evidence rather than guessing at the root cause.
- Escalate when permissions or specialist knowledge are required.

## 7. Skills Demonstrated

- Windows 11 end-user troubleshooting
- Printer queue investigation
- Basic understanding of the Print Spooler
- Driver, port, and connection checks
- User communication and service validation
- Ticket documentation and escalation
- Safe, evidence-based troubleshooting

## 8. Learning Quiz Result

**Score: 5/5**

The exercise covered initial checks, print queue investigation, safe job handling, the Print Spooler service, and printer driver/port/connection verification.

## 9. Scope and Cost

This project is documentation and simulated learning only. No Azure resources were created, started, or modified. No cloud services were required, and Azure cost for this exercise was **€0**.
