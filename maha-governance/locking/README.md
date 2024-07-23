# Locking

{% hint style="info" %}
Locking MAHA is handled by the locker contract, which is currently deployed at \[\[address]]
{% endhint %}

MAHAX is a representation of the voting power a user gets when they lock their `MAHA`. It is calculated using two metrics:

* How long is the MAHA locked for?
* How much MAHA is locked?

The goal of this kind of mechanism is to create a fair and decentralized distribution of voting power that gives as much power to the common man as compared to a whale.

In most cases, smaller holders will tend to lock their tokens for longer periods of time to get the same amount of voting power as whales, who will tend to larger amounts of tokens but for lesser periods of time.

This allows participants to have their voices recognized better by simply locking their tokens for longer periods of time.

## FAQs

#### Can I make multiple locks using a single wallet? <a href="#can-i-make-multiple-locks-using-a-single-wallet" id="can-i-make-multiple-locks-using-a-single-wallet"></a>

Yes, you can make as many locks as want as long as the lock meets the minimum locking criteria (as of writing the minimum lock criteria is set at `100 MAHAX`).

#### What happens if my lock expires? <a href="#what-happens-if-my-lock-expires" id="what-happens-if-my-lock-expires"></a>

If your lock expires, then your voting power goes to 0. However your NFT does not get burnt unless you decide to do so.

#### Do I lose my voting power over time? <a href="#do-i-lose-my-voting-power-over-time" id="do-i-lose-my-voting-power-over-time"></a>

Yes, MAHAX is a continuously decreasing value over time however in most cases your NFT you would need to be staked which freezes your voting power to the point at which it was staked at.

This voting power is recalculated if you either unstake, extend your lock or lock more MAHA.

#### What happens if a NFT is staked but it is also listed on a NFT marketplace like Opensea? <a href="#what-happens-if-a-nft-is-staked-but-it-is-also-listed-on-a-nft-marketplace-like-opensea" id="what-happens-if-a-nft-is-staked-but-it-is-also-listed-on-a-nft-marketplace-like-opensea"></a>

NFTs can get kicked from staking if it is listed on marketplaces such as OpenSea. Because NFTs cannot be transferred when they are staked, a listing on OpenSea won't get executed because the transaction would fail.

However this can cause an unwanted floor price manipulation in these marketplaces. Which is why there is a `banFromStake(...)` function that gets triggered to kick NFTs from being staked which are listed on marketplaces like Opensea so that the sale can actually happen on the platform.



## Any Further Questions? <a href="#any-further-questions" id="any-further-questions"></a>

If you have any further questions, you'd like us to answer

* You can join our discord channel [https://discord.gg/mahadao](https://discord.gg/mahadao) and ask the discord community for help.
* If you have a long and complicated query, you can create a thread on [https://discuss.maha.xyz ](https://discuss.maha.xyz)
