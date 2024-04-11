# PIT Staking

Users can earn loyalty rewards by staking their PIT tokens in projects. This staking mechanism also grants them voting rights within Pido's governance. Only PIT tokens that are staked can increase a user's voting weight.

Pido encourages users to stake their PIT tokens for the following reasons:

* It helps maintain the short-term stability of the token price in the market.
* It rewards users who are long-term supporters and loyal to the platform.
* It drives the platform towards decentralization, both in terms of asset distribution and community governance.

## Staking Process

### **Staking Contract**

The staking contract is responsible for managing PIT token staking, distribution of earnings, and governance rights allocation. It records staked funds and handles associated logic.

### **PIT Staking**

Users stake by locking a specified amount of PIT tokens into the contract using the staking function, which then logs details such as amount and duration of the stake.

### **Earnings Distribution**

* **Regular Earnings**: Profit rates vary per time cycle; longer staking periods result in higher earnings rates.
* **Dynamic Earnings**: The rate of return adjusts dynamically based on the total amount of PIT in the staking pool. More PIT in the pool leads to higher individual staking profits.

### **Source of Earnings**

Earnings in PIC tokens for staking primarily come from interest accrued in NFT lending. If this is insufficient, the system compensates the shortfall.

### **Governance Rights**

* **Acquisition**: Governance rights are granted only when PIT tokens are staked. More staked PIT increases governance weight and the rate of PIT acquisition.
* **Participation**: The staking contract allocates governance rights, enabling users to partake in community decision-making. Governance decisions, including project direction and parameter adjustments, are made via a voting mechanism involving staked token holders.

### **Unstaking**

If users want to unstake PIT early, they will be charged a fee of 2% of the amount they staked.

## Staking Rewards

### **Earning PIC from Staking**

Users earn PIC by staking their PIT tokens in a staking contract.

### **Base Staking Reward Rate**

* **Determinants**: The base reward rate, $$R$$, is determined by both the staking duration and the amount staked. Longer staking durations and larger staked amounts lead to higher reward rates.
* **Staking Terms**: Available staking periods include one week, two weeks, one month, two months, three months, six months and one year.
* **Interest Rate**: Different lending periods will have different interest rates. The specific interest rate structure needs to be further provided.

| Lending Period | Interest Rate |
| -------------- | ------------- |
| 1 week         | $$f_1$$       |
| 2 weeks        | $$f_2$$       |
| 1 month        | $$f_3$$       |
| 2 months       | $$f_4$$       |
| 3 months       | $$f_5$$       |
| 6 months       | $$f_6$$       |
| 1 year         | $$f_7$$       |

The specific numerical value of annual yield rates will be provided subsequently and $$f_i>e_i$$, check the details of $$e_i$$ in

{% content-ref url="../../artworks-and-nfts/pido-nft/nft-lending/pido-lending-mechanism.md" %}
[pido-lending-mechanism.md](../../artworks-and-nfts/pido-nft/nft-lending/pido-lending-mechanism.md)
{% endcontent-ref %}

### **Staking Mechanics**

* **Lock-In**: During the staking term, PIT tokens are locked and cannot be used elsewhere or unstaked prematurely. If users want to unstake PIT early, they will be charged a fee of 2% of the amount they staked.
* **Reward Rate Function**: The actual staking reward rate decreases as the quantity of staked PIT increases, represented by

$$
f(x,R)=\frac{\alpha x}{\beta x^2+\gamma}R
$$

* **Rate of Change**: The rate of change of the staking reward rate with respect to $$x$$ is

$$
\frac{\partial f(x)}{\partial x}=\frac{-\alpha \beta x^2+\alpha \gamma}{{(\beta x^2+\gamma)}^2}
$$

* **Inflection Point**: The inflection point, where the reward rate begins to decrease, occurs at

$$
x=\sqrt{\frac{\gamma}{\beta}}
$$

* **Peak Reward Rate**: The peak of the staking reward rate is

$$
f(\sqrt{\frac{\gamma}{\beta}},R)=\frac{\alpha}{2}\sqrt{\frac{1}{\beta \gamma}}R
$$

* **Staking Behavior**: As users increase their staked PIT quantity, $$x$$, the reward rate initially increases, then decreases, and asymptotically approaches zero.

### **Coefficients**

* **Staking Coefficient** $$\alpha$$: Determines the peak value of staking rewards.
* **Inflection Coefficients** $$\beta$$**,** $$\gamma$$: Determine the inflection point where the reward rate begins to change with the staked PIT quantity.
*   We will set $$\alpha=4,\beta=0.01,\gamma=100$$ initially and gradually adjust the value based on feedback from the system.

    <figure><img src="../../.gitbook/assets/APY Rate.png" alt=""><figcaption><p>Different trend when<br><span class="math">\alpha=8,\beta=0.1,\gamma=40</span>(Green)<br><span class="math">\alpha=4,\beta=0.01,\gamma=100</span>(Red)<br><span class="math">\alpha=10,\beta=0.01,\gamma=100</span>(Blue)</p></figcaption></figure>
