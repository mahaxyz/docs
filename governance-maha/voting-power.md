---
description: This section of the site talks about vote-escrowed MAHA.
---

# Voting Power (veMAHA)

veMAHA is a representation of the voting power a user gets when they either lock their MAHA or their MAHA/ETH LP tokens. It is calculated using two metrics:

* How long is the MAHA locked for?
* How much MAHA is locked?

The goal of this kind of mechanism is to create a fair and decentralized distribution of voting power that gives as much power to the common man as compared to a whale.

In most cases, smaller holders will tend to lock their tokens for longer periods of time to get the same amount of voting power as whales, who will tend to larger amounts of tokens but for lesser periods of time. This allows participants to have their voices recognized better by simply locking their tokens for longer periods of time.



## How is veMAHA Calculated?

veMAHA is a combination of the voting power from&#x20;

* **Single-staking MAHA:** Users can directly stake their MAHA without any risk of impermanent loss. The max lock duration for single-staking MAHA is 4 years as there's less risk with single-staking MAHA (vs LP staking)
* **LP staking MAHA/ETH:** Users can add liquidity to the MAHA/ETH liquidity pool on Curve. Due to the risks of impermanent loss, the max lock duration for LP staking is 1 year.

The voting power from a pool is calculated as a function of&#x20;

* **How many tokens have been locked:** The more tokens that have been staked, the more the voting power.
* **How long have the tokens been locked for:** The longer the tokens have been staked for, the more the voting power.
* **What is the max lock duration for the pool:** The longest duration a lock can be made for.

$$
locked(x, maxLockDuration) = \frac{\text{totalLocked(x)}}{averageLockDuration(x) / maxLockDuration}
$$

Given the above formula, the final formula is just the sum of the voting power of single staking of MAHA (with a 4-year max lock duration) and LP staking of MAHA/ETH (with a 1-year max lock duration).

$$
\text{veMAHA}= locked(\text{MAHA, 4 years}) + locked(\text{MAHA/ETH, 1 year})
$$

The below table showcases an example of how much veMAHA a person receives, given 1000 MAHA that is locked across various intervals of time. However, note that a user can choose any interval between 2 weeks to 4 years.

<table><thead><tr><th width="361">For 1000 MAHA locked</th><th>Lock Duration</th></tr></thead><tbody><tr><td>1000 veMAHA</td><td>4 years</td></tr><tr><td>250 veMAHA</td><td>1 year</td></tr><tr><td>127.4 veMAHA</td><td>6 month</td></tr><tr><td>63.7 veMAHA</td><td>3 month</td></tr><tr><td>21.23 veMAHA</td><td>1 month</td></tr><tr><td>4.79 veMAHA</td><td>1 week</td></tr></tbody></table>

<figure><img src="../.gitbook/assets/Mahax Locking.png" alt=""><figcaption><p><em>A graph showcasing the</em> <code>veMAHA</code> <em>power (y-axis) across the number of days locked (x-axis) for 1000 MAHA</em></p></figcaption></figure>

## Voting power that decays over time <a href="#voting-power-that-decays-over-time" id="voting-power-that-decays-over-time"></a>

One of the most important properties of a true democracy is the right of members to secede from the group. Transitioning of power is an important aspect of any future footed governance. Current participants need to give space for newer participants to come forward.

First-mover advantages within the MAHA ecosystem can lead to governance structures centralized to early adopters, making it harder for power to secede successfully.

This is why having the voting power decay slowly over time is important in creating future-footed governance.

Unless staked, every `veMAHA` NFT has its voting power, decay over time if it is not participating in active governance. This creates an incentive for holders to not just stake their NFTs but also have voting power that secedes if unstaked.

The end goal is to have a fully decentralized governance model that is evenly spread out and allows room for new participants to join in.

