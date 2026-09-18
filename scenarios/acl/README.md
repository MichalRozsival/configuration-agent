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
