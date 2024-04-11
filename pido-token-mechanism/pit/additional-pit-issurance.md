# Additional PIT Issurance

## **Mechanism Introduction**

The PIT token additional issuance mechanism describes an economic model designed to balance the reduction effect of token burning through an issuance mechanism. This model uses specific mathematical formulas to determine the amount of issuance and distributes the newly generated PIT according to different sub-token pools.&#x20;

1. **Relationship between Burning and Issuance**: For every 1 PIT burned, the system will issue $$U$$ new PITs, ensuring an increase in total supply.
2. **Independence of Token Pools**: The six sub-token pools in community pool operate independently, with burning and issuance happening within each respective pool.
3. **Issuance Formula**: The amount issued is $$U_i = b_4 + a_{12}^{\frac{1}{\lambda_i}}$$, where $$b_4>0, a_{12} > 1$$ are constants.
4. **Definition of** $$\lambda_i$$: $$\lambda_i$$ represents the current number of PITs in the $$i$$th PIT pool as a multiple of the original number of PITs.
5. **Classification of Token Pools**: $$i = 1,2,3,4,5,6$$, representing the six sub-token pools.
6. **Community Pool Allocation**: Burn 1 PIT, issue $$U_i$$ PITs, of which $$0.4U_i$$ go into the community pool.
7. **Marketing Pool Allocation**: Burn 1 PIT, issue $$U_i$$ PITs, of which $$0.3U_i$$ go into the marketing pool.
8. **Liquidity Pool Allocation**: Burn 1 PIT, issue $$U_i$$ PITs, of which $$0.2U_i$$ go into the liquidity pool.
9. **Treasury Pool Allocation**: Burn 1 PIT, issue $$U_i$$ PITs, of which $$0.1U_i$$ go into the treasury pool.

## Explanation

1. **Stable Token Supply:** The PIT token's issuance model is clearly designed to address the deflationary pressure that token burning may cause. In response to each burning action, the system automatically issues new tokens to maintain economic balance.&#x20;
2. **Dynamic Adjustment:** Through $$\lambda_i$$ in the formula, the issuance volume can be dynamically adjusted according to the actual status of the token pool, achieving more flexible supply management.&#x20;
3. **Issuance Formula:** The formula $$U_i = b_4 + a_{12}^{\frac{1}{\lambda_i}}$$ is the core of the issuance mechanism, defining how the quantity of issued tokens changes with $$\lambda_i$$. Here, $$b_4$$ and $$a_{12}$$ are parameters that adjust the sensitivity of issuance. $$\lambda_i$$ reflects the growth of the token pool; if the number of PITs in the pool increases, $$\lambda_i$$ increases, leading to a decrease in $$U_i$$, which is to prevent excessive issuance when the token pool is already large.

<figure><img src="../../.gitbook/assets/Additional Issurance.png" alt=""><figcaption><p>Different trend when<br><span class="math">b_4=1,a_{12}=4</span>(Blue)<br><span class="math">b_4=0.5,a_{12}=2.5</span>(Red)<br><span class="math">b_4=1,a_{12}=1.5</span>(Green)   </p></figcaption></figure>

## Impact on Token Economy

The design of this issuance mechanism aims at ensuring a stable increase in token supply and supporting different parts of the community through allocation to various token pools, including community rewards, airdrops, liquidity mining, and DAO operations.

* **Avoiding Deflation**: By issuing new tokens, the system prevents excessive deflation caused by burning.
* **Incentivizing Participation**: Allocating tokens to community and marketing pools encourages user engagement and activity.
* **Supporting Liquidity**: The liquidity pool's issuance rewards those users who provide liquidity for the token.
* **DAO Incentives**: A portion of the issuance goes into the treasury, supporting and rewarding the managers of the DAO.
