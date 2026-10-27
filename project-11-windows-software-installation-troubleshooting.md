# Project 11 — Windows Software Installation Troubleshooting

**Ticket ID:** SW-001  
**Category:** Windows support / Software installation  
**Environment:** Windows 11  
**Difficulty:** Beginner  
**Status:** Simulated troubleshooting exercise

## 1. Incident Summary

An employee using Windows 11 could not install an approved company application. The installation stopped and displayed an error message.

The simulated investigation considered application-control policies, available disk space, user permissions, and the organization's software deployment process.

**Important:** This is a simulated support case for learning and portfolio demonstration. It is not a record of a real incident.

## 2. Symptoms and Findings

- The employee reported that an application installation failed.
- The initial error stated: "This app has been blocked by your system administrator."
- The application was confirmed as approved in the simulated scenario.
- Policy checks showed no block in the exercise.
- The computer had insufficient free disk space.
- After considering disk space, the installation reported insufficient permissions.
- The simulated IT team used the approved deployment process, and the application installed successfully.

These findings belong to the fictional exercise and do not represent results from a real computer.

## 3. Troubleshooting Procedure

### Step 1 — Gather information

Ask the employee:
- What is the application's name?
- What exact error message appears?
- When does the installation fail?
- Did the installation work previously?
- Is the application approved by the organization?

Record the error message and relevant details before making changes.

### Step 2 — Check application approval and policy

If Windows reports that an administrator blocked the application:
- Confirm that the application is approved.
- Check relevant application-control or software-installation policies using authorized tools.
- Review available logs for a relevant block event.
- Contact the responsible IT team if the restriction is unclear.

Never bypass an organizational restriction or disable security controls to force an installation.

### Step 3 — Check available disk space

Compare the computer's free disk space with the application's requirements.

If space is insufficient:
- Use approved Windows storage-cleanup tools.
- Review temporary files and other safe cleanup options.
- Confirm with the user before removing personal or business data.
- Recheck available space before retrying the installation.

Never delete random files from Windows system folders.

### Step 4 — Investigate permissions

If the error indicates insufficient permissions:
- Check the user's account and applicable permissions.
- Follow the organization's software-installation procedure.
- Use authorized administrator elevation where permitted.
- Request IT deployment if the application must be installed by an administrator.

Do not grant permanent local administrator rights solely to install one application.

### Step 5 — Validate the installation

After the approved installation:
1. Confirm that the installation completed successfully.
2. Ask the employee to launch the application.
3. Check that it opens and performs the required basic function.
4. Ask the employee to confirm that it works for their task.
5. Document the result and close the ticket only when the issue is resolved.

If installation or launch still fails, record the new error and escalate with the evidence gathered.

## 4. Root Cause

**Not independently confirmed.**

The scenario includes low disk space and an insufficient-permissions message, followed by successful installation through the approved deployment process. It does not establish whether one issue or a combination of issues caused the original failure.

A real support ticket should distinguish observed symptoms from a verified root cause.

## 5. Resolution

In the simulated scenario, IT completed the installation using the approved deployment process.

A real ticket should only be marked resolved after the application has been launched and tested, the employee has confirmed that it works, and the outcome has been documented.

## 6. Security and Good Practice

- Install only approved software.
- Follow organizational application-control policies.
- Avoid disabling antivirus or endpoint protection.
- Use the principle of least privilege.
- Do not grant unnecessary permanent administrator rights.
- Protect user data during disk cleanup.
- Record evidence and escalate when required.

## 7. Skills Demonstrated

- Windows 11 software troubleshooting
- Error-message investigation
- Application approval and policy checks
- Disk-space troubleshooting
- Permissions and authorized elevation
- Software deployment awareness
- User communication and validation
- Ticket documentation and escalation

## 8. Learning Quiz Result

**Score: 5/5**

The exercise covered error investigation, application-control policies, disk-space checks, permissions, approved installation methods, and final validation.

## 9. Scope and Cost

This project is documentation and simulated learning only. No Azure resources were created, started, or modified. No cloud services were required, and Azure cost for this exercise was **€0**.
