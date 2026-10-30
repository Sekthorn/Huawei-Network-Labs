# 04 - Link Aggregation (Eth-Trunk)

## Overview
Link aggregation bundles multiple physical Ethernet links into a logical interface (Eth-Trunk) to increase bandwidth, provide redundancy, and avoid loops.

## Modes
- **Manual Mode**: Physical member interfaces are manually added without running LACP protocol.
- **LACP Mode (Dynamic)**: Uses 802.3ad Link Aggregation Control Protocol for negotiation and active/standby link management.

## Configuration Example (LACP Mode)
```text
<Huawei> system-view
[Huawei] sysname SW1

[SW1] interface Eth-Trunk 1
[SW1-Eth-Trunk1] mode lacp-static
[SW1-Eth-Trunk1] port link-type trunk
[SW1-Eth-Trunk1] port trunk allow-pass vlan 10 20
[SW1-Eth-Trunk1] quit

[SW1] interface GigabitEthernet 0/0/1
[SW1-GigabitEthernet0/0/1] eth-trunk 1
[SW1-GigabitEthernet0/0/1] quit

[SW1] interface GigabitEthernet 0/0/2
[SW1-GigabitEthernet0/0/2] eth-trunk 1
[SW1-GigabitEthernet0/0/2] quit
```

## Verification
```text
[SW1] display eth-trunk 1
```
