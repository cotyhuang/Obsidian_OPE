---
tags: [risk-assessment, governance, OPE]
sources:
  - "Web search: RCSA best practices guidelines"
created: 2026-07-03
---
# Risk and Control Self-Assessment

The **Risk and Control Self-Assessment (RCSA)** is a core process-level risk assessment methodology used in operational risk management. It allows business units to identify the risks they face, evaluate the effectiveness of the controls in place to mitigate those risks, and establish action plans for any gaps.

Unlike top-down risk evaluations, RCSA is a bottom-up methodology owned and executed by the **First Line of Defense** (the business process owners).

---

## Core Components of RCSA

A standard RCSA process involves five sequential steps:

1. **Process Mapping & Risk Identification**:
   * Map the key activities and sub-processes within a business unit.
   * Identify specific risk events that could disrupt these processes (using standardized operational risk taxonomies).
2. **Inherent Risk Assessment**:
   * Assess the risk *before* considering the impact of any mitigating controls.
   * Evaluate the **Likelihood** ($L$) and **Impact** ($I$) of the risk event using consistent rating scales (typically 1 to 5).
   * **Inherent Risk Rating** ($IR$) is calculated as:
     $$IR = L \times I$$
3. **Control Identification & Evaluation**:
   * Identify the key controls designed to prevent or detect each risk event.
   * Assess controls based on their **design effectiveness** (is the control designed correctly to mitigate the risk?) and **operating effectiveness** (is the control consistently applied and working as intended?).
4. **Residual Risk Assessment**:
   * Evaluate the remaining risk exposure *after* accounting for control effectiveness.
   * **Residual Risk** represents the actual exposure the business unit is carrying. If controls are rated weak, residual risk remains close to inherent risk.
5. **Action Plan & Remediation**:
   * Where residual risk exceeds the firm's defined risk appetite, processes must establish action plans to design new controls, modify existing processes, or transfer the risk.

---

## RCSA Best Practices

* **Business Ownership**: Business units must own the RCSA, as they have direct visibility of the processes. The Second Line of Defense (Risk Management) provides the framework and check-and-challenge support.
* **Standardized Risk & Control Libraries**: Utilizing centralized risk and control directories ensures consistent risk scoring and allows risks to be aggregated across the organization.
* **Trigger-Based Assessments**: Move from rigid annual reviews to dynamic assessments triggered by business changes (e.g., system updates, new product launches, regulatory changes).
* **Evidence-Based Rating**: Control effectiveness ratings should be backed by audit reports, self-testing, and historical loss event data rather than subjective judgment.

---

## See Also

* [[Key Risk Indicators]]
* [[Scenario Analysis]]
* [[Standardised Measurement Approach]]
* [[Loss Data Collection]]
