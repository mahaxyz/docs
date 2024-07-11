---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Redemptions with User-set Interest Rate

The introduction of user-set interest rates significantly changes the redemption process within the ZAI protocol. Here's how redemptions will work with this new system:

## How Redemptions Work

When ZAI is redeemed, the collateral provided to the redeemer is allocated from loans with the lowest interest rates first, rather than the lowest collateral ratios. This ensures that the risk and cost are fairly distributed based on the rates borrowers choose.

### Detailed Overview

1. **Redemption Trigger**: A user initiates a redemption by exchanging ZAI for its equivalent value in collateral (e.g., rzETH).
2. **Selection of Loans**: The MAHA protocol identifies the loans with the lowest interest rates for redemption. These loans are prioritized, as borrowers with lower interest rates have agreed to a higher risk of redemption.
3. **Repayment and Collateral Transfer**: The redeemed ZAI is used to repay the debt of these selected loans. The corresponding collateral is transferred to the redeemer.

#### Example

1. **Loan Details**:
   * Borrower A: 10,000 ZAI debt, 2% interest rate, 50 rzETH collateral.
   * Borrower B: 10,000 ZAI debt, 5% interest rate, 50 rzETH collateral.
2. **Redemption Initiation**:
   * A user redeems 5,000 ZAI.
3. **Redemption Process**:
   * Borrower A's loan is partially redeemed first due to the lower interest rate.
   * 5,000 ZAI of Borrower A’s debt is repaid, reducing their debt to 5,000 ZAI. Correspondingly, 25 ETH (worth 5,000 ZAI) is transferred to the redeemer.
   * Borrower B's loan remains unaffected.
4. **Impact**:
   * Borrower A’s risk strategy means they face redemption first, but they benefit from a lower interest rate.
   * Borrower B’s higher interest rate keeps them safer from redemptions but at a higher cost.

## Benefits of This Approach

* **Market-Driven**: Aligns redemption risks with the interest rates set by borrowers, ensuring fair distribution of risk.
* **Flexibility**: Borrowers can manage their redemption risk by adjusting their interest rates.
* **Efficiency**: Creates a dynamic system that responds to market conditions, helping to maintain the stability of ZAI.

{% hint style="info" %}
User-set interest rates in the ZAI protocol ensure that redemptions are handled in a fair and market-driven manner, providing flexibility and efficiency for all participants.
{% endhint %}

## Stability Fees

For each redemption, the ZAI holder must pay a fee, which is a percentage of the value being liquidated in MAHA tokens. This fee helps control the rate of redemptions and prevent negative price impacts if too many redemptions happen too quickly. The stability fee is managed through governance.

By keeping these processes in place, ZAI maintains its value and provides a secure and stable environment for users
