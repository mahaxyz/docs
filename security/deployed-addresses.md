---
description: This page contains the list of all deployed addresses for the protocol.
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

# Deployed Addresses

## Core Protocol Addresses

This table contains a list of the core addresses deployed from the [https://github.com/mahaxyz/contracts](https://github.com/mahaxyz/contracts) repository

| Contract Name               | Address                                                                                                               | Comments                                                        |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| MAHA Token (MAHA)           | [0x745407c86df8db893011912d3ab28e68b62e49b0](https://etherscan.io/token/0x745407c86df8db893011912d3ab28e68b62e49b0)   | The governance token                                            |
| ZAI Token (USDz)            | [0x69000405f9dce69bd4cbf4f2865b79144a69bfe0](https://etherscan.io/token/0x69000405f9dce69bd4cbf4f2865b79144a69bfe0)   | The USD stablecoin                                              |
| Peg Stability Module (USDC) | [0x69000052a82e218ccb61fe6e9d7e3f87b9c5916f](https://etherscan.io/address/0x69000052a82e218ccb61fe6e9d7e3f87b9c5916f) | Used to mint ZAI with USDC collateral                           |
| SafetyPool (sUSDZ)          | [0x69000e468f7f6d6f4ed00cf46f368acdac252553](https://etherscan.io/address/0x69000e468f7f6d6f4ed00cf46f368acdac252553) | Safety Pool used to stake ZAI to protect against bad debt       |
| Timelock                    | [0x690002da1f2d828d72aa89367623df7a432e85a9](https://etherscan.io/address/0x690002da1f2d828d72aa89367623df7a432e85a9) | All protocol ownership rests in this timelock                   |
| ProxyAdmin                  | [0x6900064e7a3920c114e25b5fe4780f26520e3231](https://etherscan.io/address/0x6900064e7a3920c114e25b5fe4780f26520e3231) | Used as the admin for all deployed proxies. Owned by governance |
| SafetyPool Zap              | [0x737Ce76225d5d0a1B696cdEAeB9Fa0eCbC8EF424](https://etherscan.io/address/0x737Ce76225d5d0a1B696cdEAeB9Fa0eCbC8EF424) | Used to zap into the safety pool.                               |

## Direct Deposit Modules <a href="#layer-2-addresses" id="layer-2-addresses"></a>

These addresses manage the [direct deposit module](deployed-addresses.md#layer-2-addresses), which funds various vaults with freshly minted ZAI.

| Contract Name  | Address                                                                                                                    | Comments                                                                                  |
| -------------- | -------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| DDHub          | [0x51a021e3B7874d451347a56152C47136593b6740](https://etherscan.io/address/0x51a021e3B7874d451347a56152C47136593b6740)      | Direct Deposit module that mints ZAI to be used for lending                               |
| DDMetaMorpho   | [0xe8aBC60984489C842EF9B2aDF3aF066DD260744B](https://etherscan.io/address/0xe8abc60984489c842ef9b2adf3af066dd260744b#code) | Direct Deposit MetaMorpho Pool that uses te minted ZAI to supply into a MetaMorpho vault. |
| DDOperatorPlan | [0xf9759013B0114915dC1BC1184f72830a999f4111](https://etherscan.io/address/0xf9759013B0114915dC1BC1184f72830a999f4111)      | A simple operator plan that sets the target on the MetaMorpho vaults                      |

## Staking Pools <a href="#layer-2-addresses" id="layer-2-addresses"></a>

These are the addresses of the various staking pools.

| Contract Name             | Address                                                                                                               | Comments                                  |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------- |
| ZAI / FRAXBP Staking Pool | [0x6900066d9f8df0bfaf1e25ef89c0453e8e12373d](https://etherscan.io/address/0x6900066d9f8df0bfaf1e25ef89c0453e8e12373d) | The ZAI/FRAXBP Liquidity Pool on Curve.fi |

## Governance/Security Addresses <a href="#layer-2-addresses" id="layer-2-addresses"></a>

These are the addresses of the various govenrance-related or security-related addresses.

<table><thead><tr><th width="134">Network</th><th width="156">Contract</th><th>Address</th></tr></thead><tbody><tr><td>Ethereum</td><td>5-day Timelock</td><td>0x690002da1f2d828d72aa89367623df7a432e85a9</td></tr><tr><td>Ethereum</td><td>Proxy Admin</td><td>0x6900064e7a3920c114e25b5fe4780f26520e3231</td></tr><tr><td>Arbitrum</td><td>5-day Timelock</td><td>0x690005544ba364a53dcc9e8d81c9ce1e90018ab7</td></tr><tr><td>Arbitrum</td><td>Proxy Admin</td><td>0x69000c978701fc4427d4baf749f10a5cec582863</td></tr></tbody></table>

## Cross-Chain Addresses <a href="#layer-2-addresses" id="layer-2-addresses"></a>

The protocol leverages the [connext bridge](https://www.connext.network/) to enable features such as native restaking, cross-chain bridging, and cross-chain governance.

{% tabs %}
{% tab title="ZAI" %}
<table><thead><tr><th width="121">Network</th><th width="168">Contract</th><th width="381">Address</th></tr></thead><tbody><tr><td>Ethereum</td><td>ZaiStablecoin (USDz)</td><td><a href="https://etherscan.io/token/0x69000405f9dce69bd4cbf4f2865b79144a69bfe0">0x69000405f9dce69bd4cbf4f2865b79144a69bfe0</a></td></tr><tr><td>Ethereum</td><td>ZAI Lockbox</td><td><a href="https://etherscan.io/address/0x278fb6522f962ffd7091ab103618b09aab24ae78">0x278fB6522F962ffD7091Ab103618b09aab24AE78</a></td></tr><tr><td>Ethereum</td><td>XERC20 (xUSDz)</td><td><a href="https://etherscan.io/address/0x6900070de14fffaf3a129dc3880e0153444167fa#code">0x6900070de14fffaf3a129dc3880e0153444167fa</a></td></tr><tr><td>Ethereum</td><td>L1BridgeCollateral</td><td><a href="https://etherscan.io/address/0x12c1dee2457f59401f01e881be9d0e17f9db40e2#code">0x12c1deE2457f59401f01e881bE9D0e17f9Db40e2</a></td></tr><tr><td>Arbitrum</td><td>XERC20 (USDz)</td><td><a href="https://arbiscan.io/address/0x69000ee306393ef6f9a2a57d5cb5960263bd531f#code">0x69000ee306393ef6f9a2a57d5cb5960263bd531f</a></td></tr></tbody></table>
{% endtab %}

{% tab title="MAHA" %}
<table><thead><tr><th width="129">Network</th><th width="132">Contract</th><th width="395">Address</th></tr></thead><tbody><tr><td>Ethereum</td><td>MAHAToken</td><td><a href="https://etherscan.io/token/0x745407c86df8db893011912d3ab28e68b62e49b0">0x745407c86df8db893011912d3ab28e68b62e49b0</a></td></tr></tbody></table>
{% endtab %}
{% endtabs %}
