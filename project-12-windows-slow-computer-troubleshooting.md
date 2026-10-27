# Project 12 — Windows Slow Computer Troubleshooting

## Project Overview

**Ticket ID:** PERF-001  
**Category:** Windows 11 performance troubleshooting  
**Environment:** Simulated IT support scenario  
**Status:** Resolved in the simulated scenario

This project demonstrates a structured approach to troubleshooting a slow Windows 11 computer. The focus is on identifying possible performance bottlenecks, protecting user data, making approved changes, validating results, and documenting the outcome.

**Important:** This is a simulated case study for learning and portfolio purposes. No real user's computer was investigated, and no actual diagnosis was performed.

## 1. Simulated Support Ticket

**User report:**

"My Windows 11 computer has become very slow. Applications take a long time to respond, especially when I have my browser open."

**Initial observations in the scenario:**

- CPU usage: 18%
- Memory usage: 92%
- Disk usage: 12%
- An unfamiliar application was starting automatically with Windows.
- The user had multiple browser tabs open, including unsaved work.

These are fictional observations created for this practice scenario.

## 2. Troubleshooting Objectives

- Identify which system resources may be contributing to poor performance.
- Avoid losing the user's unsaved work.
- Identify applications consuming excessive resources.
- Review startup applications safely.
- Verify whether performance improves.
- Document the actions taken and the simulated outcome.

## 3. Troubleshooting Procedure

### Step 1 — Gather Information

Ask the user:

- When did the slowdown begin?
- Does it happen immediately after startup or only when certain applications are open?
- Is the issue affecting one application or the entire computer?
- Have any new applications or updates been installed recently?

**Purpose:** Establish the symptoms and scope before making changes.

### Step 2 — Check Task Manager

Open Task Manager using `Ctrl + Shift + Esc`.

Review the Processes and Performance tabs.

Check:

- CPU usage
- Memory usage
- Disk activity
- Applications consuming significant resources

In this simulated case, memory usage was 92%, while CPU usage was 18% and disk usage was 12%.

**Interpretation:** High memory usage may contribute to poor performance, but it does not by itself confirm the root cause. Identify the applications consuming memory and gather further evidence.

### Step 3 — Review Browser Usage

The simulated investigation identified a browser with many open tabs and high memory consumption.

Actions:

1. Ask the user to save any unsaved work.
2. Review open tabs with the user's agreement.
3. Close unnecessary tabs.
4. Recheck memory usage and computer responsiveness.

**Reason:** This reduces unnecessary resource consumption while protecting the user's work.

### Step 4 — Review Startup Applications

The simulated investigation also identified an unfamiliar application that started automatically and used significant memory.

Actions:

1. Identify the application and verify its purpose.
2. Determine whether it is required for business or security operations.
3. Check the organization's IT policy and obtain appropriate approval.
4. Disable its startup entry only if it is confirmed to be non-essential and the change is permitted.
5. Restart or otherwise validate performance as appropriate.

**Important:** Do not disable security software, delete application files manually, or disable all startup applications without investigation and authorization.

### Step 5 — Validate the Outcome

In the simulated scenario:

- Unnecessary browser tabs were closed after the user saved their work.
- An approved, non-essential startup entry was disabled.
- The computer was reported to respond normally afterward.

The result represents the fictional outcome of this exercise, not a real-world test or independently verified diagnosis.

## 4. Useful Windows Troubleshooting Tools

| Tool | Purpose |
|---|---|
| Task Manager | Identify high CPU, memory, disk, and application usage |
| Resource Monitor | Investigate resource usage in greater detail |
| Startup apps in Task Manager | Review applications that launch automatically |
| Event Viewer | Investigate relevant system or application errors |
| Windows Settings | Review installed applications and available storage |

Use only authorized tools and approved procedures on company devices.

## 5. Root Cause and Limitations

**Simulated findings:** High memory usage, numerous browser tabs, and a non-essential startup application were identified as possible contributors.

**Root cause:** Not independently confirmed. The exercise demonstrates troubleshooting and validation rather than proving that one specific factor caused the slowdown.

## 6. Ticket Closure Notes

**Simulated resolution:**

- Reviewed system resource usage.
- Identified high memory consumption.
- Asked the user to save work before closing unnecessary browser tabs.
- Reviewed and safely disabled an approved, non-essential startup entry.
- Confirmed that the user reported normal responsiveness.
- Documented the troubleshooting steps and outcome.

If performance had remained poor, the next steps would include collecting further evidence, checking available storage and system errors, and escalating to the appropriate IT team when necessary.

## 7. Security and Professional Practice

- Protect user data and unsaved work.
- Do not disable security controls to improve performance.
- Follow change-management and authorization requirements.
- Avoid unnecessary reinstalls or destructive troubleshooting.
- Document evidence separately from assumptions.
- Verify the outcome with the user before closing the ticket.

## 8. Skills Demonstrated

- Windows 11 troubleshooting
- Task Manager and resource monitoring
- Basic performance analysis
- Startup application management
- User communication and data protection
- Validation and ticket documentation
- Evidence-based troubleshooting

## 9. Learning Outcome

This exercise reinforced a structured approach to Windows performance issues: gather information, investigate resource usage, make safe and approved changes, validate the result, and document the outcome.

**Portfolio disclaimer:** This project is a simulated learning exercise. It does not claim that a real incident was investigated or resolved.

**Azure cost and resource safety:** No Azure resources were created, started, or modified for this project. Azure cost remains €0.
