# Project 2: Windows Server Event Log Troubleshooting

## Ticket EV-001 — File Share Unavailable (Simulated)

### 1. Project overview

**Project type:** Windows Server troubleshooting simulation  
**Category:** IT Support / Windows Server Administration  
**Tools studied:** Windows Event Viewer, Windows Services, PowerShell concepts  
**Environment:** MacBook — simulated Windows Server evidence only

**Cost control:** No Azure resources were created, started, or modified. No Azure resource charges were incurred.

### 2. Incident description

A user reported that a shared folder was no longer accessible, although it had worked earlier.

**Reported symptom:** Network file share unavailable.

**User impact:** The user could not access the expected shared folder.

**Initial status:** Investigating.

### 3. Simulated Event Viewer findings

The following evidence was provided for this exercise. It was not collected from a live server.

| Field | Simulated finding |
|---|---|
| Log | Windows Logs — System |
| Source | Service Control Manager |
| Event ID | 7034 |
| Level | Error |
| Event message | The Server service terminated unexpectedly |
| Service status | Stopped |
| Startup type | Automatic |
| Exit code | 0 |
| User impact | Shared folder unavailable |

A separate warning indicated that a dependent service had not responded within the expected time. The available evidence did not establish a direct relationship between that warning and the Server service failure.

### 4. Troubleshooting steps

1. **Identify the relevant event.** Selected the System log error because it concerned a service potentially related to file sharing.
2. **Review event details.** Examined the source, event ID, severity, and message.
3. **Establish the timeline.** Compared the service error with nearby events and the user's report.
4. **Check service status.** The simulated Server service was stopped despite having an Automatic startup type.
5. **Investigate related events.** Reviewed the available evidence but did not identify a definitive root cause.
6. **Plan recovery safely.** Considered service dependencies, operational impact, and authorization before attempting recovery.
7. **Validate the outcome.** In the simulated final test, the Server service was running and the shared folder was accessible.
8. **Document the incident.** Recorded the evidence, recovery result, user impact, and remaining uncertainty.

### 5. Root cause assessment

**Root cause: Not confirmed.**

The simulated evidence showed that the Server service had stopped unexpectedly and that the file share was unavailable. The successful recovery restored access, but the available evidence did not prove why the service stopped.

The earlier warning was treated as a lead for investigation, not as confirmed proof of the cause.

### 6. Resolution and validation

**Simulated final status: Resolved — service restored.**

- Server service: Running.
- Shared folder access: Successful.
- New errors during validation: None observed.
- User communication: Notify the user that access has been restored.
- Ticket closure: Appropriate after the successful checks and documentation.

The original cause remains unconfirmed, so further investigation may be needed if the problem recurs.

### 7. Lessons learned

- Event Viewer provides evidence to support troubleshooting, but an error alone does not prove the root cause.
- Event timestamps help establish the order of events.
- A service being configured for Automatic startup does not guarantee that it is currently running.
- Recovery must be followed by validation of the actual user-facing service.
- Avoid repeatedly restarting services without understanding the impact.
- Document confirmed facts separately from assumptions and hypotheses.

### 8. Security and cost controls

- Use authorized access and approved recovery procedures.
- Consider service dependencies and active user connections before restarting a service.
- Do not disable security controls as a shortcut.
- Do not include passwords, secrets, or sensitive server details in GitHub.
- No live server was accessed or changed during this exercise.
- No Azure resources were created, started, or modified; no Azure resource charges were incurred.

### 9. Project conclusion

This simulation practised a structured Windows Server support workflow: identify relevant events, review the timeline, examine service status, investigate related evidence, plan a safe recovery, validate the service, and document the outcome.

The exercise demonstrates basic incident handling and troubleshooting reasoning relevant to entry-level IT support and Windows Server support roles.
