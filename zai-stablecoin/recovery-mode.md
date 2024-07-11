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

Recovery Mode is a crucial safety feature within the MAHA protocol. It is activated to maintain the system's financial stability. It is triggered when the Global Total Collateral Ratio (GTCR) drops below 150%.&#x20;

The primary goal of Recovery Mode is to prevent erosion of the system's collateral base and ensure the protocol remains resilient against market volatility.

During Recovery Mode, liquidation conditions are relaxed, and the system blocks borrower transactions that would further decrease the GTCR.

The only way new ZAI ($USDz) can be generated during this period is by improving the collateral ratio of existing vaults or by creating new vaults with a collateral ratio of 150% or higher.

{% hint style="warning" %}
If the protocol goes into recovery mode, then loans with a collateral ratio **below `150%`**can be liquidated until the protocol comes back out of recovery mode.

In general, borrowers are encouraged to always maintain a collateral ratio above`150%`.

To understand more about this behavior, read [recovery mode liquidations](recovery-mode.md#impact-on-liquidations).
{% endhint %}

## Liquidation Policies During Recovery Mode

In Recovery Mode, vaults with a collateral ratio below the system-wide GTCR are at risk of liquidation. The protocol halts transactions that could further decrease the GTCR, focusing on stabilizing the system's financial health.

## Rationale for Recovery Mode

The main objective of Recovery Mode is to encourage actions that quickly increase the GTCR above 150% and motivate ZAI ($USDz) holders to contribute to the Stability Pool. This mode promotes additional collateral deposits and debt repayments, aiming to stabilize the system swiftly. The very possibility of entering Recovery Mode acts as a preventive measure, encouraging users to maintain healthy collateral ratios.

## Impact on Fees

During Recovery Mode, the minting fee is reduced to 0% to stimulate borrowing activities that positively impact the GTCR. However, the redemption fee remains unchanged.

## Impact on Liquidations

In Recovery Mode, if your vault’s Individual Collateral Ratio (ICR) falls below the GTCR, your vault can be liquidated, even if your collateral ratio is above 110%. To avoid this, users should maintain their collateral ratio above 150% in both Normal and Recovery Mode.

During Recovery Mode, the liquidation loss is capped at 110% of a vault's collateral. Any collateral above 110% (and below the GTCR) can be claimed back by the borrower. This means that a borrower will face the same liquidation "penalty" (20%) in Recovery Mode as they would in Normal Mode if their vault is liquidated.

{% hint style="info" %}
As a system design, Recovery Mode is best avoided. Thus, the possibility of going into recovery mode should be a crucial point for ecosystem participants to make amends to their position, to ensure that they do not go into Recovery Mode
{% endhint %}
