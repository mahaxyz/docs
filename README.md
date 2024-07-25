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

MAHA (previously known as MahaDAO) is a community-powered decentralized organization. Our mission is to create a stablecoin that is deeply rooted into the Ether-sphere. With integrations towards LRTs, Lending Protocols and DeFi for growth.

At the heart of the ecosystem are two main tokens. MAHA and ZAI.

## Why ZAI?

Unlike most complicated stablecoin designs out there, ZAI focuses on a very simplistic design (the entire stablecoin is less than 400 lines of code) and provides instant liquidity to borrowers.

Combined with the [Direct Deposit Module](zai-stablecoin/peg-mechanics/direct-deposit-module-ddm.md) and the [Peg Stability Module](zai-stablecoin/peg-mechanics/), ZAI can be used to instantly leverage on these assets and able to scale to millions if not billions of dollars of liquidity quickly.

ZAI aims to provide leverage liquidity for:

* Liquid Re-staking Tokens (LRTs)
* Bitcoin Derivatives (Lombard, Merlin BTC etc..)
* RWAs
* DeFi Assets (Pendle PT tokens, LP tokens, Liquid Lockers etc..)

## Key Features <a href="#key-features" id="key-features"></a>

These are the key features that make ZAI particularly unique from other stablecoins out there.

* **Strong Peg Mechanics:** With the help of the [Peg Stability Module](zai-stablecoin/peg-mechanics/peg-stablility-module-psm.md), ZAI is kept at a peg of 1$ with a collateral basket consisting of various stablecoins.
* **Instant Lending Liquidity:** The ZAI [Direct Deposit Module](zai-stablecoin/peg-mechanics/direct-deposit-module-ddm.md) allows supplies ZAI to various lending protocols to allow users to borrow ZAI as debt with their assets as collateral. Users can then use the ZAI to either leverage or de-risk from their collateral.
* **Strong Incentive Loops:** Revenue generated from the protocol is redirected back to stakers and LPs, which creates a strong feedback loop to further create more liquidity and more incentives. See [Revenue & Liquidity Incentives](zai-stablecoin/liquidity-incentives.md).
* **Safety Pool for any bad debt**: A [safety pool](zai-stablecoin/safety-pool.md) is designed to allow the protocol to cover any kinds of bad debt that might occur when borrowing ZAI against different kinds of collateral.
* **Minimalistic Design:** The entire stablecoin design including the various modules fits in less than 400 lines of code.
