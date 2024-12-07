---
description: This page explains about staking boosts and how users.
---

# Staking Boosts

Initially inspired by the staking boosts implemented on Curve finance, the MAHA protocol also implements its own version of a staking boost, incentivizing liquidity providers who are participating within the ecosystem to also become MAHA stakers.

Every staking pool contract in the protocol implements a staking boost mechanism that gives liquidity providers who [stake MAHA](staking.md), a boost of upto 5x depending on how much MAHA has been staked.

Staking boosts not just apply to MAHA emissions but also all revenue eanred from the protocol as well.

{% hint style="success" %}
Staking boosts go all the way up to 5x and apply to all incentive contracts! The more MAHA a user stakes, the larger the boost that they get.
{% endhint %}

## How is the Boost Calculated?

Staking boost goes all the way up to 5x depending on the following variables:

1. **How much total voting power does the pool have?** The more users who have a voting power and are staking in a pool, the more competitive boosts become.&#x20;
2. **How much voting power does a user have?** Depending on the percentage of the participating voting power a user has in a pool, the boost gets calculated. If a user has staked more tokens then he/she is entitled a larger share of the boosts.

The formula for the boosts is then calculated as follows considering the following variables. First we understand how much percentage of the voting power a user has in the pool.

$$
votingShare(x, pool) = \dfrac{votingPower(x)}{totalVotingInPower(pool)}
$$

If a pool has no voting power (which means that no one participating in the pool has staked any MAHA), then everyone gets the same level of boost.&#x20;

<table><thead><tr><th>Voting Power of User</th><th>Voting Power in the Pool</th><th width="143">Effective Voting Share</th></tr></thead><tbody><tr><td>0 veMAHA</td><td>0 veMAHA</td><td>100%</td></tr><tr><td>5,000 veMAHA</td><td>100,000 veMAHA</td><td>5%</td></tr><tr><td>5,000 veMAHA</td><td>5,000 veMAHA</td><td>100%</td></tr></tbody></table>

Once we have the `votingShare` of a user in a pool, we then roughly give a boost based on how much supply of the pool the user has.

$$
supplyShare(x, pool) = \dfrac{balanceOf(x)}{totalSupply(pool)}
$$

The final boost is calculated as the following.

$$
todo
$$

The following table gives a rough idea of how staking boosts are calculated depending on the variables mentioned above.

<table><thead><tr><th>Voting Share</th><th width="143">% of Pool </th><th>Effective Boost</th></tr></thead><tbody><tr><td>0%</td><td>1%</td><td>1x</td></tr><tr><td>50%</td><td>5%</td><td>2x</td></tr><tr><td>100%</td><td>1%</td><td>5x</td></tr><tr><td>50%</td><td>1%</td><td>5x</td></tr></tbody></table>

## Source Code

The following source code is taken from the [MultiStakingRewardsERC4626](https://github.com/mahaxyz/contracts/blob/master/contracts/core/utils/MultiStakingRewardsERC4626.sol#L322-L342) contract, which is used by all the staking contracts within the protocol. Boosts are used in reward calculations only and do not affect user deposits.

Boosts are updated every time a user either stake, withdraws or claims rewards from the contracts.

```solidity
function _calculateBoostedBalance(address account) internal view returns (uint256 boostedBalance_) {
  // how much tokens a user has staked
  uint256 balance = balanceOf(account);
  
  // how much total tokens have been staked
  uint256 totalSupply = totalSupply();

  // reduce the balance by 1/5th; anyone that has not staked any tokens
  // will always have their reward balances at 1/5th the original value
  boostedBalance_ = balance / 5;
  
  // modify the balance depending on how much share of the voting power the user has
  if (_totalVotingPower > 0) {
    boostedBalance_ += totalSupply * _votingPower[account] / _totalVotingPower * 4 / 5;
  }

  // cap the new balance to the original balance effectively 
  // giving a 5x if theuser has enough voting power
  boostedBalance_ = Math.min(balance, boostedBalance_);
}
```
