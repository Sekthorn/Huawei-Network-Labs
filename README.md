<div align="center">

# 🌐 Huawei Network Labs
### *Learn • Practice • Understand • Share*

An open-source hands-on lab repository crafted to take students and engineers from Huawei networking fundamentals to competition-grade mastery.

[![Huawei VRP](https://img.shields.io/badge/Huawei-VRP%20v5%20%2F%20v8-cf0a2c?style=for-the-badge&logo=huawei&logoColor=white)](https://e.huawei.com)
[![Simulator eNSP](https://img.shields.io/badge/Simulator-Huawei%20eNSP-007ACC?style=for-the-badge&logo=virtualbox&logoColor=white)](Resources/Network-Diagrams/)
[![Roadmap](https://img.shields.io/badge/Curriculum-4%20Weeks-2ea44f?style=for-the-badge)](#-curriculum-roadmap)
[![Competition](https://img.shields.io/badge/Huawei%20ICT-Competition%20Track-E0245E?style=for-the-badge)](Week-04-Competition-Practice/)
[![License: MIT](https://img.shields.io/badge/License-MIT-F5A623?style=for-the-badge)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen?style=for-the-badge)](#-contribution)

<br/>

[📚 Curriculum Roadmap](#-curriculum-roadmap) • 
[📂 Lab Architecture](#-repository-structure) • 
[⚡ Quick Start](#-quick-start-guide) • 
[💡 CLI Cheatsheet](Resources/Huawei-CLI-Cheatsheet/) • 
[📈 Progress Tracker](Progress-Tracker/Learning-Progress.md) • 
[🤝 Contribution](#-contribution)

---

</div>

## 📌 About The Project

Welcome to **Huawei Network Labs**! 

This repository provides an organized, step-by-step practical curriculum inspired by the **Huawei ICT Competition (Network Track)** and the **HCIA-Datacom** certification pathway. Every module includes clear theoretical explanations, copy-pasteable VRP CLI scripts, network topology guidance, and systematic troubleshooting verification.

> [!NOTE]
> Whether you are a university student preparing for the ICT Competition, a CCNA learner transitioning to Huawei VRP, or an aspiring network engineer, this repository is designed to give you hands-on muscle memory in **Huawei eNSP**.

---

## ✨ Key Highlights

- 🎯 **Competition-Grade Syllabus**: Structured into a 4-week progressive bootcamp.
- 💻 **Real VRP CLI Configurations**: Fully tested on Huawei AR series routers and S-series switches.
- 🗺️ **Topology & Subnet Schemes**: Standardized IP addressing schemes and diagrams ready for eNSP.
- 🔬 **Verification & Diagnostics**: Comprehensive `display`, `ping`, and `tracert` step-by-step verification tables.
- ⚡ **Cisco vs. Huawei CLI Equivalents**: Smooth transition guide for CCNA / IOS students.
- 📊 **Self-Paced Progress Tracker**: Dedicated checklist to track your lab completions.

---

## 🗺️ Curriculum Roadmap

```mermaid
flowchart LR
    W1["Week 01<br/><b>Fundamentals & VRP</b>"] --> W2["Week 02<br/><b>Routing & Switching</b>"]
    W2 --> W3["Week 03<br/><b>Security & WLAN</b>"]
    W3 --> W4["Week 04<br/><b>Competition & Mocks</b>"]
    
    style W1 fill:#cf0a2c,stroke:#fff,stroke-width:2px,color:#fff
    style W2 fill:#007acc,stroke:#fff,stroke-width:2px,color:#fff
    style W3 fill:#2ea44f,stroke:#fff,stroke-width:2px,color:#fff
    style W4 fill:#e0245e,stroke:#fff,stroke-width:2px,color:#fff
```

### 🧱 [Week 01: Huawei Fundamentals and VRP](Week-01-Huawei-Fundamentals/)
Focus: Operating system views, command line ergonomics, IP configuration, VLANs, and configuration persistence.

| Lab # | Module | Core Topics | Key CLI Commands |
| :---: | :--- | :--- | :--- |
| **01** | [01-Huawei-VRP-Introduction](Week-01-Huawei-Fundamentals/01-Huawei-VRP-Introduction/) | VRP OS Overview, Boot modes | `system-view`, `quit`, `return` |
| **02** | [02-VRP-CLI-Commands](Week-01-Huawei-Fundamentals/02-VRP-CLI-Commands/) | Navigation, Shortcuts, Help system | `?`, `display current-configuration` |
| **03** | [03-Interface-IP-Configuration](Week-01-Huawei-Fundamentals/03-Interface-IP-Configuration/) | GE & Loopback IP configuration | `ip address`, `undo shutdown` |
| **04** | [04-IPv4-Subnetting](Week-01-Huawei-Fundamentals/04-IPv4-Subnetting/) | Subnet masks, VLSM, CIDR | Subnet calculations & IP design |
| **05** | [05-VLAN-Configuration](Week-01-Huawei-Fundamentals/05-VLAN-Configuration/) | Access ports & broadcast domains | `vlan batch`, `port default vlan` |
| **06** | [06-Trunk-Configuration](Week-01-Huawei-Fundamentals/06-Trunk-Configuration/) | 802.1Q tags & trunk link tagging | `port link-type trunk`, `allow-pass` |
| **07** | [07-Configuration-Backup](Week-01-Huawei-Fundamentals/07-Configuration-Backup/) | Saving, export & restore | `save`, `reset saved-configuration` |

---

### 🔀 [Week 02: Routing and Switching](Week-02-Routing-and-Switching/)
Focus: Dynamic routing, Layer 2 loop-free topologies, link redundancy, and Inter-VLAN routing.

| Lab # | Module | Core Topics | Key CLI Commands |
| :---: | :--- | :--- | :--- |
| **01** | [01-Static-Routing](Week-02-Routing-and-Switching/01-Static-Routing/) | Next-hop, Default & Floating routes | `ip route-static 0.0.0.0 0.0.0.0 <gw>` |
| **02** | [02-OSPF](Week-02-Routing-and-Switching/02-OSPF/) | Single/Multi-Area OSPF & Adjacencies | `ospf 1 router-id`, `network <ip> <wildcard>` |
| **03** | [03-Inter-VLAN-Routing](Week-02-Routing-and-Switching/03-Inter-VLAN-Routing/) | Sub-interfaces (dot1q) & VLANIF | `dot1q termination vid`, `interface Vlanif` |
| **04** | [04-Link-Aggregation](Week-02-Routing-and-Switching/04-Link-Aggregation/) | Eth-Trunk manual & LACP mode | `interface Eth-Trunk`, `mode lacp-static` |
| **05** | [05-STP](Week-02-Routing-and-Switching/05-STP/) | STP / RSTP / MSTP Root & Port roles | `stp mode rstp`, `stp root primary` |
| **06** | [06-Routing-Troubleshooting](Week-02-Routing-and-Switching/06-Routing-Troubleshooting/) | Diagnostic procedures & trace analysis | `display ip routing-table`, `display ospf error` |

---

### 🛡️ [Week 03: Security and WLAN](Week-03-Security-and-WLAN/)
Focus: Traffic filtering, perimeter firewalls, address translation, secure tunnels, and enterprise wireless controller setups.

| Lab # | Module | Core Topics | Key CLI Commands |
| :---: | :--- | :--- | :--- |
| **01** | [01-ACL](Week-03-Security-and-WLAN/01-ACL/) | Basic (2000+) & Advanced (3000+) ACLs | `acl number`, `rule permit/deny`, `traffic-filter` |
| **02** | [02-Firewall-Fundamentals](Week-03-Security-and-WLAN/02-Firewall-Fundamentals/) | USG Security Zones & Interzone policy | `firewall zone trust`, `security-policy` |
| **03** | [03-NAT](Week-03-Security-and-WLAN/03-NAT/) | Easy IP & NAT Server (Port Forwarding) | `nat outbound`, `nat server protocol tcp` |
| **04** | [04-VPN](Week-03-Security-and-WLAN/04-VPN/) | GRE encapsulation & IPsec tunnels | `tunnel-protocol gre`, `source`, `destination` |
| **05** | [05-WLAN-Architecture](Week-03-Security-and-WLAN/05-WLAN-Architecture/) | AC + Fit AP deployment & CAPWAP | `capwap source interface`, `ap-group` |
| **06** | [06-Wireless-Security](Week-03-Security-and-WLAN/06-Wireless-Security/) | SSID Profiles & WPA2-PSK Authentication | `security-profile`, `ssid-profile`, `vap-profile` |
| **07** | [07-Network-Segmentation](Week-03-Security-and-WLAN/07-Network-Segmentation/) | Enterprise isolation & Port Isolation | `port-isolate enable`, `vlan` segmentation |

---

### 🏆 [Week 04: Competition Practice and Mock Exams](Week-04-Competition-Practice/)
Focus: Real competition conditions, time-pressured configurations, broken network troubleshooting, and mock exams.

| Lab # | Module | Description | Goal |
| :---: | :--- | :--- | :--- |
| **01** | [01-Theory-Questions](Week-04-Competition-Practice/01-Theory-Questions/) | High-yield ICT Competition practice questions | Master theoretical concepts |
| **02** | [02-Configuration-Challenges](Week-04-Competition-Practice/02-Configuration-Challenges/) | Timed speed drills for core network services | Build rapid CLI reflexes |
| **03** | [03-Multi-Router-Labs](Week-04-Competition-Practice/03-Multi-Router-Labs/) | Comprehensive multi-tier enterprise topologies | End-to-end integration |
| **04** | [04-Troubleshooting-Challenges](Week-04-Competition-Practice/04-Troubleshooting-Challenges/) | Pre-broken topologies for root cause analysis | Systematic diagnostics |
| **05** | [05-Mock-Examinations](Week-04-Competition-Practice/05-Mock-Examinations/) | Simulated full-length competition exams | Benchmark your skills |
| **06** | [06-Competition-Review](Week-04-Competition-Practice/06-Competition-Review/) | Final strategies, checklist & tips | Exam-day excellence |

---

## 📂 Repository Structure

```text
Huawei-Network-Labs/
│
├── README.md                                  # Main Documentation Hub
├── .gitignore                                 # Git ignore filters
│
├── Progress-Tracker/
│   └── Learning-Progress.md                   # Interactive checklist & study log
│
├── Resources/
│   ├── Huawei-CLI-Cheatsheet/                 # Fast command lookup tables
│   ├── Network-Diagrams/                      # Topology blueprints & sketches
│   └── IP-Addressing-Tables/                  # Addressing scheme templates
│
├── Week-01-Huawei-Fundamentals/               # Week 1: VRP, CLI, VLANs, Backups
│   ├── 01-Huawei-VRP-Introduction/
│   ├── 02-VRP-CLI-Commands/
│   ├── 03-Interface-IP-Configuration/
│   ├── 04-IPv4-Subnetting/
│   ├── 05-VLAN-Configuration/
│   ├── 06-Trunk-Configuration/
│   └── 07-Configuration-Backup/
│
├── Week-02-Routing-and-Switching/             # Week 2: OSPF, Inter-VLAN, STP, LACP
│   ├── 01-Static-Routing/
│   ├── 02-OSPF/
│   ├── 03-Inter-VLAN-Routing/
│   ├── 04-Link-Aggregation/
│   ├── 05-STP/
│   └── 06-Routing-Troubleshooting/
│
├── Week-03-Security-and-WLAN/                 # Week 3: ACL, Firewall, NAT, VPN, WLAN
│   ├── 01-ACL/
│   ├── 02-Firewall-Fundamentals/
│   ├── 03-NAT/
│   ├── 04-VPN/
│   ├── 05-WLAN-Architecture/
│   ├── 06-Wireless-Security/
│   └── 07-Network-Segmentation/
│
└── Week-04-Competition-Practice/              # Week 4: Speed Drills, Mocks, Review
    ├── 01-Theory-Questions/
    ├── 02-Configuration-Challenges/
    ├── 03-Multi-Router-Labs/
    ├── 04-Troubleshooting-Challenges/
    ├── 05-Mock-Examinations/
    └── 06-Competition-Review/
```

---

## ⚡ Quick Start Guide

### 1. Prerequisites
- **Huawei eNSP** (Enterprise Network Simulation Platform) v1.3.00 or later
- **VirtualBox** (v5.2.x recommended for eNSP compatibility)
- **Wireshark** & **WinPcap**

### 2. Clone the Repository
```bash
git clone https://github.com/Sekthorn/Huawei-Network-Labs.git
cd Huawei-Network-Labs
```

### 3. Running a Lab
1. Navigate to the desired week and module folder (e.g., `Week-02-Routing-and-Switching/02-OSPF/`).
2. Review the lab objectives, topology diagram, and IP addressing table.
3. Open **eNSP**, lay out the designated devices, and start all devices.
4. Copy and paste or manually enter the VRP CLI commands.
5. Execute the verification commands (`display ...`) to validate the state of the network.

---

## 🔄 Quick Transition: Cisco IOS vs. Huawei VRP

If you have a Cisco CCNA background, this quick reference bridges the syntax gap immediately:

| Operation | Cisco IOS | Huawei VRP |
| :--- | :--- | :--- |
| **Enter Configuration Mode** | `enable` &rarr; `configure terminal` | `system-view` (or `sys`) |
| **Exit Current Mode** | `exit` | `quit` (or `q`) |
| **Return to Top Level** | `end` (or `Ctrl+Z`) | `return` (or `Ctrl+Z`) |
| **View Running Config** | `show running-config` | `display current-configuration` |
| **View Interface Status** | `show ip interface brief` | `display ip interface brief` |
| **View Routing Table** | `show ip route` | `display ip routing-table` |
| **Save Configuration** | `write memory` or `copy run start` | `save` |
| **Negate a Command** | `no ip address ...` | `undo ip address ...` |
| **Assign Device Name** | `hostname R1` | `sysname R1` |

---

## 🎯 Who Is This For?

<div align="center">

| 🎓 University Students | 🏆 Competition Participants | 📜 Certification Candidates | 💼 Network Engineers |
| :---: | :---: | :---: | :---: |
| Hands-on coursework support & practical networking labs | Targeted practice for Huawei ICT Competition Network Track | Fast preparation for HCIA / HCIP Datacom exams | Practical VRP syntax reference and enterprise topologies |

</div>

---

## 📈 Tracking Your Progress

Don't study blindly! Use our built-in progress tracker:

👉 **[Open Learning-Progress.md](Progress-Tracker/Learning-Progress.md)**

Mark off completed labs, record execution times for configuration speed drills, and note key troubleshooting lessons learned.

---

## 🤝 Contribution & Community

Contributions are what make the open-source community an amazing place to learn, inspire, and create:

1. **Fork** the Project
2. **Create** your Feature Branch (`git checkout -b feature/NewLabTopology`)
3. **Commit** your Changes (`git commit -m 'Add: New BGP Lab in Week 04'`)
4. **Push** to the Branch (`git push origin feature/NewLabTopology`)
5. **Open** a Pull Request

Found a typo or an incorrect CLI command? Feel free to open an **[Issue](https://github.com/Sekthorn/Huawei-Network-Labs/issues)**!

---

<div align="center">

### ⭐ If you find this repository helpful, please consider giving it a Star! ⭐

**Let's learn networking together!**

</div>
