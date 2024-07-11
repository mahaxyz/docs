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

# Earn Rewards by Staking ZAI (USDz)

Staking ZAI ($USDz) allows users to earn rewards and is managed by the StakedZAI smart contract. Users can stake and unstake $USDz directly through the MAHA dApp UI or interact with the contract directly.

## How Staking Works

### **Staking**

* Users transfer $USDz into the StakedZAI contract.
* They receive staked $USDz, an ERC20 token representing their fractional interest in the total $USDz staked.

### **Earning Rewards**:

Over time, a portion of the protocol’s revenue is transferred to the staking contract as additional $USDz.

This increases the value of $USDz, which accumulates yield without requiring users to take any action.

### **Unstaking**:

Users can unstake their $USDz at any time.

The $USDz is burned, and users receive their original ZAI plus their proportionate share of the accumulated rewards.

## User Workflow

The StakedZAI contract uses the ERC4626 Token Vault standard, which is widely recognized for on-chain savings vehicles. The ERC4626 standard ensures that $USDz staking can be integrated with various DeFi platforms and interfaces.

**Staking Process**:

* Users click "Stake" on the MAHA dApp interface.
* The wallet signs and submits the transaction to the blockchain.
* Upon confirmation, users receive $USDz.

**Unstaking Process**:

* Users click "Unstake" on the MAHA dApp interface.
* The wallet signs and submits the transaction to the blockchain.
* Upon confirmation, users receive $USDz equivalent to their staked amount plus accumulated yield.

#### Key Points

* **No Minimum Staking Period**: Users can stake and unstake at any time and still receive their share of any increase in value.
* **Positive Yield**: The value of sZAI can only increase or stay the same; it will never decrease.
* **Regular Reward Payments**: Rewards are added to the contract every **8 hours** and vest linearly, preventing sudden spikes in value.

By staking ZAI, users can benefit from the protocol's yield generation while maintaining the flexibility to unstake their assets at any time.
