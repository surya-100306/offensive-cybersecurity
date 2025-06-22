
# 🖧 Network Scanner (ARP-based)

A simple Python-based network scanner using Scapy to detect active hosts on a local network.  
It identifies IP addresses, MAC addresses, and hostnames of devices on the same subnet.

---

## ⚙️ Features

- 🔎 Scans local networks using ARP requests
- 🖥 Displays IP, MAC, and resolved hostnames
- 🚀 Fast and efficient with Scapy
- 🛡 Requires root privileges

---

## 📦 Requirements

- Python 3.x
- `scapy`

Install with:
```bash
pip install scapy
```

---

## 🚀 Usage

```bash
git clone https://github.com/PM-ADD/offensive-cybersecurity.git
cd offensive-cybersecurity
cd inlighnTech
cd 'Network Scanner'
sudo python3 network_scaner.py
```

> ⚠️ Scapy needs root privileges, so you must run the script with `sudo`.

---

## 🧭 Example

```bash
Enter network ip address: 192.168.1.0/24
```

Example Output:
```
IP                    MAC                    Hostname
--------------------------------------------------------------------------------
192.168.1.1           aa:bb:cc:dd:ee:ff      router.local
192.168.1.100         11:22:33:44:55:66      desktop.local
```



---

## 🛡 Disclaimer

This tool is for **authorized network diagnostics and educational purposes** only.  
Do **not** scan networks you do not own or have permission to audit.

---
