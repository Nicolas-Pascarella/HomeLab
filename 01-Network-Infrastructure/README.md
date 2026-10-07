# Network Infrastructure

This section documents the physical and logical network infrastructure used in my HomeLab.

The environment uses Cisco Catalyst switching to provide VLAN segmentation, Layer 2 connectivity, and Layer 3 routing between network segments.

## Core Technologies

- Cisco Catalyst 3850 Layer 3 core switch
- Cisco Catalyst 3750 access switch
- Cisco IOS / IOS XE
- VLANs
- 802.1Q trunking
- Switch Virtual Interfaces (SVIs)
- Inter-VLAN routing
- Spanning Tree Protocol
- Static routing
- Ethernet access ports
- TCP/IP networking

## Network Segmentation

| VLAN | Purpose |
|------|---------|
| 10 | Management |
| 20 | Servers |
| 30 | Clients |
| 40 | Storage |
| 50 | DMZ |
| 60 | Additional Services |
| 99 | Native VLAN |

## Skills Demonstrated

- Configuring and verifying VLANs
- Configuring access and trunk ports
- Managing allowed VLANs across trunk links
- Configuring Layer 3 SVIs
- Implementing inter-VLAN routing
- Verifying Spanning Tree operation
- Configuring management connectivity
- Troubleshooting Layer 2 and Layer 3 connectivity
- Using Cisco IOS verification and troubleshooting commands

## Documentation

Additional configuration examples, diagrams, validation results, and troubleshooting documentation will be added to this section as the HomeLab portfolio is organized.
