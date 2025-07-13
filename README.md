## Key Features & Technical Skills Familiarization

### 1. Robust Remote Desktop Access via SSH Tunneling

- **Engineered and deployed** an SSH tunneling solution, enabling secure Remote Desktop Protocol (RDP) access to internal Windows 10 client machines from an external network.
    
- **Eliminated direct RDP port exposure** to the internet by routing all RDP traffic securely through an encrypted SSH tunnel, significantly reducing attack surface.
    
- **Configured Windows 10 clients** for RDP accessibility, including user account password requirements and Windows Defender Firewall rules.
    

### 2. Centralized Secure File Management

- **Established an Ubuntu Server** as a central SFTP (SSH File Transfer Protocol) hub for secure file storage and transfer.
    
- **Implemented secure file synchronization** capabilities between local Windows machines and external clients, ensuring data integrity and availability.
    

### 3. Network Reconnaissance & Configuration Management

- **Conducted comprehensive network mapping** using `Nmap` from the Ubuntu Server to identify active hosts, their IP addresses, open ports, and device types (e.g., router, PCs, mobile devices) within the local area network.
    
- **Managed router port forwarding (NAT)** to selectively expose only the highly secured SSH service of the Ubuntu server to the internet.
    
- **Implemented and optimized Uncomplicated Firewall (UFW)** rules on the Ubuntu Server to strictly control network access and enhance server security.

### 4. Foundational Cybersecurity Principles

- **Hardened SSH access** by migrating the default SSH port to a non-standard port number, effectively mitigating automated brute-force attacks and port scans.
    
- **Applied least-privilege principles** by requiring strong passwords for all remote access accounts (Ubuntu SSH and Windows RDP users).
    
- **Utilized `ping` and `Nmap`** for active host discovery and port state verification, crucial for network troubleshooting and security assessment.
    

---

## Project Architecture

The following diagram illustrates the secure remote access architecture:

```
[Your Windows Operating System Machine] <---- (Encrypted Traffic over Internet) ---->
       |                                                                    ^
       |                                                                    |
       |-------------------SSH Tunnel to Ubuntu Server----------------------|
                                        |
                                        | (Home Public IP / Dynamic DNS)
                                        V
                                 [ISP Router (Home Gateway)]
                                        |
                                        | (Local Home Network - 192.168.xxx.0/24)
                                        V
                           [Ubuntu Server (e.g., 192.168.xxx.xxx)]
                                        |
                                        | (Internal Network Access / RDP over SSH Tunnel)
                                        |----------------------------------------------|
                                        V                                              V
                           [Office Windows PC 1 (e.g., 192.168.xxx.xxx)]   [Office Windows PC 2 (e.g., 192.168.xxx.xxx)]
                                       (RDP Port 3389 Open Locally)        (RDP Port 3389 Open Locally)
```

---

## Technologies & Tools Utilized

- **Operating Systems:** Ubuntu Server (Linux), Windows 11, Windows 10
    
- **Network Protocols:** SSH (Secure Shell), SFTP (SSH File Transfer Protocol), RDP (Remote Desktop Protocol), TCP/IP, ICMP
    
- **Networking Tools:** Nmap (Network Mapper), `ipconfig`, `ping`, Router Administration Interface (Port Forwarding, DDNS)
    
- **Linux Utilities:** UFW (Uncomplicated Firewall), `ssh` (client & server), Command Line Interface (CLI)
    
- **Windows Utilities:** Remote Desktop Connection Client (MSTSC), PowerShell / Command Prompt, Windows Defender Firewall
    
- **File Transfer Clients:** WinSCP (for SFTP to Ubuntu server)
    
- **Documentation:** Markdown
    

---

## Learnings & Key Takeaways

This project provided invaluable hands-on experience in:

- **Practical network design and implementation** for secure remote accessibility in a mixed-OS environment.
    
- **Implementing multi-layered security measures**, including SSH tunneling, firewall management, and port obfuscation, to protect internal network resources.
    
- **Diagnosing and troubleshooting complex network connectivity issues**, effectively utilizing tools like `Nmap` and `ping` for detailed reconnaissance.
    
- **Understanding the interplay** between local network security policies and external access requirements.
    
- **Developing an iterative approach** to project development, adapting configurations based on testing and troubleshooting results.


Authored by Alexander M. Muthua
