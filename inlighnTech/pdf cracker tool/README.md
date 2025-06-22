# PDF Brute-force Decryption Tool

This tool attempts to decrypt a password-protected PDF using either:
- A **custom wordlist**, or
- **Generated passwords** based on character sets and length.

It supports **multithreading** using Python's `ThreadPoolExecutor` for improved performance and uses `pikepdf` for PDF handling.

## Features

- Decrypt PDFs with a known or guessed password
- Use a custom wordlist or generate passwords on the fly
- Supports multithreading (default: 4 threads)
- Shows progress with `tqdm`

---

## 🛠 Requirements

Install the required Python libraries:

```bash
pip install pikepdf tqdm
```

---

## 📄 Usage

```bash
git clone https://github.com/PM-ADD/offensive-cybersecurity.git
cd offensive-cybersecurity
cd inlighnTech
cd 'pdf cracker tool'
```

```bash
python pdf_cracker.py <pdf_file> [OPTIONS]
```

### Arguments

| Argument          | Description                                          |
|-------------------|------------------------------------------------------|
| `pdf_file`        | Path to the password-protected PDF                   |

### Options

| Option            | Description                                          | Default |
|-------------------|------------------------------------------------------|---------|
| `--wordlist`      | Path to a wordlist file                              | `None`  |
| `--generate`      | Enable password generation mode                      | `False` |
| `--min_length`    | Minimum password length (used with `--generate`)     | `1`     |
| `--max_length`    | Maximum password length (used with `--generate`)     | `3`     |
| `--charset`       | Characters to use for password generation            | `string.ascii_letters + string.digits + string.punctuation` |
| `--max_workers`   | Number of parallel threads to use                    | `4`     |

---

## 🔍 Examples

### Example 1: Using a Wordlist

```bash
python pdf_cracker.py secret.pdf --wordlist wordlist.txt
```

### Example 2: Generating Passwords (length 1 to 3)

```bash
python pdf_cracker.py secret.pdf --generate --min_length 1 --max_length 3
```

### Example 3: Generate with Custom Charset

```bash
python pdf_cracker.py secret.pdf --generate --min_length 1 --max_length 2 --charset abc123
```

---

## 📦 Output

If the password is found:
```
[+] Password found: mypassword
PDF decrypted successfully with password: mypassword
```

If not:
```
Unable to decrypt PDF. Password not found
```

---

## ⚠️ Disclaimer

This tool is for educational and ethical testing purposes **only**. Do **not** use it on files you do not have permission to access.

---
