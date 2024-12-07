---
description: >-
  This section of the document describes the PSM and how it contributes to the
  stability of ZAI
---

# Peg Stablility Module (PSM)

The Peg Stability Module (PSM) is a crucial mechanism for minting ZAI, designed to maintain its peg to the USD. Inspired by MakerDAO's [PSM for DAI](https://mips.makerdao.com/mips/details/MIP29), the ZAI PSM allows users to mint and redeem ZAI at a 1:1 ratio with supported stablecoins like USDC and DAI.

The modules gives the advantage to ZAI holders that the protocol is stable at the $1 peg; but it also brings in the disadvantage in that ZAI becomes nothing more than a wrapper for other stablecoins. However this is offsetted with the introduction of the Direct Deposit Module, which allows ZAI to be backed by over-collateralized crypto loans.

## **Market Arbitrage keeps the peg at $1**

To understand how the fixed exchange rate provided by the PSM encourages arbitrage and maintains the peg at $1 we explore the following two scenarios.

If ZAI trades above $1, arbitrageurs can exchange USDC for ZAI through the PSM and sell ZAI on the open market, increasing the supply of ZAI and pushing its price back toward $1.&#x20;

If ZAI trades below $1, arbitrageurs can buy ZAI cheaply on the open market, exchange it for USDC through the PSM, and sell USDC at a profit, reducing the supply of ZAI and pushing its price back up toward $1.

## Fees to prevent misuse of allocation

Optionally to prevent a possible misuse of allocation, supply and redemption fees can be applied to the PSM. These fees can be used to either encourage/discourage the use of the PSM module.

However they also have direct impact on the stability of ZAI. If a 2% redemption fee is applied to redemptions, then arbitrageurs will not participate in maintaining the peg at $1 unless the price goes below $0.98.

Any fees charged by the PSM go directly back to the protocol (See [Revenue Share](../../governance-maha/revenue-share.md)).

## Source Code and Technical Documentation

The source code for the PSM can be found on the GitHub link below.

{% embed url="https://github.com/mahaxyz/contracts/tree/master/contracts/core/psm" %}

The technical documentation can be found on the [GitHub wiki pages](https://github.com/mahaxyz/contracts/wiki/PegStabilityModule), and the unit tests for the PSM can be found on the [`PegStabilityModuleTest.sol`](https://github.com/mahaxyz/contracts/blob/master/test/foundry/PegStabilityModuleTest.sol) file.
