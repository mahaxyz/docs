---
description: >-
  This section of the document describes the PSM and how it contributes to the
  stability of ZAI
---

# Peg Stablility Module

## Minting of ZAI via Peg Stability Module

The Peg Stability Module (PSM) is a crucial mechanism for minting ZAI, designed to maintain its peg to the USD. Inspired by MakerDAO's PSM for DAI, the ZAI PSM allows users to mint and redeem ZAI at a 1:1 ratio with supported stablecoins like USDC and DAI.

### **Exchange Mechanism**

The PSM enables users to directly swap stablecoins such as USDC for ZAI and vice versa at a 1:1 ratio, minimizing slippage and fees. For instance, users can exchange 1 USDC for 1 ZAI or 1 ZAI for 1 USDC without significant price fluctuations.

### **Liquidity Provision**

By holding reserves of stablecoins, the PSM provides liquidity to stabilize the ZAI peg. When demand for ZAI increases and its price exceeds $1, users can sell ZAI to the PSM in exchange for USDC. Conversely, if ZAI’s price drops below $1, users can buy ZAI from the PSM using USDC.

### **Market Arbitrage**

The fixed exchange rate provided by the PSM encourages arbitrage. If ZAI trades above $1, arbitrageurs can exchange USDC for ZAI through the PSM and sell ZAI on the open market, increasing the supply of ZAI and pushing its price back toward $1. If ZAI trades below $1, arbitrageurs can buy ZAI cheaply on the open market, exchange it for USDC through the PSM, and sell USDC at a profit, reducing the supply of ZAI and pushing its price back up toward $1.

## **How MAHA Eliminated Stability Pools and Liquidations?**

Traditional stablecoin systems often rely on stability pools and liquidation mechanisms to maintain the peg and manage collateral. MAHA's innovative approach with the PSM eliminates the need for these traditional methods:

* **No Stability Pools**: Stability pools are typically used to cover the shortfall in case of liquidations. With the PSM, since ZAI is always backed 1:1 by stablecoins, there is no need for stability pools.
* **No Liquidations**: Liquidations occur when the value of collateral falls below a certain threshold. The PSM's 1:1 backing ensures that ZAI is always fully collateralized, removing the need for liquidations. Users can always redeem ZAI for the stablecoins they deposited, ensuring stability without the risk of under-collateralization.

### Minting and redeeming of ZAI

* **Minting ZAI:**
  * Users deposit stablecoins (e.g., 1 USDC) into the PSM.
  * In return, the system mints an equivalent amount of ZAI (e.g., 1 ZAI).
  * The deposited stablecoins are locked as collateral within the system.
* **Redeeming Stablecoins:**
  * Users deposit ZAI back into the PSM.
  * The system unlocks and returns an equivalent amount of the deposited stablecoins (e.g., 1 ZAI for 1 USDC).
