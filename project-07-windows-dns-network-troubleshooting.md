# Project 7: Windows DNS and Network Troubleshooting

## Project Overview
- Ticket ID: NET-001
- Category: Windows Network Troubleshooting
- Environment: Simulated Windows 11 support scenario
- Status: Completed - simulated exercise

## 1. Problem Description

A user reports that their Windows 11 laptop is connected to Wi-Fi, but the company website does not open. The browser reports that it cannot find the website's IP address. Other websites are accessible.

## 2. Initial Investigation

- Confirm Wi-Fi connectivity.
- Check whether other websites work.
- Ask whether other users experience the same issue.
- Record the website address and exact error message.

## 3. Troubleshooting Commands

### Check DNS Resolution

Command:
nslookup company.example

Purpose: Checks whether DNS can translate a hostname into an IP address.

Simulated result: The DNS request times out.

Note: company.example is a placeholder hostname, not a real company website.

### Inspect Network Configuration

Command:
ipconfig /all

Purpose: Displays the IP address, default gateway, DNS server addresses, and other network settings.

Simulated finding: The laptop has a valid IP address and default gateway, but its DNS server configuration is unexpected.

## 3.1 Additional DNS troubleshooting commands

The following commands demonstrate additional checks an authorized support technician can perform on a Windows device. They were not executed during this simulation.

Display the current DNS cache:

ipconfig /displaydns

Clear the local DNS cache:

ipconfig /flushdns

Test DNS resolution using a specific DNS server:

nslookup company.example 192.0.2.53

Note: 192.0.2.53 is a documentation-only example address, not a real DNS server.

Check the network route:

tracert company.example

Important: Clearing the DNS cache does not correct an incorrect DNS server configuration. Do not change DNS server addresses without authorization and the correct company network settings.

## 4. Root Cause

In this simulated case, the network team confirms that the laptop is using an incorrect DNS server configuration.

No real device or company network was investigated.

**Evidence limitation:** The incorrect DNS server configuration is a simulated finding. In a real investigation, verify the configured DNS server addresses and compare them with the organization's approved network settings before identifying the root cause.

## 5. Resolution

The authorized support team corrects the DNS configuration using the approved company network settings.

The DNS lookup is repeated to verify that the hostname resolves successfully.

**Validation limitation:** The successful DNS resolution and website access are simulated outcomes. No live DNS configuration was changed, no real DNS server was queried, and no company website was tested.

## 6. Validation

- Confirm that the DNS lookup returns an IP address.
- Test whether the company website opens.
- Document the results.
- Update the support ticket before closure.

## 7. Key Learnings

- Wi-Fi connectivity does not guarantee that DNS is working.
- nslookup helps investigate hostname resolution problems.
- ipconfig /all helps identify DNS configuration issues.
- DNS settings should only be changed according to approved company procedures.
- Always test the service after applying a fix.
- Document troubleshooting steps and confirmed results.

## 8. Tools and Skills Practiced

- Windows 11 networking fundamentals
- DNS troubleshooting
- Windows Command Prompt
- IP configuration analysis
- IT service desk documentation
- Troubleshooting and validation

## Disclaimer

This is a simulated IT support exercise created for learning and portfolio purposes. No real company network, device, or DNS server was accessed or changed. No Azure resources were created, started, or modified. Azure cost remains €0.
