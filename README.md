# Enterprise Linux & Network HomeLab

## Overview

This repository documents my hands-on enterprise-style HomeLab built to develop practical skills in Linux system administration, networking, security, and cloud infrastructure.

The environment was built using physical Cisco networking equipment, Dell OptiPlex systems, a Raspberry Pi, VMware virtual machines, pfSense, Rocky Linux, and AWS.

The goal of this project was not simply to install technologies, but to configure, test, troubleshoot, and document an environment that reflects many of the technologies and administrative tasks encountered in real IT infrastructure.

---

## HomeLab Architecture

The lab includes:

- Cisco Catalyst 3850 Layer 3 core switch
- Cisco Catalyst 3750 access switch
- pfSense firewall/router
- Dell OptiPlex 3040
- Dell OptiPlex 7040
- Raspberry Pi 5
- Rocky Linux servers
- VMware Workstation virtual machines
- AWS cloud resources

The network is segmented using multiple VLANs for management, servers, clients, storage, DMZ systems, and other infrastructure.

---

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

The Cisco Catalyst 3850 provides Layer 3 routing between VLANs while the Catalyst 3750 operates as an access-layer switch.

802.1Q trunk links carry the required VLANs between network devices.

---

## Projects & Documentation

### Linux User Management Roadmap

A structured Linux administration project focused on managing users, groups, permissions, shared resources, password policies, and administrative privileges on Rocky Linux.

Topics include:

- Linux user creation and lifecycle management
- UID and GID management
- Password aging policies
- Account locking and unlocking
- Primary and supplementary groups
- Shared departmental directories
- Linux file permissions
- setgid directories
- Sticky bit behavior
- Sudo and privilege management
- SSH administration
- Troubleshooting and validation exercises

Each phase includes hands-on configuration, testing, troubleshooting, and documentation.

---

### Enterprise Network Infrastructure

Built and configured a segmented physical network using Cisco Catalyst switches.

Skills demonstrated include:

- VLAN configuration
- 802.1Q trunking
- Switch Virtual Interfaces (SVIs)
- Layer 3 switching
- Inter-VLAN routing
- Access port configuration
- Network segmentation
- Spanning Tree verification
- Routing configuration
- Connectivity troubleshooting

---

### pfSense Firewall & Routing

Configured pfSense as the firewall and routing boundary between the HomeLab and external networks.

Tasks included:

- WAN and LAN configuration
- Firewall rules
- Static routing
- Network segmentation
- Management access
- Connectivity testing
- Troubleshooting routing and firewall policies

---

### Linux Infrastructure

Deployed Rocky Linux systems to practice common Linux administration responsibilities.

Areas of practice include:

- Linux installation and configuration
- SSH administration
- User and group management
- File ownership and permissions
- Service management with systemd
- Network configuration
- Storage and shared resources
- Command-line troubleshooting

---

### AWS Cloud Infrastructure

Extended the lab into AWS to gain hands-on experience with cloud infrastructure concepts.

Areas explored include:

- Amazon EC2
- Virtual Private Cloud (VPC)
- Subnets
- Security groups
- Linux cloud instances
- SSH administration
- IAM concepts
- Cloud networking concepts

---

## Hardware

| Device | Role |
|--------|------|
| Cisco Catalyst 3850 | Layer 3 Core Switch |
| Cisco Catalyst 3750 | Access Switch |
| Dell OptiPlex 3040 | Infrastructure / pfSense |
| Dell OptiPlex 7040 | Server / Virtualization |
| Raspberry Pi 5 | Linux / DMZ Services |

---

## Technologies

**Linux**

Rocky Linux • Bash • SSH • systemd • Linux Permissions • User & Group Administration

**Networking**

Cisco IOS • VLANs • 802.1Q • Layer 3 Switching • Inter-VLAN Routing • TCP/IP • Static Routing • Spanning Tree

**Security**

pfSense • Firewall Rules • Network Segmentation • SSH • Linux Permissions • Sudo

**Virtualization & Cloud**

VMware Workstation • AWS • EC2 • VPC • IAM

---

## Skills Demonstrated

This HomeLab provides hands-on experience with:

- Linux system administration
- User and group administration
- Linux permissions and access control
- Cisco switching and routing
- VLAN design and network segmentation
- Firewall configuration
- TCP/IP networking
- SSH and remote administration
- System troubleshooting
- Virtualization
- Basic AWS infrastructure
- Technical documentation

---

## Project Goal

The purpose of this HomeLab is to build practical experience that complements my technical studies and demonstrates my ability to configure, troubleshoot, and document real systems.

The repository will continue to contain documentation from completed lab exercises and infrastructure projects that demonstrate skills relevant to entry-level Linux System Administrator, IT Infrastructure, Network Support, and IT Support roles.
