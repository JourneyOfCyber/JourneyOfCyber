# DoS attacks using Ettercap and a Python script for detecting such attacks.

### Objective
Carried out a DoS attack using Ettercap in a lab environment which caused pfSense to become unresponsive and significantly disrupt network traffic. After analysing the impact, I developed and tested a Python script to help detect potential DoS attacks.

### Tools Used
- Ettercap

## Steps

1. I used the terminal to launch Ettercap with the GUI interface, which was ran with sudo privileges to allow root access.

2. I navigated to the “Manage Plugins” section and enabled the plugin labelled “DoS Attack.”

3. I configured the attack before beginning it by specifying a target IP address and then typing an unused IP address on the network to generate spoofed traffic.

4. The DoS attack was then executed and I monitored pfSense to observe its impact. I noticed a significant increase in CPU and RAM usage, which caused a noticeable performance degradation. This effect was more severe because the pfSense virtual machine was configured with limited resources, making it much more vulnerable to high network load during the attack.

5. As shown in Wireshark, the fake IP address of ___ is a spoofed IP being sent to the pfSense router, which causes the attack. This can also be observed directly on the pfSense interface.

6. After repeating the attack and restarting pfSense multiple times, the results varied as in some attempts, remote access to pfSense through PuTTY and the pfSense login page became completely inaccessible.

7. Afterward, I decided to create a Python script to help detect any potential DoS attacks more easily than using Wireshark which makes it more accessible for users who may not be familiar with any of the advanced network analysis tools.

8. As you can see, the script is detecting any network traffic being sent by the attacker which identifies the malicious IP that was responsible for the attacks.
