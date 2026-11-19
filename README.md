 <div align="center">

# PDF Password Hash Extraction and Recovery

Extracting PDF password hashes and attempting password recovery using John the Ripper on Kali Linux.

<p align="center">
  <img src="https://img.shields.io/badge/Project-PDF%20Password%20Recovery-404040?style=flat-square&labelColor=C00000" />
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

## 🔐 PDF Password Hash Extraction and Recovery Overview

This project documents the process of extracting password-hash information from a password-protected PDF document and attempting password recovery using **John the Ripper** on Kali Linux.

The exercise uses `pdf2john` to extract the PDF password hash and John the Ripper to perform dictionary-based password recovery. It also covers Python dependency management and troubleshooting during the extraction process.

## 🎯 Project Objectives

The primary objectives of this project are to:

- Understand PDF password protection and encryption.
- Extract PDF password-hash information using `pdf2john`.
- Install and configure the required Python dependencies.
- Create and manage Python virtual environments.
- Use John the Ripper for dictionary-based password recovery.
- Understand password recovery techniques and their limitations.
- Verify password recovery results.
- Document the practical implementation and troubleshooting process.

## 🛡️ Project Purpose and Security Scope

This project provides a controlled environment for learning PDF password security, password-hash extraction, and password recovery techniques.

It supports hands-on practice in the following areas:

- PDF password protection and encryption.
- Password-hash extraction and analysis.
- Dictionary-based password attacks.
- John the Ripper configuration and usage.
- Python dependency installation and management.
- Cybersecurity troubleshooting and documentation.

**⚠️ Security Notice:** This exercise is intended for educational purposes and authorized password recovery only. Perform testing exclusively on PDF documents you own or have explicit permission to access.

## ⚙️ Lab System Specifications

| 🧩 Component | ⚙️ Configuration |
|---|---|
| 🖥️ Operating System | Kali Linux 2026.3 |
| 🐉 Security Distribution | Kali Linux |
| 🔐 Password Recovery Tool | John the Ripper |
| 📄 Hash Extraction Utility | pdf2john |
| 🐍 Programming Language | Python 3 |
| 📦 Python Dependency | pyHanko |
| 📚 Password Wordlist | RockYou |
| 🧪 Python Environment | john-pdf-env |
| 💻 Terminal | Kali Linux Terminal |
| 🎯 Target File | My Locked PDF1.pdf |
