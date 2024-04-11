# Pido Harberger Tax

## Pido Harberger Tax Process

1. **NFT Market Pricing:** Users unlock their NFT holdings and set a market sale price.
   * For both limited edition and unlimited edition NFTs, transactions are denominated in PIT tokens, and the Harberger Tax is also paid in PIT.&#x20;
   * Once the sale price is set, users can not change it within one month.
   * If a decision is made to charge for price changes, users need to pay a fee.
2. **Fee Algorithm for Price Changes**
   * **Fee Structure**: The fee for price changes is based on three parts
     * **Base Fee:** For the fixed cost associated with processing the price change request.
     * **Frequency Penalty:** If the user modifies the pricing frequently within a short time frame.
     * **Difference Fee:** Based on the variable cost due to the extent of the price modification.
   * **Base Fee:** The cost ratio for modifying the pricing will be set in 0.5%, let the new pricing set by the user be $$V$$, then the base fee will be calculated as $$0.5\%V$$.
   * **Frequency Penalty:** The frequency penalty is $$0.5\%\alpha_1(n-1)V$$where $$\alpha_1$$ is the additional fee ratio for frequency penalty and we will set $$\alpha_1=1.5$$ initially, $$n$$ is the number of modifications within one week.
   * **Difference Fee:** The cost ratio for the difference fee will be set in 1%, let the original pricing set by the user be $$V_0$$, then the difference fee will be calculated as $$1\%(V-V_0)$$.
   * **Total Fee:** The total fee for price changes is  $$0.5\%V+0.5\%\alpha_1(n-1)V+1\%(V-V_0)$$.
3.  **Collateral and Tax Rate**

    * Users must pay a one-time PIT deposit equal to 4.68% of the NFT's set price, i.e. $$4.68\%Q_0$$, as collateral. This deposit is used to deduct monthly Harberger Tax obligations. If the PIT balance in the account is insufficient, the NFT cannot be listed on the secondary market.
    * The Harberger Tax rate is set at 0.5% at the first month and decrease 0.02% per month until reaching 0.2%. Therefore, the user's deposit must be sufficient to cover at least one year of Harberger Tax.

    | Month | Tax Rate | Month | Tax Rate |
    | ----- | -------- | ----- | -------- |
    | 1     | 0.5%     | 2     | 0.48%    |
    | 3     | 0.46%    | 4     | 0.44%    |
    | 5     | 0.42%    | 6     | 0.4%     |
    | 7     | 0.38%    | 8     | 0.36%    |
    | 9     | 0.34%    | 10    | 0.32%    |
    | 11    | 0.3%     | 12    | 0.28%    |
    | 13    | 0.26%    | 14    | 0.24%    |
    | 15    | 0.22%    | 16    | 0.2%     |
4. **Maintaining Active Status:** Users are required to top up their deposit every year with an amount equal to one-year tax of the NFT's set price in PIT to maintain the NFT's active status. If the replenishment is not made in time, the NFT will automatically enter a preset auction process.
5. **Staking Earnings:** The collateral deposit is eligible for PIC rewards distributed by the system; the specific staking reward rules are detailed in

{% content-ref url="../../../../more-functions/staking/" %}
[staking](../../../../more-functions/staking/)
{% endcontent-ref %}

6. **Trading and Auction**
   * Unlimited edition NFTs are traded through a direct sale process, with the remaining PIT deposit returned after settlement.
   * Limited edition NFTs are sold via an English auction process.
     * The auction begins the moment a buyer accepts the seller's set price.&#x20;
     * Within the subsequent 24 hours, other buyers can submit higher bids.&#x20;
     * Each new highest bid extends the auction time by another 24 hours.&#x20;
     * If no new bids are made by the end of any extension period, the auction closes.
     * Upon completion of the transaction, the seller's remaining PIT deposit is refunded.
7. **Allocation of Harberger Tax:** The PIT collected as Harberger Tax in the system is distributed as follows:
   * 40% enters the community pool and is allocated proportionally to six sub-token pools.
   * 30% goes into the marketing pool, for the platform and designers/artists to distribute to eligible users.
   * 20% goes into the liquidity pool, rewarding users who provide liquidity for the PIT token.
   * 10% enters the treasure pool, rewarding the DAO's managers.
8. **Transparency and Listing Transactions**
   * All information regarding active status NFTs remains public and transparent, with all data available for inquiry.
   * All NFTs in active status are listed for trading, allowing buyers to match the price and complete the transaction at any time.

## NFT Status Transition and Fee Structure

1. **Voluntary Locking State Recovery Fee**
   * Users who wish to revert their NFT from an active state to a locked state are required to pay a certain proportion of a recovery fee.
   * The fee is collected at the time of the state change request and is non-refundable, emphasizing the commitment required to lock an NFT.
2. **Dynamic Locking Fee**: A variable fee that depends on factors such as:
   * **Frequency of State Changes**: Higher fees for users who toggle states more frequently to discourage gaming the system.
   * **NFT Valuation**: A percentage of the NFT's value with higher-value NFTs incurring higher fees to reflect their market impact.
3. **Locking Fee Algorithm**
   * **Fee Structure**: The fee for locking NFT s is based on two parts
     * **Base Fee:** For the fixed cost associated with processing the locking request.
     * **Frequency Penalty:** If the user transit the status frequently within a short time frame.
   * **Base Fee:** The cost ratio for modifying the pricing will be set in 2%, let the new pricing set by the user be $$V$$, then the base fee will be calculated as $$2\%V$$.
   * **Frequency Penalty:** The frequency penalty is $$2\%\alpha_2(n-1)V$$where $$\alpha_2$$ is the additional fee ratio for frequency penalty and we will set $$\alpha_2=1.5$$ initially, $$n$$ is the number of transitions within one week.
   * **Total Fee:** The total fee for locking is $$2\%V+2\%\alpha_2(n-1)V$$.
4. **Forced Auction Mechanism for Inability to Pay Annual Fees**
   * If a user fails to pay the Harberger Tax required to keep the NFT active within the specified time (equivalent to 4.68% of the NFT's pricing in PIT), the NFT will automatically enter a preset auction process.
   * Users should receive notifications of unpaid annual fees and be granted a grace period (30 days) during which they can take action to avoid a forced auction.
   * The starting price for the forced auction will be set 50% of the last market pricing.
5. **Auction Process**
   * The auction will take the form of open bidding.&#x20;
   * After the auction concludes, the highest bidder acquires the NFT, and the proceeds are first used to pay any unpaid annual fees and any related auction costs.
6. **Handling of Remaining Proceeds**
   * If the auction income exceeds the unpaid annual fees and related costs, the surplus will be returned to the original NFT holder.
   * If the auction proceeds are insufficient to cover the costs, the original holder need to cover the deficit.
7. **Transparency**
   * All relevant contracts and records will be updated to reflect the new ownership and status of the NFT.
   * All auction and fee information will remain public and transparent, so that all market participants can have a clear understanding of the process and outcomes.
