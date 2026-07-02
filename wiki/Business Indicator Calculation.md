---
tags: [regulation, capital, math, OPE]
sources:
  - "[[raw/OPE.pdf]]"
created: 2026-07-02
---
# Business Indicator Calculation

The **Business Indicator (BI)** is a financial-statement-based proxy used to measure a bank's operational risk exposure. It is calculated as the sum of three components, representing interest/lease/dividend, services, and trading/financial activities respectively [[raw/OPE.pdf#page=10]]:

$$BI = ILDC + SC + FC$$

Each of the components ($ILDC, SC, FC$) is calculated as a three-year average (over years $t$, $t-1$, and $t-2$). A bar above a term indicates a three-year average calculation.

---

## 1. Interest, Lease, and Dividend Component (ILDC)

The ILDC measures the net interest income generation adjusted for assets and dividend yields [[raw/OPE.pdf#page=10]]:

$$ILDC = \min\left(\overline{\text{Abs}(\text{Interest Income} - \text{Interest Expense})}, 2.25\% \times \overline{\text{Interest Earning Assets}}\right) + \overline{\text{Dividend Income}}$$

> [!important] Calculations Order
> The absolute value of the net interest item ($\text{Abs}(\text{Interest Income} - \text{Interest Expense})$) must be calculated year-by-year first. The three-year average is then taken of these absolute values [[raw/OPE.pdf#page=10]].

* **Interest Income**: Interest income from all financial assets (loans, advances, trading assets, etc.) and leases [[raw/OPE.pdf#page=5]].
* **Interest Expense**: Interest expenses from all financial liabilities and leases (including depreciation and impairment of operating leased assets) [[raw/OPE.pdf#page=5]].
* **Interest Earning Assets**: Total gross outstanding loans, advances, interest-bearing securities, and lease assets measured at the end of each financial year [[raw/OPE.pdf#page=5]].
* **Dividend Income**: Dividend income from investments in stocks and funds not consolidated in the bank's financial statements [[raw/OPE.pdf#page=5]].

---

## 2. Services Component (SC)

The SC captures fee-based business and other operating income/expenses [[raw/OPE.pdf#page=10]]:

$$SC = \max\left(\overline{\text{Other Operating Income}}, \overline{\text{Other Operating Expenses}}\right) + \max\left(\overline{\text{Fee Income}}, \overline{\text{Fee Expense}}\right)$$

* **Fee Income / Expense**: Income/expenses from providing or receiving advice and financial services (e.g., asset management, custody, payment services, clearing/settlement) [[raw/OPE.pdf#page=5-6]].
* **Other Operating Income**: Income from ordinary banking operations not included in other BI items (excluding income from operating leases) [[raw/OPE.pdf#page=6]].
* **Other Operating Expenses**: Expenses and losses from ordinary banking operations not included in other BI items, including those stemming from operational loss events [[raw/OPE.pdf#page=6]].

---

## 3. Financial Component (FC)

The FC reflects the volatility and size of the bank's trading and investment books [[raw/OPE.pdf#page=10]]:

$$FC = \overline{\text{Abs}(\text{Net Trading Book P\&L})} + \overline{\text{Abs}(\text{Net Banking Book P\&L})}$$

* **Net Trading Book P&L**: Net profit/loss on trading assets and liabilities (derivatives, short positions, etc.) including hedge accounting and exchange differences [[raw/OPE.pdf#page=6]].
* **Net Banking Book P&L**: Net profit/loss on financial assets/liabilities measured at fair value through P&L, realized gains/losses on items measured at amortized cost, hedge accounting, and exchange differences [[raw/OPE.pdf#page=7]].

---

## Excluded Profit and Loss Items

According to section 10.3 of the regulatory standard, the following items **do not contribute** to the Business Indicator calculation [[raw/OPE.pdf#page=7]]:
1. Income and expenses from insurance or reinsurance businesses.
2. Administrative expenses (e.g., staff expenses, IT, utilities, office supplies, postage).
3. Outsourcing fees paid for the supply of non-financial services (e.g., logistical, HR, IT).
4. Expenses of premises and fixed assets (unless they directly result from operational loss events).
5. Depreciation/amortization of tangible and intangible assets (except lease assets).
6. Corporate income tax (current and deferred).

---

## See Also

* [[Standardised Measurement Approach]]
* [[Business Indicator Component]]
* [[Internal Loss Multiplier]]
* [[Loss Data Collection]]
