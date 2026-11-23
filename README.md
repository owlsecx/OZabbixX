# 🦉 OZabbixX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OZabbixX** — Monitoring-Agent Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview


OZabbixX is an offline, read-only Zabbix server/proxy/agent configuration auditor that parses zabbix_server.conf, zabbix_proxy.conf and agent configs with stdlib-only parsers. It evaluates database credential exposure, encryption (PSK/cert TLSConnect/TLSAccept), remote-command and unsafe-parameter exposure, and management interface binding. Secrets are masked, findings are mapped to CWE and MITRE ATT&CK, and reports export to TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- Parsers for zabbix_server.conf, zabbix_proxy.conf and zabbix_agentd/agent2 configs
- Database credential exposure (DBPassword masked) and DB-host/socket hardening checks
- Encryption review: TLSConnect/TLSAccept, PSK vs cert, TLS PSK file permissions
- Remote-command execution risk (EnableRemoteCommands, AllowKey/DenyKey, UnsafeUserParameters)
- Management/listener exposure (ListenIP 0.0.0.0, Server/ServerActive trust) checks
- Secrets masked, CWE+ATT&CK mapping and TXT/MD/JSON/CSV/SARIF export with --fail-on gating

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OZabbixX --scan -f sarif -o zabbix.sarif
./OZabbixX --server /etc/zabbix/zabbix_server.conf --agent /etc/zabbix/zabbix_agentd.conf
./OZabbixX -r /mnt/image --fail-on high --json
./OZabbixX --demo
./OZabbixX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*
