# IP Addressing Schemes & Subnet Tables

## Overview
Reference tables and IP address planning templates for enterprise network topologies and competition challenges.

## Standard Lab Addressing Template
| Device | Interface | IP Address | Subnet Mask | Default Gateway | Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| R1 | GE0/0/0 | 192.168.1.1 | 255.255.255.0 | N/A | LAN Gateway |
| R1 | GE0/0/1 | 10.1.1.1 | 255.255.255.252 | N/A | WAN to R2 |
| R2 | GE0/0/1 | 10.1.1.2 | 255.255.255.252 | N/A | WAN to R1 |
| SW1 | Vlanif 10 | 192.168.10.1 | 255.255.255.0 | N/A | Management / Gateway |
| PC1 | NIC | 192.168.10.10 | 255.255.255.0 | 192.168.10.1 | Client Host |
