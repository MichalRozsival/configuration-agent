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
  
## An overview of evaluated tasks
| Scenario | Number of devices | Evaluated tasks |
| :------- | :---------------- | :-------------- |
| ACL | 3 routers | IP addressing, DHCP server, SSH access, OSPF routing, ACL filtering |
