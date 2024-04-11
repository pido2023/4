# Yield Farming

## PIT-ETH Trading Pair

To facilitate asset diversification for our users, we will establish a PIT-ETH trading pair on Pido, enabling users to exchange PIT for ETH and vice versa.

### **Exchange Mechanics**

* **Smart Contract**: PIT and ETH exchanges are managed by a smart contract, which handles price calculations, fund transfers, and event logging.
* **Initial Price Setting**: The initial exchange ratio between PIT and ETH is set by the platform at the beginning. After PIT's official public release, this ratio will be determined by a price oracle for real-time market rates.
* **Exchange Functions**: We have implemented `swapPITforETH` and `swapETHforPIT` functions for the respective currency exchanges.
* **Price Calculation**: The exchange functions calculate the amount of currency a user will receive based on the current price ratio of PIT to ETH.
* **Funds Transfer**:
  * The exchange functions are responsible for transferring funds.
  * For PIT to ETH exchanges, the contract deducts PIT from the user's wallet and transfers the corresponding amount of ETH.
  * For ETH to PIT exchanges, the contract deducts ETH from the user's wallet and transfers the corresponding amount of PIT.
* **Event Logging**: Exchange functions trigger events to notify users of the outcomes and details of their transactions, which can be monitored for detailed trade information.

### Liquidity

Liquidity mining with PIT on Pido is a mechanism to engage in liquidity provision using PIT tokens, aiming to enhance the liquidity of the PIT-ETH trading pair for a superior trading experience and to offer economic incentives to participants.

* **Increasing Liquidity:** By participating in PIT liquidity mining, users contribute to the liquidity pool by locking their PIT tokens, thereby stabilizing the trading pair's price and reducing slippage.
* **Reward Mechanism:** Liquidity providers earn mining rewards proportionate to their contribution, paid in PIT tokens, which allows them to increase their token holdings.
* **Decentralization and Fairness:** The open and decentralized nature of the liquidity mining mechanism ensures that anyone can participate without geographic or identity restrictions, fostering a fair opportunity for global users and community growth.

### Yield Farming Rewards

1. The initial liquidity pool in Pido constitutes 4% of the total, amounting to 40,000,000 PIT.
2. The reward pool will be replenished with additional PIT tokens generated through token issuance and Harberger taxes.
3. The system contributes liquidity worth $$Z$$ PIT and $$\lambda Z$$ ETH to the liquidity pool, where $$\lambda$$ denotes the exchange rate between PIT and ETH.
4. Token proportions are based on the total value of liquidity provided, calculated against the asset values:
   * PIT Value: $$Z$$ PIT
   * ETH Value: $$\lambda Z$$ ETH
5. Assuming the system contributes a fraction $$\eta$$ of tokens, this translates to:
   * PIT Contribution: $$\eta Z$$ PIT
   * ETH Contribution: $$\eta \lambda Z$$ ETH
6. The liquidity mining contract specifies a reward of $$r$$ PIT tokens distributed to liquidity providers for each time period.
7. A user who provides $$\eta Z_i$$ PIT and $$\eta \lambda Z$$ ETH in liquidity, where $$Z=\sum Z_i$$, contributes to the overall pool.
8. User rewards are calculated based on their proportion of the total contribution: $$\frac {Z_i}{Z}r$$ PIT tokens per user.
9. Rewards from liquidity mining can accumulate within the contract and are available for users to claim at any time or can be distributed automatically.
