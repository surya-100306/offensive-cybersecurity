
# 🔐 Hash Cracker

A multithreaded Python hash cracking tool that supports both **wordlist attacks** and **brute-force password generation**. It supports common hash algorithms such as MD5, SHA1, SHA256, and more.

---

## 🚀 Features

- 🔢 Supports hash types: `md5`, `sha1`, `sha224`, `sha256`, `sha384`, `sha512`, `sha3_224`, `sha3_256`, `sha3_384`, `sha3_512`
- 🚀 Multithreaded with `ThreadPoolExecutor` for speed
- 🔍 Supports both wordlist and brute-force attacks
- 📊 Live progress display with `tqdm`

---

## 🧭 How to Use This Tool

### 1. 📥 Clone or Download
```bash
git clone https://github.com/PM-ADD/offensive-cybersecurity.git
cd offensive-cybersecurity
cd inlighnTech
cd hash_cracker
```

### 2. 📦 Install Dependencies
```bash
pip install tqdm
```

### 3. 🛠️ Run the Tool

#### 🔑 Wordlist Mode
```bash
python3 hash_cracker.py <hash> -w <wordlist_path> --hash_type md5
```

**Example:**
```bash
python3 hash_cracker.py d8578edf8458ce06fbc5bb76a58c5ca4 -w wordlist.txt --hash_type md5
```

#### 💥 Brute-force Mode
```bash
python3 hash_cracker.py <hash> --hash_type sha1 --min_length 1 --max_length 5
```

**Example:**
```bash
python3 hash_cracker.py aaf4c61ddcc5e8a2dabede0f3b482cd9aea9434d --hash_type sha1 --min_length 1 --max_length 5
```

### 4. 🧪 Optional Flags

| Flag               | Description                                      | Default                |
|--------------------|--------------------------------------------------|------------------------|
| `-w, --wordlist`   | Path to wordlist file                            | None                   |
| `--hash_type`      | Hash algorithm (e.g. md5, sha256, sha3_512)      | `md5`                  |
| `--min_length`     | Minimum length of passwords (brute-force only)   | None                   |
| `--max_length`     | Maximum length of passwords (brute-force only)   | None                   |
| `-c, --characters` | Characters to use in brute-force mode            | `a-zA-Z0-9`            |
| `--max_workers`    | Number of threads to use                         | `4`                    |

---



## 🧪 Test Hashes

| Text     | MD5                                | SHA1                                      |
|----------|------------------------------------|-------------------------------------------|
| `hello`  | `5d41402abc4b2a76b9719d911017c592` | `aaf4c61ddcc5e8a2dabede0f3b482cd9aea9434d` |
| `qwerty` | `d8578edf8458ce06fbc5bb76a58c5ca4` | `b1b3773a05c0ed0176787a4f1574ff0075f7521e` |

---

## ⚠️ Disclaimer

This tool is intended for **educational and ethical** use only. Do not use it on systems or hashes without **explicit authorization**. Misuse of this tool may be illegal.

---

