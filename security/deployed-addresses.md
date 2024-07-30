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

### Staking Pools <a href="#layer-2-addresses" id="layer-2-addresses"></a>

These are the addresses of the various staking pools.

| Contract Name             | Address                                                                                                               | Comments                                  |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------- |
| ZAI / FRAXBP Staking Pool | [0x6900066d9f8df0bfaf1e25ef89c0453e8e12373d](https://etherscan.io/address/0x6900066d9f8df0bfaf1e25ef89c0453e8e12373d) | The ZAI/FRAXBP Liquidity Pool on Curve.fi |

### Cross-Chain Addresses <a href="#layer-2-addresses" id="layer-2-addresses"></a>

The protocol leverages the [connext bridge](https://www.connext.network/) to enable features such as native restaking, cross-chain bridging, and cross-chain governance.

{% tabs %}
{% tab title="ZAI" %}
<table><thead><tr><th width="129">Network</th><th width="132">Contract</th><th width="174">Address</th><th>Comments</th></tr></thead><tbody><tr><td>Ethereum</td><td>ZaiStablecoin</td><td><a href="https://etherscan.io/token/0x69000405f9dce69bd4cbf4f2865b79144a69bfe0">0x69000405f9dce69bd4cbf4f2865b79144a69bfe0</a></td><td>The main token on the Ethereum network</td></tr></tbody></table>
{% endtab %}

{% tab title="MAHA" %}
<table><thead><tr><th width="129">Network</th><th width="132">Contract</th><th width="174">Address</th><th>Comments</th></tr></thead><tbody><tr><td>Ethereum</td><td>MAHAToken</td><td><a href="https://etherscan.io/token/0x745407c86df8db893011912d3ab28e68b62e49b0">0x745407c86df8db893011912d3ab28e68b62e49b0</a></td><td>The main token on the Ethereum network</td></tr></tbody></table>
{% endtab %}
{% endtabs %}
