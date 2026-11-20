 <div align="center">

# Password Cracking with John the Ripper (JTR)

Practical password-cracking techniques using John the Ripper on Kali Linux, including PDF password-hash extraction and dictionary-based attacks.

<p align="center">
  <img src="https://img.shields.io/badge/Project-Password%20Cracking-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Tool-John%20the%20Ripper-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Utility-pdf2john-238F89?style=flat-square" />
  <img src="https://img.shields.io/badge/OS-Kali%20Linux-E87500?style=flat-square&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Technique-Dictionary%20Attack-C00000?style=flat-square" />
  <img src="https://img.shields.io/badge/Language-Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Focus-Password%20Security-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Program-NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Mentor-Waqas%20Karim%20(CCIE)-C00000?style=flat-square" />
</p>
</div>

## 🔐 Password Cracking Overview

This project documents practical password-cracking techniques using **John the Ripper (JTR)** on Kali Linux.

The exercise focuses on extracting password-hash information from a password-protected PDF document using `pdf2john` and attempting password recovery through dictionary-based attacks using John the Ripper.

It also covers Python dependency management, virtual environment configuration, and troubleshooting during the hash extraction process.

## 🎯 Project Objectives

The primary objectives of this project are to:

- Understand password hashing and password-cracking techniques.
- Understand how password-protected PDF documents use encryption.
- Extract PDF password-hash information using `pdf2john`.
- Install and configure the required Python dependencies.
- Create and manage Python virtual environments.
- Use John the Ripper for dictionary-based password recovery.
- Understand the use of password wordlists such as RockYou.
- Verify password recovery results.
- Document the practical implementation and troubleshooting process.

## 🛡️ Project Purpose and Security Scope

This project provides a controlled environment for learning password security, hash extraction, and password-cracking techniques.

It supports hands-on practice in the following areas:

- Password hashing and hash extraction.
- PDF password protection and encryption.
- Dictionary-based password attacks.
- John the Ripper configuration and usage.
- Password wordlist analysis.
- Python dependency installation and management.
- Cybersecurity troubleshooting and documentation.

**⚠️ Security Notice:** This exercise is intended for educational purposes and authorized password recovery only. Perform testing exclusively on documents and systems you own or have explicit permission to assess.

## ⚙️ Lab System Specifications

| 🧩 Component | ⚙️ Configuration |
|---|---|
| 🖥️ Operating System | Kali Linux 2026.3 |
| 🔐 Password Recovery Tool | John the Ripper |
| 📄 Hash Extraction Utility | pdf2john |
| 🐍 Programming Language | Python 3 |
| 📦 Python Dependency | pyHanko |
| 📚 Password Wordlist | RockYou |
| 🧪 Python Environment | john-pdf-env |
| 💻 Terminal | Kali Linux Terminal |
| 🎯 Target File | My Locked PDF1.pdf |

## ⚙️ Password Cracking Implementation Steps

## Step 1: Install John the Ripper on Kali Linux

John the Ripper was installed using the APT package manager to provide password-cracking and recovery capabilities.

**Tool:** John the Ripper

**Installation commands:**

```bash
sudo apt update
sudo apt install john -y
```

**Verify the installation:**

```bash
john --version
```

## Step 2: Locate the Password-Protected PDF

The password-protected PDF document was located in the NetworkWalks project directory using the `ls` command.

**Commands:**

```bash
cd ~/Downloads/NetworkWalks/WK3-PM
ls
```

**Target File:** `My Locked PDF1.pdf`

## Step 3: Extract the PDF Password Hash

The `pdf2john` utility was used to extract password-hash information from the protected PDF document.

**Activate the Python virtual environment:**

```bash
source ~/john-pdf-env/bin/activate
```

**Extract the PDF password hash:**

```bash
pdf2john "My Locked PDF1.pdf" > pdf_hash2.txt
```

The extracted password-hash information was saved in `pdf_hash2.txt` for subsequent password recovery attempts.

## Step 4: Read and Verify the Extracted PDF Hash

After successfully extracting the PDF password hash, the generated hash file was read using the `cat` command to inspect the extracted password-hash information.

**Command:**

```bash
cat pdf_hash2.txt
```

The extracted hash information was displayed in the terminal and verified before proceeding with password recovery using John the Ripper.

## Step 5: Prepare the RockYou Password Wordlist

The RockYou wordlist was selected for dictionary-based password recovery using John the Ripper.

**Check the wordlist:**

```bash
ls -lh /usr/share/wordlists/rockyou.txt*
```

If the wordlist is compressed, extract it using:

```bash
sudo gzip -dk /usr/share/wordlists/rockyou.txt.gz
```

## Step 6: Attempt Password Recovery Using John the Ripper

John the Ripper was configured to use the RockYou wordlist to test candidate passwords against the extracted PDF hash.

**Command:**

```bash
john --wordlist=/usr/share/wordlists/rockyou.txt pdf_hash2.txt
```

## Step 7: Display Password Recovery Results

The `--show` option was used to display any passwords successfully recovered by John the Ripper.

**Command:**

```bash
john --show pdf_hash2.txt
```

A password is displayed only if John successfully recovers a matching candidate.

# 🐞 Problems Encountered & Solutions

Documenting troubleshooting steps helps improve the workflow and provides a reference for resolving similar issues in future cybersecurity exercises.

## Problem 1: Missing pyHanko Python Dependency

During PDF password-hash extraction using `pdf2john`, the following error was encountered:

```text
pyhanko is missing, run 'pip install --user pyhanko' to install it!
```

**Cause:** The required Python dependency, `pyHanko`, was not installed in the environment.

**Solution:** A Python virtual environment was created and activated to install the missing dependency without modifying Kali Linux's system-managed Python packages.

**Create the virtual environment:**

```bash
python3 -m venv ~/john-pdf-env
```

**Activate the environment:**

```bash
source ~/john-pdf-env/bin/activate
```

**Install the missing dependency:**

```bash
pip install pyhanko
```

After installing the dependency, the PDF hash extraction command was executed again successfully.

---

# 💡 What I Learned

Through this project, I gained practical experience in password-cracking techniques, PDF password-hash extraction, and Python dependency management using Kali Linux.

The most important concepts I learned include:

### 1. John the Ripper

I learned how to use John the Ripper as a password-cracking tool and understand its role in testing password candidates against extracted password hashes.

### 2. Password Hash Extraction

I learned how to use `pdf2john` to extract password-hash information from a password-protected PDF document for further analysis and recovery attempts.

### 3. Python Virtual Environments

I learned how to create, activate, and manage isolated Python environments to install dependencies without modifying Kali Linux's system-managed Python packages.

### 4. Python Dependency Management

I gained experience installing and verifying Python packages using `pip`, including troubleshooting missing dependencies such as `pyHanko`.

### 5. Dictionary-Based Password Attacks

I learned how dictionary-based password attacks work and how John the Ripper uses wordlists such as RockYou to test possible password combinations.

### 6. Troubleshooting and Documentation

I improved my ability to identify command-line errors, investigate missing dependencies, apply appropriate solutions, and document technical procedures in a structured GitHub repository.

### 7. Password Security

I developed a better understanding of password hashing, PDF password protection, hash extraction, and the limitations of dictionary-based password recovery.

---

# 🔐 Security & Ethical Use

This exercise is intended strictly for educational purposes and authorized password recovery. Testing must only be performed on documents and systems you own or have explicit permission to assess.

---

# 🔗 Tools & Resources

- **Kali Linux:** https://www.kali.org/get-kali/
- **John the Ripper:** https://www.openwall.com/john/
- **pyHanko:** https://pyhanko.readthedocs.io/
- **Python:** https://www.python.org/
- **RockYou Wordlist:** Available through Kali Linux's wordlists package.

---

# 👤 Author

**Amon Alex**  
Cybersecurity Student B084 | Electronics, Telecommunications & Cybersecurity

**LinkedIn:** [Amon Alex](https://www.linkedin.com/in/amon-lowasa-60877a42a/)

## 📌 Project Information

**Program Name:** Cybersecurity at NetworkWalks | **Week:** 03 | **Project:** W3-PM1: Password Cracking with JTR | **Repository:** GitHub
