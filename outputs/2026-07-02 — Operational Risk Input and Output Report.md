# Operational Risk Input and Output Report

**Date**: 2026-07-02  
**Purpose**: This report presents the analysis of the input data structure and the capital calculation outputs for operational risk under the Basel III Standardised Measurement Approach (SMA) based on the SAS scripts:
- Input data preparation: [00_PrepareData.sas](file:///d:/MyApp/SAS_OpRisk/Ref/00_PrepareData.sas)
- Capital & RWA calculation: [02_Calculate OpRisk RWA and Capital.sas](file:///d:/MyApp/SAS_OpRisk/Ref/02_Calculate%20OpRisk%20RWA%20and%20Capital.sas)

---

## 1. Input Data Structure

The calculation requires two primary input tables, configured in the SAS system as follows:

### 1.1 `OP_RISK_DATA`
This table holds the entity-specific historical financial metrics over a three-year period (designated as $Y0$ for the current year, $YM1$ for year minus one, and $YM2$ for year minus two).

| Field Name                                | Type           | Description                                                        |
| :---------------------------------------- | :------------- | :----------------------------------------------------------------- |
| **ENTITY_ID**                             | Character (32) | Unique identifier of the legal entity (Primary Key)                |
| **INTERNAL_ORG_RK**                       | Numeric (8)    | Internal organization surrogate key                                |
| **INTEREST_INCOME_Y[0/M1/M2]**            | Numeric (8)    | Interest income from loans, advances, trading assets, etc.         |
| **INTEREST_EXPENSES_Y[0/M1/M2]**          | Numeric (8)    | Interest expenses from liabilities and leases                      |
| **INTEREST_EARNING_ASSETS_Y[0/M1/M2]**    | Numeric (8)    | Gross outstanding loans, advances, and interest-bearing securities |
| **DIVIDEND_INCOME_Y[0/M1/M2]**            | Numeric (8)    | Dividend income from non-consolidated equity investments           |
| **FEE_COMMISSION_INCOME_Y[0/M1/M2]**      | Numeric (8)    | Fee income from financial services                                 |
| **FEE_COMMISSION_EXPENSES_Y[0/M1/M2]**    | Numeric (8)    | Fee expenses paid for financial services                           |
| **OTHER_OPE_INCOME_Y[0/M1/M2]**           | Numeric (8)    | Other operational income (excluding lease income)                  |
| **OTHER_OPE_EXPENSES_Y[0/M1/M2]**         | Numeric (8)    | Other operational expenses (excluding administrative expenses)     |
| **NET_PROFIT_LOSS_TRADING_BK_Y[0/M1/M2]** | Numeric (8)    | Net trading book profit/loss                                       |
| **NET_PROFIT_LOSS_BANKING_BK_Y[0/M1/M2]** | Numeric (8)    | Net banking book profit/loss                                       |
| **AVG_ANNUAL_OP_RISK_LOSSES**             | Numeric (8)    | Historical average annual operational risk loss net of recoveries  |

### 1.2 `X_MAP_BI_RANGE`
This table defines the progressive regulatory brackets and marginal coefficients ($\alpha_i$) for computing the Business Indicator Component (BIC).

| Bucket | BI Start Range | BI End Range | Marginal Coefficient |
| :---: | :--- | :--- | :---: |
| **1** | 0 | 1,000,000,000 | 12% |
| **2** | 1,000,000,000 | 30,000,000,000 | 15% |
| **3** | 30,000,000,000 | 1,000,000,000,000 | 18% |

---

## 2. Calculation Logic & Formulas

The operational risk capital requirement is calculated through the following steps:

### Step 2.1: Calculate 3-Year Averages
For all financial fields, three-year averages are computed. Note that net interest trading and banking book profit/losses are averaged using absolute values computed year-by-year:
*   $\text{Avg. Net Interest Income} = \text{mean}\left(\text{Abs}(I_{Y0} - E_{Y0}), \text{Abs}(I_{YM1} - E_{YM1}), \text{Abs}(I_{YM2} - E_{YM2})\right)$
*   $\text{Avg. Trading Book P\&L} = \text{mean}\left(\text{Abs}(T_{Y0}), \text{Abs}(T_{YM1}), \text{Abs}(T_{YM2})\right)$
*   $\text{Avg. Banking Book P\&L} = \text{mean}\left(\text{Abs}(B_{Y0}), \text{Abs}(B_{YM1}), \text{Abs}(B_{YM2})\right)$

### Step 2.2: Compute Business Indicator (BI) Components
*   **Interest, Lease, and Dividend Component (ILDC)**:
    $$ILDC = \min\left(\text{Avg. Net Interest Income}, 2.25\% \times \text{Avg. Interest Earning Assets}\right) + \text{Avg. Dividend Income}$$
*   **Services Component (SC)**:
    $$SC = \max\left(\text{Avg. Other Operating Income}, \text{Avg. Other Operating Expenses}\right) + \max\left(\text{Avg. Fee Income}, \text{Avg. Fee Expense}\right)$$
*   **Financial Component (FC)**:
    $$FC = \text{Avg. Trading Book P\&L} + \text{Avg. Banking Book P\&L}$$
*   **Business Indicator (BI)**:
    $$BI = ILDC + SC + FC$$

### Step 2.3: Compute Business Indicator Component (BIC)
Based on the BI value and the brackets from `X_MAP_BI_RANGE`, the BIC is computed using progressive marginal rates:
*   **If $BI \le \text{1,000,000,000}$**:
    $$BIC = BI \times 0.12$$
*   **If $\text{1,000,000,000} < BI \le \text{30,000,000,000}$**:
    $$BIC = (\text{1,000,000,000} \times 0.12) + (BI - \text{1,000,000,000}) \times 0.15$$
*   **If $BI > \text{30,000,000,000}$**:
    $$BIC = (\text{1,000,000,000} \times 0.12) + (\text{29,000,000,000} \times 0.15) + (BI - \text{30,000,000,000}) \times 0.18$$

### Step 2.4: Compute Loss Component (LC) and Internal Loss Multiplier (ILM)
*   **Loss Component (LC)**:
    $$LC = 15 \times \text{AVG\_ANNUAL\_OP\_RISK\_LOSSES}$$
*   **Internal Loss Multiplier (ILM)**:
    $$ILM = \ln\left(e - 1 + \left(\frac{LC}{BIC}\right)^{0.8}\right)$$
    *Where $e \approx 2.71828$ is Euler's number ($e-1 \approx 1.71828$).*

### Step 2.5: Compute Capital & RWA
*   **Operational Risk Capital (OP_RISK_CAPITAL)**:
    $$\text{Capital} = BIC \times ILM$$
*   **Operational Risk Risk-Weighted Assets (OP_RWA)**:
    $$\text{OP\_RWA} = \text{Capital} \times 12.5$$

---

## 3. Output Table (Calculated Results)

The following table presents the verified calculation results for the four legal entities specified in `00_PrepareData.sas`:

| Entity ID | Org RK | BI (Currency) | BIC (Currency) | LC (Currency) | ILM | Capital (Currency) | RWA (Currency) |
| :---: | :---: | :--- | :--- | :--- | :---: | :--- | :--- |
| **CLU** | 1000 | 6,556,666.67 | 786,800.00 | 600,000.00 | 0.9256 | 728,250.34 | 9,103,129.25 |
| **RLU** | 2000 | 6,678,333.33 | 801,400.00 | 1,500,000.00 | 1.2148 | 973,502.29 | 12,168,778.57 |
| **GLU** | 3000 | 19,558,750.00 | 2,347,050.00 | 7,500,000.00 | 1.4472 | 3,396,685.93 | 42,458,574.12 |
| **BHC** | 10000 | 33,291,666.67 | 3,995,000.00 | 4,500,000.00 | 1.0361 | 4,139,199.42 | 51,739,992.80 |

### Key Observations:
1.  **Scale and Buckets**: All four entities have Business Indicators (BI) well below the 1 billion threshold (ranging from 6.56 million to 33.29 million). Therefore, they all fall within **Bucket 1** where a flat 12% marginal coefficient is applied directly.
2.  **Internal Loss Multiplier (ILM) Sensitivity**:
    *   **CLU** has lower historical losses relative to its size ($LC < BIC$), resulting in an $ILM < 1$ (0.9256). This acts as a capital discount.
    *   **RLU**, **GLU**, and **BHC** have higher historical losses relative to their size ($LC > BIC$), leading to $ILM > 1$ and resulting in capital surcharges.
    *   **GLU** experiences the highest surcharge ($ILM = 1.4472$) due to a high Loss Component (7.5 million) compared to its BIC (2.35 million).
