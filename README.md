# Enterprise Linux & Network HomeLab

## Overview

This repository documents my hands-on HomeLab built to develop practical skills in Linux system administration, networking, security, virtualization, and cloud infrastructure.

The environment combines physical Cisco networking equipment, pfSense, Rocky Linux, VMware Workstation, Dell OptiPlex systems, a Raspberry Pi, and AWS resources.

The goal of the HomeLab is to gain practical experience by configuring, testing, troubleshooting, securing, and documenting infrastructure rather than relying only on theoretical study.

---

## HomeLab Architecture

The environment includes:

- Cisco Catalyst 3850 Layer 3 core switch
- Cisco Catalyst 3750 access switch
- pfSense firewall/router
- Dell OptiPlex 3040
- Dell OptiPlex 7040
- Raspberry Pi 5
- Rocky Linux virtual machines
- VMware Workstation
- AWS cloud resources

The Cisco Catalyst 3850 provides Layer 3 routing for internal networks, while the Catalyst 3750 provides access-layer switching.

pfSense operates as the firewall and upstream routing boundary for the HomeLab.

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

The network uses VLAN segmentation to separate infrastructure based on function.

802.1Q trunks transport the required VLANs between switches, while Switch Virtual Interfaces (SVIs) on the Cisco Catalyst 3850 provide Layer 3 connectivity between VLANs.

Traffic between network segments can be controlled using Layer 3 access control policies.

---

# Projects & Documentation

The following sections contain configuration details, troubleshooting notes, and verification evidence from the HomeLab.

## 01 — Enterprise Network Infrastructure

[View Network Infrastructure Documentation](01-Network-Infrastructure/README.md)

Built and configured a segmented physical network using Cisco Catalyst switches.

### Skills Demonstrated

- VLAN configuration
- 802.1Q trunking
- Access and trunk ports
- Switch Virtual Interfaces (SVIs)
- Layer 3 switching
- Inter-VLAN routing
- Static and default routing
- Extended access control lists
- Network segmentation
- Spanning Tree verification
- Cisco IOS troubleshooting
- Connectivity validation

The documentation includes Cisco command output verifying trunk operation, Layer 3 routing, and VLAN access-control policies.

---

## 02 — pfSense Firewall & Routing

[View pfSense Firewall Documentation](02-pfSense-Firewall/README.md)

Configured pfSense as the firewall and routing boundary between the internal HomeLab infrastructure and the upstream network.

### Skills Demonstrated

- WAN and LAN interface configuration
- IPv4 addressing and subnetting
- `/30` routed transit networking
- Static routing
- Default routing
- Firewall policy
- Management access
- Cisco-to-pfSense integration
- Connectivity troubleshooting
- Routing validation

The Cisco Catalyst 3850 and pfSense are connected through the `10.255.255.0/30` transit network.

The documentation includes verification of pfSense interface addressing and static routes to the internal VLAN networks.

---

## 03 — Linux User Management Roadmap

[View Linux User Management Documentation](03-Linux-User-Management/README.md)

A structured Rocky Linux administration project focused on identity, permissions, access control, and least-privilege administration.

The project progresses through six completed phases:

### Phase 1 — User Account Administration

- User creation and deletion
- UID and GID management
- Password configuration
- Password-aging policies
- Account locking and unlocking
- Account lifecycle management

### Phase 2 — Groups & Membership

- Primary and supplementary groups
- Department groups
- Group membership management
- Group renaming
- GID persistence
- Group troubleshooting

### Phase 3 — Shared Team Directories

- Departmental shared resources
- Group ownership
- setgid directories
- Sticky bit behavior
- Permission inheritance
- Collaborative access

### Phase 4 — Linux File Permissions

- Symbolic and octal permissions
- File and directory permissions
- `chmod`, `chown`, and `chgrp`
- Sensitive-file protection
- Executable permissions
- Least-privilege filesystem design

### Phase 5 — POSIX ACLs

- Named-user ACLs
- Named-group ACLs
- ACL masks
- Default ACLs
- ACL inheritance
- Cross-team access control

### Phase 6 — Sudo & Delegated Administration

- `/etc/sudoers.d`
- `visudo`
- Command-specific sudo delegation
- Administrative groups
- Allowed and denied command testing
- Least-privilege administrative access

### Phase 7 — Final Enterprise Challenge

**Status: Planned**

The Linux documentation includes terminal-based verification for each completed phase, including account configuration, group membership, shared directories, permissions, ACLs, and sudo authorization testing.

---

## AWS Cloud Infrastructure

The HomeLab was also extended into AWS to gain introductory hands-on experience with cloud infrastructure concepts.

Areas explored include:

- Amazon EC2
- Virtual Private Cloud (VPC)
- Subnets
- Security groups
- Linux cloud instances
- SSH administration
- IAM concepts
- Cloud networking concepts

AWS is included as a supporting component of the overall infrastructure lab while the primary focus of this repository remains Linux administration and networking.

---

# Hardware

| Device | Role |
|--------|------|
| Cisco Catalyst 3850 | Layer 3 Core Switch |
| Cisco Catalyst 3750 | Access Switch |
| Dell OptiPlex 3040 | Infrastructure / pfSense |
| Dell OptiPlex 7040 | Server / Virtualization |
| Raspberry Pi 5 | Linux / DMZ Services |

---

# Technologies

### Linux

Rocky Linux • Bash • SSH • systemd • Linux Permissions • POSIX ACLs • Sudo • User & Group Administration

### Networking

Cisco IOS / IOS XE • VLANs • 802.1Q • SVIs • Layer 3 Switching • Inter-VLAN Routing • TCP/IP • Static Routing • Spanning Tree • ACLs

### Security

pfSense • Firewall Rules • Network Segmentation • Cisco ACLs • SSH • Linux Permissions • POSIX ACLs • Least-Privilege Sudo

### Virtualization & Cloud

VMware Workstation • AWS • EC2 • VPC • IAM

---

# Skills Demonstrated

This HomeLab provides hands-on experience with:

- Linux system administration
- User and group administration
- Password and account policies
- Linux permissions and access control
- POSIX ACL administration
- Sudo and least-privilege delegation
- SSH and remote administration
- Cisco switching and routing
- VLAN design and network segmentation
- Inter-VLAN routing
- Network access control
- Firewall configuration
- Static and default routing
- TCP/IP networking
- System and network troubleshooting
- Virtualization
- Basic AWS infrastructure
- Technical documentation
- Configuration testing and validation

---

# Troubleshooting & Validation

Configuration changes throughout the HomeLab are tested and verified rather than assumed to be successful.

Examples include:

- Verifying Cisco trunks and allowed VLANs
- Inspecting Layer 3 routing tables
- Testing inter-VLAN connectivity
- Validating network ACL behavior
- Verifying pfSense interfaces and static routes
- Inspecting Linux user and group databases
- Validating password-aging policies
- Testing filesystem permissions
- Inspecting POSIX ACLs
- Testing authorized and unauthorized sudo commands
- Verifying Linux service state

Troubleshooting results and final-state verification are documented alongside the relevant configurations.

---

# Project Goal

The purpose of this HomeLab is to build practical experience that complements my technical studies and demonstrates my ability to configure, secure, troubleshoot, verify, and document real systems.

The repository is designed to demonstrate skills relevant to entry-level roles including:

- Linux System Administration
- IT Infrastructure
- Network Support
- Systems Support
- Technical Support

The HomeLab will continue to serve as a controlled environment for developing and validating new infrastructure skills.
