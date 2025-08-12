# Penetration Testing Labs – Chapter 1: Environment Setup

This lab follows **Georgia Weidman’s _Penetration Testing: A Hands-On Introduction to Hacking_** and sets up a safe environment for practicing ethical hacking skills.

---

## **Lab Overview**
The goal of this lab was to configure an isolated penetration testing environment using:

- **Kali Linux** (Attacker Machine)
- **Metasploitable 2** (Vulnerable Linux Target)
- **Windows XP** (Vulnerable Windows Target)

The network is configured as **Host-Only** in VMware, ensuring no interaction with the internet and safe exploitation practice.

---

## **Tools Verified Installed**
All essential tools required for the book’s labs were verified:


---

## **Network Configuration**
- **VMware Network Adapter**: `vmnet0` set to *Host-Only*
- **Kali Linux IP**: `192.168.56.128`
- **Metasploitable 2 IP**: `192.168.56.129`
- **Windows XP IP**: `192.168.56.101`

---

## **Connectivity Test**
We verified that Kali could communicate with both targets using `ping`.

### **Ping to Metasploitable 2**
```bash
ping -c 3 192.168.56.129
64 bytes from 192.168.56.129: icmp_seq=1 ttl=64 time=2.10 ms
64 bytes from 192.168.56.129: icmp_seq=2 ttl=64 time=1.50 ms
64 bytes from 192.168.56.129: icmp_seq=3 ttl=64 time=1.40 ms
