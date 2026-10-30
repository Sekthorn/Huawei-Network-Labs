# 05 - Spanning Tree Protocol (STP / RSTP / MSTP)

## Overview
Spanning Tree Protocol prevents Layer 2 switching loops and broadcast storms while maintaining network redundancy.

## Supported Modes on Huawei VRP
- **STP (IEEE 802.1D)**: Legacy spanning tree.
- **RSTP (IEEE 802.1w)**: Rapid Spanning Tree Protocol, offering fast convergence.
- **MSTP (IEEE 802.1s)**: Multiple Spanning Tree Protocol, mapping multiple VLANs to spanning tree instances.

## Configuration Example (RSTP)
```text
<Huawei> system-view
[Huawei] sysname SW1

# Set STP mode to RSTP
[SW1] stp mode rstp

# Configure as Root Primary or set priority (multiples of 4096)
[SW1] stp root primary
# Or: [SW1] stp priority 4096

# Configure edge port facing host
[SW1] interface GigabitEthernet 0/0/10
[SW1-GigabitEthernet0/0/10] stp edged-port enable
[SW1-GigabitEthernet0/0/10] quit
```

## Verification
```text
[SW1] display stp brief
[SW1] display stp
```

