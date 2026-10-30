# 05 - VLAN Configuration

## Overview
Virtual Local Area Networks (VLANs) divide physical switches into multiple logical broadcast domains to improve network security, manageability, and performance.

## Basic Configuration
```text
<Huawei> system-view
[Huawei] sysname SW1
[SW1] vlan batch 10 20

[SW1] interface GigabitEthernet 0/0/1
[SW1-GigabitEthernet0/0/1] port link-type access
[SW1-GigabitEthernet0/0/1] port default vlan 10
[SW1-GigabitEthernet0/0/1] quit
```

## Verification
```text
[SW1] display vlan
[SW1] display port vlan
```
