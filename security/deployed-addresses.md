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

| Contract Name             | Address                                                                                                             | Comments                                                        |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| MAHA Token                | [0x745407c86df8db893011912d3ab28e68b62e49b0](https://etherscan.io/token/0x745407c86df8db893011912d3ab28e68b62e49b0) | The governance token                                            |
| ZAI Token                 | [0x6900057428c99fb373397d657beb40d92d8ac97f](https://etherscan.io/token/0x6900057428c99fb373397d657beb40d92d8ac97f) | The USD stablecoin                                              |
| 14 day Timelock           |                                                                                                                     | All protocol ownership rests in this timelock                   |
| PegStabilityModule (USDC) |                                                                                                                     | Used to mint ZAI with USDC collateral                           |
| PegStabilityModule (DAI)  |                                                                                                                     | Used to mint ZAI with DAI collateral                            |
| PegStabilityModule (USDT) |                                                                                                                     | Used to mint ZAI with USDT collateral                           |
| ProxyAdmin                |                                                                                                                     | Used as the admin for all deployed proxies. Owned by governance |

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
