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

1. Before starting I opened the virtual network editor to create a host-only network using VMnet1 and disabled the local DHCP service so VMware would not automatically assign IP addresses to virtual machines.
<img width="692" height="652" alt="image" src="https://github.com/user-attachments/assets/8ab3f68d-1f16-4416-92f7-c4431d367378" />

2. Once I set up pfSense using the default VMware setup process, I configured pfSense by setting Network Adapter 1 to Bridged mode and Network Adapter 2 to the host-only network created on VMnet1.
<img width="885" height="465" alt="image" src="https://github.com/user-attachments/assets/8785a6d3-3720-4c59-a3cb-bdaa3ba5ed32" />
<img width="882" height="467" alt="image" src="https://github.com/user-attachments/assets/d0b6642c-1396-437f-89c3-8c6b05a261eb" />

3. The pfsense was opened and press enter on this screen
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/26a703e8-6f5f-4ca0-be71-45d206e162cc" />

4. On the select WAN interface i selected em0 as the WAN
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/a1fda63b-1244-4144-b397-06ca4b8fffdb" />

5. all settigns here are left as default
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/74a07f44-f4e0-48d5-bd2a-2faefe19ecb6" />

6. On the LAN select interface I selected em1 was the LAN
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/8603df3d-949b-4834-89dd-0ba3b48128d6" />

7. All network settings left as default and enter was clicked to contineu with the installation
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/953373cc-9c44-4756-be0d-645101c28377" />

8. Lan was selected as this
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/336847e9-6d60-442d-b808-f30e7bbacae6" />

9. The subcription screen showed and was skipepd by enter and on this screen the file system type was left as defaults
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/fe850d53-45c7-41cb-b52f-4dfca2378d24" />

10. After that 4 options showed up and were all pressed enter on which was just showing that the disk needed to be erased and which version to isntall in which  the current stable version currently being isntalled in this picture.
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/2f2cc870-5f44-464d-ad0f-c3979a5cd338" />




