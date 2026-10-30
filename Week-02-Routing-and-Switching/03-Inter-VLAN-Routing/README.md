# 03 - Inter-VLAN Routing

## Overview
Inter-VLAN routing enables communication between different VLANs using either Router-on-a-Stick (sub-interfaces) or Layer 3 Switch VLANIF interfaces.

## 1. Router-on-a-Stick (Sub-Interfaces)
```text
<Huawei> system-view
[Huawei] sysname R1
[R1] interface GigabitEthernet 0/0/1.10
[R1-GigabitEthernet0/0/1.10] dot1q termination vid 10
[R1-GigabitEthernet0/0/1.10] ip address 192.168.10.1 255.255.255.0
[R1-GigabitEthernet0/0/1.10] arp broadcast enable
[R1-GigabitEthernet0/0/1.10] quit

[R1] interface GigabitEthernet 0/0/1.20
[R1-GigabitEthernet0/0/1.20] dot1q termination vid 20
[R1-GigabitEthernet0/0/1.20] ip address 192.168.20.1 255.255.255.0
[R1-GigabitEthernet0/0/1.20] arp broadcast enable
[R1-GigabitEthernet0/0/1.20] quit
```

## 2. Layer 3 Switch VLANIF
```text
<Huawei> system-view
[Huawei] sysname L3-SW
[L3-SW] vlan batch 10 20

[L3-SW] interface Vlanif 10
[L3-SW-Vlanif10] ip address 192.168.10.1 24
[L3-SW-Vlanif10] quit

[L3-SW] interface Vlanif 20
[L3-SW-Vlanif20] ip address 192.168.20.1 24
[L3-SW-Vlanif20] quit
```

