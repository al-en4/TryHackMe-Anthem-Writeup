# TryHackMe – Anthem | Learning-Based Write-Up

## 📌 Overview
This repository documents my learning experience from completing the **Anthem** room on **TryHackMe**.  
As a beginner, this room helped me understand **Windows enumeration** and the practical use of tools like **Nmap**, **Hydra**, and **rdesktop**.

- **Platform**: TryHackMe  
- **Room**: Anthem  
- **Difficulty**: Beginner  
- **Operating System**: Windows  
- **Status**: Completed ✅  

---

## 🎯 What I Learned from This Room

- Network and service enumeration using **Nmap**
- Identifying exposed services on a Windows machine
- Understanding password reuse vulnerabilities
- Credential testing using **Hydra**
- Remote access to Windows systems using **rdesktop**
- Importance of proper enumeration before exploitation

---

## 🔍 Learning Nmap (Service Enumeration)

### What is Nmap?
**Nmap (Network Mapper)** is a powerful tool used to discover hosts, open ports, running services, and operating systems on a network.

### Nmap Scan Used
```bash
 nmap 10.81.133.238 -sC -sV -F -Pn
Starting Nmap 7.95 ( https://nmap.org ) at 2025-12-15 10:06 IST
Nmap scan report for 10.81.133.238
Host is up (0.24s latency).
Not shown: 98 filtered tcp ports (no-response)
PORT     STATE SERVICE       VERSION
80/tcp   open  http          Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Anthem.com - Welcome to our blog
| http-robots.txt: 4 disallowed entries 
|_/bin/ /config/ /umbraco/ /umbraco_client/
3389/tcp open  ms-wbt-server Microsoft Terminal Services
| ssl-cert: Subject: commonName=WIN-LU09299160F
| Not valid before: 2025-12-14T04:28:26
|_Not valid after:  2026-06-15T04:28:26
|_ssl-date: 2025-12-15T04:36:52+00:00; 0s from scanner time.
| rdp-ntlm-info: 
|   Target_Name: WIN-LU09299160F
|   NetBIOS_Domain_Name: WIN-LU09299160F
|   NetBIOS_Computer_Name: WIN-LU09299160F
|   DNS_Domain_Name: WIN-LU09299160F
|   DNS_Computer_Name: WIN-LU09299160F
|   Product_Version: 10.0.17763
|_  System_Time: 2025-12-15T04:36:42+00:00
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 39.50 seconds






