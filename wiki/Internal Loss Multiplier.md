---
tags: [regulation, capital, math, OPE]
sources:
  - "[[raw/OPE.pdf]]"
  - "[[raw/DIS60.pdf]]"
  - "[[raw/DIS10_20260101_20240717.xlsx]]"
created: 2026-07-02
---
# Internal Loss Multiplier

The **Internal Loss Multiplier (ILM)** is a risk-sensitive scaling factor that adjusts a bank's baseline capital requirement (BIC) based on its historical operational risk loss experience over the prior decade [[raw/OPE.pdf#page=11]].

---

## The Formula

The ILM is calculated using the following mathematical function [[raw/OPE.pdf#page=11]]:

$$ILM = \ln\left(\exp(1) - 1 + \left(\frac{LC}{BIC}\right)^{0.8}\right)$$

Where:
* **$\exp(1)$** is Euler's number ($e \approx 2.7183$)
* **$BIC$** is the [[Business Indicator Component]]
* **$LC$** is the **Loss Component**, defined as [[raw/OPE.pdf#page=11]]:

$$LC = 15 \times \text{Average Annual Operational Risk Losses}$$

> [!note] Net Losses
> The average annual operational risk losses must be calculated **net of recoveries** (both insurance and non-insurance recoveries) [[raw/OPE.pdf#page=11]].

---

## Behaviour of the Multiplier

The relationship between the Loss Component ($LC$) and the Business Indicator Component ($BIC$) determines the scaling effect [[raw/OPE.pdf#page=11]]:

* **Neutral ($ILM = 1$)**: When historical losses are proportional to bank size ($LC = BIC$), the multiplier is exactly 1.
* **Capital Surcharge ($ILM > 1$)**: When a bank has high historical losses relative to its size ($LC > BIC$), the ILM is greater than 1, requiring the bank to hold additional capital.
* **Capital Discount ($ILM < 1$)**: When a bank has successfully managed operational risk and exhibits low historical losses ($LC < BIC$), the ILM is less than 1, reducing the capital requirement.

---

## Regulatory Rules and Exceptions

* **Bucket 1 Banks ($BI \le \text{€}1\text{ bn}$)**: The ILM is set to 1 by default ($ORC = BIC$) [[raw/OPE.pdf#page=11]]. However, national supervisors have the discretion to allow or require these banks to calculate their ILM using internal loss data.
* **Data Quality Threshold**: Calculation of the LC requires a minimum of **10 years** of high-quality loss data [[raw/OPE.pdf#page=11]]. During transition, a minimum of **5 years** of data may be accepted.
* **Default to 1**: If a bank in Bucket 2 or 3 does not have at least 5 years of high-quality loss data, it must calculate its capital requirement based solely on the BIC (effectively forcing $ILM = 1$) [[raw/OPE.pdf#page=11]]. Supervisors may also apply a multiplier greater than 1 if compliance with qualitative standards is poor [[raw/OPE.pdf#page=12]].

---

## Derivation

The formula is an **empirical regulatory formula** designed by the Basel Committee on Banking Supervision (BCBS), not derived from first mathematical principles. It is designed to achieve specific policy goals:
1. Ensuring an anchor point where $LC = BIC$ yields exactly an $ILM = 1$.
2. Providing a non-linear transition that rewards good risk management while penalizing poor risk management.
3. Using the $0.8$ exponent and the logarithmic dampening to prevent capital requirements from being overly sensitive to single, massive "fat-tail" loss events common in operational risk.

---

## Intuitive Number Explanation (Why `ln` and `e`)

A simple way to read the formula is to define a ratio:

$$r = \frac{LC}{BIC}$$

Then:

$$ILM = \ln\left(e - 1 + r^{0.8}\right)$$

This form gives four useful properties:

1. **Neutral anchor at 1**: if $r = 1$ then
  $$ILM = \ln(e - 1 + 1) = \ln(e) = 1$$
  This is exactly why the constant $(e - 1)$ appears.

2. **Controlled discount floor**: as $r \to 0$,
  $$ILM \to \ln(e - 1) \approx 0.5413$$
  So even with very low losses, capital is not reduced to near zero.

3. **Surcharge grows, but smoothly**: when $r > 1$, ILM increases above 1, but the logarithm dampens very large increases.

4. **Tail dampening**: the exponent $0.8$ makes the response less aggressive than a linear $r^1$ relationship.

### Numeric Examples

| $LC/BIC$ ratio ($r$) | ILM | Interpretation |
| :---: | :---: | :--- |
| 0.10 | 0.6298 | Large discount, but bounded by the floor |
| 0.25 | 0.7168 | Discount |
| 0.50 | 0.8298 | Discount |
| 1.00 | 1.0000 | Neutral |
| 1.20 | 1.0562 | Mild surcharge |
| 2.00 | 1.2411 | Surcharge |
| 4.00 | 1.5581 | Strong surcharge, still smoothed |

In short, the structure with $\ln(\cdot)$ and $(e-1)$ is a calibration choice that gives a stable, smooth, and interpretable multiplier around the policy anchor $ILM=1$.

---

## Calculation Example

Assume a hypothetical mid-sized bank with the following metrics:
* **Business Indicator Component (BIC):** €100,000,000 
* **Average Annual Operational Risk Losses (over 10 years):** €8,000,000

**Step 1: Calculate the Loss Component (LC)**
$$LC = 15 \times 8,000,000 = \text{€}120,000,000$$

**Step 2: Calculate the Ratio ($LC / BIC$)**
$$\frac{LC}{BIC} = \frac{120,000,000}{100,000,000} = 1.2$$
*(Because $LC > BIC$, the ILM will be greater than 1, resulting in a capital surcharge).*

**Step 3: Apply the Exponent**
$$1.2^{0.8} \approx 1.157$$

**Step 4: Plug into the main formula**
$$ILM = \ln(\exp(1) - 1 + 1.157)$$
$$ILM \approx \ln(1.7183 + 1.157)$$
$$ILM = \ln(2.8753)$$
**$ILM \approx 1.056$**

**Conclusion:**
Because the bank's operational losses were historically high relative to its size, its Internal Loss Multiplier is `1.056`. Its final Operational Risk Capital ($ORC$) would be $BIC \times ILM = \text{€}100,000,000 \times 1.056 = \text{€}105,600,000$, representing a 5.6% capital surcharge.

---

## Pillar 3 Disclosure

Under the Basel III Pillar 3 disclosure framework, the ILM must be publicly reported annually. See [[Operational Risk Disclosure Templates]] for all template layouts. The two templates directly relevant to the ILM are shown below.

### Template OR3 — Minimum Required Operational Risk Capital

The ILM is disclosed in **row 2** of this template [[raw/DIS60.pdf#page=8]] [[raw/DIS10_20260101_20240717.xlsx]]:

| Row | Description | Value (a) |
| :---: | :--- | :---: |
| **1** | [[Business Indicator Component\|Business indicator component (BIC)]] | |
| **2** | **[[Internal Loss Multiplier\|Internal loss multiplier (ILM)]]** | |
| **3** | Minimum required operational risk capital (ORC) | |
| **4** | Operational risk RWA | |

* **Row 2**: The ILM value used for calculating minimum regulatory capital requirements. Where national jurisdictions choose to exclude losses, the $ILM$ is set equal to 1.
* **Row 3**: $ORC = BIC \times ILM$ (or just $BIC$ if losses are not used).
* **Row 4**: $RWA = 12.5 \times ORC$.

### Template OR1 — Historical Losses (ILM-related rows)

Whether and how losses feed the ILM is disclosed in **rows 11–13** of Template OR1 [[raw/DIS60.pdf#page=4]] [[raw/DIS10_20260101_20240717.xlsx]]:

| Row | Description | T | T–1 | … | T–9 | 10yr Avg |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: |
| **1** | Total amount of operational losses net of recoveries (no exclusions) | | | | | |
| **2** | Total number of operational risk losses | | | | | |
| **3** | Total amount of excluded operational risk losses | | | | | |
| **4** | Total number of exclusions | | | | | |
| **5** | Total amount of operational losses net of recoveries and net of excluded losses | | | | | |

*(Rows 6–10 repeat the above using the €100,000 threshold.)*

| Row | Description | Value |
| :---: | :--- | :---: |
| **11** | Are losses used to calculate the ILM? (yes/no) | |
| **12** | If "no" in row 11, is the exclusion due to non-compliance with minimum loss data standards? (yes/no) | |
| **13** | Loss event threshold: €20,000 or €100,000 for the capital calculation | |

> [!note] National Discretion
> Where national jurisdictions choose to exclude losses from the operational risk calculation, the ILM is set equal to one and disclosed accordingly [[raw/DIS60.pdf#page=8]]. Any resulting multipliers from non-compliance with data standards must be disclosed in OR3 row 2 with narrative [[raw/DIS60.pdf#page=4]].

---

## See Also

* [[Standardised Measurement Approach]]
* [[Business Indicator Component]]
* [[Loss Data Collection]]
* [[Operational Risk Disclosure Templates]]
