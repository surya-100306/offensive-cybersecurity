# 🔍 Multi-threaded Port Scanner with Banner Grabbing

A Python-based multi-threaded port scanner that checks for open TCP ports on a target host and optionally retrieves service banners.

---

## ✅ Features

- Multi-threaded scanning for high performance
- Detects open ports and tries to identify the service
- Grabs banners for open ports (if available)
- Colored terminal output for visibility

---

## 🛠 Requirements

Python 3.x (standard libraries only)

---

## 🚀 Usage

Run the script in a terminal:

```bash
git clone https://github.com/PM-ADD/offensive-cybersecurity.git
cd offensive-cybersecurity
cd inlighnTech
cd 'Port Scanner'
```

```bash
python3 port_scanner.py
```

### Example Prompt

```
Enter your target ip: 192.168.1.1
Enter the start port: 1
Enter end port: 100
```

---

## ⚙️ How It Works

- Uses `ThreadPoolExecutor` to scan multiple ports in parallel
- For each open port, attempts to identify the service using `socket.getservbyport()`
- If possible, grabs and prints the service banner

---

## 📌 Output Format

```
Port Scan Results:
Port     Service         Status
-----------------------------------------------
22       ssh             Open
         OpenSSH 8.2p1 Ubuntu 4ubuntu0.3
80       http            Open
         Apache httpd
...
```

---



## 🔒 Disclaimer

Use this tool responsibly. Scanning systems without permission is illegal and unethical.

---

