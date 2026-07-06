---
tags: [regulation, capital, OPE]
sources:
  - "[[raw/OPE.pdf]]"
  - "[[raw/DIS60.pdf]]"
  - "[[raw/DIS10_20260101_20240717.xlsx]]"
created: 2026-07-02
---
# Business Indicator Component

The **Business Indicator Component (BIC)** represents the baseline capital requirement for operational risk under the Basel III standardised approach. It is calculated by multiplying the [[Business Indicator Calculation|Business Indicator (BI)]] by specific regulatory marginal coefficients ($\alpha_i$) [[raw/OPE.pdf#page=10]].

---

## Progressive Brackets and Marginal Coefficients

Similar to a progressive tax system, the marginal coefficients increase as the bank's BI grows. The BI is divided into three size buckets [[raw/OPE.pdf#page=10-11]]:

| Bucket | BI Range (in €bn) | Marginal Coefficient ($\alpha_i$) | Baseline Formula |
| :---: | :--- | :---: | :--- |
| **1** | $\le 1$ | 12% | $BI \times 12\%$ |
| **2** | $1 < BI \le 30$ | 15% | $0.12 + (BI - 1) \times 15\%$ |
| **3** | $> 30$ | 18% | $4.47 + (BI - 30) \times 18\%$ |

---

## Calculation Example

For a bank with a **BI of €35 billion** [[raw/OPE.pdf#page=11]]:
1. **First Bracket** ($\le \text{€}1\text{ bn}$): 
   $$\text{€}1\text{ bn} \times 12\% = \text{€}0.12\text{ bn}$$
2. **Second Bracket** ($\text{€}1\text{ bn} \text{ to } \text{€}30\text{ bn}$): 
   $$(\text{€}30 - \text{€}1)\text{ bn} \times 15\% = \text{€}29\text{ bn} \times 15\% = \text{€}4.35\text{ bn}$$
3. **Third Bracket** ($> \text{€}30\text{ bn}$): 
   $$(\text{€}35 - \text{€}30)\text{ bn} \times 18\% = \text{€}5\text{ bn} \times 18\% = \text{€}0.90\text{ bn}$$

$$\text{Total BIC} = 0.12 + 4.35 + 0.90 = \text{€}5.37\text{ billion}$$

---

## Pillar 3 Disclosure

The BIC must be disclosed in two templates under the Basel III Pillar 3 framework. See [[Operational Risk Disclosure Templates]] for the full report layouts.

* **Template OR2** (row 5): The BIC derived from the BI and marginal coefficients, reported alongside the full BI subcomponent breakdown [[raw/DIS60.pdf#page=5]].
* **Template OR3** (row 1): The BIC used for calculating the minimum regulatory capital requirement for operational risk [[raw/DIS60.pdf#page=7]].

These two values are linked: `[OR2:5/a]` equals `[OR3:1/a]` [[raw/DIS60.pdf#page=7]].

---

## See Also

* [[Standardised Measurement Approach]]
* [[Business Indicator Calculation]]
* [[Internal Loss Multiplier]]
* [[Operational Risk Disclosure Templates]]
