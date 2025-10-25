## Author
**Kunal Kawale**  
Cybersecurity Intern | Firewall Configuration Project

# firewall-configuration
Internship project demonstrating firewall configuration using UFW on Linux and Windows Defender Firewall — includes scripts, documentation, and screenshots for blocking and allowing network ports.

# Firewall Configuration Task (Windows/Linux)

## Objective
Configure and test basic firewall rules to allow or block specific network traffic using:
- **UFW (Uncomplicated Firewall)** on Linux
- **Windows Defender Firewall** on Windows

## Tools Used
- **Linux (Ubuntu 20.04+)** — UFW
- **Windows 10/11** — Windows Defender Firewall
- **Telnet Utility** — for testing blocked ports

## Steps (Linux - UFW)

1️⃣ **Check current firewall status**
```bash
sudo ufw status

## Enable firewall
sudo ufw enable

##List current rules
sudo ufw status numbered

##Block inbound traffic on port 23 (Telnet)
sudo ufw deny 23

##Test the rule
telnet localhost 23
Expected: Connection refused

##Allow SSH (port 22)
sudo ufw allow 22

##Remove the block rule
sudo ufw delete deny 23
