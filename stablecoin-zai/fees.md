# Fees

The ZAI platform imposes three types of fees:

1. **Mint & Redemption Fees**: Charged in ETH and ZAI ($USDz)
2. **Stability Fees**: Charged in MAHA tokens
3. **Refundable Liquidation Fee**: Set at 50 ZAI ($USDz)

## Stability Fees

* **Purpose**: Manage collateral redemption within the protocol.
* **Charged In**: MAHA tokens.
* **Mechanism**: Collected MAHA tokens are burned, reducing supply.
* **Governance Adjustment**:
  * High Risk: 5-20%
  * Low Risk: 0-5%

## Fee Schedule

**Redemption and Issuance Fees**:

* **BaseRate**: Dynamically updated in the TroveManager.
  * Increases with each redemption.
  * Decays over time since the last fee event.

**Redemption Fee Calculation**:

`min{REDEMPTION_FEE_FLOOR + baseRate * ETHdrawn, DECIMAL_PRECISION}`

$$
min(REDEMPTIONFEEFLOOR + baseRate * ETHdrawn, DECIMALPRECISION)
$$

* **Redemption Fee Floor**: 0.5%
* **Decimal Precision**: 100%

**Borrowing Fee Calculation**:

`min{BORROWING_FEE_FLOOR + baseRate * newDebtIssued, MAX_BORROWING_FEE}`

* **Borrowing Fee Floor**: 0.5%
* **Max Borrowing Fee**: 1%

{% hint style="info" %}
Values can be changed by governance through voting.
{% endhint %}

## Intuition Behind Fees

* **Redemption Volume**: Higher volume leads to higher fees.
* **Time Decay**: Fees decrease over time if redemption volumes are low.
* **Protection**: Minimum fee of 0.5% to prevent front-running by arbitrageurs.
* **Borrowing Fees**: Capped at 1% to remain attractive even during monetary contraction.
