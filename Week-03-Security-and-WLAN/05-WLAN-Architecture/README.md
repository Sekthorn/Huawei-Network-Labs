# 05 - WLAN Architecture

## Overview
Learn Huawei Enterprise WLAN architecture, including Access Controller (AC) and Fit Access Point (Fit AP) deployments with CAPWAP tunnels.

## Key Concepts
- **Fat AP vs. Fit AP**: Standalone vs. centralized management.
- **CAPWAP (Control And Provisioning of Wireless Access Points)**: Control tunnel (UDP 5246) and data tunnel (UDP 5247).
- **Forwarding Modes**: Direct forwarding (local switching) vs. Tunnel forwarding (centralized at AC).

## Configuration Highlights
```text
<AC> system-view
[AC] capwap source interface Vlanif 100
[AC] wlan
[AC-wlan-view] ap-group name default
[AC-wlan-view] ap-id 0 ap-mac 00e0-fc01-2345
[AC-wlan-ap-0] ap-name Office-AP1
[AC-wlan-ap-0] ap-group default
```
