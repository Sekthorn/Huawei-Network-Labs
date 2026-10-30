# 06 - Trunk Configuration

## Overview
Trunk links carry traffic for multiple VLANs between switches using IEEE 802.1Q encapsulation tags.

## Basic Configuration
```text
<Huawei> system-view
[Huawei] sysname SW1

[SW1] interface GigabitEthernet 0/0/24
[SW1-GigabitEthernet0/0/24] port link-type trunk
[SW1-GigabitEthernet0/0/24] port trunk allow-pass vlan 10 20
[SW1-GigabitEthernet0/0/24] quit
```

## Verification
```text
[SW1] display port vlan
[SW1] display vlan
```
