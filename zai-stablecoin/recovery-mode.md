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

# Recovery Mode

Recovery Mode is a crucial safety feature within the MAHA protocol, activated to maintain the system's financial stability. It is triggered when the Global Total Collateral Ratio (GTCR) drops below 150%. The primary goal of Recovery Mode is to prevent erosion of the system's collateral base and ensure the protocol remains resilient against market volatility.

When Recovery Mode is activated, borrower transactions that could worsen the GTCR are halted. The only way new ZAI ($USDz) can be generated during this period is by improving the collateral ratio of existing vaults or by creating new vaults with a collateral ratio of 150% or higher.

## What is GTCR?

The Global Total Collateral Ratio (GTCR) refers to the ratio of the total value of all collaterals within the protocol (valued at current prices) to the total outstanding debt across the protocol. In simpler terms, it is the total value of all vaults' collateral measured in USD divided by the cumulative debt of all vaults in ZAI ($USDz).

## Why Recovery Mode?

Recovery Mode aims to quickly restore the GTCR above 150% by encouraging positive contributions to the Stability Pool and strategic debt repayments. During this period, minting fees are eliminated, while redemption fees remain unchanged. Liquidation rules are adjusted to allow borrowers to recover excess collateral, minimizing potential losses.

## Liquidation Policies During Recovery Mode

In Recovery Mode, vaults with a collateral ratio below the system-wide GTCR are at risk of liquidation. The protocol halts transactions that could further decrease the GTCR, focusing on stabilizing the system's financial health.

## Rationale for Recovery Mode

The main objective of Recovery Mode is to encourage actions that quickly increase the GTCR above 150% and motivate ZAI ($USDz) holders to contribute to the Stability Pool. This mode promotes additional collateral deposits and debt repayments, aiming to stabilize the system swiftly. The very possibility of entering Recovery Mode acts as a preventive measure, encouraging users to maintain healthy collateral ratios.

## Impact on Fees

During Recovery Mode, the minting fee is reduced to 0% to stimulate borrowing activities that positively impact the GTCR. However, the redemption fee remains unchanged.

## Impact on Liquidations

In Recovery Mode, if your vault’s Individual Collateral Ratio (ICR) falls below the GTCR, your vault can be liquidated, even if your collateral ratio is above 110%. To avoid this, users should maintain their collateral ratio above 150% in both Normal and Recovery Mode.

During Recovery Mode, the liquidation loss is capped at 110% of a vault's collateral. Any collateral above 110% (and below the GTCR) can be claimed back by the borrower. This means that a borrower will face the same liquidation "penalty" (20%) in Recovery Mode as they would in Normal Mode if their vault is liquidated.
