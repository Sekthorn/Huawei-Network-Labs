# 06 - Wireless Security

## Overview
Configure wireless authentication and encryption schemes (WPA2-PSK / WPA3 / 802.1X) to protect enterprise wireless networks.

## Configuration Example
```text
<AC> system-view
[AC] wlan

# Security Profile
[AC-wlan-view] security-profile name sec-corp
[AC-wlan-sec-prof-sec-corp] security wpa2 psk pass-phrase Huawei@123 aes
[AC-wlan-sec-prof-sec-corp] quit

# SSID Profile
[AC-wlan-view] ssid-profile name ssid-corp
[AC-wlan-ssid-prof-ssid-corp] ssid Huawei-Corp
[AC-wlan-ssid-prof-ssid-corp] quit

# VAP Profile
[AC-wlan-view] vap-profile name vap-corp
[AC-wlan-vap-prof-vap-corp] service-vlan vlan-id 10
[AC-wlan-vap-prof-vap-corp] ssid-profile ssid-corp
[AC-wlan-vap-prof-vap-corp] security-profile sec-corp
[AC-wlan-vap-prof-vap-corp] quit
```
