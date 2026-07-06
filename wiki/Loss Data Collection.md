---
tags: [data, collection, regulation, OPE]
sources:
  - "[[raw/OPE.pdf]]"
  - "[[raw/DIS60.pdf]]"
  - "[[raw/DIS10_20260101_20240717.xlsx]]"
created: 2026-07-02
---
# Loss Data Collection

The proper identification, collection, and treatment of internal loss data are essential regulatory requirements for banks using the standardised approach to calculate operational risk capital. High-quality loss data is a direct input for the calculation of the [[Internal Loss Multiplier|Loss Component (LC)]] [[raw/OPE.pdf#page=12]].

---

## 1. Materiality Thresholds

To be included in the Loss Component calculation dataset, an operational loss event must meet the materiality threshold [[raw/OPE.pdf#page=14]]:
* **Standard Threshold**: **€20,000** (net of recoveries) [[raw/OPE.pdf#page=14]].
* **Supervisory Discretion**: National supervisors may increase the threshold to **€100,000** for banks in Buckets 2 and 3 [[raw/OPE.pdf#page=14]].
* **Cumulative Impact**: For events that result in multiple accounting impacts over time, the net loss is calculated by summing all impacts within the 10-year window and subtracting all recoveries. If the cumulative net total equals or exceeds the threshold, the event must be included [[raw/OPE.pdf#page=14-15]].

---

## 2. Gross Loss vs. Net Loss

Banks must identify and collect both gross loss and recovery information for every event.

### Gross Loss Components
Gross loss is the loss before any recoveries. The following items **must be included** in the gross loss computation [[raw/OPE.pdf#page=16]]:
1. **Direct Charges**: Impairments, settlements, write-offs, and P&L charges.
2. **Direct Expenses**: Legal fees directly linked to the event, advisor fees, and repair/replacement costs to restore the bank's position.
3. **Provisions**: P&L provisions or reserves set aside against potential operational loss impacts.
4. **Pending Losses**: Transitory or suspense account items with a definitive financial impact not yet reflected in the P&L.
5. **Timing Losses**: Negative economic impacts stemming from operational risk events that distort previous financial periods and give rise to legal risk.

### Excluded Items
The following items **must be excluded** from gross loss [[raw/OPE.pdf#page=18]]:
* Costs of general maintenance contracts on property, plant, or equipment.
* Expenses incurred to enhance or upgrade the business after a loss (upgrades, risk assessment initiatives).
* Paid insurance premiums.

### Recoveries
Net loss is calculated by subtracting recoveries from the gross loss [[raw/OPE.pdf#page=15]]. 
* **Eligible Recoveries**: Payments actually received from a third party (e.g., insurance payouts, fraud repayments, or recovered transfers) [[raw/OPE.pdf#page=15-16]].
* **Exclusion**: Receivables (expected recoveries not yet paid) cannot be used to reduce loss amounts [[raw/OPE.pdf#page=16]].

---

## 3. Required Data Fields

For every recorded operational loss event, the database must capture [[raw/OPE.pdf#page=15]]:
* **Gross Loss & Recovery Amounts**
* **Reference Dates**:
  * *Date of Occurrence*: When the event started or happened.
  * *Date of Discovery*: When the bank became aware of the event.
  * *Date of Accounting*: When the loss or provision was first recognized in the P&L.
* **Descriptive Information**: Contextual details on the drivers and root causes of the loss.
* **Supervisory Mapping**: Mapping of the event to the 7 regulatory [[Operational Risk Event Categories|event categories]].

---

## 4. Special Treatments

* **Grouped Losses**: Multiple losses caused by a common underlying trigger or root cause must be grouped and treated as a single operational loss event [[raw/OPE.pdf#page=18]].
* **Loss Exclusions**: A bank may request supervisory approval to exclude a historical loss event from the LC if it is no longer relevant to its risk profile (e.g., a completely divested business unit). This is rare, requires strong justification, and is subject to a materiality threshold (e.g., the event must represent >5% of the bank's average losses) [[raw/OPE.pdf#page=18-19]].

---

## 5. Pillar 3 Disclosure

Historical loss data must be publicly disclosed under **Template OR1 – Historical losses** [[raw/DIS60.pdf#page=3]]. See [[Operational Risk Disclosure Templates]] for the full report layout. Key requirements:

* **Scope**: Mandatory for all banks in BI Buckets 2 and 3 (regardless of whether their supervisor has set $ILM = 1$), and Bucket 1 banks approved to use internal loss data [[raw/DIS60.pdf#page=3]].
* **Thresholds**: The template provides parallel sections for both the €20,000 and €100,000 loss event thresholds, reporting total losses net of recoveries, total number of losses, excluded amounts, and exclusion counts [[raw/DIS60.pdf#page=3-4]].
* **10-Year History**: Loss amounts must be reported for each of the last 10 years (T through T-9), plus a 10-year average in column (k) [[raw/DIS60.pdf#page=3-4]].
* **Narrative**: Banks must explain the rationale, in aggregate, for any new loss exclusions since the previous disclosure [[raw/DIS60.pdf#page=3]].

---

## See Also

* [[Standardised Measurement Approach]]
* [[Internal Loss Multiplier]]
* [[Operational Risk Event Categories]]
* [[Operational Risk Disclosure Templates]]
