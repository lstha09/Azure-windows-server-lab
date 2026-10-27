# Project 8: Windows DHCP and IP Address Troubleshooting

## Project Overview
- Ticket ID: DHCP-001
- Category: Windows Network Troubleshooting
- Environment: Simulated Windows 11 support scenario
- Status: Completed - simulated exercise

## 1. Problem Description

A user reports that their Windows 11 laptop is connected to office Wi-Fi but cannot access the internet or internal company services.

The laptop has an IP address beginning with 169.254, which may indicate that Windows could not obtain a valid IP address from a DHCP server.

## 2. Initial Investigation

The first troubleshooting steps are:
- Confirm that Wi-Fi is connected.
- Check whether other devices can access the network.
- Inspect the laptop's IP configuration.
- Determine whether the problem affects one device or multiple devices.

## 3. Troubleshooting Commands

### Command 1: Inspect IP Configuration

Command:
ipconfig /all

Purpose:
Displays the computer's IP address, subnet mask, default gateway, DHCP status, and DNS server information.

Simulated findings:
- DHCP Enabled: Yes
- IPv4 Address: 169.254.18.42
- Default Gateway: Not shown
- DHCP Server: No server address shown

These fictional findings suggest that the laptop did not obtain a normal IP configuration from DHCP.

### Command 2: Release the Current IPv4 Configuration

Command:
ipconfig /release

Purpose:
Releases the current DHCP-assigned IPv4 configuration.

### Command 3: Request a New IP Configuration

Command:
ipconfig /renew

Purpose:
Requests a new IP configuration from the DHCP server.

Note: These commands are documented for learning purposes. They were not run against a real company device.

## 4. Investigation

In this simulated scenario, other devices successfully obtain valid IP addresses from the office network.

This suggests that the problem may be isolated to the laptop, although further investigation would be needed to confirm the cause.

## 5. Simulated Resolution

An authorized support technician investigates the laptop's DHCP connectivity and performs the appropriate corrective steps.

The laptop subsequently receives a valid company IP address, a default gateway, and DHCP server information.

The exact underlying cause is not confirmed in this exercise.

## 6. Validation

After the simulated correction:
- Confirm that the laptop has a valid IP configuration.
- Verify that a default gateway is present.
- Test internet and internal company connectivity as appropriate.
- Ask the user to confirm that the service works.
- Document the findings and update the support ticket.

## 7. Key Learnings

- An IP address beginning with 169.254 is commonly an APIPA address.
- APIPA may occur when Windows cannot obtain an IP address through DHCP.
- The command ipconfig /all helps identify network configuration problems.
- The commands ipconfig /release and ipconfig /renew can help request a fresh DHCP configuration.
- Comparing the affected device with other devices helps narrow down the problem.
- Always validate the result and document the troubleshooting steps.

## 8. Tools and Skills Practiced

- Windows 11 networking fundamentals
- DHCP and IP address troubleshooting
- Command Prompt
- IP configuration analysis
- Basic network connectivity checks
- IT service desk ticket documentation

## Disclaimer

This project is a simulated IT support exercise created for learning and portfolio purposes. No real company device or network was investigated or modified. No Azure resources were created, started, or modified. Azure cost remains €0.
