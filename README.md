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