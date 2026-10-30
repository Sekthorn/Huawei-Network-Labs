# Huawei VRP CLI Quick Cheatsheet

A handy quick reference for the most commonly used commands across Huawei VRP routers and switches.

---

### System Navigation
| Command | Description |
| :--- | :--- |
| `system-view` (`sys`) | Enter system configuration view |
| `quit` (`q`) | Go back one hierarchy level |
| `return` (or `Ctrl+Z`) | Return directly to user view |
| `display current-configuration` (`dis cur`) | View running configuration |
| `display interface brief` | View brief status of all interfaces |
| `save` | Save configuration to flash storage |
| `reboot` | Reboot the device |

---

### Basic Device Setup
```text
sysname <Device-Name>
header login information "Authorized Access Only"
clock timezone UTC add 07:00:00
```

---

### Interface & IP
```text
interface GigabitEthernet 0/0/0
 ip address 192.168.1.1 24
 undo shutdown
quit
```

---

### VLANs & Switching
```text
vlan batch 10 20 30

interface GigabitEthernet 0/0/1
 port link-type access
 port default vlan 10

interface GigabitEthernet 0/0/24
 port link-type trunk
 port trunk allow-pass vlan 10 20 30
```

---

### Static Routing & OSPF
```text
# Static Route
ip route-static 0.0.0.0 0.0.0.0 10.1.1.2

# OSPF
ospf 1 router-id 1.1.1.1
 area 0
  network 192.168.1.0 0.0.0.255
  network 10.1.1.0 0.0.0.3
```

---

### Useful Display & Verification Commands
- `display ip interface brief`
- `display ip routing-table`
- `display vlan`
- `display stp brief`
- `display ospf peer brief`
- `display acl all`
- `display nat session all`
