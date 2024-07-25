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

# Risks

Being a lending focused stablecoin, there are mainly two kinds of risks that the entire protocol can be exposed to and what preventive measures have been taken to protect the protocol.

1. **Technical Risks**: Risks relating to the smart-contracts, code, frontends, infrastructure. Technical risks can be mitigated with audits and best security practices.
2. **Economic Risks**: Risks relating to the liquidity, incentives, governance, peg etc.. Economic risks can be mitigated with dedicated risk managers observing the protocol.

## Technical Risks

### Collateral Risks

### Oracle Risks

## Economic Risks

### Collateral Risks

### Bad Debt

### Governance Attacks

### 1. Market Risk

* **Liquidity**: Risk related to the ease of buying or selling assets without affecting prices.
* **Volatility**: Risk from significant price variations affecting collateral value.

### 2. Technology Risk

* **Smart Contracts**: Vulnerabilities in the code that could be exploited.
* **Dependencies**: Risks from other protocols or services the ZAI protocol relies on.
* **Oracle Price Feeds**: Risk from inaccurate external price data.

### 3. Counterparty Risk

* **Governance**: Risks from governance decisions impacting the protocol.
* **Legal and Regulatory**: Compliance risks varying across jurisdictions.

## Security

Ensuring the security of the ZAI protocol is a top priority. Key measures include:

### Smart Contract Security

* **Audits**: Regular independent audits to identify and fix vulnerabilities.
* **Formal Verification**: Ensuring smart contracts behave as expected through mathematical proofs.

### Dependency Management

* **Code Reviews**: Thorough reviews of dependencies to avoid vulnerabilities.
* **Regular Updates**: Keeping dependencies up to date with the latest security patches.

### Oracle Security

* **Multiple Oracles**: Using multiple providers for accurate and reliable price feeds.
* **Fallback Mechanisms**: Handling failures or inaccuracies in oracle data.

## Risk Parameters Analysis

Risk parameters mitigate market risks associated with the collateral. Each ZAI minted is over-collateralized with listed collateral. Adequate margins and incentives keep positions collateralized during adverse conditions. If collateral value falls below a threshold, the vault is liquidated to repay the debt.

## Supply Caps

Supply caps limit the maximum amount of an asset supplied to the protocol, reducing exposure to riskier assets. Caps are based on on-chain liquidity and the total volume of collateral assets.

By understanding and managing these risks, the ZAI protocol aims to provide a secure and stable environment for all users



#### **Collateralization**

* **Full Collateralization:** Ensures that every minted ZAI is fully backed by an equivalent amount of stablecoins, maintaining the peg and providing security.
* **Reserve Management:** The system manages the collateral reserves to ensure they remain sufficient and secure.

#### **Governance and Oversight**

* **Community Governance:** MAHA’s governance framework oversees the operation of the PSM and Direct Deposits.
* **Risk Parameters:** Risk parameters, such as collateralization ratios and deposit caps, are determined and adjusted through community governance to manage systemic risk.

#### **Security Measures**

* **Regular Audits:** Regular audits and security assessments are conducted to safeguard the smart contracts and overall system integrity.
* **Transparency:** Ensures transparency in operations and reserves.
