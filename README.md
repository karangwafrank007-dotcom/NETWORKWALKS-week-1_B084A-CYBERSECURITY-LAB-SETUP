# Cybersecurity Lab Environment Setup

## Project Overview
This project focuses on setting up a virtual cybersecurity and penetration-testing laboratory using VirtualBox and Kali Linux. The lab is configured on an isolated private virtual network so that additional machines can be securely added later as targets for analysis and testing.

## Completed Tasks & Configurations

### 1. VirtualBox Infrastructure
- **Network Subnet:** Configured a custom global NATNetwork on the `10.0.0.0/24` subnet.
- **Guest Configuration:** Attached the Kali Linux virtual machine profile directly to the new `NatNetwork` switch.
- **System Settings:** Shared Clipboard and Drag-and-Drop parameters set to **Bidirectional**.
- **Shared Storage:** Connected the host folder mapping to `/downloads` with **Auto-mount** enabled.

### 2. Kali Linux Operating System
- **Adapter Optimization:** Flushed dynamic DHCP clutter from the active network card.
- **Network Mapping:** Forcefully assigned a permanent Static IP address of `10.0.0.2/24` to the `eth0` device interface.
- **Routing Configuration:** Manually mapped a default gateway path pointing directly to the VirtualBox routing junction at `10.0.0.1`.
- **Connectivity Testing:** Successfully executed ICMP pings out to Google public DNS (`8.8.8.8`), confirming fully optimized external internet traversal.
### Visual Verification

**VirtualBox NAT Network Configuration (`10.0.0.0/24`):**
![VirtualBox NAT Network Setup](Screenshot%202026-10-27%20163825.png)

**Kali Linux Static IP Configuration (`10.0.0.2`) & Connectivity Test:**
![Kali Linux Static IP and Ping Test](Screenshot%202026-10-27%20162357.png)
---

## Project 2: Security Operations Center (SOC) Packet Analysis

### Project Overview
In this module, I acted as a junior SOC Analyst investigating suspicious activities, protocol vulnerabilities, and threat signatures across a series of live traffic captures using Wireshark.

### Analytical Skills & Techniques Applied
- **Packet Quantification:** Measured precise ingestion metrics across captured endpoints.
- **Display Filtering:** Leveraged targeted network protocol display filters (`http`, `dns`, `tcp`, `icmp`) to separate malicious anomalies from baseline network chatter.
- **Stream Rehearsal:** Utilized the 'Follow TCP Stream' feature to rebuild full textual conversations, exposing attackers' commands and protocol traversal.
- **Credential Auditing:** Investigated unencrypted HTTP traffic streams to extract exposed clear-text authentication tokens (usernames and passwords).
- **Attack Profiling:** Successfully identified malicious traffic signatures, isolated a Brute Force threat actor IP address, and audited an unencrypted malicious VoIP/SIP call stream.


