
# 🌐 Domain & Subdomain Enumeration Tool

This is a Python-based multithreaded tool designed to enumerate active subdomains of a target domain using brute-force and HTTP probing.

---

## 🔍 Features

- ✅ Multi-threaded for faster subdomain resolution
- 🌐 Supports HTTP and HTTPS protocol checking
- 🧠 Outputs only live and accessible subdomains
- 📁 Saves results to a text file (`found_subdomains.txt`)

---

## 📦 Requirements

- Python 3.x
- `requests`

Install using:
```bash
pip install requests
```

---

## 🚀 Usage

```bash
git clone https://github.com/PM-ADD/offensive-cybersecurity.git
cd offensive-cybersecurity
cd inlighnTech
cd 'Domain enumeration tool'
python3 subdomain_enum.py
```

Make sure you have a file named `subdomains.txt` in the same directory containing possible subdomain names (one per line).

---

## 🧾 Example `subdomains.txt`

```
www
testphp
admin
blog
ftp
dev
```

---

## 📄 How It Works

1. Reads subdomain list from `subdomains.txt`
2. Appends each subdomain to the base domain (default: `vulnweb.com`)
3. Checks HTTP and HTTPS availability
4. Writes all discovered, reachable subdomains to `found_subdomains.txt`

---

## 💡 Sample Output

```
[+] Discovered subdomain: http://testphp.vulnweb.com
[+] Discovered subdomain: https://testphp.vulnweb.com
```

---

## 🛠 Customize Your Scan

You can edit the script to:
- Change the base domain:
```python
domain = 'example.com'
```
- Add logging or output to JSON/CSV
- Use a wordlist from another path:
```python
with open('subdomains/mylist.txt') as file:
```

---

## ⚠️ Legal Disclaimer

This tool is intended for **authorized security testing and research only**.  
Do not scan or enumerate domains without explicit permission.
