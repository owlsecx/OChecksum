# 🦉 OChecksum

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-Security-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OChecksum** — part of the OwlSec Toolkit.

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OChecksum handles file hashing and integrity checks in one tool. It hashes files and whole directory trees in parallel, writes manifests that work with sha256sum -c, and verifies them later to catch modified, missing or new files. It also compares files and directories, finds duplicate files and identifies unknown hashes.

---

## ✨ Features

- 20 algorithms: MD5, SHA-1, SHA-2, SHA-3, CRC-32/32C/64, Adler-32 and FNV-1a 32/64/128
- Parallel hashing with live progress and throughput
- Manifests in GNU *sum, BSD tagged, SFV and JSON format; verify auto-detects the format and flags new files
- Checks a file against a pasted hash (constant-time) and compares files or whole directories (modified / added / removed / renamed)
- Duplicate finder with a wasted-space report
- HMAC, hash-type identifier (hex, crypt, LDAP, SRI) and algorithm benchmark; sha256sum-style CLI for scripts and CI

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OChecksum                                  # interactive menu
./OChecksum --algo sha256 file1 file2
./OChecksum --create ./release -o SHA256SUMS
./OChecksum --verify SHA256SUMS --new
./OChecksum --dupes ~/Downloads
```

Run `./OChecksum --help` for the full list of options.

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
