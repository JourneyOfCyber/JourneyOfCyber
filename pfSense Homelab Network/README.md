# pfSense Homelab Network

### Objective
Built and configured a virtualised network using VMware to install and set up a functional pfSense firewall.

### Tools Used

- VMware
- Pfsense installer https://www.pfsense.org/download/

## Steps

1. Before starting I opened the virtual network editor to create a host-only network using VMnet1 and disabled the local DHCP service so VMware would not automatically assign IP addresses to virtual machines.
<img width="692" height="652" alt="image" src="https://github.com/user-attachments/assets/8ab3f68d-1f16-4416-92f7-c4431d367378" />

2. Once I set up pfSense using the default VMware setup process, I configured pfSense by setting Network Adapter 1 to Bridged mode and Network Adapter to the host-only network created on VMnet1. The host-only network is an internal network that the virtual machines will use once pfSense is installed which allows them to communicate through pfSense.
<img width="885" height="465" alt="image" src="https://github.com/user-attachments/assets/8785a6d3-3720-4c59-a3cb-bdaa3ba5ed32" />
<img width="882" height="467" alt="image" src="https://github.com/user-attachments/assets/d0b6642c-1396-437f-89c3-8c6b05a261eb" />

3. pfSense was launched, and I pressed Enter on the initial boot screen to continue.
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/26a703e8-6f5f-4ca0-be71-45d206e162cc" />

4. On the select WAN interface I selected em0 as the WAN
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/a1fda63b-1244-4144-b397-06ca4b8fffdb" />

5. All settings on this screen were left at their default values.
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/74a07f44-f4e0-48d5-bd2a-2faefe19ecb6" />

6. On the LAN select interface I selected em1 was the LAN
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/8603df3d-949b-4834-89dd-0ba3b48128d6" />

7. All network settings were left at their default values, and Enter was pressed to continue with the installation.
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/953373cc-9c44-4756-be0d-645101c28377" />

8. The LAN interface was selected accordingly.
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/336847e9-6d60-442d-b808-f30e7bbacae6" />

9. The subcription screen showed and was skipepd by enter and on this screen the file system type was left as defaults.
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/fe850d53-45c7-41cb-b52f-4dfca2378d24" />

10. After that, four options were displayed and each was confirmed by pressing Enter, including erasing the disk and selecting the current stable version of pfSense to install. The system then began the installation process which is seen bellow.
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/2f2cc870-5f44-464d-ad0f-c3979a5cd338" />

11. After the installation completed, a prompt appeared asking to restart the virtual machine, and Enter was pressed to reboot the system.
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/248eba12-56a9-40e9-b5bf-3dd93cccc286" />

12. Once the system rebooted, the pfSense console screen was displayed showing that the boot process had completed successfully and all services had started
<img width="720" height="400" alt="image" src="https://github.com/user-attachments/assets/9f0616bc-83a4-4f52-85b1-603fb9d02fff" />


