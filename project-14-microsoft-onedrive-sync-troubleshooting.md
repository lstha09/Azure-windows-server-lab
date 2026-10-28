# Project 14 — Microsoft OneDrive Sync Troubleshooting

## Project Overview

- **Ticket ID:** OD-001
- **Category:** Microsoft 365 / OneDrive / End-user support
- **Environment:** Simulated Microsoft 365 work environment
- **Device:** Windows 11
- **Issue:** A file saved in a OneDrive folder does not appear for colleagues.
- **Status:** Simulated troubleshooting completed for learning purposes
- **Tools:** OneDrive sync status, OneDrive error messages, Windows file management, and user verification

> **Important:** This is a simulated support case created for a learning portfolio. No real user's account or files were accessed, and no real Microsoft 365 tenant was changed. No Azure resources were created, started, or modified. Azure cost: €0.

## 1. User-Reported Problem

A user reports that a file saved in their OneDrive folder is not visible to colleagues. The OneDrive system tray icon displays a synchronization warning.

The user needs help determining why the file is not syncing and restoring access without losing data.

## 2. Initial Assessment

Before making changes, a support technician should gather the following information:

- When did the problem begin?
- Is the issue affecting one file or multiple files?
- Is the user signed in with the correct work or school account?
- What synchronization status and error message does OneDrive display?
- Is sufficient OneDrive storage available?
- Does the file name or path violate OneDrive restrictions?
- Is the file saved in the intended OneDrive location?
- Can the intended colleagues access other shared files?

The technician should record the exact error message and avoid destructive actions until the cause is better understood.

## 3. Troubleshooting Procedure

### Step 1 — Check OneDrive Sync Status

Inspect the OneDrive icon in the Windows notification area.

Check:
- Whether OneDrive is running.
- Whether synchronization is paused.
- Whether OneDrive displays an error or warning.
- Whether the correct work or school account is signed in.

**Simulated finding:** The correct work account is signed in, and OneDrive displays a synchronization warning.

**Action:** Record the warning and continue investigating.

### Step 2 — Check Available Storage

Check the user's OneDrive storage usage and quota using authorized Microsoft 365 tools.

**Simulated finding:** Storage is available, so a full storage quota is not the identified explanation in this scenario.

**Action:** Continue to the file-specific checks.

**Safety note:** Never delete files indiscriminately to free storage. Deletions in a synchronized folder can propagate to the cloud and other connected devices.

### Step 3 — Investigate the File Name and Path

Review the exact OneDrive error message.

Check whether:
- The file name contains unsupported characters.
- The file name or folder path exceeds applicable limits.
- The file is open or locked by another application.
- The file is located in the intended synchronized folder.
- Another restriction is preventing synchronization.

**Simulated finding:** OneDrive displays a file-name error for the affected file.

**Action:** Identify the restriction and, if appropriate, make an approved change to the file name or path. Preserve the original file and its contents before making changes.

### Step 4 — Investigate Persistent Synchronization

If the file name has been corrected but OneDrive remains on “Processing changes,” inspect the sync activity and any new error messages.

Check whether the file remains available locally and whether other files are syncing normally.

Use safe, approved troubleshooting steps. Avoid immediately unlinking the account, deleting the OneDrive folder, or resetting Windows.

If the problem persists, document the findings and escalate to the appropriate Microsoft 365 support team.

**Simulated finding:** The case includes a persistent synchronization stage requiring further status and error checks. No independently verified real-world root cause is established.

### Step 5 — Verify the Outcome

Before closing a real support ticket, ask the user to verify that:

1. OneDrive reports that synchronization is complete.
2. The file appears in the intended OneDrive location.
3. The file can be opened and its contents are correct.
4. The intended colleagues can access the file with the expected permissions.
5. No new synchronization errors remain.

Document any remaining issues rather than marking the ticket resolved prematurely.

**Simulated closure criterion:** The user confirms that the file is available to the intended colleagues and the issue is resolved. This is the expected validation procedure, not a claim that a real account was tested.

## 4. Example Troubleshooting Decision Table

| Observation | Possible explanation | Recommended action |
|---|---|---|
| OneDrive is paused | Synchronization is not currently running | Resume syncing if authorized |
| Storage quota is full | New content may not sync | Review usage and follow approved storage procedures |
| File-name error | Name or path restriction | Inspect the exact error and correct the issue safely |
| “Processing changes” persists | Sync may be delayed or stuck | Inspect activity, status, and new errors |
| File syncs but colleagues cannot access it | Sharing or permissions issue | Verify sharing settings and intended recipients |
| Problem remains unresolved | Cause is still unknown | Document evidence and escalate |

## 5. Data Protection and Security Considerations

- Verify the user's identity according to company policy before accessing account information.
- Use authorized Microsoft 365 administration tools only.
- Do not ask users to share passwords or authentication codes.
- Do not delete synchronized files without understanding the impact.
- Preserve the original file before attempting a corrective change.
- Verify sharing permissions rather than making a file public.
- Record only the information necessary for the support ticket.
- Escalate unresolved synchronization or permissions problems through the approved process.

## 6. Example Support Ticket Notes

**Ticket:** OD-001

**Reported issue:** A file saved in OneDrive is not appearing for colleagues. OneDrive displays a sync warning.

**Checks performed in the simulated scenario:**
- Verified the work account and synchronization status.
- Checked the storage quota.
- Investigated the file-name error.
- Considered persistent “Processing changes” status.
- Defined user and colleague verification steps.

**Actions:** Follow the approved troubleshooting procedure, preserve the original file, inspect error messages, and verify synchronization and sharing access.

**Outcome:** This is a simulated learning case. The procedure describes how to investigate and validate the issue; no real account was accessed and no real synchronization result was observed.

**Root cause:** Not independently confirmed.

**Escalation:** Required if synchronization or colleague access remains unresolved after approved troubleshooting.

## 7. Skills Demonstrated

- Microsoft OneDrive synchronization troubleshooting
- Microsoft 365 end-user support
- Error-message analysis
- Storage-quota investigation
- File-name and path troubleshooting
- Basic sharing and permissions awareness
- Data-loss prevention
- User communication and verification
- Ticket documentation and escalation

## 8. Learning Reflection

This exercise demonstrates a structured approach to OneDrive synchronization problems. A technician should begin with the sync status, account, and exact error message before making changes.

The most important lesson is to protect user data, avoid unnecessary resets or deletions, and verify both synchronization and colleague access before closing a ticket.

**Portfolio note:** This is a simulated troubleshooting exercise, not evidence of a production incident or a real Microsoft 365 tenant change.
