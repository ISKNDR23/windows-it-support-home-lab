# Lab 03 - Network Configuration and Troubleshooting

## Overview
This lab demonstrates basic Windows network configuration checks and connectivity troubleshooting using Command Prompt tools.

The goal was to verify local network settings, confirm internet connectivity, test DNS name resolution, and perform a basic DNS troubleshooting action.

## Objective
Validate network connectivity and DNS functionality using common IT support commands.

## Tools Used
- Windows Command Prompt
- ipconfig
- ping
- nslookup

## Tasks Performed
1. Reviewed network configuration using `ipconfig /all`.
2. Identified key network settings such as IPv4 address, subnet mask, default gateway, and DNS servers.
3. Tested internet connectivity by pinging `8.8.8.8`.
4. Confirmed domain name resolution by pinging `google.com`.
5. Used `nslookup google.com` to verify DNS resolution.
6. Flushed the DNS resolver cache using `ipconfig /flushdns`.

## Screenshots

### 1. Network configuration
![Network configuration](screenshots/01-ipconfig-all.png)

### 2. IP connectivity test
![Ping IP](screenshots/02-ping-ip-success.png)

### 3. Domain connectivity test
![Ping domain](screenshots/03-ping-domain-success.png)

### 4. DNS lookup
![NSLookup](screenshots/04-nslookup-google.png)

### 5. DNS cache flush
![Flush DNS](screenshots/05-flushdns-success.png)

## Result
The device successfully connected to an external IP address and resolved a domain name using DNS. DNS lookup completed successfully, and the DNS resolver cache was flushed as part of the troubleshooting process.

## Skills Demonstrated
- Network troubleshooting
- TCP/IP fundamentals
- DNS troubleshooting
- Command-line diagnostics
- Connectivity testing
- Windows IT support