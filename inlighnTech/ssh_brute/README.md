
# 🔐 SSH Brute Force Tool

A multithreaded SSH brute force script built with Python. Created for penetration testers, red teamers, and cybersecurity students — strictly for **authorized use**.

> ⚠️ **Warning:** Unauthorized access to systems is illegal. This tool is for ethical testing only.

---

## 📦 Features

- ✅ Supports password lists or on-the-fly password generation
- ✅ Single username or full userlist support
- ✅ Retry on SSH connection failures
- ✅ Saves valid credentials to `credentials.txt`
- ✅ Multithreaded for high-speed attacks
- ✅ Colorized terminal output using Colorama

---

## 🛠 Installation

You can install the dependencies using the provided `requirements.txt`.

### 🐧 Linux / Kali

```bash
sudo apt update
sudo apt install python3 python3-venv -y
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### 🪟 Windows (PowerShell)

1. Install Python from https://www.python.org
2. Open PowerShell in the project folder:

```powershell
python -m venv venv
.\venv\Scripts\activate
pip install -r requirements.txt
```

### 🍎 macOS

```bash
brew install python3
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

---

## 🚀 Usage


```bash
git clone https://github.com/PM-ADD/offensive-cybersecurity.git
cd offensive-cybersecurity
cd inlighnTech
cd ssh_brute
```

### Basic usage with password list:

```bash
python advanced_ssh_brute.py 192.168.1.100 -u root -P wordlists/passwords.txt --threads 5
```

### Using username and password lists:

```bash
python advanced_ssh_brute.py 192.168.1.100 -U wordlists/users.txt -P wordlists/passwords.txt --threads 10
```

### Using generated passwords:

```bash
python advanced_ssh_brute.py 192.168.1.100 -u admin --generate --min-length 3 --max-length 5 --chars abc123 --threads 4
```

---

## ⚙️ Arguments

| Option             | Description                                       |
|--------------------|---------------------------------------------------|
| `host`             | IP or hostname of the SSH target                  |
| `-u`               | Single username                                   |
| `-U`               | Username list file                                |
| `-P`               | Password list file                                |
| `--generate`       | Use password generator                            |
| `--min-length`     | Minimum generated password length                 |
| `--max-length`     | Maximum generated password length                 |
| `--chars`          | Character set to use in generation                |
| `--threads`        | Number of concurrent threads                      |

---

### 📝 Example Command

```bash
python advanced_ssh_brute.py 192.168.1.100 -U wordlists/users.txt -P wordlists/passwords.txt --threads 5
```

Or using password generation:

```bash
python advanced_ssh_brute.py 192.168.1.100 -u root --generate --min-length 3 --max-length 4 --chars abc123 --threads 5
```

---
## 💾 Output

- ✅ Successful logins are saved to `credentials.txt`
- ❌ Invalid attempts and errors are printed in red or blue

---

## 🔐 Disclaimer

This tool is for **educational and authorized penetration testing** only.  
You must have explicit permission to test any system using this script.  
**Unauthorized use is illegal and unethical.**



## 👤 Author

- GitHub: [PM-ADD](https://github.com/PM-ADD)
