---
description: This page explains the various incentives given to liquidity provides
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

# Liquidity Incentives

Liquidity is one of the key aspects of the protocol. Without liquidity, the ecosystem cannot leverage itself.

Within the entire protocol there are 3-4 kinds of incentives given to liquidity providers.

1. **MAHA Emissions:** These are emissions directly in the form of MAHA tokens that can be claimed by liquidity providers at any time.&#x20;
2. **Protocol Revenue:** Over 60-80% of the protocol revenue is given back to liquidity providers in the form of either ETH or USDC. See [revenue share](../governance/revenue-share.md).
3. **Points & Airdrop:** More information about an airdrop will be [coming soon](../governance/points-and-airdrop.md) 👀.
4. **Partner Points**: Points and incentives given to by partner protocols for integrating or using ZAI within their ecosystem.

{% hint style="info" %}
Users who have staked MAHA get a boost in all their liquidity incentives of up-to 5x! Read more about [staking boosts](../governance/staking-boosts.md).
{% endhint %}

Staking in various pools come with their own risks and rewards. See [risks](../security/risks.md) for more details.

## How to earn Liquidity Incentives?

There are many different kinds of liquidity incentive programs within the ecosystem that will allow users to earn points, MAHA emissions, protocol revenue or even partner incentives. We detail a few of these programs here.

### ZAI/USDC LP Staking

The [ZAI/USDC pair on curve](https://curve.fi/#/ethereum/pools/factory-stable-ng-213/deposit) is the most important liquidity pair for the protocol. All liquidity supplied is used to allow borrowers to leverage gets executed within this pool.

Which is why most of the protocol incentives and rewards are redirected to this pool for LP staking.&#x20;

Besides protocol level incentives, liquidity providers also earn trading fees from borrowers when the open/close their positions.

{% hint style="success" %}
There is no withdrawal delay when unstaking from this pool and there is very little impermanent loss as both assets are pegged to 1$.
{% endhint %}

### Safety Pool Staking

The [Safety Pool](safety-pool.md) is a single-token staking contract that allows ZAI holders to stake and earn a portion of their fees and revenue by providing enough backstop liquidity to cover off any bad debt from the protocol.

Users who supply ZAI into this pool will earn 10% of all protocol revenue, emissions in MAHA and earn points!

There is a 10 day withdrawal delay when unstaking from this pool.

{% hint style="info" %}
There is a 10 day withdrawal delay when unstaking from this pool however there is no impermanent loss as only one asset is staked in this pool.
{% endhint %}

### MAHA/ETH Staking

The MAHA/ETH pair is crucial for allowing the governance token to have enough liquidity to allow traders to speculate on the MAHA token. Stakers can lock their MAHA/ETH curve tokens for a lock duration anywhere from 2 weeks up-to  1 year.

Stakers in this pool also earn a voting power which is used in governance and earns a staking boost.

There is no withdrawal delay when unstaking however every stake has an unlock time that needs to be passed before a deposit can be unstaked.&#x20;

{% hint style="warning" %}
This pair could be subject to impermanent loss as both assets (MAHA & ETH) in the pool are very volatile.
{% endhint %}

{% hint style="success" %}
Staking in this pool will increase your [staking boosts](../governance/staking-boosts.md)! 🎉
{% endhint %}

### MAHA Staking

Alternative to the MAHA/ETH LP Staking, users can also choose to simply stake MAHA without having to provide liquidity into a DEX. Stakers can lock their MAHA tokens for a lock duration anywhere from 2 weeks up-to  4 year.

Stakers in this pool also earn a voting power which is used in governance and earns a staking boost.

There is no withdrawal delay when unstaking however every stake has an unlock time that needs to be passed before a deposit can be unstaked.&#x20;

{% hint style="success" %}
Staking in this pool will increase your [staking boosts](../governance/staking-boosts.md)! 🎉 and there is no impermanent loss in interacting with this pool.
{% endhint %}
