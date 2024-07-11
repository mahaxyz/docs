---
description: >-
  The stability pool acts as a strong mechanism to substantially support the
  protocol by providing incentives to pooled users
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Stability Pool and Liquidation

Liquidations and stability pools are crucial components of MAHA ecosystem, it ensures the solvency of the system by maintaining the total supply of stablecoins backed by collateral.

## What is stability pool?

The stability pool is a liquidity pool that maintains the solvency of the protocol by ensuring that the total supply of stablecoin ZAI is always backed by collateral. They provide the necessary liquidity to cover the debt from liquidated loans. Stability pools are funded by users, known as stability providers, who deposit ZAI into the pool. Over time, these providers see a proportional reduction in their ZAI deposits but gain a proportional share of the liquidated collateral.

{% hint style="info" %}
The stability pool is currently deployed at:

_TBD_
{% endhint %}

## **Liquidations**

When a vault falls below a minimum collateral ratio of 110%, it is liquidated. The debt of the liquidated asset is canceled, and the collateral is transferred to the stability pool. The stability pool then uses this collateral to repay the debt.

Even though the loan is liquidated, the borrower keeps the full amount of ZAI borrowed but suffers a loss of up to 20% in value. Therefore, it's important for borrowers to maintain their collateral ratio above the minimum threshold of 110%, ideally aiming for 150% or higher.

## **Redistribution Mechanism**

If the stability pool lacks funds when liquidations occur, a secondary mechanism called redistribution is used. In this scenario, the system redistributes the debt and collateral from liquidated vaults to all other existing vaults, ensuring that liquidations remain profitable even in times of low liquidity

## Liquidators

Anyone can initiate the liquidation of a loan once its collateral ratio falls below the Minimum Collateral Ratio of 110%. To encourage this action, liquidators receive a gas compensation.

Liquidating loans involves gas costs, which the liquidator must cover. To reduce these costs, MAHA allows batch liquidations of multiple loans. However, to ensure profitability even when gas prices are high, the protocol provides gas compensation based on the following formula:

**Gas Compensation** = 200 ZAI ($USDz) + 0.5% of the loan's collateral.

The 200 ZAI ($USDz) is taken from the Liquidation Reserve, while the 0.5% comes from the liquidated collateral, slightly reducing the liquidation gain for stability providers.

## Liquidation Rules

Liquidations occur under different conditions based on the Individual Collateral Ratio (ICR), Minimum Collateral Ratio (MCR), and Global Total Collateral Ratio (GTCR). Here are the scenarios:

* **ICR <= 100%**: Redistribute all debt and collateral (minus gas compensation) to active loans.
* **100% < ICR < MCR**: The stability pool covers the debt from the loan. A fraction of the loan's collateral is shared among depositors. Any remaining debt and collateral (minus gas compensation) is redistributed to active loans.
* **GTCR < 150% & MCR <= ICR < GTCR & stability pool ZAI >= loan debt**: The protocol enters recovery mode. The stability pool covers the debt, and a fraction of collateral equal to 1.2 times the debt is shared among depositors. The borrower can claim any remaining collateral.

## Claiming Liquidated Collateral

Collateral transferred to the stability pool during liquidations can be claimed by depositors. Before claiming, users must accrue their current apportioned amounts through operations like depositing to the pool, withdrawing from the pool, or claiming MAHA rewards.

To avoid extra transactions, users can check if their claimable balance is up to date using a client-side check. If the check passes, they can call `claimCollateralGains` using the indexes with non-zero claimable amounts. If the check fails, they must claim any pending MAHA rewards first or send a transaction to update their claimable balance.
