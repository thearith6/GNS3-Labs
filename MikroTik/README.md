# MikroTik Labs
### MikroTik RouterOS (CHR) practice labs in GNS3, each with a fault-injection exercise

Part of the [GNS3 labs repository](../README.md).

---

## Summary

My MikroTik labs, built and tested in GNS3 on Cloud Hosted Router (CHR). Each lab has the topology, the RouterOS config with its addressing plan, verification output with screenshots, and a "Break-It" exercise: a fault injected on purpose, the symptom it caused, and how I found and fixed it.

## Lab Environment

| Component | Specification | Purpose |
| :--- | :--- | :--- |
| **Network Emulator** | GNS3 Server / Client v3.1 | Topology |
| **Router** | MikroTik CHR (QEMU), RouterOS 7.22.1 (`chr-7.22.1.img`), 1 vCPU / 384 MB | Interfaces, routing, NAT, firewall |
| **End Systems** | VPCS | Host IP and reachability tests |

CHR images are not included in this repo. Download them from mikrotik.com.

---

## Labs

### Module 1: Fundamentals

| Lab | Title | Key Technologies | Documentation |
| :---: | :--- | :--- | :---: |
| **1.1** | Troubleshooting IP Addressing & Static Routing | `/ip address`, `/ip route`, route flags (`A` / `I`), VPCS testing | [View Lab](Module%201%20%E2%80%93%20Fundamentals/Lab%201%20%E2%80%93%20Troubleshooting%20IP%20Addressing%20and%20Static%20Routing/README.md) |
| **1.2** | Troubleshooting Source NAT (Masquerade) | `srcnat` masquerade, `out-interface`, `print stats`, `/tool sniffer` | [View Lab](Module%201%20%E2%80%93%20Fundamentals/Lab%202%20%E2%80%93%20Troubleshooting%20Source%20NAT%20and%20Firewall%20Filter/README.md) |

---

## Planned

- **Module 2: Switching** (bridge, VLAN filtering)
- **Module 3: Routing** (OSPF, BGP)
- **Module 4: VPN** (WireGuard, IPsec)
