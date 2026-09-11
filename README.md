# NETWORKWALKS-B083-WK1-PM1-CYBERSECURITY-LAB-SETUP
**1.	Executive Summary**

This practical cybersecurity laboratory was established to provide a controlled environment for learning and demonstrating penetration testing, ethical hacking, vulnerability assessment, and cybersecurity techniques. The lab was implemented using Oracle VirtualBox, with Kali Linux configured as the primary penetration-testing machine and Windows 10, Window Server 2019, window 7 and Android configured as the target system.
The virtual machines are connected through a dedicated VirtualBox NAT Network using the 10.0.0.0/24 private network. The Kali Linux system is configured with the IP address 10.0.0.2, while 10.0.0.1 is configured as the network gateway and DNS server. This configuration provides controlled network communication between the laboratory systems while maintaining separation from the organization's production environment.
The laboratory supports a structured penetration-testing methodology consisting of reconnaissance, network discovery, scanning, enumeration, vulnerability assessment, controlled exploitation, analysis, remediation, and security reporting. VirtualBox snapshots can also be used to preserve clean system states and restore the laboratory after testing.

**2.	Objectives**


The primary objective of the laboratory is to develop practical knowledge and experience in cybersecurity testing through a controlled virtual environment.
The specific objectives are to:
•	Configure a functional cybersecurity laboratory using VirtualBox.
•	Install and configure Kali Linux as the penetration-testing platform.
•	Configure Windows 10 as a controlled target system.
•	Establish network connectivity between the virtual machines.
•	Configure basic IP addressing, gateways, DNS, and virtual networking.
•	Perform network discovery and host identification.
•	Take a clean VM snapshot for recovery.
•	Document the complete setup process.
•	Prepare the environment for future cybersecurity projects


**3.	Methodology**


The practical assessment followed a structured penetration-testing methodology. The process was designed to progressively move from understanding the environment to identifying and analyzing potential weaknesses.
•	Laboratory Configuration
•	Connectivity Verification
•	Network Discovery


**4.	Scope**


The scope of this practical laboratory is limited to the virtual machines and network resources specifically created for authorized cybersecurity training.
The laboratory includes:
•	Kali Linux as the attacker/security-testing machine.
•	Windows 10 as the target machine.
•	Oracle VirtualBox as the virtualization platform.
•	VirtualBox NAT Network using 10.0.0.0/24.
•	Kali Linux IP address: 10.0.0.2.
•	Gateway/DNS: 10.0.0.1.
•	Network discovery and connectivity testing.
•	Port and service enumeration.
•	Vulnerability assessment.
•	Controlled penetration-testing activities.
•	Security analysis and documentation.
Testing is restricted to the laboratory environment and systems for which authorization has been obtained. No production, third-party, or unauthorized systems are included within the scope of the assessment.


**5.	Lab Architecture**


The laboratory was implemented using Oracle VirtualBox with two primary virtual machines. Kali Linux functions as the security-testing/attacker machine, while Windows 10 functions as the controlled target. He followings are lab logical architecture and Ip configuration.
<img width="304" height="414" alt="image" src="https://github.com/user-attachments/assets/6919b003-fa05-4e3c-bb90-f7f5aa112307" />


**6.	Tools Used**


The laboratory makes use of several security and networking tools available within Kali Linux.
Tool	              Primary Purpose
7-Zip	To extract the Kali Linux virtual-machine package
Linux	Penetration-testing platform
Oracle VirtualBox	Virtual machine and laboratory management
Target 	Windows, Android 


**7. Lab Setup Procedure**
_Step 1. Install 7-Zip_
7-Zip was installed to extract the Kali Linux virtual-machine package, which may be distributed as a .7z archive.

Tool: 7-Zip

_Step 2. Install VirtualBox
_VirtualBox was installed as the hypervisor.

_Step 3. Create the NAT Network_
A dedicated NAT Network was created in VirtualBox.

Configuration: Network Name: NatNetwork IPv4 Prefix: 10.0.0.0/24 DHCP: Enabled IPv6: Disabled
<img width="2729" height="1686" alt="image" src="https://github.com/user-attachments/assets/d26ae3dc-82c0-48a6-a51e-bba0b3dcd9dd" />

A NAT Network was selected because multiple virtual machines connected to the same NAT Network can communicate with one another while also having outbound network connectivity.

This will allow future attacker and target VMs to communicate within the lab.

_Step 4. Import Kali Linux_
The Kali Linux virtual machine was downloaded from the official Kali Linux website and imported into VirtualBox.

The VM network adapter was configured as follows:

Adapter 1
Attached to: NAT Network
Network:     NatNetwork
Adapter Type: Intel PRO/1000 MT Desktop
The VM was allocated:

RAM: 2048 MB
A shared folder was also configured for transferring required files between the host operating system and the Kali VM.
 <img width="624" height="333" alt="image" src="https://github.com/user-attachments/assets/2c352275-7406-4628-99fc-5986bc7d7fec" />

Step 5. Configure the Kali Linux Network
The Kali Linux network configuration was checked and configured with a consistent IPv4 address.

Example configuration:

IP Address: 10.0.0.2
Subnet Mask: 255.255.255.0
Gateway: 10.0.0.1
DNS: 8.8.8.8
A consistent IP address makes it easier to document the lab and reference the Kali machine in future exercises.

<img width="624" height="320" alt="image" src="https://github.com/user-attachments/assets/be53ef83-79fc-466f-8d03-830bf43275b1" />
<img width="624" height="302" alt="image" src="https://github.com/user-attachments/assets/9a5f87df-cd63-4e49-8829-ea6ec257b39d" />

**Lab Verification**
 <img width="1095" height="397" alt="image" src="https://github.com/user-attachments/assets/f5d55388-9d6d-46a6-bd8d-7f50ec3f1b5e" />
Example Results
IP Address:
10.0.0.2/24

Gateway:
10.0.0.1

DNS:
8.8.8.8

Problems Encountered & Solutions
Documenting problems is an important part of the project.

Problem 1. Internet Connectivity After Static IP Configuration
After manually configuring the IPv4 settings, Internet connectivity may fail depending on the Kali/NetworkManager configuration.

One workaround used during this lab was:

sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0
The network connection was then restarted/rebooted and connectivity was tested again.

Important: Network interface and connection names may differ between systems. Students should first identify their actual connection name before running an nmcli command.

Problem 2. VirtualBox VT-x / Virtualization Error
The VM initially failed to start because hardware virtualization was disabled in the system firmware/BIOS.

The issue was resolved by:

Restarting the computer.
Entering BIOS/UEFI settings.
Enabling Intel VT-x / hardware virtualization.
Saving the configuration.
Restarting the computer.
Starting the Kali VM again.
After enabling virtualization, the VM started successfully.

💡 What I Learned
Through this project, I learned how to create and configure a virtual environment for cybersecurity practice.

The most important concepts I learned include:

1. NAT vs NAT Network
A standard NAT configuration and a NAT Network serve different purposes.

A NAT Network allows multiple VMs connected to the same virtual network to communicate with one another while providing network address translation for external connectivity.

This makes it useful for building a multi-machine cybersecurity laboratory.

2. Virtual Machine Networking
I learned how VirtualBox virtual network adapters connect virtual machines to different types of networks and how network configuration affects communication between machines.

3. Static IP Configuration
I learned how to configure and verify IPv4 addressing, subnet masks, gateways, and DNS settings in Kali Linux.

4. VM Snapshots
I learned that a clean snapshot should be created before performing risky or experimental activities.

This provides a known-good recovery point for future cybersecurity exercises.

5. Documentation
I learned that documenting commands, configuration, screenshots, problems, and solutions is an important part of a professional cybersecurity project.

🔐 Security & Ethical Use
This laboratory is intended strictly for education purposes only.

🔗 Tools & Resources
7-Zip: https://7-zip.org/download.html
VirtualBox: https://virtualbox.org/wiki/Downloads
Kali Linux: https://kali.org/get-kali



Author
BIKILA GIRAGN
Cybersecurity Professional B083

LinkedIn: linkedin.com/in/bikila-giragn-827499241
Email: bikila.girag@gmail.com

📌 Project Information
Program Name: Cybersecurity at Networkwalks | Week: 01 | Project: Cybersecurity & Pentesting Lab Setup | Repository: GitHub
