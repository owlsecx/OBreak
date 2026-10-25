# 🦉 OBreak

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OAttack%20/%20Offensive-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.1.0-cyan?style=flat-square"/>
</p>

> **OBreak** — HTTP Form Credential Tester

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OBreak is an HTTP login-form credential tester for authorised authentication testing. It supports GET, POST and JSON logins with failure and success detection, response-length deviation analysis, redirect tracking and CSRF token refresh. Robustness features include retry with backoff, user-agent rotation, proxy support and WAF/lockout watching, with reports exported to HTML, JSON or TXT.

---

## ✨ Features

- GET / POST / JSON login testing with success and failure detection
- Response-length deviation analysis and redirect tracking
- CSRF token refresh and automatic login-form analysis
- Retry with backoff, user-agent rotation and WAF/lockout detection
- Proxy support, cookie injection and profile save/load
- HTML / JSON / TXT report export with ETA and speed display

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OBreak
./OBreak --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
