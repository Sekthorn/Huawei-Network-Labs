# 04 - Virtual Private Networks (VPN)

## Overview
Virtual Private Networks (VPN) provide secure, encrypted site-to-site and remote access connectivity over untrusted public networks.

## Topics Covered
- **Generic Routing Encapsulation (GRE)**: Encapsulates packet types inside IP tunnels.
- **IPsec VPN**: Provides confidentiality, data integrity, and authentication using IKE and ESP/AH.

## Basic GRE Configuration Example
```text
<Huawei> system-view
[Huawei] sysname R1

[R1] interface Tunnel 0/0/1
[R1-Tunnel0/0/1] tunnel-protocol gre
[R1-Tunnel0/0/1] source 203.0.113.1
[R1-Tunnel0/0/1] destination 203.0.113.2
[R1-Tunnel0/0/1] ip address 10.255.255.1 255.255.255.252
[R1-Tunnel0/0/1] quit

[R1] ip route-static 192.168.20.0 255.255.255.0 Tunnel 0/0/1
```

## Verification
```text
[R1] display interface Tunnel 0/0/1
```
