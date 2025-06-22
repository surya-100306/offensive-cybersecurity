# 🛠️ SSH Botnet Controller

## 📜 Description

This script is a **Botnet Controller** that uses SSH to remotely control multiple machines (bots) for educational and ethical penetration testing purposes. It supports:

- Listing connected bots
- Running shell commands
- Interactive bash mode
- Simulating DDoS attacks
- Saving and loading botnet data from a JSON file

> ⚠️ **DISCLAIMER:**  
> This script is meant strictly for **educational** and **authorized** use only. Unauthorized access or attacks on systems you do not own or have permission to test is illegal and unethical.

---

## ⚙️ Features

- 📡 Connect to remote SSH machines (bots)
- 📝 Send shell commands to all connected bots
- 💻 Bash mode to simulate terminal interactions
- 📂 Save/load botnet configuration using `botnet.json`
- 💥 Simulated TCP SYN flood attack with Scapy

---

## 🧪 Requirements

Install the dependencies using:

```bash
pip install colorama pexpect scapy
```

---

## ▶️ Usage

```bash
git clone https://github.com/PM-ADD/offensive-cybersecurity.git
cd offensive-cybersecurity
cd inlighnTech
cd ssh_botnet
python3 ssh_botnet.py
```

### 🟢 Menu Options

| Option | Description                        |
|--------|------------------------------------|
| 1      | List all connected bots            |
| 2      | Run a single command on all bots   |
| 3      | Bash shell for live commands       |
| 4      | Add a new bot (SSH login required) |
| 5      | Simulate DDoS attack (Scapy)       |
| 6      | Exit and save current session      |

---



## 💣 DDoS Simulation

**Note**: The DDoS feature sends TCP SYN packets in an infinite loop.

> Use only in **lab/test environments** (e.g., your own VM or test router).

---

## 🔐 Security Note

Stored passwords in `botnet.json` are **not encrypted**. Avoid storing credentials for production or real-world systems.

---

## 📚 Educational Purpose Only

This project is designed for learning:

- SSH automation
- Remote command execution
- Network packet crafting (Scapy)
- Ethical hacking scripting

---
