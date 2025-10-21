#  Agodjié Pro ~Network Audit Framework


<pre> 
  _____    ________ ________  ________        ____.______________    ____________________ ________   
  /  _  \  /  _____/ \_____  \ \______ \      |    |   \_   _____/    \______   \______   \\_____  \  
 /  /_\  \/   \  ___  /   |   \ |    |  \     |    |   ||    __)_      |     ___/|       _/ /   |   \ 
/    |    \    \_\  \/    |    \|    `   \/\__|    |   ||        \     |    |    |    |   \/    |    \
\____|__  /\______  /\_______  /_______  /\________|___/_______  /     |____|    |____|_  /\_______  /
        \/        \/         \/        \/                      \/                       \/         \/ 
~ Bassitou404                                                                                                                                                    
                                                                                                                                                    

</pre>
<br>

                    



## Overview

**Agodjié Pro** is a professional, modular, high-performance network auditing framework developed in Python.  
It is designed for security professionals, penetration testers, and network engineers to perform comprehensive network assessments quickly and safely.

The framework provides tools for:

- **Host discovery** – identify devices on a network using ARP, ping, or LAN scanning.  
- **Port scanning** – perform asynchronous TCP scans with customizable concurrency and rate-limiting.  
- **Operating system detection** – estimate the OS using ICMP TTL heuristics.  
- **Firewall detection** – infer host- or network-level filtering.  
- **Basic vulnerability checks** – inspect HTTP headers, TLS versions, and anonymous FTP login.  
- **Plugin support** – safely extend functionality with local Python scripts.  
- **Reporting** – generate structured JSON and interactive HTML reports with ASCII-branded headers.

Agodjié Pro is built with **security, modularity, and performance** in mind. Asynchronous scanning, input validation, safe plugin execution, and cross-platform support ensure reliable and efficient auditing.

> ⚠️ **Legal Notice:** Use only on networks and systems you own or have explicit permission to audit. Unauthorized scanning is illegal and strictly prohibited.

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/Bassitou404/agodjie-pro.git
cd agodjie-pro




