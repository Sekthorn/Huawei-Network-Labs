# 03 - Interface IP Configuration

## Overview
Configure IP addresses on Ethernet interfaces and Loopback interfaces on Huawei routers and switches.

## Configuration Example
```text
<Huawei> system-view
[Huawei] sysname R1
[R1] interface GigabitEthernet 0/0/0
[R1-GigabitEthernet0/0/0] ip address 192.168.1.1 255.255.255.0
[R1-GigabitEthernet0/0/0] undo shutdown
[R1-GigabitEthernet0/0/0] quit

[R1] interface LoopBack 0
[R1-LoopBack0] ip address 1.1.1.1 255.255.255.255
[R1-LoopBack0] quit
```

## Verification
```text
<R1> display ip interface brief
<R1> display interface GigabitEthernet 0/0/0
```
