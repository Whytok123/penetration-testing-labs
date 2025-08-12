# Penetration Testing Labs – Chapter 1: Environment Setup

This project follows the labs from **Georgia Weidman’s _Penetration Testing: A Hands-On Introduction to Hacking_**.  
Chapter 1 focuses on creating a safe and isolated environment for practicing penetration testing.

---

## 📚 Lab Overview
The goal of this lab was to:
- Set up a virtual penetration testing lab using **Kali Linux** as the attacker machine.
- Deploy vulnerable target machines (e.g., Metasploitable2, Windows XP) inside a **Host-Only network**.
- Verify connectivity between machines for future exploitation exercises.

---

## 🛠 Environment Details
**Tools Installed on Kali:**
- `nmap`, `netcat`, `tcpdump`, `wireshark`, `gobuster`, `nikto`, `burpsuite`, `msfconsole`
- `hydra`, `john`, `hashcat`, `aircrack-ng`, `reaver`
- `gdb`, `radare2`, `strings`, `whois`, `dig`, `dnsenum`
- `curl`, `wget`, `python3`, `ssh`, `openssl`

**Virtual Network Configuration:**
- VMware **Host-Only Adapter** (`VMnet0`)
- Subnet: `192.168.56.0/24`
- Kali Linux IP: `192.168.56.128`
- Metasploitable2 IP: `192.168.56.129`

---

## 🔍 Connectivity Test
To confirm network connectivity, the following ping command was used from Kali to Metasploitable2:

```bash
ping -c 3 192.168.56.129

