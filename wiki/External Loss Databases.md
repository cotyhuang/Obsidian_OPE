---
tags: [loss-data, benchmarking, OPE]
sources:
  - "Web search: External Loss Databases ORX operational risk"
created: 2026-07-03
---
# External Loss Databases

**External Loss Databases** are repositories of operational risk loss events experienced by other institutions in the financial services industry. These databases are a critical tool for banks to benchmark their risk profile, scale scenario analysis parameters, and learn from industry-wide operational failures.

---

## Types of External Databases

1. **Consortium Databases (e.g., ORX)**:
   * **ORX (Operational Riskdata eXchange)** is the largest global member-owned consortium.
   * Members anonymously pool their operational loss events.
   * Data is highly structured, audited, and categorized according to regulatory lines.
2. **Public / Subscription Databases (e.g., SAS OpRisk Global Data, IBM First)**:
   * Compiled from public media releases, regulatory action filings, and legal court proceedings.
   * Often focus on large, high-profile tail risk events (typically above $1 million).

---

## Core Uses in Operational Risk

* **[[Scenario Analysis]] Parameter Calibration**: If a bank has never experienced a massive cyber breach, external databases provide concrete examples of what such an event cost similar-sized peers.
* **Capital Modeling / Scaling**: Historically used under the Advanced Measurement Approach (AMA) to scale loss severity distributions based on the bank's asset size relative to peer institutions.
* **Risk Identification**: Highlight emerging operational risks in the industry (e.g., new fraud vectors or AI-related technology failures) before they impact the bank.

---

## Challenges and Scaling Biases

Because external data comes from institutions of varying sizes, business models, and geographic jurisdictions, banks cannot import raw numbers directly. They must account for:
* **Scale Bias**: Larger banks experience larger operational losses. Scaling formulas (e.g., power-law adjustments using assets or revenue) are applied to adjust the severity distribution.
* **Reporting Bias**: Different organizations have different reporting thresholds, although consortium rules (like ORX's €20,000 threshold) help standardize data.

---

## See Also

* [[Loss Data Collection]]
* [[Scenario Analysis]]
* [[Standardised Measurement Approach]]
