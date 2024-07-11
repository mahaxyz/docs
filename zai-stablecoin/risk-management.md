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

# Risk Management

Managing risk is essential for the stability and success of the ZAI protocol. Risks within the ZAI protocol are categorized into three main types:

## 1. Market Risk

* **Liquidity**: Risk related to the ease of buying or selling assets without affecting prices.
* **Volatility**: Risk from significant price variations affecting collateral value.

#### 2. Technology Risk

* **Smart Contracts**: Vulnerabilities in the code that could be exploited.
* **Dependencies**: Risks from other protocols or services the ZAI protocol relies on.
* **Oracle Price Feeds**: Risk from inaccurate external price data.

#### 3. Counterparty Risk

* **Governance**: Risks from governance decisions impacting the protocol.
* **Legal and Regulatory**: Compliance risks varying across jurisdictions.

#### Security

Ensuring the security of the ZAI protocol is a top priority. Key measures include:

#### Smart Contract Security

* **Audits**: Regular independent audits to identify and fix vulnerabilities.
* **Formal Verification**: Ensuring smart contracts behave as expected through mathematical proofs.

#### Dependency Management

* **Code Reviews**: Thorough reviews of dependencies to avoid vulnerabilities.
* **Regular Updates**: Keeping dependencies up to date with the latest security patches.

#### Oracle Security

* **Multiple Oracles**: Using multiple providers for accurate and reliable price feeds.
* **Fallback Mechanisms**: Handling failures or inaccuracies in oracle data.

#### Risk Parameters Analysis

Risk parameters mitigate market risks associated with the collateral. Each ZAI minted is over-collateralized with listed collateral. Adequate margins and incentives keep positions collateralized during adverse conditions. If collateral value falls below a threshold, the vault is liquidated to repay the debt.

#### Supply Caps

Supply caps limit the maximum amount of an asset supplied to the protocol, reducing exposure to riskier assets. Caps are based on on-chain liquidity and the total volume of collateral assets.

For detailed information on our security measures and smart contract audits, please visit the [Security](notion://www.notion.so/akanshajain/Stablecoin-ZAI-5cf5e268def6459b9fb8771371f88bb2#security) section.

By understanding and managing these risks, the ZAI protocol aims to provide a secure and stable environment for all users
