---
description: This page explains the various use-cases that users can use ZAI with.
hidden: true
---

# Use Cases

ZAI is a lending-focused stablecoin designed for **AI-optimized yield leverage.** While pegged to $1, its primary utility lies in enabling users to amplify exposure to crypto-native assets via **dynamic liquidity provisioning** managed by JeremyAI. Governance votes initiate these strategies, but execution is now enhanced by AI-driven risk/reward analysis and incentive allocation. &#x20;

### **Leveraging on Yield-Bearing Assets**

Users leverage yield-bearing stablecoins (e.g., USDe, sDAI, aUSDC) to borrow ZAI, amplifying returns through recursive loops. &#x20;

**AI Enhancement**: &#x20;

JeremyAI monitors real-time yields and adjusts MAHA incentives to ensure ZAI borrowing rates remain competitive. &#x20;

**Example**: If USDe’s yield spikes, JeremyAI allocates extra MAHA rewards to ZAI/USDe pools, attracting liquidity to meet demand. &#x20;

**Ideal Assets:** USDe, sDAI, aUSDC.

### **Leveraging on Pendle PT tokens**

Borrow ZAI against PT tokens (e.g., PT-USDe, PT-sDAI) to supercharge yield-trading strategies. &#x20;

AI Enhancement: &#x20;

JeremyAI identifies underutilized PT markets and deploys ZAI liquidity via the Direct Deposit Module, prioritizing pools with the highest implied yields. &#x20;

Governance proposals are pre-analyzed by JeremyAI, which simulates ROI and risks for voter transparency. &#x20;

**Ideal Assets**: PT-USDe, PT-aUSDC, PT-sDAI.

### Liquidity Against Locked veTokens

A lot of veTokens (such as veCrv and veBal) are not highly liquid but are still financial assets as they are backed by governance tokens, which, upon the expiry of a lock, can become unlocked and traded in the open market.

**Use Case**: Unlock liquidity against illiquid veTokens (e.g., sdCRV, cvxCRV) at higher interest rates. &#x20;

**AI Enhancement:** &#x20;

JeremyAI assesses veToken volatility and protocol revenue potential, adjusting MAHA emissions to offset risk. &#x20;

**Example:** During Curve gauge votes, JeremyAI boosts incentives for sdCRV/ZAI pools to attract governance-focused borrowers. &#x20;

**Ideal Assets:** sdCRV, cvxCRV, sdBAL.

### LP Tokens as Collateral &#x20;

While super risky, LP tokens are complex DeFi tokens and their usage as collateral allows users to leverage up on certain positions.&#x20;

Furthermore, with the introduction of Uniswap V3 vaults such as Ichi and Gamma, this can be further extended to leverage highly capital-efficient Uniswap V3 positions.

**Use Case**: Use concentrated LP tokens (e.g., Ichi/Gamma vaults) to borrow ZAI for leveraged farming. &#x20;

**AI Enhancement:**&#x20;

JeremyAI monitors impermanent loss risks in Uniswap V3 positions, dynamically adjusting LTVs and interest rates to protect protocol solvency. &#x20;

Automated alerts notify governance if a vault’s TVL drops below safe thresholds. &#x20;

**Ideal Assets:** Ichi Vault Tokens, Gamma Vault Tokens.&#x20;

### Memecoins & Short-Term Speculation

A lot of memecoin users are looking for avenues to long/short memecoins with leverage. By providing liquidity to a lending market with these memecoins, traders can now find liquidity to long/short memecoins with leverage.

The protocol can also charge a lot higher interest fees due to the high-risk profiles of these tokens.

**Use Case:** Traders borrow ZAI to long/short volatile memecoins (e.g., PEPE, Shiba Inu) with leverage. &#x20;

AI Enhancement: &#x20;

JeremyAI detects memecoin liquidity surges and temporarily raises borrowing fees to mitigate risk, while allocating MAHA rewards to stabilize ZAI’s peg. &#x20;

SocialFi campaigns promote ZAI’s availability for trending memecoins, attracting opportunistic traders. &#x20;

**Ideal Assets**: PEPE, Shiba Inu.&#x20;



### Governance Token Loans

Governance tokens are known to be highly volatile and illiquid at times. By providing liquidity to a lending market with these governance tokens, we allow long-term contributors to find liquidity against their illiquid governance tokens.

The protocol can also charge a lot higher interest fees due to the high-risk profiles of these tokens.

&#x20;**Use Case:** Long-term holders borrow ZAI against illiquid governance tokens (e.g., UNI, CRV). &#x20;

AI Enhancement: &#x20;

JeremyAI calculates token holder lockup behavior to optimize LTVs and interest rates (e.g., lower rates for MAHA stakers with 4-year locks). &#x20;

Liquidity for “blue-chip” governance tokens (UNI, CRV) is prioritized in JeremyAI’s weekly incentive cycles. &#x20;

**Ideal Assets:** UNI, CRV, MAHA.&#x20;

***

### &#x20;Role of JeremyAI in Scaling Use Cases &#x20;

1\. **Risk-Adjusted Incentives:** Allocates MAHA emissions to pools with the highest risk-adjusted returns, replacing static farming. &#x20;

2\. **Automated Liquidity Deployment:** Uses the Direct Deposit Module to mint ZAI into lending protocols when demand spikes (e.g., during Ethena’s sUSDe yield surges). &#x20;

3\. **Governance Proposals:** Publishes on-chain reports (e.g., [Jan 30th Report](https://jpowell.ai/report?id=679ac11ebdbcc6bdc030ea92)) to guide voting on new collateral types. &#x20;

4\. **Bad Debt Prevention:** Monitors LTVs and liquidations in real-time, temporarily freezing risky pools flagged in [Safety Pool alerts](https://jpowell.ai/alerts).
