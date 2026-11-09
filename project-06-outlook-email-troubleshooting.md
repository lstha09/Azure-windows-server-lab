# Project 06: Microsoft Outlook Email Troubleshooting

## Project Overview

**Ticket ID:** EXCHANGE-001  
**Category:** Microsoft Outlook / Exchange Online  
**Difficulty:** Beginner  
**Environment:** Simulated support scenario  
**Status:** Resolved in simulation  
**Cost:** €0

## 1. Initial Support Ticket

**User report:**

"Outlook opens, and I can see my old emails, but messages I send stay in the Outbox. I also haven't received any new emails since this morning."

### Initial findings

- Outlook opens and displays existing emails.
- Outgoing messages remain in the Outbox.
- New incoming emails appear to be missing.
- The initial cause is unknown.

## 2. Troubleshooting Process

### Step 1: Check connectivity

Gather the exact error message, check Outlook's connection status and network connectivity, and determine whether other users are affected.

### Step 2: Check Work Offline mode

The user reports that Outlook displays "Working Offline."

**Action:** Check whether Work Offline mode is enabled. Turn it off if appropriate and verify whether Outlook reconnects.

**Simulated result:** Outlook reconnects, but the test email still remains in the Outbox.

### Step 3: Test the outgoing message

The user confirms that websites work normally and a colleague can send email.

**Action:** Check for an unusually large message or problematic attachment. Try a short test email without an attachment and record any error.

**Simulated result:** The short test email also fails to send.

### Step 4: Compare Outlook desktop with Outlook on the web

The user reports that Outlook on the web can send and receive emails successfully, while the desktop application cannot send messages.

**Action:** Focus troubleshooting on the desktop Outlook client. Record the Outlook version and error details, restart Outlook, and follow approved troubleshooting procedures or escalate if necessary.

**Evidence limitation:** The desktop-client-specific finding is based on simulated test results. In a real investigation, an authorized technician should verify Outlook connection status, application version, relevant error messages, and Microsoft 365 service health before identifying the cause.

### Step 5: Verify the resolution

In the simulation, further approved troubleshooting restores the desktop application's ability to connect.

The user confirms that:
- A test email sends successfully.
- New emails can be received.
- Outlook desktop is functioning normally again.

  ## 2.1 Example Outlook investigation checks

The following checks demonstrate how an authorized support technician could investigate an Outlook desktop issue. They were not performed against a live Microsoft 365 environment during this simulation.

**Check Outlook connection status:**
1. Open Outlook desktop.
2. Check whether Outlook displays Working Offline or Disconnected.
3. Verify that the device has a working internet connection.
4. If appropriate, turn off Work Offline and check whether Outlook reconnects.

**Compare with Outlook on the web:**
1. Sign in to Outlook on the web using the user's authorized account.
2. Send a short test email.
3. Check whether new messages arrive.
4. Compare the results with Outlook desktop.

**Check Microsoft 365 service health (administrator access):**
1. Open the Microsoft 365 admin center.
2. Navigate to **Health → Service health**.
3. Review any Exchange Online or Outlook-related service incidents.
4. Record relevant incidents and follow the organization's support procedures.

**Important:** Successful Outlook on the web access does not prove that every Exchange Online service is functioning normally. Check the available evidence before deciding whether to repair the desktop application or escalate the issue.

## 3. Root Cause and Resolution

**Resolution:** The desktop Outlook application was restored in the simulated case, and successful sending and receiving were verified.

**Root cause:** The exact underlying cause was not established in the scenario. The evidence indicated a desktop-client-specific issue because Outlook on the web worked.

**Ticket status:** Resolved in simulation after successful tests and user confirmation.

**Validation limitation:** The successful restoration of Outlook desktop is a simulated outcome. No live Outlook application was repaired, no Microsoft 365 mailbox was tested, and no actual Exchange Online service was modified.

## 4. Support Best Practices

- Gather evidence before making changes.
- Check connection status before reinstalling applications.
- Test with a simple email without an attachment.
- Compare desktop Outlook with Outlook on the web.
- Avoid deleting mailboxes or disabling security settings without a justified, authorised process.
- Document troubleshooting actions and observed results.
- Confirm both sending and receiving work before closing the ticket.

## 5. Quiz Results

| Question | Answer | Result |
|---|---|---|
| Q1: Initial investigation | B | Correct |
| Q2: Work Offline mode | C | Correct |
| Q3: Test the outgoing message | B | Correct |
| Q4: Compare desktop and web Outlook | C | Correct |
| Q5: Verify and document the fix | B | Correct |

**Score: 5/5 (100%)**

## 6. Skills Practised

- Outlook connectivity troubleshooting
- Work Offline mode
- Outbox and attachment troubleshooting
- Outlook desktop versus web comparison
- Basic Exchange Online support concepts
- Ticket documentation and escalation
- Service restoration verification

## 7. Lab Safety and Limitations

This is a simulated learning exercise. No real Outlook client, Microsoft 365 mailbox, or Exchange Online tenant was accessed.

**Azure resources created, started, or modified:** None  
**Azure cost:** €0

## Conclusion

This project demonstrates a structured approach to email troubleshooting: check connectivity, test the message, compare applications, follow approved troubleshooting procedures, and verify that sending and receiving work before closing the ticket.
