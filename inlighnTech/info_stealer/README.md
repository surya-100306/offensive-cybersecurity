# 🛑 Chrome Password Extractor (Windows Only)

This Python tool extracts saved Chrome browser passwords, clipboard content, and basic system information **from Windows systems**.  
It uses native Windows APIs and Chrome's internal database to retrieve and decrypt stored credentials.

---

## ⚠️ Legal Warning

> **This tool is intended for educational and authorized security auditing purposes only.**  
> Unauthorized access to systems or data is illegal and unethical. Do **not** use this on systems you do not own or have explicit permission to test.

---

## 🧠 Features

- 🔐 Decrypts saved passwords from Google Chrome (Windows DPAPI + AES key)
- 📋 Captures current clipboard contents
- 🖥️ Gathers basic system information including local/global IP, hostname, MAC address, etc.

---

## 📦 Requirements

- Python 3.x
- Dependencies:
```bash
pip install pycryptodome
pip install pyperclip
pip install pypiwin32
pip install requests
```

---

## 🚀 Usage

```bash
git clone https://github.com/PM-ADD/offensive-cybersecurity.git
cd offensive-cybersecurity
cd inlighnTech
cd info_stealer
python info_stealer.py
```

- Extracted credentials are printed to the terminal.
- Clipboard content and system info are also shown.

---

## 💡 How It Works (Windows Specific)

1. Retrieves Chrome’s encrypted AES key from `Local State` file.
2. Decrypts the key using `CryptUnprotectData` (Windows DPAPI).
3. Reads encrypted login data from the `Login Data` SQLite DB.
4. Decrypts saved credentials using AES-GCM or legacy DPAPI.
5. Displays results and clipboard/system info.

---

## ❌ Limitations

- ❗ Only works on **Windows** (uses `win32crypt`)
- ❌ Will **not** work on Linux or macOS without major changes
- 🔒 May require elevated privileges depending on system config

---

## 📁 Example Output

```
Extracted Browser Password:
Profile: Default
URL: https://accounts.google.com
Username: example@gmail.com
Password: supersecret123
----------------------------------------

Clipboard Content:
Hello from the clipboard!

System Information:
platform:Windows
platform-release:10
ip-address:192.168.1.10
global-ip-address:203.0.113.55
...
```

---

