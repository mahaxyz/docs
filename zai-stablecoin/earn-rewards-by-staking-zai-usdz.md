# Earn Rewards by Staking ZAI (USDz)

Staking ZAI (USDz) allows users to earn rewards and is managed by the StakedZAI smart contract. Users can stake and unstake ZAI directly through the MAHA dApp UI or interact with the contract directly.

#### How Staking Works

1. **Staking**:
   * Users transfer ZAI into the StakedZAI contract.
   * They receive staked ZAI (sZAI), an ERC20 token representing their fractional interest in the total ZAI staked.
2. **Earning Rewards**:
   * Over time, a portion of the protocol’s revenue is transferred to the staking contract as additional ZAI.
   * This increases the value of sZAI, which accumulates yield without requiring users to take any action.
3. **Unstaking**:
   * Users can unstake their sZAI at any time.
   * The sZAI is burned, and users receive their original ZAI plus their proportionate share of the accumulated rewards.

#### User Workflow

The StakedZAI contract uses the ERC4626 Token Vault standard, which is widely recognized for on-chain savings vehicles. The ERC4626 standard ensures that ZAI staking can be integrated with various DeFi platforms and interfaces.

1. **Staking Process**:
   * Users click "Stake" on the MAHA dApp interface.
   * The wallet signs and submits the transaction to the blockchain.
   * Upon confirmation, users receive sZAI.
2. **Unstaking Process**:
   * Users click "Unstake" on the MAHA dApp interface.
   * The wallet signs and submits the transaction to the blockchain.
   * Upon confirmation, users receive ZAI equivalent to their staked amount plus accumulated yield.

#### Key Points

* **No Minimum Staking Period**: Users can stake and unstake at any time and still receive their share of any increase in value.
* **Positive Yield**: The value of sZAI can only increase or stay the same; it will never decrease.
* **Regular Reward Payments**: Rewards are added to the contract every **8 hours** and vest linearly, preventing sudden spikes in value.

#### Example

1. **Staking**:
   * User A stakes 100 ZAI and receives 100 sZAI.
   * Over a month, the protocol generates yield and adds 10 ZAI to the contract.
2. **Unstaking**:
   * When User A decides to unstake, their 100 sZAI is burned.
   * They receive 110 ZAI (their original 100 ZAI plus their share of the 10 ZAI yield).

By staking ZAI, users can benefit from the protocol's yield generation while maintaining the flexibility to unstake their assets at any time.
