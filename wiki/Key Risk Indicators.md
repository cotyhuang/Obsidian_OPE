---
tags: [risk-monitoring, metrics, OPE]
sources:
  - "Web search: Key Risk Indicators operational risk guidelines"
created: 2026-07-03
---
# Key Risk Indicators

A **Key Risk Indicator (KRI)** is a metric used to monitor and measure the level of operational risk exposure in a specific process or business unit. Unlike historical metrics (such as loss data), KRIs are ideally designed to be **forward-looking leading indicators** that warn management of changing risk exposures before loss events actually occur.

---

## KRI Design Principles

To be effective, a KRI must be:

* **Measurable**: Expressed quantitatively (e.g., percentages, count, currency) to ensure objectivity.
* **Predictive**: Serve as a leading indicator of an underlying risk trend (e.g., a rise in employee turnover rates can predict process execution failures).
* **Informative**: Directly linked to a specific process risk identified in the [[Risk and Control Self-Assessment]] (RCSA).
* **Comparable**: Monitored consistently over time to detect shifts in operational risk profile.

---

## Thresholds and the GAR System

KRIs are monitored against predefined thresholds to prompt management action. A standard industry convention is the **Green-Amber-Red (GAR)** alert system:

| Alert Level | Meaning | Management Action |
| :--- | :--- | :--- |
| **Green** | Risk is within appetite. | Normal monitoring continues. |
| **Amber** | Risk is rising and approaching appetite limits. | Investigation is triggered; initial corrective measures implemented. |
| **Red** | Risk exceeds appetite limits. | Immediate escalation to senior management; mandatory remediation action plan. |

### Example KRI Setup

* **Risk**: Business interruption due to system outages.
* **KRI**: Critical IT system uptime percentage (monthly).
* **Thresholds**:
  * **Green**: $\ge 99.9\%$
  * **Amber**: $99.5\% \text{ to } 99.89\%$
  * **Red**: $< 99.5\%$

---

## Difference Between KRI, KPI, and KCI

Operational risk frameworks distinguish between three types of metrics:

1. **Key Performance Indicators (KPIs)**: Measure business performance and success against goals (e.g., transaction volume processed).
2. **Key Risk Indicators (KRIs)**: Measure risk exposure relative to risk appetite (e.g., percentage of transaction errors).
3. **Key Control Indicators (KCIs)**: Measure the operational effectiveness of a control (e.g., percentage of staff completing mandatory compliance training).

---

## See Also

* [[Risk and Control Self-Assessment]]
* [[Scenario Analysis]]
* [[Principles for Operational Resilience]]
