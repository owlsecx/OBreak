# 🦉 OBreak

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-informational?style=flat-square&logo=linux&logoColor=white&color=0a0c10"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OBreak** is an HTTP form credential tester for authorised security testing.
> It supports GET/POST forms, multi-mode credential loading, smart success detection, live progress, and TXT report export.

---

> ⚠️ **AUTHORISED USE ONLY** — OBreak must only be used on systems you own or have **explicit written permission** to test. Unauthorised credential testing is illegal.

---

## 📌 Overview

OBreak submits credential pairs against HTTP login forms and analyses every response to determine success or failure using:

- **Failure string detection** — response not containing a known failure message
- **Success string detection** — response containing a known success keyword
- **HTTP status code detection** — matching expected redirect or success codes
- **Combination mode** — combine all three for maximum accuracy

---

## 🖥️ Interface

| Option | Description |
|--------|-------------|
| **[1] Brute Force** | Wordlist-based credential testing against an HTTP form |
| **[2] Quick Test** | Single username:password pair check |
| **[3] Page Analyser** | Fetch a login page and extract all form fields, action URL, method, and hidden fields |
| **[H] Help** | Display usage guide |
| **[X] Exit** | Quit OBreak |

---

## 🔍 Features

- **GET & POST** support for any HTTP login form
- **Three credential modes** — single user + wordlist, user list × password list, or pre-built pairs file
- **Extra field support** — add CSRF tokens, hidden fields, or any custom form data
- **Custom headers** — inject cookies, auth tokens, or any HTTP header
- **Live progress bar** — real-time display of attempts, found count, and percentage
- **Multi-threaded** — up to 10 parallel threads with configurable delay between attempts
- **TXT report** — saves found credentials to `obreak_reports/` with timestamp, URL, and HTTP details
- **Built-in disclaimer** — requires explicit confirmation before any test begins

---

## 🎯 Credential Modes

| Mode | Description |
|------|-------------|
| **[1] Single user + wordlist** | One username tested against every password in a wordlist |
| **[2] User list × password list** | Every user tested against every password (full matrix) |
| **[3] Pairs file** | Pre-built `user:password` pairs loaded from a file, one per line |

---

## 🛡️ Detection Methods

| Method | Logic |
|--------|-------|
| **Failure string** | Success = response does NOT contain the failure string |
| **Success string** | Success = response DOES contain the success string |
| **HTTP code** | Success = response matches expected code (e.g. `302`) |
| **Default** | Falls back to HTTP `200` if no method is specified |

---

## ⚙️ Requirements

- **Linux** (any modern distro)
- **No Python installation needed** — runs as a standalone executable
- **Authorised access** to the target system

---

## 🚀 Usage

```bash
./OBreak
```

---

## 📤 Reports

Found credentials are saved automatically to:

```
obreak_reports/obreak_YYYYMMDD_HHMMSS.txt
```

Each report includes the target URL, method, field names, timestamp, elapsed time, total attempts, and all discovered credentials with HTTP status codes and response times.

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
