Nmap Network Scan and Wireshark Analysis
Overview
This project involved scanning a local network using Nmap to discover active devices, open ports, and running services. The captured network traffic was then analyzed using Wireshark to understand how port scanning works at the packet level.

Objectives
Identify devices connected to the local Wi-Fi network.

Find open TCP ports and services on those devices.

Understand potential security risks.

Capture and analyze the scanning traffic using Wireshark.

Save the scan results in both text and HTML formats.

Commands Used
1. Check Nmap Installation
bash
Copy
Edit
nmap --version
Verifies that Nmap is installed and shows the current version.

2. Identify Local IP Range
bash
Copy
Edit
ip a
Displays network interfaces and IP addresses. From the output, the active local IP range was found to be 192.168.0.0/24.

3. Perform a TCP SYN Scan
bash
Copy
Edit
sudo nmap -sS 192.168.0.0/24
Scans all devices in the subnet using TCP SYN packets to find open ports.

4. Save Scan Results as a Text File
bash
Copy
Edit
sudo nmap -sS 192.168.0.0/24 -oN scanned_results.txt
Saves the Nmap output in a human-readable .txt file.

5. Save Scan Results as HTML
bash
Copy
Edit
sudo nmap -sS 192.168.0.0/24 -oX scan_results.xml
xsltproc scan_results.xml -o scan_results.html
Saves the scan as XML and converts it to an HTML report.

6. Capture Network Traffic with Wireshark
Interface: wlp0s20f3 (Wi-Fi)

Capture started before running the Nmap command

Traffic was stopped after scan completion

Summary of Findings
Devices with closed ports are secure.

Open ports like SSH (22), Telnet (23), HTTP (80), and SMB (445) can pose risks if misconfigured or exposed.

Telnet and UPnP are outdated or potentially dangerous and should be disabled unless necessary.

SMB services should be reviewed for security if not needed.

Important Notes
Nmap scanning should only be done on networks you own or have permission to scan.

Telnet and UPnP are common targets for exploitation.

Wireshark should be run with care; it captures all packets, including sensitive data if unencrypted.
