# 01 - Static Routing

## Overview
Static routing allows network administrators to manually define paths to destination networks.

## Basic Configuration
```text
<Huawei> system-view
[Huawei] sysname R1

# ip route-static <destination-ip> <mask> <next-hop-ip> [preference <value>]
[R1] ip route-static 192.168.2.0 255.255.255.0 10.1.1.2

# Default Route
[R1] ip route-static 0.0.0.0 0.0.0.0 10.1.1.2
```

## Verification
```text
[R1] display ip routing-table
[R1] display ip routing-table protocol static
```
