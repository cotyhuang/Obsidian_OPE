---
tags: [regulation, disclosure, reporting, OPE]
sources:
  - "[[raw/DIS60.pdf]]"
  - "[[raw/DIS10_20260101_20240717.xlsx]]"
created: 2026-07-06
---
# Operational Risk Disclosure Templates

Under the Basel III Pillar 3 framework (**DIS60 – Operational risk**), banks must publish annual disclosures on operational risk through one qualitative table and three quantitative templates [[raw/DIS60.pdf#page=3]]. The official report layouts are defined in the BCBS disclosure workbook [[raw/DIS10_20260101_20240717.xlsx]].

---

## Table ORA — General Qualitative Information

**Purpose**: Describe the main characteristics and elements of a bank's operational risk management framework [[raw/DIS60.pdf#page=3]].

| Attribute | Detail |
| :--- | :--- |
| **Scope** | Mandatory for all banks |
| **Content** | Qualitative information |
| **Frequency** | Annual |
| **Format** | Flexible |

### Required Disclosures

Banks must describe [[raw/DIS60.pdf#page=3]]:

| Item | Description |
| :---: | :--- |
| **(a)** | Policies, frameworks, and guidelines for the management of operational risk |
| **(b)** | Structure and organisation of the operational risk management and control function |
| **(c)** | Operational risk measurement system (systems and data used to estimate the capital charge) |
| **(d)** | Scope and main context of the reporting framework on operational risk to executive management and the board |
| **(e)** | Risk mitigation and risk transfer used in managing operational risk (policy-based mitigation, divestitures, controls, insurance) |

---

## Template OR1 — Historical Losses

**Purpose**: Disclose aggregate operational losses incurred over the past 10 years, based on the accounting date of the incurred losses [[raw/DIS60.pdf#page=3]].

| Attribute | Detail |
| :--- | :--- |
| **Scope** | Mandatory for: (i) all Bucket 2 and 3 banks (regardless of ILM discretion); (ii) Bucket 1 banks approved to use internal loss data |
| **Content** | Quantitative information |
| **Frequency** | Annual |
| **Format** | Fixed |

### Understanding the €20,000 Threshold

The **loss event threshold** determines the minimum size of an operational loss event that must be captured in the bank's loss dataset and disclosed in Template OR1 [[raw/OPE.pdf#page=14]]:

* **€20,000** is the **standard threshold**. Any individual operational risk loss event (or grouped event) whose cumulative net loss ≥ €20,000 must be included in the loss dataset.
* **€100,000** is an **alternative threshold** that national supervisors may permit for banks in Buckets 2 and 3 [[raw/OPE.pdf#page=14]].
* The threshold is applied **net of recoveries** — meaning if a bank suffers a gross loss of €30,000 but recovers €15,000, the net loss is €15,000 and the event falls **below** the €20,000 threshold (i.e. it would be excluded from the dataset).
* Both threshold sections (rows 1–5 for €20k; rows 6–10 for €100k) must be reported side-by-side in the template so that users can observe the impact of the threshold choice on reported loss volumes.

> [!important] Why the Threshold Matters for Capital
> The threshold directly affects the **Loss Component (LC)** and therefore the [[Internal Loss Multiplier|ILM]]. A lower threshold (€20,000) captures more loss events, potentially resulting in a higher average annual loss figure and a higher ILM. Conversely, a €100,000 threshold excludes smaller events, which could reduce the reported average.

### Report Layout

#### Using €20,000 Threshold

| Row | Description | T | T–1 | T–2 | T–3 | T–4 | T–5 | T–6 | T–7 | T–8 | T–9 | 10yr Avg |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **1** | Total amount of operational losses net of recoveries (no exclusions) | | | | | | | | | | | |
| **2** | Total number of operational risk losses | | | | | | | | | | | |
| **3** | Total amount of excluded operational risk losses | | | | | | | | | | | |
| **4** | Total number of exclusions | | | | | | | | | | | |
| **5** | Total amount of operational losses net of recoveries and net of excluded losses | | | | | | | | | | | |

#### Using €100,000 Threshold

| Row | Description | T | T–1 | T–2 | T–3 | T–4 | T–5 | T–6 | T–7 | T–8 | T–9 | 10yr Avg |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **6** | Total amount of operational losses net of recoveries (no exclusions) | | | | | | | | | | | |
| **7** | Total number of operational risk losses | | | | | | | | | | | |
| **8** | Total amount of excluded operational risk losses | | | | | | | | | | | |
| **9** | Total number of exclusions | | | | | | | | | | | |
| **10** | Total amount of operational losses net of recoveries and net of excluded losses | | | | | | | | | | | |

#### Details of Operational Risk Capital Calculation

| Row | Description | Value |
| :---: | :--- | :---: |
| **11** | Are losses used to calculate the ILM? (yes/no) | |
| **12** | If "no" in row 11, is the exclusion due to non-compliance with minimum loss data standards? (yes/no) | |
| **13** | Loss event threshold: €20,000 or €100,000 for the capital calculation | |

### Row Definitions

* **Row 1**: Total loss amount net of recoveries at €20,000 threshold. Excluded losses must still be included here.
* **Row 2**: Total number of loss events at €20,000 threshold.
* **Row 3**: Total net loss amounts excluded (e.g. due to divestitures) at €20,000 threshold.
* **Row 4**: Total number of exclusions at €20,000 threshold.
* **Row 5**: Total losses net of recoveries and excluded losses at €20,000 threshold.
* **Rows 6–10**: Equivalent to rows 1–5 using the €100,000 threshold.
* **Row 11**: Whether the bank uses operational risk losses to calculate the [[Internal Loss Multiplier|ILM]]. Banks using $ILM = 1$ due to national discretion should answer "no".
* **Row 12**: Whether internal loss data are not used due to non-compliance with minimum loss data standards ([OPE25.12] and [OPE25.13]). Any resulting multipliers must be disclosed in OR3 row 2 with narrative.
* **Row 13**: The actual loss event threshold used in the capital calculation.

> [!note] Reporting Convention
> Loss amounts and associated recoveries should be reported in the year in which they were recorded in financial statements. Column (k) refers to the average annual losses net of recoveries and excluded losses over 10 years [[raw/DIS60.pdf#page=4]].

### Worked Example — Template OR1

Assume a hypothetical **Bucket 2 bank** using the **€20,000 threshold**, which uses internal loss data to calculate the ILM. In year T–3, one loss event (from a divested business unit) was excluded with supervisory approval.

#### Rows 1–5 (€20,000 Threshold)

|  Row  | Description                              |   T | T–1 |  T–2 |  T–3 | T–4 | T–5 | T–6 | T–7 | T–8 | T–9 | 10yr Avg |
| :---: | :--------------------------------------- | --: | --: | ---: | ---: | --: | --: | --: | --: | --: | --: | -------: |
| **1** | Losses net of recoveries (no exclusions) | 9.2 | 7.8 | 10.5 | 12.3 | 6.4 | 8.1 | 7.0 | 5.5 | 9.8 | 6.0 | **8.26** |
| **2** | Number of loss events                    |  42 |  38 |   51 |   55 |  30 |  40 |  35 |  28 |  45 |  32 | **39.6** |
| **3** | Excluded loss amounts                    |   0 |   0 |    0 |  4.0 |   0 |   0 |   0 |   0 |   0 |   0 | **0.40** |
| **4** | Number of exclusions                     |   0 |   0 |    0 |    1 |   0 |   0 |   0 |   0 |   0 |   0 |  **0.1** |
| **5** | Losses net of recoveries & exclusions    | 9.2 | 7.8 | 10.5 |  8.3 | 6.4 | 8.1 | 7.0 | 5.5 | 9.8 | 6.0 | **7.86** |

*(All amounts in €millions)*

**Reading the example:**
* **Row 1** shows the total losses each year including all events (even those later excluded). In T–3, the bank recorded €12.3m in total losses net of recoveries.
* **Row 3** shows that €4.0m was excluded in T–3 because it arose from a divested business unit.
* **Row 5** = Row 1 − Row 3: the loss figure actually used in the capital calculation. In T–3 this is €12.3m − €4.0m = €8.3m.
* **Column 10yr Avg** (Row 5): The average annual loss used for the [[Internal Loss Multiplier|LC calculation]] is **€7.86m**.

#### Rows 11–13 (Capital Calculation Details)

| Row | Description | Value |
| :---: | :--- | :--- |
| **11** | Are losses used to calculate the ILM? | **Yes** |
| **12** | Non-compliance with loss data standards? | **No** |
| **13** | Loss event threshold | **€20,000** |

#### How This Feeds the ILM

Using the 10-year average from Row 5:

$$LC = 15 \times 7.86\text{m} = \text{€}117.9\text{m}$$

If the bank's $BIC = \text{€}100\text{m}$, then:

$$ILM = \ln\left(e - 1 + \left(\frac{117.9}{100}\right)^{0.8}\right) = \ln(1.7183 + 1.141) = \ln(2.859) \approx 1.050$$

$$ORC = BIC \times ILM = \text{€}100\text{m} \times 1.050 = \text{€}105.0\text{m}$$

This result would be disclosed in **Template OR3** (rows 1–4).


---

## Template OR2 — Business Indicator and Subcomponents

**Purpose**: Disclose the [[Business Indicator Calculation|Business Indicator (BI)]] and its subcomponents, which inform the operational risk capital calculation [[raw/DIS60.pdf#page=5]].

| Attribute | Detail |
| :--- | :--- |
| **Scope** | Mandatory for all banks |
| **Content** | Quantitative information |
| **Frequency** | Annual |
| **Format** | Fixed |

### Report Layout

| Row | BI and its subcomponents | T | T–1 | T–2 |
| :---: | :--- | :---: | :---: | :---: |
| **1** | Interest, lease and dividend component | | | |
| 1a | Interest and lease income | | | |
| 1b | Interest and lease expense | | | |
| 1c | Interest earning assets | | | |
| 1d | Dividend income | | | |
| **2** | Services component | | | |
| 2a | Fee and commission income | | | |
| 2b | Fee and commission expense | | | |
| 2c | Other operating income | | | |
| 2d | Other operating expense | | | |
| **3** | Financial component | | | |
| 3a | Net P&L on the trading book | | | |
| 3b | Net P&L on the banking book | | | |
| **4** | **BI** | | | |
| **5** | **[[Business Indicator Component\|Business indicator component (BIC)]]** | | | |

#### Disclosure on Divested Activities

| Row | Description | Value |
| :---: | :--- | :---: |
| **6a** | BI gross of excluded divested activities | |
| **6b** | Reduction in BI due to excluded divested activities | |

> [!note] Divested Activities
> Rows 6a and 6b should only be reported by banks that have received supervisory approval to exclude divested activities from the BI calculation [[raw/DIS60.pdf#page=5]].

### Row Definitions

* **Row 1**: $ILDC = \min\left[\text{Abs}(\text{Interest Income} - \text{Interest Expense}),\; 2.25\% \times \text{Interest Earning Assets}\right] + \text{Dividend Income}$ (3-year average).
* **Row 2**: $SC = \max(\text{Fee Income},\; \text{Fee Expense}) + \max(\text{Other Operating Income},\; \text{Other Operating Expense})$ (3-year average).
* **Row 3**: $FC = \text{Abs}(\text{Net P\&L Trading Book}) + \text{Abs}(\text{Net P\&L Banking Book})$ (3-year average).
* **Row 4**: $BI = ILDC + SC + FC$.
* **Row 5**: BIC = BI × marginal coefficients ($\alpha_i$): 12% for $BI \le \text{€}1\text{bn}$; 15% for $\text{€}1\text{bn} < BI \le \text{€}30\text{bn}$; 18% for $BI > \text{€}30\text{bn}$.

### Linkages Across Templates

`[OR2:5/a]` is equal to `[OR3:1/a]` [[raw/DIS60.pdf#page=7]].

---

## Template OR3 — Minimum Required Operational Risk Capital

**Purpose**: Disclose operational risk regulatory capital requirements [[raw/DIS60.pdf#page=7]].

| Attribute | Detail |
| :--- | :--- |
| **Scope** | Mandatory for all banks |
| **Content** | Quantitative information |
| **Frequency** | Annual |
| **Format** | Fixed |

### Report Layout

| Row | Description | Value (a) |
| :---: | :--- | :---: |
| **1** | [[Business Indicator Component\|Business indicator component (BIC)]] | |
| **2** | [[Internal Loss Multiplier\|Internal loss multiplier (ILM)]] | |
| **3** | Minimum required operational risk capital (ORC) | |
| **4** | Operational risk RWA | |

### Row Definitions

* **Row 1**: The BIC used for calculating minimum regulatory capital requirements for operational risk.
* **Row 2**: The ILM used for calculating minimum regulatory capital requirements. Where national jurisdictions choose to exclude losses from the operational risk calculation, the $ILM$ is set equal to 1.
* **Row 3**: Minimum Pillar 1 operational risk capital requirements. For banks using losses: $ORC = BIC \times ILM$. For banks not using losses: $ORC = BIC$.
* **Row 4**: Converts the minimum Pillar 1 capital requirement into RWA: $RWA = 12.5 \times ORC$.

---

## See Also

* [[Standardised Measurement Approach]]
* [[Business Indicator Calculation]]
* [[Business Indicator Component]]
* [[Internal Loss Multiplier]]
* [[Loss Data Collection]]
