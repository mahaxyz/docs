---
description: This page explains how the ZAI stablecoin maintains it's peg
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

# Peg Mechanics

The pegging mechanism of ZAI ($USDz) ensures that it maintains a 1:1 ratio with the US Dollar. This is achieved through a combination of collateralization, algorithmic adjustments, and market incentives.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

There are two core modules that allow for ZAI to achieve stability and scale.

* [The Peg Stability Module](peg-stablility-module-psm.md): Inspired by MakerDAO's PSM, the ZAI PSM allows users to mint/redeem ZAI for stablecoins at a 1:1 ratio. This ensures stability for ZAI at the 1$ price mark.
* [The Direct Deposit Module](direct-deposit-module-ddm.md): Inspired by MakerDAO's DD module, the ZAI DD module allows the protocol to mint large amounts of ZAI into lending protocols allowing borrowers to take over-collateralized loans in ZAI generating interest for users.

***

## Peg Mechanics

At no point in time does ZAI become under-collateralized. It is either backed by stablecoins via the Peg Stability Module (PSM) or it is backed by over-collateralized loans via the Direct Deposit Module (DDM).

* **When ZAI is trading above 1$,** arbitrageurs can simply mint more ZAI by depositing USDC (or other stablecoins) onto the PSM module and sell the newly minted ZAI into the open market bringing the peg back to 1$. At the same time the protocol can also issue more debt (priced at 1$) to encourage users to borrow ZAI and sell it in the open market.
* When ZAI is trading below 1$, arbitrageuers can simply buyback the ZAI from the open market and redeem USDC (or other stablecoins) from the PSM, bringing the peg back to 1$. If the PSM does not have enough liquidity to maintain the peg, then the protocol can recall the loans issued by the Direct Deposit Module forcing borrowers to repay their loans in ZAI.

Because in both mechanisms where ZAI is either minted using the PSM or lent using the DDM, the positions are always over collateralized, ZAI will be able to maintain it's peg at 1$.&#x20;

Please read the [risks section](../../security/risks.md) to understand more deeply about situations when this is not the case.
