# pfSense Homelab Network

### Objective
Carried out a DoS attack using Ettercap in a lab environment which caused pfSense to become unresponsive and significantly disrupt network traffic. After analysing the impact, I developed and tested a Python script to help detect potential DoS attacks.

### Tools Used


## Steps

1. I used the terminal to launch Ettercap with the GUI interface, which was ran with sudo privileges to allow root access.

2. I navigated to the “Manage Plugins” section and enabled the plugin labelled “DoS Attack.”

3. I configured the attack before beginning it by specifying a target IP address and then typing an unused IP address on the network to generate spoofed traffic.

4. The DoS attack was then executed and I monitored pfSense to observe its impact. I noticed a significant increase in CPU and RAM usage, which caused a noticeable performance degradation. This effect was more severe because the pfSense virtual machine was configured with limited resources, making it much more vulnerable to high network load during the attack.

5. After repeating the attack and restarting pfSense multiple times, the results varied as in some attempts, remote access to pfSense through PuTTY and the pfSense login page became completely inaccessible.

6. I then decided to create a Python script to help detect any potential DoS attacks more easily than using Wireshark which makes it more accessible for users who may not be familiar with any of the advanced network analysis tools.