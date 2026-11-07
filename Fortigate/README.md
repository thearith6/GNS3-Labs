# FortiGate Labs
### FortiGate (FortiOS) practice labs in GNS3, each with a fault-injection exercise

Part of the [GNS3 labs repository](../README.md).

---

## Summary

My FortiGate labs, built and tested in GNS3. Each lab has the topology, the FortiOS config with its addressing plan, verification output with screenshots, and a "Break-It" exercise: something I broke on purpose, the symptom it caused, and how I fixed it.

## Lab Environment

| Component | Specification | Purpose |
| :--- | :--- | :--- |
| **Network Emulator** | GNS3 Server / Client v3.1 | Topology |
| **Firewall** | FortiGate-VM (QEMU), FortiOS 7.4.7 / 8.0.1 | Policies, NAT, VPN, security profiles |
| **Switching / Routing** | Cisco IOL (L2 / L3) | Devices around the firewall |
| **End Systems** | VPCS, Alpine Linux (`alpine-ssh:latest`) | Connectivity and service tests |

FortiGate images and licenses are not included in this repo.

---

## Labs

### Module 1: Fundamentals

| Lab | Title | Key Technologies | Documentation |
| :---: | :--- | :--- | :---: |
| **1.1** | Interfaces, Static Routing & Firewall Policy _(draft)_ | Interfaces, static default route, firewall policy, source NAT | [View Lab](Module%201%20%E2%80%93%20Fundamentals/Lab%201%20%E2%80%93%20Interfaces%2C%20Static%20Routing%20and%20Firewall%20Policy/README.md) |
| **1.2** | Troubleshooting an Expired One-Time Schedule | Address objects & groups, custom services & groups, one-time schedules | [View Lab](Module%201%20%E2%80%93%20Fundamentals/Lab%202%20%E2%80%93%20Address%20Objects%2C%20Service%20Objects%20and%20Schedules/README.md) |

---

## Planned

- **Module 1: Fundamentals** (SNAT and VIPs)
- **Module 2: Security profiles** (web filter, application control, antivirus, SSL inspection)
- **Module 3: VPN** (IPsec site-to-site, SSL VPN / ZTNA)
- **Module 4: Routing & HA** (OSPF, BGP, SD-WAN, FGCP HA)
- **Module 5: Management & logging** (admin profiles, syslog, SNMP, FortiAnalyzer)
