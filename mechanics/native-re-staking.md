---
description: >-
  This page explains how ZAI can be minted across various other chains through
  native re-staking
---

# Native Re-staking

In collaboration with Connext Network, ZAI Stablecoin is introducing cross-chain Native Restaking to layer-2 networks.

USDC holders can now restake on leading layer 2 chains partnered with ZAI, enhancing liquidity and accessibility while simplifying the complexities associated with traditional re-staking methods.&#x20;

{% hint style="success" %}
Native re-staking allows ZAI to be minted across mulitple other chains natively with USDC without the user ever having to interact with the Ethereum mainnet.
{% endhint %}

## What is native re-staking?

Native re-staking is a process where staked assets on one blockchain can be securely and efficiently re-staked on another blockchain, enhancing the liquidity and utility of these assets. This approach leverages cross-chain interoperability to allow users to maximize their staking rewards across multiple blockchain ecosystems.

The concept of native re-staking was [first introduced by the Renzo Protocol](https://docs.renzoprotocol.com/docs/integrations/l2-native-restaking). Renzo's innovative approach has set the foundation for this advanced staking method, showcasing how cross-chain interoperability can be leveraged to enhance the utility and profitability of staked assets.&#x20;

Native re-staking significantly eases the user experience for minting ZAI by abstracting the complexities involved in depositing USDC on layer 2 networks and bridging to the mainnet. The advantages of native restaking are as follows:

1. **User-Friendly Process**: By abstracting the technical complexities, users can easily mint ZAI without needing in-depth knowledge of cross-chain mechanics.
2. **Enhanced Liquidity**: Users can gain immediate access to $USDz tokens on L2 networks, providing more liquidity options and faster transactions.
3. **Seamless Interoperability**: The integration with Connext and native bridges ensures smooth and secure asset transfers between L2 and mainnet.

## **How Native Re-Staking Simplifies ZAI Minting**

* **User Interaction**: Users initiate the process by depositing USDC into the xZaiDeposit contract on a layer 2 (L2) network.
* **Minting $USDZ**: The [L2DepositCollateral](https://github.com/mahaxyz/contracts/blob/master/contracts/periphery/restaking/connext/L2DepositCollateral.sol) contract mints $USDz tokens, which are pegged to $USDz on mainnet and represent the user's deposit on the L2 network. The minted $USDZ tokens are XERC20 tokens and are sent back to the user, providing immediate liquidity on the L2 network.
* **Bridge Trigger**: Periodically, the L2DepositCollateral contract triggers a bridge transaction through Connext or through the native bridge. This action sends all deposited USDC to the [L1BridgeCollateral](https://github.com/mahaxyz/contracts/blob/master/contracts/periphery/restaking/connext/L1BridgeCollateral.sol) contract on the Ethereum mainnet.
* **Bridge Deposit & Minting**: The L1BridgeCollateral contract's bridgeDeposit() function processes the USDC received on the mainnet. The [Peg Stability Module](peg-mechanics/peg-stablility-module-psm.md) then handles the USDC, minting ZAI tokens that are sent to the Lockbox contract to be wrapped into $USDz.

