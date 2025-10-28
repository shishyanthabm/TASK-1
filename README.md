# Network Scanning and Analysis – Task 1

This project demonstrates how to **scan a local network for open ports** using Nmap and analyze network traffic using Wireshark. It focuses on identifying potential vulnerabilities and improving security configurations.

## Overview

The goal of this task is to perform a **TCP SYN scan** using Nmap on a local IP address, identify open ports, and analyze packet traffic using Wireshark.  
Through this process, we evaluate potential **security risks** associated with exposed network services.

## Tools Used

- **Nmap** – For scanning open ports and detecting active services.  
- **Wireshark** – For packet capture and network traffic analysis.  
- **Kali Linux** – Environment used to run the scan and analysis.

## Procedure

### 1. Identify Local Network Range
ip a
### 2. Nmap SYN Scan
sudo nmap -sS 192.168.0.118
## Results
Starting Nmap 7.95 ( https://nmap.org )
Nmap scan report for 192.168.0.118
Host is up (0.00077s latency).
Not shown: 999 filtered tcp ports (no-response)
PORT     STATE SERVICE
3306/tcp open  mysql
MAC Address: 50:5A:65:7C:68:D7 (AzureWave Technology)

## Analysis
Open Port: 3306 (MySQL Database Service)
Risk Level: High (if accessible externally)
## Potential Threats: 
Unauthorized data access, brute-force attacks, SQL injection through exposed DB, data interception.
## Recommendations: 
Restrict access, enable encryption, apply authentication hardening, and regularly patch MySQL.

