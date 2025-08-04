# Nmap Network Scan and Wireshark Packet Analysis

## Overview

This project demonstrates how to scan a local network using **Nmap** and analyze network activity with **Wireshark**. The goal is to learn how to detect active devices, identify open ports, recognize exposed services, assess potential risks, and observe real-time packet exchange during a port scan.

---

## Objectives

- Discover devices connected to the local Wi-Fi network.
- Detect open TCP ports and identify services running on them.
- Analyze potential security risks of exposed services.
- Use Wireshark to view and understand network traffic during scans.
- Save scan results in text and HTML format for documentation.

---

## Step-by-Step Workflow

### 1. Verify Nmap Installation
Use the following command to confirm that Nmap is installed:

```bash
nmap --version

Nmap version 7.80 ( https://nmap.org )
Platform: x86_64-pc-linux-gnu

ip a


inet 192.168.0.7/24 brd 192.168.0.255 scope global dynamic ...

