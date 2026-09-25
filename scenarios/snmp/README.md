## Evaluation of the SNMP scenario 

The explanation of the metrics and details of the evaluation framework will be published at the NCA 2026 conference in November 2026. 
Here, we present a final evaluation using three scores: 
- Configuration Accuracy Score (CAS): compares a generated configuration with the reference configuration.
- Weighted Feature Coverage (WFC): measures the percentage of feature tests that successfully passed.
- Regression Preservation Rate (RPR): quantifies the proportion of scenario-level invariants that hold after the configuration update.

| Model | CAS | WFC | RPR |
| :----| :-: | :-: | :-: |
| Grok  | 89.4% | 91.7% |  100% |
| Deepseek | 74.5% | 58.3 | 100% |
| GTP 5 | 79.6% | 100% | 100% |
| GTP-OSS, run 1 | 52.0% | 58.3% | 100% |
| GTP-OSS, run 2 | 68.5% | 41.7% | 100% |
| GTP-OSS, run 3 | 61.4% | 100% | 100% |
| GTP-OSS, run 4 | 64.7% | 50% | 100% |
| GTP-OSS, run 5 | 83.2% | 66.7% | 97.8 |

### Overview of the regression tests applied
| Task   |  Regression tests |
| :------| :----|
| TBD | TBD |


### Description of the regression tests
| Regression test   |  Descrioption |
| :------| :----|
| TBD  | TBD |
