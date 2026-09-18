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

### Overview of the regression tests
| Task   |  Regression tests |
| :------| :----|
| Task 1 | cmp_domain_name, cmp_interfaces_definitions, cmp_interfaces_status, cmp_interfaces_ip, cmp_interfaces_ospf |
| Task 2 | cmp_hostname, cmp_domain_name, cmp_users_definitions, cmp_users_properties, cmp_dns_lookup_status |
| Task 3 | cmp_hostname, cmp_domain_name, cmp_interface_definitions, cmp_interfaces_status, cmp_interfaces_ip, cmps_interfaces_ospf, cmp_users_definition, cmp_users_properties, cmp_dns_lookup_status |
| Task 4 | cmp_hostname, cmp_interface_definitions, cmp_interfaces_status, cmp_interfaces_ip, cmps_interfaces_ospf, cmp_users_definition, cmp_users_properties, cmp_dns_lookup_status|
| Task 5 | cmp_hostname, cmp_domain_name, mp_users_definition, cmp_users_properties, cmp_dns_lookup_status|
| Task 6 | cmp_hostname, cmp_domain_name,  cmp_interface_definitions, cmp_interfaces_status, cmp_interfaces_ip, cmps_interfaces_ospf, cmp_users_definition, cmp_users_properties, cmp_dns_lookup_status |
