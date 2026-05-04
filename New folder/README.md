# pfSense Homelab Network Simulation

### Objective
Built and configured a virtualised network using VMware to install and set up a functional pfSense firewall.

### Skills Learned
[Bullet Points - Remove this afterwards]

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used
[Bullet Points - Remove this afterwards]

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Steps

1. Before starting, I created a host-only network using VMnet1 and disabled the local DHCP service so VMware would not automatically assign IP addresses to virtual machines.
<img width="692" height="652" alt="image" src="https://github.com/user-attachments/assets/8ab3f68d-1f16-4416-92f7-c4431d367378" />

2. I configured pfSense by setting Network Adapter 1 to Bridged mode and Network Adapter 2 to the host-only network created on VMnet1.
<img width="885" height="465" alt="image" src="https://github.com/user-attachments/assets/8785a6d3-3720-4c59-a3cb-bdaa3ba5ed32" />
<img width="882" height="467" alt="image" src="https://github.com/user-attachments/assets/d0b6642c-1396-437f-89c3-8c6b05a261eb" />


