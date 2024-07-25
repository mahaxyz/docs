---
description: >-
  The safety pool is a staking pool for ZAI that is used to protect the protocol
  against bad debt.
---

# Safety Pool

One of the major risks of any lending market is the accumulation of bad debt in the protocol. In this document we describe the Safety Pool, a ERC4626 vault that is used to cover any bad debt that might accumulate in the protocol.

{% hint style="warning" %}
The Safety Pool is only used as a means of last resort and works like an insurance fund where depositors stake their ZAI in return for protocol revenue and MAHA emissions; Staked ZAI can be the governance to write off any bad debt that has been incurred by the protocol.
{% endhint %}

## What is Bad Debt?

Bad debt accrual in a protocol means that one or multiple positions have less collateral than liabilities, which leads to a situation on which the user has no incentive to repay and consequently, if all depositors of the borrowed asset would try to withdraw (or cause a bank run), there would be a deficit in the protocol.

Protecting bad debt has been attempted by many different DeFi lending protocols in the past in various kinds of implementation.

* [Stability Pool](https://docs.liquity.org/faq/stability-pool-and-liquidations) by Liquity &#x20;
* [Safety Module](https://docs.aave.com/aavenomics/safety-module) by Aave&#x20;
* [Insurance Fund](https://ethena-labs.gitbook.io/ethena-labs/solution-design/reserve-fund) by Ethena

While each implementation has it's pro's and con's, the ZAI Safety Pool takes some of the best ideas of the various models mentioned above and builds a single-staking vault that is built more like an DeFi insurance vault.

## Why a Safety Pool?

Like any lending protocol, one of the biggest risks is the accumulation of bad debt. While in most cases the bad debt can be prevented with effective risk management, it's not always the case and especially in situations of a flash crash or a hack, liquidations might not happen quick enough to safely clear off any unhealthy positions in the protocol.

See the following instances in DeFi history where major lending protocols have incurred bad debt.

* [Feature or Flaw? Aave Left With $1.7M in Bad Debt](https://blockworks.co/news/aave-curve-bad-debt) (Aave)
* [Bad Debt Piles up at DeFi Lending Protocols](https://thedefiant.io/news/defi/bad-debt-defi-protocols) (Venus Protocol & Iron bank)
* [TrueFi's $4M Bad Debt in Limbo Shows Risk of Crypto Lending Without Collateral](https://www.coindesk.com/markets/2022/10/13/truefis-4m-bad-debt-in-limbo-shows-risk-of-crypto-lending-without-collateral/) (TrueFi)&#x20;

Which is why assuming that no matter how safe risk managers tend to be, nor how quickly liquidations will clear off any unhealthy positions, a secondary fallback mechanism needs to be put into place that'll allow the protocol to pay of any bad debt in the unlikely event it'll have to do so.

Tackling bad debt efficiently will further allow the protocol to scale and accept assets with higher risk profiles as time goes on.

## How does the Safety Pool work?

Similar to various Insurance vaults, users can stake their ZAI into the ZAI safety pool in return for yield from revenue and a share of MAHA emissions.

Users who pledge their ZAI tokens into the safety pool to receive a ERC4626 vault token. The ZAI deposited into the vault can at any time (using on-chain data) be used to cover any bad-debt position that has been accumulated in the protocol.

When the ZAI is used to pay off any bad debt, a user's deposit of ZAI tokens into the vault gets slashed to pay off the bad debt. To compensate for this risk, the safety pool rewards liquidity providers with MAHA emissions and protocol revenue.

## Withdrawal Delay

Similar to other slashing mechanisms that have existed in the Ethereum re-staking ecosystem, depositors who look to withdraw funds from the protocol will go through a 10 day delay.

This is done to ensure that in the event of a bad debt repayment, governance has enough time to execute a payment of debt with sufficient liquidity in the pool.

## Design Decisions with the Safety Pool

As documented above, we have made a few design decisions when building the Safety Pool to make sure we take the best of the various models mentioned above.

1. **A 10-day withdrawal period**: 10 days lets the MAHA governance quickly make a decision on the debt repayments before depositors withdraw their funds.
2. **Rewards instead of an insurance/reserve fund**: Providing rewards is a much more scalable way of growing the safety pool than maintaining an insurance/reserve fund.&#x20;
3. **Multiple rewards to compensate for the slashing risk**: Since users who deposit into the safety pool go through a risk of slashing, there needs to enough rewards to incentivize such a high risk activity. Rewards in the form revenue helps the safety pool scale along with the protocol.
4. **Designed as an ERC4626 vault**: The ERC4626 standard allows for simplicity in the safety pool design and allows for users to easily move their position across other wallets or allow other protocols to directly integrate with the safety pool.

## Example Scenarios

If users have supplied 1,000,000 ZAI in the safety pool and the protocol is supplying 5,000,000 ZAI into the lending pool, we explore the following scenarios.

1. The lending pool the protocol supplied liquidity to incurs a bad debt position of over 10,000 ZAI.
   1. The protocol makes a governance proposal or executes a smart contract function to claim the 10,000 ZAI from the safety pool and square off all the bad debt from the protocol
   2. The balance in the safety pool reduces by 1% and every user that supplied to this pool will have their deposit slashed by 1%. This means that every user will now get 99% of their deposit back (instead of 100%).
   3. Depositors will continue to claim MAHA and protocol fees for their deposit.
2. No bad debt gets accumulated by the protocol.
   1. In this situation governance nor any smart contract execute any action to claim any ZAI from the safety pool.
   2. No slashing happens and users get 100% of their deposit back.
   3. Depositors will continue to claim MAHA and protocol fees for their deposit.
