# Project 16 — Microsoft 365 MFA Troubleshooting

## Project Overview

- **Ticket ID:** MFA-001
- **Category:** Microsoft 365 / Identity and Access / Multi-Factor Authentication (MFA)
- **Environment:** Simulated Microsoft 365 support environment
- **Priority:** High — the user cannot sign in, and unexpected MFA requests may indicate a security risk
- **Status:** Simulated troubleshooting exercise completed for learning purposes

> **Important:** This is a simulated support case. No real account was accessed or changed. No Azure resources were created, started, or modified. Azure cost: €0.

## 1. User-Reported Problem

A user cannot sign in to Microsoft 365. Their password appears to be accepted, but they are not receiving Microsoft Authenticator approval notifications on their phone.

During the investigation, the user also reports receiving several unexpected MFA approval requests that they did not initiate.

The technician must investigate the authentication problem while protecting the user's account.

## 2. Initial Assessment

Gather the following information:

- Can the user reach the Microsoft 365 sign-in page?
- Does the password appear to be accepted?
- Which MFA method is registered?
- Is Microsoft Authenticator installed and accessible?
- Does the phone have internet connectivity?
- Are notifications enabled for the authenticator app?
- Does the user recognize the recent MFA requests?
- Are other users experiencing similar sign-in problems?

Verify the user's identity according to organizational policy before making account changes.

**Security consideration:** Unexpected MFA requests must be treated as a potential security incident, not merely as a notification problem.

## 3. Troubleshooting Procedure

### Step 1 — Verify Identity and Check the Authentication Setup

Confirm the user's identity through the approved verification process.

Check whether the user is signing in with the expected work or school account. Ask whether Microsoft Authenticator is installed and whether the user can open the app.

Check the phone's internet connection and notification settings.

**Simulated finding:** The authenticator app is installed and the phone has internet access, but approval notifications are not arriving.

**Action:** Continue investigating the registered authentication method and available verification options.

### Step 2 — Review Notification Settings and Authentication Methods

Check the notification settings and registered authentication methods using approved procedures.

If the user cannot complete the usual verification method, determine whether an alternative method is available under organizational policy.

Do not bypass MFA simply to restore access.

**Simulated finding:** The ordinary approval notification still does not work.

**Action:** Continue troubleshooting using approved authentication and recovery procedures.

### Step 3 — Identify a Potential Security Incident

The user reports several MFA requests they did not initiate.

This may indicate that someone is attempting to access the account using compromised credentials or another unauthorized sign-in attempt. The requests alone do not prove that the account has been compromised.

The technician should:

1. Tell the user not to approve unexpected requests.
2. Ask the user to deny requests they did not initiate.
3. Follow the organization's incident-reporting and escalation procedures.
4. Preserve relevant evidence using authorized tools.
5. Avoid collecting passwords or MFA codes.
6. Follow the security team's instructions for protecting the account.

**Simulated finding:** The unexpected requests are escalated for security review.

**Action:** Follow the approved account-recovery process only after the required authorization and identity verification.

### Step 4 — Restore Secure Authentication

After the simulated security team authorizes recovery, review the user's registered authentication methods.

If required, re-register the authentication method using the organization's approved process. Use an approved alternative verification method when available and permitted.

Do not permanently disable MFA or weaken security policies as a workaround.

**Simulated finding:** The user can sign in through an approved alternative authentication method.

**Action:** Restore the intended MFA method and test the sign-in process with the user.

### Step 5 — Verify Sign-In and MFA

Ask the user to complete a sign-in using the restored authentication method.

Verify that:

- The user can sign in to Microsoft 365.
- The expected MFA prompt or verification method works.
- The user recognizes the authentication method being used.
- No unexpected requests are being approved.
- Any remaining security investigation has been handed over appropriately.

**Simulated finding:** The user successfully signs in using the restored MFA method, and the security team has completed its initial review.

**Action:** Document the results and any remaining security follow-up.

## 4. Example Troubleshooting Decision Table

| Observation | Possible explanation | Recommended action |
|---|---|---|
| Authenticator notifications do not arrive | Notification, connectivity, or app issue | Check connectivity, app access and notification settings |
| Registered authentication method appears incorrect | Outdated or unsuitable registration | Review it through approved identity tools |
| User cannot use the usual MFA method | Authentication method unavailable | Use an approved alternative if available |
| Unexpected MFA requests appear | Possible unauthorized sign-in attempts | Tell the user to deny them and follow incident procedures |
| User signs in after recovery | Access has been restored | Verify MFA and document the result |
| The issue persists after recovery | Unresolved authentication or security issue | Escalate with evidence to the appropriate support team |

## 5. Example Support Ticket Notes

**Ticket ID:** MFA-001

**Reported issue:** The user cannot complete Microsoft 365 MFA because approval notifications are not arriving.

**Additional concern:** The user reports unexpected MFA requests they did not initiate.

**Checks performed in the simulated scenario:**
- Verified user identity through the approved process.
- Checked authenticator availability and phone connectivity.
- Reviewed notification settings and registered authentication methods.
- Identified the unexpected requests as a potential security incident.
- Escalated the concern and followed an authorized recovery workflow.
- Verified successful sign-in using the restored authentication method.

**Actions:** Investigate the authentication method, protect the account, escalate suspicious activity, and restore access using approved procedures.

**Outcome:** Successful sign-in is reported in the simulated scenario. The security team's initial review is complete, but no claim is made that a real account was investigated or that a real security incident was resolved.

**Root cause:** Not independently confirmed.

**Follow-up:** Complete any remaining security investigation or monitoring required by organizational policy.

## 6. Security and Privacy Best Practices

- Never ask users to disclose passwords or MFA codes.
- Never approve an MFA request on behalf of a user.
- Never advise users to approve requests they did not initiate.
- Verify identity before changing authentication settings.
- Use approved alternative authentication and recovery procedures.
- Do not disable MFA permanently to resolve a routine support issue.
- Record only necessary information in support tickets.
- Escalate suspected account compromise promptly.

## 7. Skills Demonstrated

- Microsoft 365 identity and access support
- Multi-factor authentication troubleshooting
- Authentication method verification
- Basic mobile application troubleshooting
- Security incident recognition
- Identity verification and account recovery
- User communication and security awareness
- Ticket documentation and escalation

## 8. Learning Reflection

This exercise demonstrates that MFA troubleshooting involves both technical diagnosis and security judgment.

A missing notification may be caused by a device, application, notification, or registration problem. Unexpected MFA requests introduce a separate security concern that must be investigated rather than ignored.

A good Service Desk technician protects the account, follows approved recovery procedures, verifies successful sign-in, and documents the work without collecting sensitive authentication information.

**Portfolio note:** This project is a simulated learning exercise, not evidence of a production incident or a real Microsoft 365 tenant change.
