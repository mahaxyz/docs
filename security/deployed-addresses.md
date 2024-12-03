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
| ZAI Token (ZAI)             | [0x69000dFD5025E82f48Eb28325A2B88a241182CEd](https://etherscan.io/token/0x69000dFD5025E82f48Eb28325A2B88a241182CEd)   | The USD stablecoin                                              |
| Peg Stability Module (USDC) | [0x69000052a82e218ccb61fe6e9d7e3f87b9c5916f](https://etherscan.io/address/0x69000052a82e218ccb61fe6e9d7e3f87b9c5916f) | Used to mint ZAI with USDC collateral                           |
| SafetyPool (sUSDZ)          | [0x69000e468f7f6d6f4ed00cf46f368acdac252553](https://etherscan.io/address/0x69000e468f7f6d6f4ed00cf46f368acdac252553) | Safety Pool used to stake ZAI to protect against bad debt       |
| Timelock                    | [0x690002da1f2d828d72aa89367623df7a432e85a9](https://etherscan.io/address/0x690002da1f2d828d72aa89367623df7a432e85a9) | All protocol ownership rests in this timelock                   |
| ProxyAdmin                  | [0x6900064e7a3920c114e25b5fe4780f26520e3231](https://etherscan.io/address/0x6900064e7a3920c114e25b5fe4780f26520e3231) | Used as the admin for all deployed proxies. Owned by governance |
| SafetyPool Zap              | [0x737Ce76225d5d0a1B696cdEAeB9Fa0eCbC8EF424](https://etherscan.io/address/0x737Ce76225d5d0a1B696cdEAeB9Fa0eCbC8EF424) | Used to zap into the safety pool.                               |

## Direct Deposit Modules <a href="#layer-2-addresses" id="layer-2-addresses"></a>

These addresses manage the [direct deposit module](deployed-addresses.md#layer-2-addresses), which funds various vaults with freshly minted ZAI.

| Contract Name  | Address                                                                                                               | Comments                                                                                  |
| -------------- | --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| DDHub          | [0x51a021e3B7874d451347a56152C47136593b6740](https://etherscan.io/address/0x51a021e3B7874d451347a56152C47136593b6740) | Direct Deposit module that mints ZAI to be used for lending                               |
| DDMetaMorpho   | [0xe8aBC60984489C842EF9B2aDF3aF066DD260744B](https://etherscan.io/address/0xe8abc60984489c842ef9b2adf3af066dd260744b) | Direct Deposit MetaMorpho Pool that uses te minted ZAI to supply into a MetaMorpho vault. |
| DDOperatorPlan | [0xf9759013B0114915dC1BC1184f72830a999f4111](https://etherscan.io/address/0xf9759013B0114915dC1BC1184f72830a999f4111) | A simple operator plan that sets the target on the MetaMorpho vaults                      |

## Staking Pools <a href="#layer-2-addresses" id="layer-2-addresses"></a>

These are the addresses of the various staking pools.

| Contract Name               | Address                                                                                                               | Comments                                                                                                                        |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| ZAI/USDC Curve Staking Pool | [0x154F52B347D8E48b8DbD8D8325Fe5bb45AAdCCDa](https://etherscan.io/address/0x154F52B347D8E48b8DbD8D8325Fe5bb45AAdCCDa) | The staking pool for the [ZAI/USDC Liquidity Pool](https://curve.fi/#/ethereum/pools/factory-stable-ng-229/deposit) on Curve.fi |
| ZAI/MAHA Curve Staking Pool | [0x237efE587f2cB44597063DC8403a4892a60A5a4f](https://etherscan.io/address/0x237efE587f2cB44597063DC8403a4892a60A5a4f) | The staking pool for the [ZAI/MAHA Liquidity Pool](https://curve.fi/#/ethereum/pools/factory-twocrypto-54/deposit) on Curve.fi  |
| ZAI/sZAI Curve Staking Pool | [0xeF12d1614eb0e2bC8E8884c7d4C7f15E34164F40](https://etherscan.io/address/0xeF12d1614eb0e2bC8E8884c7d4C7f15E34164F40) | The staking pool for the [ZAI/sZAI Liquidity Pool](https://curve.fi/#/ethereum/pools/factory-stable-ng-230/deposit) on Curve.fi |

## Governance/Security Addresses <a href="#layer-2-addresses" id="layer-2-addresses"></a>

These are the addresses of the various govenrance-related or security-related addresses.

<table><thead><tr><th width="134">Network</th><th width="156">Contract</th><th>Address</th></tr></thead><tbody><tr><td>Ethereum</td><td>5-day Timelock</td><td>0x690002da1f2d828d72aa89367623df7a432e85a9</td></tr><tr><td>Ethereum</td><td>Proxy Admin</td><td>0x6900064e7a3920c114e25b5fe4780f26520e3231</td></tr><tr><td>Arbitrum</td><td>5-day Timelock</td><td>0x690005544ba364a53dcc9e8d81c9ce1e90018ab7</td></tr><tr><td>Arbitrum</td><td>Proxy Admin</td><td>0x69000c978701fc4427d4baf749f10a5cec582863</td></tr></tbody></table>

## Cross-Chain Addresses <a href="#layer-2-addresses" id="layer-2-addresses"></a>

The protocol leverages the [connext bridge](https://www.connext.network/) to enable features such as native restaking, cross-chain bridging, and cross-chain governance.

{% tabs %}
{% tab title="ZAI" %}

<table><thead><tr><th width="200">Network</th><th>Address</th><th data-hidden>Contract</th></tr></thead><tbody><tr><td>Scroll</td><td><a href="https://scrollscan.com/address/0x44D4B627997b41aBd2BF2ea05B731fE535f01C3D">0x44D4B627997b41aBd2BF2ea05B731fE535f01C3D</a></td><td></td></tr><tr><td>Arbitrum</td><td><a href="https://arbiscan.io/address/0x47dE40eC7AA115FbC1f7b99CA4eFfc46A113De9B">0x47dE40eC7AA115FbC1f7b99CA4eFfc46A113De9B</a></td><td></td></tr><tr><td>Base</td><td><a href="https://basescan.org/address/0x0a27e060c0406f8ab7b64e3bee036a37e5a62853">0x0A27E060C0406f8Ab7B64e3BEE036a37e5a62853</a></td><td></td></tr><tr><td>Blast</td><td><a href="https://blastscan.io/address/0x58e6489eca0E55A16AdEe6F37301638470738ce6">0x58e6489eca0E55A16AdEe6F37301638470738ce6</a></td><td></td></tr><tr><td>BSC</td><td><a href="https://bscscan.com/address/0x3B2A34C8A085a6cA425eA64192D9f3A0B5dFb397">0x3B2A34C8A085a6cA425eA64192D9f3A0B5dFb397</a></td><td></td></tr><tr><td>Linea</td><td><a href="https://lineascan.build/address/0xb7f8f05825f3e37DFA68e1F3DF8b6D4B5829bc78">0xb7f8f05825f3e37DFA68e1F3DF8b6D4B5829bc78</a></td><td></td></tr><tr><td>Optimism</td><td><a href="https://optimistic.etherscan.io/address/0x3B2A34C8A085a6cA425eA64192D9f3A0B5dFb397">0x3B2A34C8A085a6cA425eA64192D9f3A0B5dFb397</a></td><td></td></tr><tr><td>X Layer</td><td><a href="https://www.oklink.com/xlayer/token/0xd077ABE1663166c0920d41Fd37ea2D9A00faBd40">0xd077ABE1663166c0920d41Fd37ea2D9A00faBd40</a></td><td></td></tr><tr><td>Mainnet</td><td><a href="https://etherscan.io/token/0x69000dFD5025E82f48Eb28325A2B88a241182CEd">0x69000dFD5025E82f48Eb28325A2B88a241182CEd</a></td><td></td></tr><tr><td>Mainnet OFT Adapter</td><td><a href="https://etherscan.io/address/0x90fD843fA0222E4222b5b8F2c839699eE84e50a0">0x90fD843fA0222E4222b5b8F2c839699eE84e50a0</a></td><td></td></tr></tbody></table>
{% endtab %}

{% tab title="MAHA" %}

<table><thead><tr><th width="153">Network</th><th>Address</th><th data-hidden>Contract</th></tr></thead><tbody><tr><td>Ethereum (Mainnet)</td><td><a href="https://etherscan.io/token/0x745407c86df8db893011912d3ab28e68b62e49b0">0x745407c86df8db893011912d3ab28e68b62e49b0</a></td><td>MAHAToken</td></tr><tr><td>Scroll</td><td><a href="https://scrollscan.com/token/0x6A661312938D22A2A0e27F585073E4406903990a">0x6A661312938D22A2A0e27F585073E4406903990a</a></td><td></td></tr><tr><td>Arbitrum</td><td><a href="https://arbiscan.io/token/0xdd2F41340A1fFcf1c22C7a8Be4E525D7A2De642b">0xdd2F41340A1fFcf1c22C7a8Be4E525D7A2De642b</a></td><td></td></tr><tr><td>Base</td><td><a href="https://basescan.org/token/0x554bba833518793056CF105E66aBEA330672c0dE">0x554bba833518793056CF105E66aBEA330672c0dE</a></td><td></td></tr><tr><td>Blast</td><td><a href="https://blastscan.io/token/0x6A661312938D22A2A0e27F585073E4406903990a">0x6A661312938D22A2A0e27F585073E4406903990a</a></td><td></td></tr><tr><td>BSC</td><td><a href="https://bscscan.com/token/0x6A661312938D22A2A0e27F585073E4406903990a">0x6A661312938D22A2A0e27F585073E4406903990a</a></td><td></td></tr><tr><td>Linea</td><td><a href="https://lineascan.build/token/0x6A661312938D22A2A0e27F585073E4406903990a">0x6A661312938D22A2A0e27F585073E4406903990a</a></td><td></td></tr><tr><td>Optimism</td><td><a href="https://optimistic.etherscan.io/token/0x6A661312938D22A2A0e27F585073E4406903990a">0x6A661312938D22A2A0e27F585073E4406903990a</a></td><td></td></tr><tr><td>X Layer</td><td><a href="https://www.oklink.com/xlayer/token/0xbc3186B68d1a7B771288122386288Aca9c1561a9">0xbc3186B68d1a7B771288122386288Aca9c1561a9</a></td><td></td></tr><tr><td>Mainnet OFT Adapter</td><td><a href="https://etherscan.io/address/0x3a7b708E71Ff72506afA674Ea14881E39CE9fdE2">0x3a7b708E71Ff72506afA674Ea14881E39CE9fdE2</a></td><td></td></tr></tbody></table>
{% endtab %}
{% endtabs %}
