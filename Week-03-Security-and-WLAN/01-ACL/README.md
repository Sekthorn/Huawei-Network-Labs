# 01 - Access Control Lists (ACL)

## Overview
Access Control Lists (ACLs) filter traffic based on IP headers, port numbers, and protocols to secure network boundaries.

## ACL Types & Numbering in VRP
- **Basic ACL (2000–2999)**: Matches source IP address only.
- **Advanced ACL (3000–3999)**: Matches source IP, destination IP, protocol (TCP/UDP/ICMP), and port numbers.
- **Layer 2 ACL (4000–4999)**: Matches source MAC, destination MAC, and Ethernet frame types.

## Configuration Example
```text
<Huawei> system-view
[Huawei] acl number 3000
[Huawei-acl-adv-3000] rule 5 permit tcp source 192.168.1.0 0.0.0.255 destination 10.1.1.100 0 destination-eq 80
[Huawei-acl-adv-3000] rule 10 deny ip source any destination any
[Huawei-acl-adv-3000] quit

[Huawei] interface GigabitEthernet 0/0/0
[Huawei-GigabitEthernet0/0/0] traffic-filter inbound acl 3000
[Huawei-GigabitEthernet0/0/0] quit
```

## Verification
```text
[Huawei] display acl 3000
```
