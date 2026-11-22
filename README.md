# Hospital Enterprise Network Infrastructure

A secure multi-site hospital network designed and simulated in Cisco Packet Tracer. The network connects a Main Hospital Headquarters with a Branch Hospital through an ISP network, using a hierarchical architecture with core, distribution, and access layers. Each hospital department is assigned a separate VLAN, and the design includes inter-VLAN routing, OSPF and static routing, NAT/PAT, an IPsec site-to-site VPN, SSH, ACLs, and end-to-end connectivity testing.

**Course:** Computer Communication and Networking (CEL-223), Bahria University Karachi Campus, BSE-5(B)

---

## Tech Stack

- Cisco Packet Tracer (network design and simulation)
- Cisco IOS CLI (router and switch configuration)
- Wireshark (packet capture and IP header analysis)
- VLANs, 802.1Q Trunking, STP
- OSPF, RIP, EIGRP, Static Routing
- DHCP, NAT/PAT
- IPsec Site-to-Site VPN
- SSH and ACLs

---

## Network Design

Main Hospital HQ and Branch Hospital connect through an ISP network over an IPsec site-to-site VPN.

Each site uses a three-layer hierarchical model:

- **Core Layer** — Multilayer switches
- **Distribution Layer** — Switches
- **Access Layer** — Department VLANs (Administration, Doctors, Nurses, Laboratory, Pharmacy, IT, Server Room)

---

## Folder Structure

```
topology/          Packet Tracer (.pkt) files for HQ, Branch, and full network
configs/           Device configuration files (routers, switches)
  hq/              HQ router and switch configs
  branch/          Branch router and switch configs
  isp/             ISP router configs
docs/              Proposal, topology diagrams, and testing reports
screenshots/       Verification screenshots (ping, traceroute, VPN, ACL tests)
README.md
```

---

## Features

- IP addressing and subnetting across all departmental networks
- VLAN creation and port assignment per department
- Inter-VLAN routing via multilayer switches
- 802.1Q trunking between switches
- Spanning Tree Protocol (STP) for loop prevention and redundancy
- OSPF for internal dynamic routing, static routing for WAN
- RIP and EIGRP demonstrated on separate test segments
- DHCP for automatic IP allocation
- NAT/PAT for external connectivity
- IPsec site-to-site VPN between HQ and Branch
- SSH and ACLs for secure management and access control
- Connectivity testing with ping and traceroute
- Packet analysis with Wireshark

---

## Setup

1. Install Cisco Packet Tracer (version 8.x or later).
2. Clone the repository and open the folder.
3. Open the `.pkt` file from `topology/` in Packet Tracer.
4. Allow devices to boot and STP to converge.
5. Verify connectivity:
   - Ping from HQ departments to Branch departments
   - Traceroute across the ISP link
   - Confirm the IPsec VPN tunnel is up
6. Apply or review device configurations from `configs/` as needed.
7. Use Simulation Mode to trace packet flow and inspect protocol behavior.

---

## Testing

| Test | Command / Method |
|---|---|
| End-to-end connectivity | `ping` between HQ and Branch hosts |
| Path verification | `traceroute` across the WAN |
| VPN status | `show crypto isakmp sa`, `show crypto ipsec sa` |
| ACL validation | Attempt blocked vs. permitted traffic |
| VLAN/trunk check | `show vlan brief`, `show interfaces trunk` |
| Routing tables | `show ip route` (OSPF, static, RIP, EIGRP) |

---

## Team

- Iffat Batool (Team Leader)
- Kanwal Bibi
- Aamnah Attariah
