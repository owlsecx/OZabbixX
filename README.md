# 🦉 OZabbixX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OZabbixX** — Monitoring-Agent Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline monitoring-agent configuration auditor (Zabbix / NRPE / Icinga2 / Netdata)

---

## ✨ Features

- Zabbix agent / agent2 — EnableRemoteCommands, AllowKey system.run[*], UnsafeUserParameters, UserParameter $1 shell injection, Server ACL width, TLSAccept/TLSConnect, PSK strength (masked), AllowRoot, LogRemoteCommands
- Zabbix server / proxy — DBPassword (masked), DB TLS, proxy TLS, AlertScriptsPath / ExternalScripts perms, StatsAllowedIP, EnableGlobalScripts, Vault tokens
- Zabbix frontend zabbix.conf.php — DB creds, DB TLS, default Admin / zabbix credential reminder
- NRPE — dont_blame_nrpe, bash command substitution, allowed_hosts, ADH / no-SSL, $ARGn$ commands, root, sudo
- Icinga2 — ApiUser permissions [*] / console, default passwords, accept_commands / accept_config, TicketSalt
- Netdata — bind to *, allow-from ACLs, management API, registry, streaming API keys, run-as root, TLS
- CWE + MITRE ATT&CK mapping, score / grade, --root discovery
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OZabbixX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
