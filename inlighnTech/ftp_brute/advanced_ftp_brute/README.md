# Advanced Multithreaded FTP Brute Force Tool

## 📌 Overview

This script is a comprehensive, multithreaded FTP brute-force tool written in Python. It supports both static and dynamic password strategies, including:

- Username list or single username
- Password list or on-the-fly password generation
- Adjustable thread count
- Custom character sets and password lengths

Designed for **authorized penetration testing**, CTFs, and ethical hacking research.

## ⚠️ Legal Disclaimer

> **WARNING**: This tool is intended strictly for educational use and **authorized penetration testing** only.
>
> Do not use this tool on systems without **explicit written permission**. Misuse may lead to **legal consequences**.

## 🚀 Features

- Multithreaded FTP brute-force attack
- Static or dynamic password support
- Single or multiple usernames
- Configurable password generation parameters
- Informative output with color-coded results

## 🧰 Requirements

- Python 3.x
- `colorama` (`pip install colorama`)



## 🛠️ Usage

```bash
git clone https://github.com/PM-ADD/offensive-cybersecurity.git
cd offensive-cybersecurity
cd inlighnTech
cd ftp_brute
cd advanced_ftp_brute
```

### Static Username and Wordlist

```bash
python3 advanced_ftp_brute.py --host 192.168.1.195 -u admin -w passwords.txt
```

### Using Username List

```bash
python3 advanced_ftp_brute.py --host 192.168.1.195 -U usernames.txt -w passwords.txt
```

### Generating Passwords On-the-Fly

```bash
python3 advanced_ftp_brute.py --host 192.168.1.195 -u admin -g --min_length 1 --max_length 3 -c abc123
```

### Custom Thread Count

```bash
python3 advanced_ftp_brute.py --host 192.168.1.195 -u admin -w passwords.txt -t 50
```

## ⚙️ Command Line Options

| Option | Description |
|--------|-------------|
| `--host` | Target FTP server IP or hostname (**required**) |
| `--port` | Target port (default: 21) |
| `-u` | Single username |
| `-U` | Username list file |
| `-w` | Password list file |
| `-g` | Generate passwords instead of using a list |
| `--min_length` | Minimum password length (for generation) |
| `--max_length` | Maximum password length (for generation) |
| `-c` | Characters used in password generation |
| `-t` | Number of threads (default: 30) |

## 🧯 Defensive Recommendations

- Disable FTP in favor of SFTP or FTPS
- Implement rate limiting and account lockouts
- Monitor for brute-force attempts in server logs
- Use strong, unique passwords for all accounts

