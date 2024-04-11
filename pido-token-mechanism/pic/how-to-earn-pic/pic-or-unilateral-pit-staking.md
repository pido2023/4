# PIC | Unilateral PIT Staking

Within Pido, users can earn PIC returns by locking and staking PIT (the governance token). Here are the specific rules and methods for calculating returns for PIT staking.

## **Staking Rules**

1. **Staking for PIC Earnings**: Users can earn PIC returns by locking and staking PIT.
2. **Harberger Tax Staking**: When listing NFTs on the secondary market, users must pay a Harberger tax and stake a certain amount of PIT as collateral. This collateral is also considered staked and can earn PIC returns. Check the details of Harberger Tax in&#x20;

{% content-ref url="../../../artworks-and-nfts/pido-nft/nft-transaction/harberger-tax/" %}
[harberger-tax](../../../artworks-and-nfts/pido-nft/nft-transaction/harberger-tax/)
{% endcontent-ref %}

3. **Staking Yield Rate**: The base staking yield rate $$R$$ depends on the duration and amount of the stake. The longer the staking time and the higher the staked amount, the higher the yield rate.
4. **Staking Duration**: The available staking periods include one week, two weeks, one month, two months, three months, six months and one year.
5. **Staking Lock-up**: During the staking period, PIT will be locked up and cannot be used for other purposes. If users want to unstake PIT early, they will be charged a fee of 2% of the amount they staked.

## **Yield Rate Calculation**

1. **Actual Yield Rate Formula**:  Let $$x$$ be the quantity of PIT staked, then the actual staking yield rate is calculated as&#x20;

$$
f(x,R)=\frac{\alpha x}{\beta x^2 + \gamma}R
$$

2. **Yield Rate Change Rate**: The rate of change in the staking yield rate with respect to $$x$$ is&#x20;

$$
\frac{\partial f(x)}{\partial x}=\frac{-\alpha \beta x^2 + \alpha \gamma}{(\beta x^2 + \gamma)^2}
$$

3. **Yield Rate Extreme Point**: The extreme point for the yield rate is at

$$
x=\sqrt{\frac{\gamma}{\beta}}
$$

4. **Yield Rate Peak**: The peak of the yield rate is

$$
f(\sqrt{\frac{\gamma}{\beta}},R)=\frac{\alpha}{2}\sqrt{\frac{1}{\beta \gamma}}R
$$

5. **Staking Earnings Variation**: The staking yield rate obtained by users first increases and then decreases with the increase of $$x$$, eventually approaching zero.
6. **Coefficient Explanation**
   * $$\alpha$$ is the staking coefficient, which determines the peak value of the staking returns.
   * $$\beta$$ and $$\gamma$$ are inflection point coefficients, which determine the position of the yield rate change inflection point with respect to $$x$$.
   * We will set $$\alpha=4,\beta=0.01,\gamma=100$$ initially and gradually adjust the value based on feedback from the system.

<figure><img src="../../../.gitbook/assets/APY Rate.png" alt=""><figcaption><p>Different trend when<br><span class="math">\alpha=8,\beta=0.1,\gamma=40</span>(Green)<br><span class="math">\alpha=4,\beta=0.01,\gamma=100</span>(Red)<br><span class="math">\alpha=10,\beta=0.01,\gamma=100</span>(Blue)</p></figcaption></figure>

## **Notes**

* This staking mechanism encourages users to hold PIT for the long term.
* Users need to carefully consider their staking strategy to maximize their returns, while being aware of the non-linear changes in the staking yield rate with the staked amount.
* The design of the staking is to balance the returns between long-term holders and short-term participants and to prevent market manipulation that may be caused by excessive concentration of large holders.
* This part is also included in the MORE FUNCTIONS>Staking section,   check the details in&#x20;

{% content-ref url="../../../more-functions/staking/" %}
[staking](../../../more-functions/staking/)
{% endcontent-ref %}
