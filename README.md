# 🔐 FortiGate Site-to-Site IPsec VPN

Complete route-based IPsec VPN configuration between two FortiGate-VM64-KVM firewalls.

## Network Topology
- FW1: 10.10.30.5 (WAN) | 10.10.10.1/24 (LAN)
- FW2: 10.10.30.6 (WAN) | 10.20.0.1/24 (LAN)

## What's Included
- Phase 1 & Phase 2 configurations
- Static routes
- Firewall policies (NAT disabled)
- Ubuntu client routing setup
- Troubleshooting commands

## Quick Apply
```bash
# On FW1
config vpn ipsec phase1-interface
    edit "to-forti-2"
        set interface "port2"
        set remote-gw 10.10.30.6
        set proposal des-md5
    next
end
