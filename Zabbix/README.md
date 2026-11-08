# Zabbix Labs
### Zabbix 7.0 network monitoring practice labs, each with a fault-injection exercise

Part of the [GNS3 labs repository](../README.md).

---

## Summary

My Zabbix labs. Each lab has the host layout, the symptom of a fault injected on purpose, how I diagnosed and fixed it, and verification with screenshots.

## Lab Environment

| Component | Specification | Purpose |
| :--- | :--- | :--- |
| **Hypervisor** | Proxmox VE, LXC containers | Hosts the lab |
| **Monitoring** | Zabbix server 7.0 (web UI) | Data collection, triggers, alerts |
| **Monitored hosts** | Debian 12, zabbix-agent2 7.0.32 (lab-web, lab-db) | Targets for checks and faults |
| **Alerting** | Telegram bot (Zabbix built-in webhook) | Problem and recovery notifications |

No credentials, bot tokens or chat IDs are stored in this repo.

---

## Labs

### Module 1: Fundamentals

| Lab | Title | Key Technologies | Documentation |
| :---: | :--- | :--- | :---: |
| **1.1** | Troubleshooting Agent Availability (Firewall) | Passive checks (10050), `ss`, `nft list ruleset`, delete by handle | [View Lab](Module%201%20%E2%80%93%20Fundamentals/Lab%201%20%E2%80%93%20Troubleshooting%20Agent%20Availability%20%28Firewall%29/README.md) |
| **1.2** | Trigger and Telegram Alert | `nodata()`, media type, user media, trigger action, Action log | [View Lab](Module%201%20%E2%80%93%20Fundamentals/Lab%202%20%E2%80%93%20Trigger%20and%20Telegram%20Alert/README.md) |

---

## Planned

- **SNMP monitoring** of a Cisco / MikroTik device
- **Dashboard** for the lab hosts
