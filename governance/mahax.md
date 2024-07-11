---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# MAHAX

MAHAX represents the voting power a user gets when they lock their MAHA tokens. It is designed to decentralize voting power, giving smaller holders the ability to have significant influence by locking their tokens for longer periods.

#### How is MAHAX calculated?

MAHAX is calculated based on two factors:

**Amount of MAHA locked**

**Duration of the lock period**



For example, locking 1000 MAHA yields:

* 4 years: 1000 MAHAX
* 1 year: 250 MAHAX
* 6 months: 127.4 MAHAX
* 3 months: 63.7 MAHAX
* 1 month: 21.23 MAHAX
* 1 week: 4.79 MAHAX

## Staking FAQs

**Can I make multiple locks using a single wallet?**&#x20;

Yes, you can create multiple locks as long as each meets the minimum criteria (currently set at 100 MAHAX).

**What happens if my lock expires?**

When a lock expires, your voting power drops to 0. The NFT does not get burnt unless you choose to do so.

**Do I lose my voting power over time?**

Yes, MAHAX decays over time unless staked, which freezes the voting power. If you unstake, extend your lock, or lock more MAHA, the voting power is recalculated.

**What happens if an NFT is staked but also listed on an NFT marketplace like OpenSea?**

Staked NFTs cannot be transferred. If listed on OpenSea, the transaction will fail, and a function will kick the NFT from staking to allow the sale to proceed. This prevents unwanted floor price manipulation.
