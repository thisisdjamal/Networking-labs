## Multi-site_OSPF-network

## Overview
This network architecture connects a main headquarters (Agency A) and a branch office (Agency B) over a dedicated cross-site backbone with redundant internet edges (simulated internet connection). Agency A implements a fully redundant 3-tier switching layout (Core, Distribution, Access) to maximize uptime, whereas Agency B uses a cost-effective collapsed-core model. Internal departmental traffic is strictly segmented across custom VLANs (/27 subnets) using the address 172.16.0.0, while public-facing web and DNS servers are sandboxed in a dedicated DMZ. Point-to-point links are segmented across /30 subnets using 10.0.0.0 range while internet links use public IPs.

## Objectives
The key objectives of this architecture are :

High Availability: Eliminate single points of failure at HQ through dual-homed distribution uplinks and inter-site link aggregation. 
Perimeter Security: Sandbox public HTTPS/DNS servers inside a dedicated DMZ to protect internal host data. 
Network Segmentation: Reduced broadcast domains using isolated VLANs. 
Cost-Optimized Scalability: Deploy a full 3-tier architecture at HQ for performance, paired with a collapsed core at the branch office to reduce hardware costs. Efficient IP Allocation: Use VLSM (/27 for departments and /30 for point-to-point transit links) to eliminate IPv4 waste.

## Technologies

This architecture using several technologies such us :
- VLAN, IPv4 addressing , Inter-VLAN Routing, DHCP, OSPF, HSRP, LACP, BGP, Zone-Based Firewall, NAT, L3 routing

## Documentation

- [Design](design/) contains the diagram of the network
- [Addressing](addressing/) explains how the whole network was addressed
- [Configurations](configurations/) contains the configurations for each device
- [Validation](validation/)
- [Packet Tracer Files](packet-tracer/) contains .pkt lab file
- [Changelog](CHANGELOG.md)

## Limitations

This is a simulated Cisco Packet Tracer environment.
<Real limitation 1>
<Real limitation 2>

## Future Improvements

- <Improvement 1>
- <Improvement 2>
