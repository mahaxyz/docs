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

# Collateralization Mechanism

Every ZAI ($USDz) minted is over-collateralized with LRTs such as Renzo Restaked ETH (rzETH). Borrowers must maintain a collateral ratio above 110% to avoid liquidation. Higher collateral ratios reduce the risk of liquidation, providing more security for borrowers.

Here are the key collateral ratios to understand:

## 1. Individual Collateralization Ratio (ICR)

The Individual Collateralization Ratio (ICR) determines how much ZAI ($USDz) a borrower will receive for a specific LRT they are willing to collateralize.

* The ICR is set by the user when opening a loan and can be adjusted later by adding or removing collateral or debt.
* The minimum ICR required is 110%.

**Examples:**

* **Example 1**: If User A sets an ICR of 110% and creates a position of $10,000 in ZAI ($USDz), they must collateralize at least $11,000 worth of rsETH. This position is highly prone to liquidation if the ICR falls below 110%.
* **Example 2**: If User B sets an ICR of 150% and creates a position of $10,000 in ZAI ($USDz), they must collateralize at least $15,000 worth of rsETH. This position is more secure than Example 1.

Higher ICR means a user's position is less prone to liquidation but results in receiving less ZAI ($USDz) for the collateralized asset. A lower ICR means the user's position is more prone to liquidation but results in receiving more ZAI ($USDz) for their collateral.

## 2. Minimum Collateralization Ratio (MCR)

The Minimum Collateralization Ratio (MCR) is the lowest ratio of collateral that will not trigger liquidation. Under normal conditions, this is set at 110%.

{% hint style="info" %}
In recovery mode, the MCR is set to 150%. To avoid liquidation during Recovery Mode, it is recommended to maintain a ratio above 150%.
{% endhint %}

As a borrower, it is advisable to open a loan with a high enough collateral ratio (recommended 200%+) to avoid liquidation and loss of funds.

## 3. Total Collateral Ratio (TCR)

The Total Collateral Ratio (TCR) is the ratio of the dollar value of the entire system collateral at the current protocol price to the entire system debt.

This is calculated as the sum of the collateral of all loans (expressed in protocol price) divided by the debt of all loans (expressed in ZAI).

## 4. Nominal Collateral Ratio (NCR)

The Nominal Collateral Ratio (NCR) for a loan is its entire collateral (in rsETH) multiplied by 100e18 and divided by its entire debt.

#### Summary

* **ICR (Individual Collateralization Ratio)**: User-set ratio determining ZAI received per asset collateralized. Minimum 110%
* **MCR (Minimum Collateralization Ratio)**: Lowest ratio to avoid liquidation, set at 110% normally, and 150% in recovery mode.
* **TCR (Total Collateral Ratio)**: System-wide ratio of total collateral value to total debt.
* **NCR (Nominal Collateral Ratio)**: Ratio of a loan's total collateral to its total debt.
