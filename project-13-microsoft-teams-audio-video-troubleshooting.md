# Project 13 — Microsoft Teams Audio and Video Troubleshooting

## Project Overview

**Ticket ID:** TEAMS-001  
**Category:** Microsoft Teams audio troubleshooting  
**Environment:** Simulated IT support scenario  
**Status:** Resolved in the simulated scenario

This project demonstrates a structured approach to troubleshooting a Microsoft Teams microphone problem. It covers Teams device settings, Windows microphone permissions, sound input testing, application troubleshooting, and ticket documentation.

**Important:** This is a simulated learning exercise. No real user's computer was investigated, and no actual incident was diagnosed or resolved.

## 1. Simulated Support Ticket

**User report:**

"I can join a Microsoft Teams meeting, but my colleagues cannot hear me. My microphone works in another application."

**Initial observations in the scenario:**

- The user can join Teams meetings.
- The selected microphone appears to be correct.
- The microphone is not muted.
- Windows microphone permissions are enabled.
- The microphone works in Windows sound settings.
- Other colleagues can use Teams normally.

These are fictional observations created for practice.

## 2. Troubleshooting Objectives

- Identify whether the problem is related to microphone selection, permissions, hardware, or the Teams client.
- Use low-risk troubleshooting steps first.
- Avoid unnecessary changes to Windows security settings.
- Test the microphone after each relevant change.
- Confirm the outcome with the user.
- Document the findings and actions taken.

## 3. Troubleshooting Procedure

### Step 1 — Check Teams Microphone Settings

Open Microsoft Teams and navigate to its device settings.

Check:

- Whether the correct microphone is selected.
- Whether the microphone is muted.
- Whether the microphone input indicator responds when the user speaks.
- Whether the correct headset or audio device is connected.

**Purpose:** Confirm that Teams is using the intended audio input device.

### Step 2 — Check Windows Microphone Permissions

On Windows 11:

1. Open **Settings**.
2. Select **Privacy & security**.
3. Open **Microphone**.
4. Review microphone access and the relevant application permissions.
5. Confirm that access is allowed according to organizational policy.

**Purpose:** Windows privacy settings can prevent applications from accessing the microphone even when the correct device is selected.

Do not bypass organizational security policies or change managed settings without authorization.

### Step 3 — Test the Microphone in Windows

Open:

**Settings → System → Sound → Input**

Then:

1. Select the intended microphone.
2. Check that the input device is enabled.
3. Review the input volume.
4. Use the available input test to determine whether Windows detects the user's voice.

If the microphone does not work in Windows either, investigate the device connection, headset, driver, and relevant Windows sound settings.

If it works in Windows but not Teams, continue investigating Teams.

### Step 4 — Restart and Update Teams

In the simulated scenario, the microphone works in Windows but initially fails in the Teams desktop application.

Actions:

1. Save any work and leave meetings appropriately.
2. Restart Teams.
3. Check for available Teams updates through the supported update process.
4. Test the microphone again.
5. If necessary, compare the result with Teams on the web using a supported browser and the appropriate microphone permissions.

**Purpose:** Comparing the desktop application with the web version can help determine whether the problem is specific to the Teams client.

### Step 5 — Validate the Resolution

In the simulated scenario:

- Teams on the web successfully captures the user's microphone audio.
- The desktop application is restarted and updated.
- The microphone then works in Teams desktop.
- The user confirms successful audio during a test call.

These results describe the fictional exercise and are not evidence of a real incident or independently verified diagnosis.

## 4. Useful Troubleshooting Tools and Settings

| Tool or setting | Purpose |
|---|---|
| Teams device settings | Verify the selected microphone and mute status |
| Windows microphone privacy settings | Check application access permissions |
| Windows Sound settings | Test microphone input and input level |
| Teams web client | Compare behavior with the desktop client |
| Teams update process | Check for available application updates |
| IT service desk ticketing system | Record symptoms, steps, findings, and outcome |

## 5. Root Cause and Limitations

**Simulated finding:** The microphone worked in Windows and Teams on the web. Restarting and updating the Teams desktop application was followed by successful microphone operation.

**Root cause:** Not independently confirmed. The scenario suggests a possible desktop-client issue but does not prove exactly why the original failure occurred.

## 6. Ticket Closure Notes

**Simulated resolution:**

- Verified the selected microphone and mute status.
- Checked Windows microphone permissions.
- Tested microphone input in Windows sound settings.
- Restarted and updated the Teams desktop application.
- Compared behavior with Teams on the web.
- Confirmed successful audio in a test call.
- Documented the troubleshooting steps and outcome.

If the issue had continued, the next steps would include reviewing approved diagnostic information, checking device or driver issues, and escalating to the appropriate support team.

## 7. Security and Professional Practice

- Protect user privacy and meeting confidentiality.
- Do not disable firewalls or security software as a first-line fix.
- Follow organizational policies for managed devices.
- Make only authorized changes.
- Test the service after troubleshooting.
- Obtain user confirmation before closing the ticket.
- Separate confirmed evidence from assumptions in the ticket notes.

## 8. Skills Demonstrated

- Microsoft Teams troubleshooting
- Windows 11 sound settings
- Microphone permissions and device selection
- Application troubleshooting and comparison testing
- User communication
- Verification and ticket closure
- Evidence-based problem isolation

## 9. Learning Outcome

This exercise reinforced a systematic troubleshooting process: check the application settings, verify operating-system permissions, test the device independently, isolate application-specific problems, and confirm the result with the user.

**Portfolio disclaimer:** This project is a simulated learning exercise. It does not claim that a real support incident was investigated or resolved.

**Azure cost and resource safety:** No Azure resources were created, started, or modified for this project. Azure cost remains €0.
