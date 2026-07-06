---
tags: [regulation, capital, OPE]
sources:
  - "[[raw/OPE.pdf]]"
  - "[[raw/NotebooklmSummaryOP.md]]"
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

## See Also

* [[Business Indicator Calculation]]
* [[Business Indicator Component]]
* [[Internal Loss Multiplier]]
* [[Loss Data Collection]]
* [[Operational Risk Event Categories]]
