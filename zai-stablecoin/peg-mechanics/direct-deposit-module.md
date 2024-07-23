---
description: This page explains the Direct Deposit Module (DDM) and how it works.
---

# Direct Deposit Module

The ZAI Direct Deposit Module (DDM) integrates ZAI with various lending pools and other DeFi protocols. This allows the MAHA ecosystem to generate ZAI dynamically to manage liquidity and stabilize interest rates in lending pools. This capability ensures that borrowing costs remain predictable and that sufficient liquidity is always available.

**Example: Lending an LRT (Liquidity Restaking Token) and Borrowing ZAI**

1. **Lending LRT**:
   * A user deposits LRT into the MAHA lending platform.
   * The platform allows users to borrow ZAI against their LRT collateral.
   * The borrowing interest rate is determined by the utilization rate of the ZAI pool.
2. **Managing Interest Rates**:
   * The variable interest rate in lending pools depends on the utilization ratio (total debt/total liquidity).
   * When the utilization is high, interest rates increase, making borrowing more expensive.
3. **D3M Intervention**:
   * If the borrowing interest rate exceeds the target set by MAHA governance, the D3M deposits additional ZAI into the lending pool.
   * This increases the pool’s liquidity, reducing the utilization rate and lowering the interest rate.
   * Conversely, if the interest rate is too low, indicating underutilization, the D3M can withdraw ZAI from the pool, raising the utilization rate and stabilizing the interest rate.
4. **Generating ZAI**:
   * The D3M can generate ZAI on the fly without traditional collateral.
   * This is done by operating on a special ilk (a type of collateral) with a fixed rate and spot price set to 1.
   * The generated ZAI is backed by aZAI (interest-bearing ZAI tokens), ensuring full collateralization.
5. **Interest Earnings**:
   * The ZAI deposited into lending pools earns interest.
   * This benefits the entire MAHA ecosystem by providing additional revenue streams.
