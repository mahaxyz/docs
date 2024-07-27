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
    visible: false
  pagination:
    visible: true
---

# Deployed Addresses

This table contains a list of the core addresses deployed from the [https://github.com/mahaxyz/contracts](https://github.com/mahaxyz/contracts) repository

| Contract Name             | Address                                                                                                               | Comments                                                        |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| MAHA Token                | [0x745407c86df8db893011912d3ab28e68b62e49b0](https://etherscan.io/token/0x745407c86df8db893011912d3ab28e68b62e49b0)   | The governance token                                            |
| ZAI Token                 | [0x6900057428c99fb373397d657beb40d92d8ac97f](https://etherscan.io/address/0x6900057428c99fb373397d657beb40d92d8ac97f) | The USD stablecoin                                              |
| Timelock                  | [0x69000d5a9f4ca229227b90f61285f5866d139f11](https://etherscan.io/address/0x69000d5a9f4ca229227b90f61285f5866d139f11) | All protocol ownership rests in this timelock                   |
| PegStabilityModule (USDC) | [0x69000a93c8acf8126d6ef5b1054c2695744ca4ee](https://etherscan.io/address/0x69000a93c8acf8126d6ef5b1054c2695744ca4ee) | Used to mint ZAI with USDC collateral                           |
| PegStabilityModule (USDT) | [0x690006c6bcd62d06b935050729b3004e962ba708](https://etherscan.io/address/0x690006c6bcd62d06b935050729b3004e962ba708) | Used to mint ZAI with USDT collateral                           |
| ProxyAdmin                | [0x69000f2f879ee598ddf16c6c33cfc4f2d983b6bd](https://etherscan.io/address/0x69000f2f879ee598ddf16c6c33cfc4f2d983b6bd) | Used as the admin for all deployed proxies. Owned by governance |

### Cross-Chain Addresses <a href="#layer-2-addresses" id="layer-2-addresses"></a>

The protocol leverages on the [connext bridge](https://www.connext.network/) to enable features such as native restaking, cross-chain bridging and cross-chain governance.

{% tabs %}
{% tab title="ZAI" %}

<table><thead><tr><th width="129">Network</th><th width="132">Contract</th><th width="174">Address</th><th>Comments</th></tr></thead><tbody><tr><td>Ethereum</td><td>ZaiStablecoin</td><td><a href="https://etherscan.io/token/0x6900057428c99fb373397d657beb40d92d8ac97f">0x6900057428c99fb373397d657beb40d92d8ac97f</a></td><td>The main token on the Ethereum network</td></tr></tbody></table>

{% endtab %}

{% tab title="MAHA" %}

<table><thead><tr><th width="129">Network</th><th width="132">Contract</th><th width="174">Address</th><th>Comments</th></tr></thead><tbody><tr><td>Ethereum</td><td>MAHAToken</td><td><a href="https://etherscan.io/token/0x745407c86df8db893011912d3ab28e68b62e49b0">0x745407c86df8db893011912d3ab28e68b62e49b0</a></td><td>The main token on the Ethereum network</td></tr></tbody></table>
{% endtab %}
{% endtabs %}
