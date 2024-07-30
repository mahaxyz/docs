---
description: This page explains the Direct Deposit Module (DDM) and how it works.
---

# Direct Deposit Module (DDM)

The ZAI Direct Deposit Module (DDM) integrates ZAI with various lending pools and other DeFi protocols. This allows the MAHA ecosystem to generate ZAI dynamically to instantly meet the liquidity demands of borrowers across various lending protocols.

## Meet Demand & Scale Revenue

The main focus of the DDM is to meet the demand for leverage using ZAI and scale revenue for the protocol.

By allowing the protocol to mint unbacked ZAI into lending protocols to allow borrowers to take out over-collateralized loans in ZAI, we allow borrowers to get instant liquidity to ZAI at low-interest fees.

Borrowers can then use the borrowed ZAI to leverage themselves on various assets (and possibly earn an extra yield) by selling their ZAI for more exposure.

This brings various use cases into the picture:

* **Borrowers can leverage their yields:** For example, if a ZAI/USDe lending pool exists and it allows users to borrow ZAI at a 95% LTV with a 5% interest fee and if users natively earn a 15% yield on USDe, then by borrowing at 95% LTV and looping multiple times, users get a leveraged exposure of upto 20x ie (300% yield) at a cost of 100% interest (which gives a net yield of 200%).
* **Borrowers can take loans against their illiquid assets:** For certain asset classes, the protocol can decide to give out loans in ZAI (at much higher interest rates) to give borrowers liquidity against these assets.
* **Traders can short ZAI**: Whilst not beneficial to the protocol, traders can also choose to short ZAI by borrowing it from the open market.

All of these use-cases generate revenue to the protocol which then gets distributed back to liquidity providers (see [revenue share](../../governance/revenue-share.md)).

## Risk Management

Like any lending protocol, there is active risk management that takes place with the Direct Deposit Module. Because ZAI is being used as debt to lend out across multiple other assets, active risk management is needed to ensure that the protocol does not incur any bad debt from these operations.

Lending out ZAI against non-stablecoin assets can generate revenue but also carries the risk of bad debt, which can potentially create a de-peg event.

In such situations, the DAO/Risk Managers need to make the risk-reward analysis to sufficiently decide on the various assets to give loans.

In the event that the risk managers and liquidations don't sufficiently stop the protocol from incurring any bad debt, [the safety pool](../safety-pool.md) can be used to write off any bad debt.

See [Risks](../../security/risks.md) for more details.

## Peg Stability with Lending Debt

Historically, lending-backed stablecoins ([as seen with GHO](https://blockworks.co/news/gho-aave-peg-stablecoin-arbitrage)) have had a hard time maintaining the peg because the repayment mechanisms for when the stablecoin is trading below the peg haven't been strong enough to encourage arbitrageurs to get the peg back to the $1 mark.

Nevertheless, in the case of ZAI, when the peg goes below the $1 mark, the risk managers of the protocol can trigger a recall of debt by withdrawing any available ZAI liquidity from lending pools, forcing interest rates to rise and hence getting borrowers to unwind their positions and repay their debt.

While this has a weaker effect in retaining the peg when compared to the [arbitrage mechanism](peg-stablility-module-psm.md#market-arbitrage-keeps-the-peg-at-1usd) that happens in the PSM module, the DDM is mainly responsible for scaling ZAI across other markets. So as long loans are given out with proper risk management, in most cases a de-peg can be prevented.&#x20;

## Source Code and Technical Documentation

The source code for the DDM can be found on the GitHub link below.

{% embed url="https://github.com/mahaxyz/contracts/tree/develop/contracts/core/direct-deposit" %}

The technical documentation can be found on the [GitHub wiki page](https://github.com/mahaxyz/contracts/wiki/DDHub), and the unit tests for the DDM can be found on the [`DDHubTest.simple.sol`](https://github.com/mahaxyz/contracts/blob/master/test/foundry/DDHubTest.simple.sol) file.
