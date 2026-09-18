## Evaluation of the ACL scenario on the LLM model GTP-OSS

The explanation of the metrics and details of the evaluation framework will be published at the NCA 2026 conference in November 2026. 
Here, we present a final evaluation using three scores: 
- Configuration Accuracy Score (CAS): compares a generated configuration with the reference configuration.
- Weighted Feature Coverage (WFC): measures the percentage of feature tests that successfully passed.
- Regression Preservation Rate (RPR): quantifies the proportion of scenario-level invariants that hold after the configuration update.

| Task | CAS | WFC | RPR | Task description |
| :----| :-: | :-: | :-: |:----|
| Task 1 | 92,9% | 100% | 100% | hostname, DNS, user account |
| Task 2 | 92,9% | 100% | 100% | configuration of interface: IP addresses and masks, loopback |
| Task 3 | 87% | 66,67% | 100% | configuration of the DHCP server|
| Task 4 | 0% | 66,67% | 100% | SSH configuration |
| Task 5 | 83% | 100% | 100% | OSPF routing |
| Task 6 | 0% | 0% | 100% | ACL filtering |

### Overview of the feature tests
| Task   |  Feater test | Description |
| :------| :----|:----|
| Task 1 | eval_hostname | hostname is Vienna |
| Task 1 | eval_dns_lookup_status | DNS lookup is disabled |
| Task 1 | eval_user | existence of an user with name admin, password cisco123 and the root access |
| Task 2 | eval_serial_interface | existence of the serial interface s1/0 with the IP address 10.2.2.2/30 |
| Task 2 | eval_lan_interfac e| existence of the ethernet interface eth0/0 with the IP address 192.168.30.1/24 |
| Task 2 | eval_loopback_interface | existence of the loopback interface with the IP address 192.168.40.1/24 |
| Task 3 | eval_lan_ip_address_exclude | exclusion of the IP range 192.168.30.1 - 192.168.30.10 |
| Task 3 | eval_default_gateway | the default gateway set to 192.168.30.1 |
| Task 3 | eval_dns | the DNS server set to 8.8.8.8 |
| Task 4 | eval_domain_name | ssh domain name set to vienna.com |
| Task 4 | eval_ssh_access_vty | ssh configurated on the VTY device |
| Task 4 | eval_ssh_reachability | reachability via SSH |
| Task 5 | eval_ospf_area | all interfaces are within OSPF area 0 |
| Task 5 | eval_updates_sending | LAN interfaces are passive and WAN interfaces are active |
| Task 6 | eval_30_to_40_communication | all traffic allowed from 192.168.30.0/24 to 192.168.40.0/24 |
| Task 6 | eval_30_to_web | network 192.168.30.0/24 can access the web server at 10.1.1.10 |
| Task 6 | eval_dns_communication_local_networks | DNS traffic can pass from 192.168.30.0/24 to 192.168.40.0/24 |
| Task 6 | eval_icmp_communication_local_networks | ICMP traffic can pass from 192.168.30.0/24 to 192.168.40.0/24 |

### Overview of the regression tests
| Task   |  Regression tests |
| :------| :----|
| Task 1 | cmp_domain_name, cmp_interfaces_definitions, cmp_interfaces_status, cmp_interfaces_ip, cmp_interfaces_ospf |
| Task 2 | cmp_hostname, cmp_domain_name, cmp_users_definitions, cmp_users_properties, cmp_dns_lookup_status |
| Task 3 | cmp_hostname, cmp_domain_name, cmp_interface_definitions, cmp_interfaces_status, cmp_interfaces_ip, cmps_interfaces_ospf, cmp_users_definition, cmp_users_properties, cmp_dns_lookup_status |
| Task 4 | cmp_hostname, cmp_interface_definitions, cmp_interfaces_status, cmp_interfaces_ip, cmps_interfaces_ospf, cmp_users_definition, cmp_users_properties, cmp_dns_lookup_status|
| Task 5 | cmp_hostname, cmp_domain_name, mp_users_definition, cmp_users_properties, cmp_dns_lookup_status|
| Task 6 | cmp_hostname, cmp_domain_name,  cmp_interface_definitions, cmp_interfaces_status, cmp_interfaces_ip, cmps_interfaces_ospf, cmp_users_definition, cmp_users_properties, cmp_dns_lookup_status |
