---
description: Welcome to MAHA and ZAI, the stable money of the Ethermind.
cover: .gitbook/assets/1500x500.png
coverY: 0
layout:
  cover:
    visible: true
    size: full
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

# Welcome

MAHA (previously known as MahaDAO) is a community-powered decentralized organization focused on creating a better stable economy.

At the heart of the ecosystem are two main tokens - MAHA and ZAI.

## Why ZAI?

Unlike most complicated stablecoin designs out there, ZAI is incredibly minimalistic _(the_ [_core modules_](https://github.com/mahaxyz/contracts/tree/master/contracts/core) _is less than 700 lines of code)_, highly scalable and decentralized.

Combined with the [Direct Deposit Module](stablecoin-zai/peg-mechanics/direct-deposit-module-ddm.md) and the [Peg Stability Module](stablecoin-zai/peg-mechanics/), ZAI can be used to instantly leverage on these assets and able to scale to millions if not billions of dollars of liquidity quickly.

ZAI aims to provide leverage liquidity for:

* Liquid Re-staking Tokens (LRTs)
* Bitcoin Derivatives (Lombard, Merlin BTC, etc..)
* RWAs (Real World Assets)
* Defi Assets (Pendle PT tokens, LP tokens, Liquid Lockers, etc..)

ZAI is primarily a lending-focused stablecoin. Whilst it is pegged at $1, it is not really focused on being used as a means of payment nor as a means of holding wealth. It is designed specifically to allow users to allow themselves to leverage various assets and yields (see [use-cases](stablecoin-zai/use-cases.md)).

## Key Features <a href="#key-features" id="key-features"></a>

These are the key features that make ZAI particularly unique from other stablecoins out there.

* **Strong Peg Mechanics:** With the help of the [Peg Stability Module](stablecoin-zai/peg-mechanics/peg-stablility-module-psm.md), ZAI is kept at a peg of $1 with a collateral basket consisting of various stablecoins.
* **Instant Lending Liquidity:** The ZAI [Direct Deposit Module](stablecoin-zai/peg-mechanics/direct-deposit-module-ddm.md) allows supplies ZAI to various lending protocols to allow users to borrow ZAI as debt with their assets as collateral. Users can then use the ZAI to either leverage or de-risk from their collateral.
* **Strong Incentive Loops:** Revenue generated from the protocol is redirected back to stakers and LPs, which creates a strong feedback loop to further create more liquidity and more incentives. See [Revenue & Liquidity Incentives](stablecoin-zai/liquidity-incentives.md).
* **Safety Pool for Any Bad Debt**: A [safety pool](stablecoin-zai/safety-pool.md) is designed to allow the protocol to cover any kind of bad debt that might occur when borrowing ZAI against different kinds of collateral.
* **Minimalistic Design:** The entire stablecoin design, including the core modules, fits in less than 700 lines of code.
