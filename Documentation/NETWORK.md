# Network

## The networks at Acme Inc.

- 192.0.2.0/24 LAN VLAN-1
- 198.51.100.0/24 Internet Provider VLAN-1 WAN
- 203.0.113.0/24 VOIP VLAN-15
- 2001:DB8::2:1/64 LAN VLAN-1
- 2001:DB8::3:1/64 VOIP VLAN-15
- 2001:DB8::4:1/64 ADMIN VLAN-42

## The network devices at Acme Inc.

- Network services may be listed in SYSTEMS.txt
- router: superrouter.acme.example.com 192.0.2.1, 2001:DB8::1:1
  - Make: MegaRouters
  - Model: 2000XL
  - Config: Git
  - Firmware: 1234
  - OOBM: ssh://192.0.2.3:3001
  - Last Audit: 2025-04-18

## Common Services

- Internal
  - DNS 192.0.2.10, 192.0.2.20, 2001:DB8::1:10, 2001:DB8::1:20
  - NTP 192.0.2.15, 2001:DB8::1:15

## Resources

- rfc5737
- rfc3849
