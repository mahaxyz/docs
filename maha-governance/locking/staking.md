# Staking

{% hint style="info" %}
Staking MAHAX NFTs is handled by the Staker Contract which is currently deployed at \[\[contract address]]
{% endhint %}

MAHAX NFTs unless staked, have no functionality within the governance platform. These include benefits like earning fees, exercising voting power, providing legitimacy to a group of individuals, and so on.

Once an NFT is staked:

* It cannot be moved to another wallet address, and its voting power (MAHAX balance) is frozen
* It also cannot be traded on third-party marketplaces such as [OpenSea](https://opensea.io/)
* It can be unstaked at any point in time
* It will start earning fees and can be used for governance, voting, and boosting

Unstaking an NFT removes all the restrictions above, but at the same time unfreezes the voting power (MAHAX balance) which will start to decay over time.

To claim the underlying MAHA behind an NFT or to merge an NFT with another NFT, they both need to be unstaked.

{% hint style="info" %}
When a MAHAX NFT lock is created, the user gets an option to decide if he/she wishes to also stake the NFT in the same transaction. By default this is enabled.
{% endhint %}

## Merging NFTs

MAHAX NFTs can be merged into one another, allowing for voting power to get combined and a greater MAHAX balance.

When an NFT has merged, the following steps take place:

* A check is run if both NFTs are staked or not. Merging happens only if both NFTs are unstaked
* The first NFT is burnt
* The second NFT is updated with the combined underlying MAHA balances for both NFTs
* The second NFT is updated with a lock duration that is longer than the two NFTs

{% hint style="info" %}
Merging NFTs creates more powerful NFTs with a net combined voting power.
{% endhint %}

## Role of Governance

### Governance <a href="#governance" id="governance"></a>

The MAHAX NFT locker has various parameters that can be controlled by Governance:

* **The minimum amount of MAHA required for a lock:** This is currently set at `99 MAHAX` (or rather approximately `100 MAHA` locked for 4 years). If the cost of minting an NFT becomes higher, then ideally, lowering the minimum mint floor will allow for more NFTs to be minted as the cost of minting a piece becomes lower.
* **NFT minting privileges:** Currently only used for the migration of NFTs from the polygon, this function allows addresses/contracts to mint NFTs at will. Only to be used in rare scenarios.