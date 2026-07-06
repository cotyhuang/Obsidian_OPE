---
tags: [regulation, capital, OPE]
sources:
  - "[[raw/OPE.pdf]]"
  - "[[raw/NotebooklmSummaryOP.md]]"
  - "[[raw/DIS60.pdf]]"
  - "[[raw/DIS10_20260101_20240717.xlsx]]"
created: 2026-07-02
---
# Standardised Measurement Approach

The **Standardised Measurement Approach (SMA)** is the Basel III regulatory framework for calculating minimum operational risk capital requirements. Effective January 1, 2023, it replaces all three previous operational risk capital approaches: the Basic Indicator Approach (BIA), the Standardised Approach (TSA), and the Advanced Measurement Approaches (AMA) [[raw/OPE.pdf#page=4]].

Under this standardised methodology, internal models are removed to ensure consistency, comparability, and simplicity across the banking sector.

---

## Comparison: Basel II/2.5 vs. Basel III

The table below outlines the core changes in operational risk capital requirements following the Basel III reforms:

| Requirements                | Basel 2/2.5                                                                                                                                                                                                                                                                                  | Basel III                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Calculation Methodology** | Three methods available:<br>• Basic Indicator Approach (BIA)<br>• Standardised Approach (SA)<br>• Advanced Measurement Approach (AMA) [[raw/OPE.pdf#page=4,11]].                                                                                                                             | • The three legacy approaches (BIA, SA, AMA) are replaced by a single non-model-based Standardised Approach (SA). AMA is removed, ending internal modelling of operational-risk capital.<br>• Introduction of a simplified SA for smaller banks (e.g. Bucket 1, where the Internal Loss Multiplier defaults to 1) [[raw/OPE.pdf#page=11]].                                                                                                                                                                                                                    |
| **Basis of Calculation**    | • **BIA**: Capital based on 15% of average annual gross income over the last 3 years.<br>• **SA**: Capital based on weighted gross income across eight business lines.<br>• **AMA**: Capital derived from internal models using loss events, scenario analysis, and qualitative adjustments. | Gross-income measures give way to a formula: **$ORC = BIC \times ILM$**<br>• **[[Business Indicator Component]] (BIC)** (baseline charge): Business Indicator (interest, services and financial components, 3-year average) × a marginal coefficient of 12/15/18%, scaled by size like a tax bracket [[raw/OPE.pdf#page=10]].<br>• **[[Internal Loss Multiplier]] (ILM)** (loss-sensitivity factor): Adjusts the baseline up or down based on the bank's 10-year internal loss history (Loss Component = 15 × average annual losses) [[raw/OPE.pdf#page=11]]. |
| **Data Requirements**       | Loss data collection was required only for banks using AMA.                                                                                                                                                                                                                                  | Under the Thai SA (and Basel III generally), loss-data collection becomes integral since internal loss history feeds the ILM and the capital charge, except where supervisors exercise discretion to set ILM = 1 [[raw/OPE.pdf#page=11-12]].                                                                                                                                                                                                                                                                                                                  |

---

## Core Capital Formulas

Operational Risk Capital (ORC) requirements are calculated as the product of two main components [[raw/OPE.pdf#page=10]]:

$$ORC = BIC \times ILM$$

Risk-Weighted Assets (RWA) for operational risk are obtained by multiplying the capital requirement by 12.5 [[raw/OPE.pdf#page=10]]:

$$RWA = 12.5 \times ORC$$

---

## Core Components

The calculation is driven by three underlying regulatory metrics:

1. **[[Business Indicator Calculation|Business Indicator (BI)]]**: A financial-statement-based proxy for a bank's operational risk exposure, calculated as the sum of three main components: Interest, Leases & Dividend (ILDC), Services (SC), and Financial (FC) [[raw/OPE.pdf#page=10]].
2. **[[Business Indicator Component|Business Indicator Component (BIC)]]**: Calculated by multiplying the BI by specific, progressively higher marginal coefficients based on the bank's size bucket (12%, 15%, or 18%) [[raw/OPE.pdf#page=10]].
3. **[[Internal Loss Multiplier|Internal Loss Multiplier (ILM)]]**: A scaling factor that compares the bank's historical 10-year operational risk losses (the Loss Component, LC) against its BIC. If historical losses are high relative to the BIC, the ILM increases the capital requirement ($ILM > 1$); if they are low, the capital requirement is scaled down ($ILM < 1$) [[raw/OPE.pdf#page=11]].

---

## Pillar 3 Disclosure Requirements

Under Basel III, banks are required to make annual public disclosures on operational risk through one qualitative table and three quantitative templates, defined in **DIS60 – Operational risk** [[raw/DIS60.pdf#page=3]]. See [[Operational Risk Disclosure Templates]] for the full report layouts extracted from the official BCBS workbook [[raw/DIS10_20260101_20240717.xlsx]].

| Template | Name | Content | Scope |
| :--- | :--- | :--- | :--- |
| **Table ORA** | General qualitative information | Policies, frameworks, risk management structure, measurement systems, and risk mitigation/transfer approaches | All banks [[raw/DIS60.pdf#page=3]] |
| **Template OR1** | Historical losses | 10-year operational loss history (at €20k and €100k thresholds), exclusions, and ILM usage details | Bucket 2 & 3 banks; Bucket 1 banks using internal loss data [[raw/DIS60.pdf#page=3]] |
| **Template OR2** | Business indicator and subcomponents | BI and its three subcomponents (ILDC, SC, FC) with line-item detail for T, T-1, T-2 | All banks [[raw/DIS60.pdf#page=5]] |
| **Template OR3** | Minimum required operational risk capital | BIC, ILM, ORC, and operational risk RWA | All banks [[raw/DIS60.pdf#page=7]] |

All templates use a **fixed format** and are disclosed on an **annual** basis. Banks are expected to supplement quantitative disclosures with narrative commentary [[raw/DIS60.pdf#page=3]].

---

## See Also

* [[Business Indicator Calculation]]
* [[Business Indicator Component]]
* [[Internal Loss Multiplier]]
* [[Loss Data Collection]]
* [[Operational Risk Event Categories]]
* [[Operational Risk Disclosure Templates]]
