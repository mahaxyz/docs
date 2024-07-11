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

# Emission Voting

Users who have locked MAHA tokens can participate in emission voting to determine how MAHA emissions are distributed within the protocol. This process is similar to Curve's gauge weight voting system.

## How It Works

Users can allocate their lock weight towards one or more emission receivers. At the start of each week, receivers are allocated a fraction of the weekly MAHA emissions, proportional to the lock weight they were allocated.

**Lock Weight**: Allocated in percentage. Each user has a maximum of 100%. Users must allocate all 100% to vote with their entire lock weight. Votes can be modified at any time.

**Weekly Voting**: Votes submitted by the start of Thursday each week apply to the following week. Votes persist week-to-week unless overridden or cleared on the MAHA tab.

This feature saves gas and prevents users from missing voting deadlines.

### Registering Vote Weight

**Initial Lock**: The first year of MAHA emissions are distributed as locked positions. Users must register their lock weight within the voting contract to submit a vote.

**Changing Lock Weight**: If a user's lock weight increases after submitting a vote, they may optionally resubmit the vote with the increased weight.

{% hint style="info" %}
This functionality is largely abstracted for end users via MAHA's front-end but integrators should review the IncentiveVoting contract.
{% endhint %}

## Voting on Weekly Emissions

Users can vote on various actions across the protocol to earn MAHA. These actions include:

1. **Depositing to the Stability Pools**: Providing liquidity to stability pools.
2. **Minting New ZAI**: Creating new ZAI ($USDz) with specific collateral.
3. **Maintaining an Active ZAI Debt**: Keeping an active debt position with specific collateral.
4. **Staking ZAI/MAHA LP Tokens**: Providing liquidity to the ZAI/MAHA pool and staking LP tokens.

**Example**: If you have an active debt position collateralized by rzETH, you could vote for maintaining an active ZAI debt collateralized by rzETH. This would direct more MAHA emissions for the following week towards this action.

Alternatively, you could vote for minting new ZAI with rzETH as collateral if you plan to mint more ZAI. You may also wish to deposit more rzETH and mint ZAI against it to receive a portion of that week’s MAHA emissions allocated to this action.
