---
tags: [regulation, capital, math, OPE]
sources:
  - "[[raw/OPE.pdf]]"
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

## See Also

* [[Standardised Measurement Approach]]
* [[Business Indicator Component]]
* [[Loss Data Collection]]
