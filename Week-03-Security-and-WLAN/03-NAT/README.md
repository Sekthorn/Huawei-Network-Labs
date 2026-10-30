# 03 - Network Address Translation (NAT)

## Overview
NAT maps private IPv4 addresses to public IPv4 addresses, conserving public IP addresses and concealing internal topologies.

## Key Types
1. **Easy IP (PAT using interface IP)**: Ideal for dynamic dial-up or single public IP scenarios.
2. **NAT Server (Port Forwarding)**: Exposes internal servers to the public Internet.
3. **NAT Address Pool (NAPT)**: Uses a pool of public IP addresses for translation.

## Configuration Example (Easy IP)
```text
<Huawei> system-view
[Huawei] acl number 2000
[Huawei-acl-basic-2000] rule 5 permit source 192.168.1.0 0.0.0.255
[Huawei-acl-basic-2000] quit

[Huawei] interface GigabitEthernet 0/0/0
[Huawei-GigabitEthernet0/0/0] nat outbound 2000
[Huawei-GigabitEthernet0/0/0] quit
```

## NAT Server (Port Forwarding Example)
```text
[Huawei-GigabitEthernet0/0/0] nat server protocol tcp global current-interface 80 inside 192.168.1.100 80
```

## Verification
```text
<Huawei> display nat session all
<Huawei> display nat outbound
```

