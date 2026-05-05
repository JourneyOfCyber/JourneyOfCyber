# Network DoS Attack, Detection with Python and pfSense Mitigation

### Objective
Carried out a DoS attack using Ettercap in a lab environment which caused pfSense to become unresponsive and significantly disrupt network traffic. After analysing the impact, I developed and tested a Python script to help detect potential DoS attacks.

### Tools Used
- Ettercap

## Steps

1. I used the terminal to launch Ettercap with the GUI interface, which was ran with sudo privileges to allow root access.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cd64841e-1b36-4c64-9bbf-5c84e21467eb" />

2. I navigated to the “Manage Plugins” section and clicked  the plugin labelled “DoS Attack.”
<img width="866" height="502" alt="image" src="https://github.com/user-attachments/assets/eb3b8d7f-d582-4134-bb69-a7fb5a5e6f31" />


3. To use it I had to configure the attack before beginning it by specifying a target IP address and then typing an unused IP address on the network to generate spoofed traffic.
<img width="829" height="496" alt="image" src="https://github.com/user-attachments/assets/926fed80-8606-44e5-8d46-919115c9330f" />
<img width="833" height="492" alt="image" src="https://github.com/user-attachments/assets/466ace2b-7b90-47bd-99d3-8574c9791e50" />

4. The DoS attack was then executed and I monitored pfSense to observe its impact. I noticed a significant increase in CPU and RAM usage, which caused a noticeable performance degradation. This effect was more severe because the pfSense virtual machine was configured with limited resources, making it much more vulnerable to high network load during the attack.

Before:
<img width="629" height="370" alt="Screenshot 2026-05-03 154448" src="https://github.com/user-attachments/assets/55a8bacf-36f7-489b-b089-c862f87aac8d" />
After:
<img width="622" height="411" alt="Screenshot 2026-05-03 154915" src="https://github.com/user-attachments/assets/b1572b21-b732-461e-a571-d328475de4c6" />

6. As shown in Wireshark, the fake IP address of 192.168.1.200 is a spoofed IP being sent to the pfSense router, which causes the attack. This can also be observed directly on the pfSense interface.

7. After repeating the attack and restarting pfSense multiple times, the results varied as in some attempts, remote access to pfSense through PuTTY and the pfSense login page became completely inaccessible.
<img width="948" height="566" alt="Screenshot 2026-05-03 151224" src="https://github.com/user-attachments/assets/2b817448-c25e-4f1a-b333-f0f3e721a985" />
<img width="1554" height="873" alt="Screenshot 2026-05-03 155028" src="https://github.com/user-attachments/assets/f234a94a-7786-41a5-97a4-de8668690167" />

8. Afterward, I decided to create a Python script to help detect any potential DoS attacks more easily than using Wireshark which makes it more accessible for users who may not be familiar with any of the advanced network analysis tools.

9. As you can see, the script is detecting any network traffic being sent by the attacker which identifies the malicious IP that was responsible for the attacks.
