# 02 - Firewall Fundamentals

## Overview
Learn Huawei USG series firewall fundamentals, security zones, and security policy configuration.

## Key Concepts
- **Default Security Zones**:
  - `Trust` (Priority 85)
  - `DMZ` (Priority 50)
  - `Untrust` (Priority 5)
  - `Local` (Priority 100)
- **Security Policy**: Controls traffic between zones based on source/destination IP, service, and action (permit/deny).

## Configuration Example
```text
<USG> system-view
[USG] firewall zone trust
[USG-zone-trust] add interface GigabitEthernet 1/0/1
[USG-zone-trust] quit

[USG] firewall zone untrust
[USG-zone-untrust] add interface GigabitEthernet 1/0/0
[USG-zone-untrust] quit

[USG] security-policy
[USG-policy-security] default action deny
[USG-policy-security] rule name trust_to_untrust
[USG-policy-security-rule-trust_to_untrust] source-zone trust
[USG-policy-security-rule-trust_to_untrust] destination-zone untrust
[USG-policy-security-rule-trust_to_untrust] action permit
[USG-policy-security-rule-trust_to_untrust] quit
```

