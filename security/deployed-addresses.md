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

| Contract Name                | Address                                                                                                               | Comments                                                        |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| MAHA Token (MAHA)            | [0x554bba833518793056CF105E66aBEA330672c0dE](https://basescan.org/address/0x554bba833518793056CF105E66aBEA330672c0dE) | The governance token                                            |
| ZAI Token (ZAI)              | [0x69000dFD5025E82f48Eb28325A2B88a241182CEd](https://basescan.org/address/0x69000dfd5025e82f48eb28325a2b88a241182ced) | The USD stablecoin                                              |
| ZAI Staking (sZAI)           | [0x69000195D5e3201Cf73C9Ae4a1559244DF38D47C](https://etherscan.io/address/0x69000195D5e3201Cf73C9Ae4a1559244DF38D47C) | Safety Pool used to stake ZAI to protect against bad debt       |
| Peg Stability Module (sUSDe) | [0x7DCdE153e4cACe9Ca852590d9654c7694388Db54](https://etherscan.io/address/0x7DCdE153e4cACe9Ca852590d9654c7694388Db54) | Used to mint ZAI with sUSDe collateral                          |
| Timelock                     | [0x690002da1f2d828d72aa89367623df7a432e85a9](https://etherscan.io/address/0x690002da1f2d828d72aa89367623df7a432e85a9) | All protocol ownership rests in this timelock                   |
| ProxyAdmin                   | [0x6900064e7a3920c114e25b5fe4780f26520e3231](https://etherscan.io/address/0x6900064e7a3920c114e25b5fe4780f26520e3231) | Used as the admin for all deployed proxies. Owned by governance |

## Direct Deposit Modules <a href="#layer-2-addresses" id="layer-2-addresses"></a>

These addresses manage the [direct deposit module](deployed-addresses.md#layer-2-addresses), which funds various vaults with freshly minted ZAI.

| Contract Name  | Address                                                                                                               | Comments                                                                                  |
| -------------- | --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| DDHub          | [0xD14688cb29dd1925d2C26F3B0F08Fd2c85db54bF](https://etherscan.io/address/0xD14688cb29dd1925d2C26F3B0F08Fd2c85db54bF) | Direct Deposit module that mints ZAI to be used for lending                               |
| DDMetaMorpho   | [0xe8aBC60984489C842EF9B2aDF3aF066DD260744B](https://etherscan.io/address/0xe8abc60984489c842ef9b2adf3af066dd260744b) | Direct Deposit MetaMorpho Pool that uses te minted ZAI to supply into a MetaMorpho vault. |
| DDOperatorPlan | [0xf9759013B0114915dC1BC1184f72830a999f4111](https://etherscan.io/address/0xf9759013B0114915dC1BC1184f72830a999f4111) | A simple operator plan that sets the target on the MetaMorpho vaults                      |

## Staking Pools <a href="#layer-2-addresses" id="layer-2-addresses"></a>

These are the addresses of the various staking pools.

| Contract Name               | Address                                                                                                               | Comments                                                                                                                        |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| ZAI/USDC Curve Staking Pool | [0xdFB06C4c562Bcc810C112FBAC99c59C2856b86D1](https://etherscan.io/address/0xdFB06C4c562Bcc810C112FBAC99c59C2856b86D1) | The staking pool for the [ZAI/USDC Liquidity Pool](https://curve.fi/#/ethereum/pools/factory-stable-ng-229/deposit) on Curve.fi |
| ZAI/MAHA Curve Staking Pool | [0xE2EbBf803d0199A5A26108bA36FBAc366b201Be1](https://etherscan.io/address/0xE2EbBf803d0199A5A26108bA36FBAc366b201Be1) | The staking pool for the [ZAI/MAHA Liquidity Pool](https://curve.fi/#/ethereum/pools/factory-twocrypto-54/deposit) on Curve.fi  |
| ZAI/sZAI Curve Staking Pool | [0xfDAeB792FF19e7bd4f7ED5d6ce2ef7925d002A19](https://etherscan.io/address/0xfDAeB792FF19e7bd4f7ED5d6ce2ef7925d002A19) | The staking pool for the [ZAI/sZAI Liquidity Pool](https://curve.fi/#/ethereum/pools/factory-stable-ng-230/deposit) on Curve.fi |

## Governance/Security Addresses <a href="#layer-2-addresses" id="layer-2-addresses"></a>

These are the addresses of the various govenrance-related or security-related addresses.

<table><thead><tr><th width="134">Network</th><th width="156">Contract</th><th>Address</th></tr></thead><tbody><tr><td>Ethereum</td><td>5-day Timelock</td><td>0x690002da1f2d828d72aa89367623df7a432e85a9</td></tr><tr><td>Ethereum</td><td>Proxy Admin</td><td>0x6900064e7a3920c114e25b5fe4780f26520e3231</td></tr><tr><td>Arbitrum</td><td>5-day Timelock</td><td>0x690005544ba364a53dcc9e8d81c9ce1e90018ab7</td></tr><tr><td>Arbitrum</td><td>Proxy Admin</td><td>0x69000c978701fc4427d4baf749f10a5cec582863</td></tr></tbody></table>

## Cross-Chain Addresses <a href="#layer-2-addresses" id="layer-2-addresses"></a>

The protocol leverages the [LayerZero Bridge](https://layerzero.network/) to enable features such as native restaking, cross-chain bridging, and cross-chain governance.

{% tabs %}
{% tab title="ZAI" %}
<table><thead><tr><th width="200">Network</th><th>Address</th><th data-hidden>Contract</th></tr></thead><tbody><tr><td>Arbitrum</td><td><a href="https://arbiscan.io/address/0x69000dFD5025E82f48Eb28325A2B88a241182CEd">0x69000dFD5025E82f48Eb28325A2B88a241182CEd</a></td><td></td></tr><tr><td>Base</td><td><a href="https://basescan.org/address/0x69000dFD5025E82f48Eb28325A2B88a241182CEd">0x69000dFD5025E82f48Eb28325A2B88a241182CEd</a></td><td></td></tr><tr><td>BSC</td><td><a href="https://bscscan.com/address/0x69000dFD5025E82f48Eb28325A2B88a241182CEd">0x69000dFD5025E82f48Eb28325A2B88a241182CEd</a></td><td></td></tr><tr><td>Linea</td><td><a href="https://lineascan.build/address/0x69000dFD5025E82f48Eb28325A2B88a241182CEd">0x69000dFD5025E82f48Eb28325A2B88a241182CEd</a></td><td></td></tr><tr><td>X Layer</td><td><a href="https://www.oklink.com/xlayer/token/0x69000dFD5025E82f48Eb28325A2B88a241182CEd">0x69000dFD5025E82f48Eb28325A2B88a241182CEd</a></td><td></td></tr><tr><td>Mainnet</td><td><a href="https://etherscan.io/token/0x69000dFD5025E82f48Eb28325A2B88a241182CEd">0x69000dFD5025E82f48Eb28325A2B88a241182CEd</a></td><td></td></tr><tr><td>Mainnet OFT Adapter</td><td><a href="https://etherscan.io/address/0x557177Aa5F5303dED2fa56b413631bAb22a73872">0x557177Aa5F5303dED2fa56b413631bAb22a73872</a></td><td></td></tr></tbody></table>
{% endtab %}

{% tab title="MAHA" %}
<table><thead><tr><th width="153">Network</th><th>Address</th><th data-hidden>Contract</th></tr></thead><tbody><tr><td>Ethereum (Mainnet)</td><td><a href="https://etherscan.io/token/0x745407c86df8db893011912d3ab28e68b62e49b0">0x745407c86df8db893011912d3ab28e68b62e49b0</a></td><td>MAHAToken</td></tr><tr><td>Scroll</td><td><a href="https://scrollscan.com/token/0x6A661312938D22A2A0e27F585073E4406903990a">0x6A661312938D22A2A0e27F585073E4406903990a</a></td><td></td></tr><tr><td>Arbitrum</td><td><a href="https://arbiscan.io/token/0xdd2F41340A1fFcf1c22C7a8Be4E525D7A2De642b">0xdd2F41340A1fFcf1c22C7a8Be4E525D7A2De642b</a></td><td></td></tr><tr><td>Base</td><td><a href="https://basescan.org/token/0x554bba833518793056CF105E66aBEA330672c0dE">0x554bba833518793056CF105E66aBEA330672c0dE</a></td><td></td></tr><tr><td>Blast</td><td><a href="https://blastscan.io/token/0x6A661312938D22A2A0e27F585073E4406903990a">0x6A661312938D22A2A0e27F585073E4406903990a</a></td><td></td></tr><tr><td>BSC</td><td><a href="https://bscscan.com/token/0x6A661312938D22A2A0e27F585073E4406903990a">0x6A661312938D22A2A0e27F585073E4406903990a</a></td><td></td></tr><tr><td>Linea</td><td><a href="https://lineascan.build/token/0x6A661312938D22A2A0e27F585073E4406903990a">0x6A661312938D22A2A0e27F585073E4406903990a</a></td><td></td></tr><tr><td>Optimism</td><td><a href="https://optimistic.etherscan.io/token/0x6A661312938D22A2A0e27F585073E4406903990a">0x6A661312938D22A2A0e27F585073E4406903990a</a></td><td></td></tr><tr><td>X Layer</td><td><a href="https://www.oklink.com/xlayer/token/0xbc3186B68d1a7B771288122386288Aca9c1561a9">0xbc3186B68d1a7B771288122386288Aca9c1561a9</a></td><td></td></tr><tr><td>Mainnet OFT Adapter</td><td><a href="https://etherscan.io/address/0x3a7b708E71Ff72506afA674Ea14881E39CE9fdE2">0x3a7b708E71Ff72506afA674Ea14881E39CE9fdE2</a></td><td></td></tr></tbody></table>
{% endtab %}
{% endtabs %}
