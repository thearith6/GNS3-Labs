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
| **SNMP device** | FortiGate VM, FortiOS 8.0.1 (FGT1, GNS3 behind a NAT node) | SNMP v2c polling target |
| **Alerting** | Telegram bot (Zabbix built-in webhook) | Problem and recovery notifications |

No credentials, bot tokens or chat IDs are stored in this repo.

---

## Labs

### Module 1: Fundamentals

| Lab | Title | Key Technologies | Documentation |
| :---: | :--- | :--- | :---: |
| **1.1** | Troubleshooting Agent Availability (Firewall) | Passive checks (10050), `ss`, `nft list ruleset`, delete by handle | [View Lab](Module%201%20%E2%80%93%20Fundamentals/Lab%201%20%E2%80%93%20Troubleshooting%20Agent%20Availability%20%28Firewall%29/README.md) |
| **1.2** | Trigger and Telegram Alert | `nodata()`, media type, user media, trigger action, Action log | [View Lab](Module%201%20%E2%80%93%20Fundamentals/Lab%202%20%E2%80%93%20Trigger%20and%20Telegram%20Alert/README.md) |
| **1.3** | Trigger Fires but Host Is Green (DenyKey) | `DenyKey`, include files, `zabbix_agent2 -t`, item vs. interface availability | [View Lab](Module%201%20%E2%80%93%20Fundamentals/Lab%203%20%E2%80%93%20Trigger%20Fires%20but%20Host%20Is%20Green%20%28DenyKey%29/README.md) |
| **1.4** | Agent Listening Only on Localhost (ListenIP) | `ListenIP`, `ss -tlnp`, `nc -zv` / `/dev/tcp` port tests, alert severity filter | [View Lab](Module%201%20%E2%80%93%20Fundamentals/Lab%204%20%E2%80%93%20Agent%20Listening%20Only%20on%20Localhost%20%28ListenIP%29/README.md) |

### Module 2: SNMP Monitoring

| Lab | Title | Key Technologies | Documentation |
| :---: | :--- | :--- | :---: |
| **2.1** | FortiGate SNMP v2c Host and SNMP-Only Fault | `snmpwalk`, FortiOS SNMP community, `diagnose sniffer packet`, static route, libvirt iptables | [View Lab](Module%202%20%E2%80%93%20SNMP%20Monitoring/Lab%201%20%E2%80%93%20FortiGate%20SNMP%20v2c%20Host/README.md) |

---

## Planned

- **SNMP monitoring** of a Cisco IOSv router
- **Dashboard** for the lab hosts
