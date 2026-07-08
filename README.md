# Enterprise Network Design & Implementation

![Cisco Packet Tracer](https://img.shields.io/badge/Cisco-Packet%20Tracer-1BA0D7?style=for-the-badge)
![Enterprise Networking](https://img.shields.io/badge/Enterprise-Networking-blue?style=for-the-badge)
![Network Security](https://img.shields.io/badge/Network-Security-red?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

## Project Overview

This repository presents the design, implementation and validation of a secure enterprise network for **EmboArts**, a fictional creative agency used to simulate the networking requirements of a modern medium-sized business.

The network was implemented in **Cisco Packet Tracer** and follows enterprise networking principles including hierarchical design, VLAN segmentation, Layer 3 routing, DHCP, NAT/PAT, secure management, wireless guest access and layered security controls.

The objective was to build a network that is:

- Secure
- Scalable
- Maintainable
- Well documented
- Suitable for enterprise-style infrastructure scenarios

---

## Project Highlights

| Area | Implementation |
|---|---|
| Network Type | Enterprise campus-style network |
| VLANs | 6 VLANs |
| Routing | Layer 3 Inter-VLAN Routing |
| Addressing | IPv4 /24 networks per VLAN |
| DHCP | Centralised DHCP pools |
| Internet Access | NAT/PAT |
| Public Services | Static NAT for DMZ web and email servers |
| Wireless | WPA2 guest wireless network |
| Security | SSH, Port Security, DHCP Snooping, ACL design |
| Testing | 43 functional test scenarios |
| Overall Test Success | 84% |
| Critical Services | 100% success |

---

## Enterprise Architecture

The network uses a hierarchical enterprise design with a Layer 3 core switch, three access switches, an edge router, a simulated ISP router, a DMZ network and a guest wireless network.

![Enterprise Topology](diagrams/enterprise-topology.png)

---

## VLAN Architecture

The network is segmented into six VLANs to separate departments, reduce broadcast traffic and improve security.

![VLAN Architecture](diagrams/vlan-architecture.png)

| VLAN | Department / Function | Network | Gateway |
|---:|---|---|---|
| 10 | Management | 192.168.10.0/24 | 192.168.10.1 |
| 20 | IT Operations | 192.168.20.0/24 | 192.168.20.1 |
| 30 | Finance | 192.168.30.0/24 | 192.168.30.1 |
| 40 | Sales | 192.168.40.0/24 | 192.168.40.1 |
| 99 | DMZ | 192.168.99.0/24 | 192.168.99.1 |
| 100 | Guest Wireless | 192.168.100.0/24 | 192.168.100.1 |

---

## Security Zones

The design separates internal users, public-facing services, guest wireless clients and external internet traffic into distinct security zones.

![Security Zones](diagrams/security-zones.png)

Security features include:

- VLAN segmentation
- SSH-only management access
- Encrypted passwords
- Port Security
- DHCP Snooping
- Guest network isolation
- DMZ separation
- ACL design
- NAT address hiding

---

## Routing and NAT Flow

Internal users access external resources through the edge router using PAT, while public-facing DMZ services use Static NAT.

![NAT and Routing Flow](diagrams/nat-routing-flow.png)

---

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS
- Cisco Catalyst 3650 Layer 3 Switch
- Cisco Catalyst 2960 Access Switches
- Cisco 2911 Routers
- VLANs
- Inter-VLAN Routing
- Static Routing
- DHCP
- NAT/PAT
- Static NAT
- SSH
- ACLs
- DHCP Snooping
- Port Security
- WPA2 Wireless

---

## Testing and Validation

The implementation was validated using structured functional testing across connectivity, routing, NAT, DHCP, wireless and performance areas.

| Test Area | Result |
|---|---|
| Intra-VLAN Connectivity | Passed |
| Inter-VLAN Routing | Passed |
| DHCP Services | Passed |
| NAT/PAT | Passed |
| Static NAT | Passed |
| Wireless Connectivity | Passed |
| Gateway Operations | Passed |
| Performance | Passed |

Performance summary:

| Metric | Result |
|---|---:|
| Wired Latency | <1 ms |
| Wireless Latency | 17 ms average |
| Packet Loss | 0% |
| Overall Success Rate | 84% |

---

## Repository Structure

```text
enterprise-network-design-cisco/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── .gitignore
│
├── lab/
│   └── EmboArts_Enterprise_Network.pkt
│
├── report/
│   └── Network_Design_Report.pdf
│
├── diagrams/
│   ├── enterprise-topology.png
│   ├── vlan-architecture.png
│   ├── security-zones.png
│   └── nat-routing-flow.png
│
├── screenshots/
│   └── add-your-packet-tracer-screenshots-here.txt
│
├── docs/
│   ├── Design.md
│   ├── Security.md
│   ├── Testing.md
│   └── Lessons-Learned.md
│
└── configs/
    └── add-your-cisco-configs-here.txt
```

---

## Documentation

Detailed documentation is available in the `docs/` folder:

- [Design Documentation](docs/Design.md)
- [Security Documentation](docs/Security.md)
- [Testing Documentation](docs/Testing.md)
- [Lessons Learned](docs/Lessons-Learned.md)

---

## Future Improvements

Future versions of this project could include:

- OSPF dynamic routing
- HSRP gateway redundancy
- EtherChannel
- IPv6 dual-stack
- RADIUS/TACACS+ authentication
- 802.1X network access control
- Cisco ASA or Firepower firewall
- SNMP monitoring
- Syslog server
- VPN remote access
- Python or Ansible network automation

---

## Skills Demonstrated

This project demonstrates practical experience with:

- Enterprise network design
- Cisco IOS configuration
- VLAN implementation
- Layer 2 switching
- Layer 3 routing
- IPv4 addressing
- DHCP
- NAT/PAT
- Wireless networking
- Network security
- Infrastructure troubleshooting
- Technical documentation

---

## About This Project

This project was originally developed during my HND Computer Science studies and has been refined into a professional portfolio project focused on enterprise networking, infrastructure and cybersecurity fundamentals.
