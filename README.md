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

**7.	VirtualBox Settings**
<img width="624" height="331" alt="image" src="https://github.com/user-attachments/assets/41f53444-3806-4a20-b6f8-4413f04db6a2" />

**8.	VirtualBox Settings for Kali Linux VM**
9.	<img width="624" height="320" alt="image" src="https://github.com/user-attachments/assets/3e493224-5f66-489c-aa2a-5a45322c9544" />
<img width="624" height="302" alt="image" src="https://github.com/user-attachments/assets/b123efaf-acd4-45e8-8d94-1446ce0bb5b3" />
**Shared Folders**
<img width="624" height="333" alt="image" src="https://github.com/user-attachments/assets/a412f264-bebe-4396-8dec-e59154a33223" />

**Ip ADDRESS INFO **
<img width="624" height="316" alt="image" src="https://github.com/user-attachments/assets/1012a506-d5e8-4a00-abd0-2e584674a6b0" />
Clipboard And Drag-Drop Are Enabled
<img width="624" height="332" alt="image" src="https://github.com/user-attachments/assets/3a3b5fa1-58ba-43c2-af2b-2fd96141d243" />
9.	Conclusion
The practical cybersecurity laboratory successfully established a controlled environment for developing hands-on skills in penetration testing, ethical hacking, network security, vulnerability assessment, and security analysis.
The combination of Oracle VirtualBox, Kali Linux, Windows 10, and a dedicated 10.0.0.0/24 NAT Network provided a practical foundation for conducting authorized security assessments. The laboratory demonstrated the complete progression from network configuration and reconnaissance to scanning, enumeration, vulnerability assessment, analysis, and reporting.
The exercises also highlighted the importance of understanding both offensive and defensive perspectives. The same scanning and testing activities performed by a penetration tester can generate network and endpoint events that a SOC analyst may need to detect, investigate, and respond to.
Overall, the laboratory provides a safe and repeatable platform for continuing cybersecurity development. 
