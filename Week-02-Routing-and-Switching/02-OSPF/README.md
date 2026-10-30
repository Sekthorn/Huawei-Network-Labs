# 02 - Open Shortest Path First (OSPF)

## Overview
OSPF is an open standard link-state routing protocol using Dijkstra's algorithm to compute loop-free shortest path trees within an autonomous system.

## Basic Single-Area Configuration
```text
<Huawei> system-view
[Huawei] sysname R1

[R1] ospf 1 router-id 1.1.1.1
[R1-ospf-1] area 0
[R1-ospf-1-area-0.0.0.0] network 192.168.1.0 0.0.0.255
[R1-ospf-1-area-0.0.0.0] network 10.1.1.0 0.0.0.3
[R1-ospf-1-area-0.0.0.0] quit
```

## Verification
```text
[R1] display ospf peer brief
[R1] display ospf routing
[R1] display ip routing-table protocol ospf
```
