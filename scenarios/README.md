# Scenarios

This directory contains various scenarios of WAN network topology and Cisco configuration files for the project experiments. 

The scenarios were deployed on Cisco router ISR 2911 with IOS 15.1, Catalyst 8200 L with Cisco IOS XE 17.6, and L2 switches Catalyst 2950 with IOS 15.0. The configuration files include routers (options for ISR 2911, Catalyst 8200 L) and switches (Catalyst 2950).

## A list of available scenarios:
  * [acl - ACL rules](acl): filtering network traffic using standard and extended ACL rules. 
  * [gre - VPN tunnel using GRE](gre): implementation of VPN tunnel using GRE. 
  * [ipv6 - IPv6 addressing](ipv6): combination of IPv4 and IPv6 networking with an IPv6 tunnel.
  * [bgp - BPG routing](bgp): a simple BGP routing between ASes
  * [mpls - MPLS switching](mpls): a combination of MPLS switching with OSPF and iBGP.
  * [hsrp - router redundancy](hsrp): configuring router redundancy using HSRP.
  * [ipsec - IPSec security](ipsec): creating an IPSec tunnel between remote routers.
  * [snmp - SNMP configuration ](snmp): configuring SNMP monitoring on the existing topology with firewalls. 
  
## An overview of evaluated tasks
| Scenario | Number of devices | Evaluated tasks for tested scenarios |
| :------- | :---------------- | :-------------------------------- |
| ACL | 3 routers | IP addressing, DHCP server, SSH access, OSPF routing, ACL filtering |
| GRE | 3 routers, 1 switch | IP addressing, DHCP server, NAT translation, GRE tunnel, OSPF routing |
| HSRP | 5 routers, 2 switches | IP addressing, static routing, NAT translation, DHCP, HSRP configuration |
| IPv6 | 3 routers, 1 switch | IPv4 and IPv6 addressing, DHCPv4 and DHCPv6, IPv6 tunnelling, OSPF and RIPng routing |
| BGP | 3 routers | IP addressing, BGP routing, route redistribution |
| IPSec | 2 routers | IP addressing, static routers, ISAKMP configuration, key distribution, ACL, IPSec tunnelling |
| Monitoring | 3 routers, 2 switches | NTP synchronisation, NAT, DHCP, Syslog, SNMPv2 and v3, CDP |
| MPLS | 6 routers | IP addressing, OSPF routing, MPLS encapsulation, VRF, BGP routing |
| SNMP | 7 routers, 2 firewalls | Configuring SNMP agent on routers RA, RB, RC, configuring ACLs on FW1 and FW2 to pass the SNMP traffic |
