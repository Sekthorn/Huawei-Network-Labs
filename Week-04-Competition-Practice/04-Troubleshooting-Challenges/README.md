# 04 - Troubleshooting Challenges

## Overview
Broken lab topologies provided as challenge files. Your task is to diagnose the fault, determine root cause, and restore proper connectivity without resetting or wiping configurations.

## Common Competition Fault Scenarios
- Subnet mask mismatch on point-to-point router links
- OSPF Hello/Dead interval or Area ID mismatch
- Missing `arp broadcast enable` on router sub-interfaces (dot1q)
- Trunk `allow-pass vlan` omitting necessary transit VLANs
- ACL rule numbering / default implicit deny blocking legitimate traffic
- NAT outbound ACL matching improper source subnets

