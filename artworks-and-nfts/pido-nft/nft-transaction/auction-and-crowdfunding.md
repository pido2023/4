# Auction & Crowdfunding

Pido employs a sophisticated multiple-token economic model to facilitate transactions within its ecosystem, consisting of limited auctions and crowdfunding projects. The tokens, known as PIC and PIT, are designed to incentivize and reward both designers/artists and consumers for their participation.&#x20;

## Limited Auctions

### **Financial Distribution**

* **Designers/Artists** receive 95% of auction proceeds (fiat currency) as income, incentivizing high-quality design/art submissions.
* **Pido** retains a 5% service fee (fiat currency) from the auction proceeds to sustain and enhance the platform's operations.

### **Token Dynamics**

* Designers/Artists expend a predetermined amount of PIT to initiate an auction.
* Consumers are awarded 80% of system-generated PIT rewards, with the winning bidder receiving 160%.
* Designers/Artists are allocated 15% of PIT rewards for each participation.
* Pido accrues 2% of PIT rewards for service facilitation.
* A deflationary mechanism burns 3% of PIT rewards per participation.

## Crowdfunding

### Auction and Profit-Sharing Mechanism

* **Limited Edition Works Auction**: Works are sold through an English auction, determining the final holders.
* **Profit Sharing**: Holders who participate in the auction and successfully bid on limited edition works will have the opportunity to receive a certain percentage of revenue from subsequent crowdfunding sales based on the premium ratio of their auction success.

### Profit Distribution Method

* The share $$s_i$$ is allocated based on each user's auction premium ratio. The share for each holder is proportional to their individual premium $$\Delta p_i$$ relative to the total sum of all premiums, calculated using the following formula:

$$
s_i = \frac{\Delta p_i}{\sum_{i=1}^{n} \Delta p_i} S
$$

* $$n$$: The number of limited edition works successfully auctioned.
* $$p_i$$: The final auction price of the $$i^{th}$$ work.
* $$p_0$$: The floor price of the work.
* $$\Delta p_i$$: The auction premium for the $$i^{th}$$ work where $$\Delta p_i=p_i-p_0$$.
* $$S$$: Total profit to the holders of limited editions.

### Price Determination

* **Submission of Drafts:** Designers/Artists are required to submit their comprehensive drafts to Pido.&#x20;
* **Solicitation of Quotations:** Pido disseminates these requirements to an array of OEM manufacturers that specialize in the relevant product categories, then obtain a spectrum of price quotations that reflect the varying cost structures across different manufacturers.
* **Crowdfunding Cost Price:** Upon receipt of the quoted price range, the designer/artist is tasked with endorsing the highest quoted price, which is ratified as the crowdfunding cost price $$c$$.
*   **Relationship Between Profit and Quantity:** The profit of the crowdfunding work $$\Delta c$$ is related to the number of successfully auctioned works $$n$$, calculated using the following formula:&#x20;

    $$
    \Delta c=f(n)=kcn^r
    $$

    Initially, $$k=0.25, r=0.3$$.
* **Computation of Initial Price:** The initial total unit price for crowdfunding purposes is $$c+\Delta c$$.
* **Computation of Final Price:** Post completion and success of the crowdfunding campaign, the final product price is computed, which is predicated on the total funds accumulated during the crowdfunding stage, ensuring that the financial metrics align with the actual consumer support and capital raised for the project.

### **Financial Distribution**

* The total sales revenue in crowdfunding is $$Q=m(c+\Delta c)$$ and the total profit from sales in crowdfunding is $$\Delta Q=m\Delta c$$, where $$m$$ is the total number of units sold in crowdfunding.
* **OEM Manufacturers** are allocated $$mc$$ (fiat currency) , reflecting their production role.
* **Designers/Artists** establish the crowdfunding unit price based on quotations from OEM manufacturers and receive 30% of the total profits in the post-successful crowdfunding (fiat currency), i.e. $$30\%m\Delta c$$.
* **Holders** of limited edition works is distributed for 50% of the total profits (fiat currency), i.e. $$50\%m\Delta c$$, and $$S=50\%m\Delta c$$.
* **Pido** collects a total of 20% in fees (fiat currency) , split into a 10% service fee (fiat currency) and a 10% management fee (fiat currency), i.e. $$20\%m\Delta c$$.

### Example Calculation

Assuming $$m=100$$ as the total products of $$100$$ and $$c=100$$ as the production cost of $$100$$, taking $$n = 2, 4, 8, 16, 32$$ as examples and assuming that each person's auction transaction premium is the same, we can calculate:

* When $$n = 2$$, the total revenue is $$100 \times (100 + 0.25 \times 100 \times 2^{0.3}) = 13077.86$$.
  * The total cost is $$10000$$, accounting for $$76.47\%$$ of the total revenue.
  * The total profit is $$100 \times 0.25 \times 100 \times 2^{0.3} = 3077.86$$, accounting for $$23.53\%$$ of the total revenue.
  * The total profit received by the designers/artists is $$30\% \times 100 \times 0.25 \times 100 \times 2^{0.3} = 923.36$$, accounting for $$7.06\%$$ of the total revenue.
  * The total profit received by all successful bidders is $$50\% \times 100 \times 0.25 \times 100 \times 2^{0.3} = 1538.93$$, accounting for $$11.77\%$$ of the total revenue.
  * The profit received by each successful bidder is $$1538.93 \div 2 = 769.47$$, accounting for $$5.88\%$$ of the total revenue.
  * The profit received by the platform is $$20\% \times 100 \times 0.25 \times 100 \times 2^{0.3} = 615.57$$, accounting for $$4.71\%$$ of the total revenue.
* When $$n = 4$$, the total revenue is $$100 \times (100 + 0.25 \times 100 \times 4^{0.3}) = 13789.29$$.
  * The total cost is $$10000$$, accounting for $$72.52\%$$ of the total revenue.
  * The total profit is $$100 \times 0.25 \times 100 \times 4^{0.3} = 3789.29$$, accounting for $$27.48\%$$ of the total revenue.
  * The total profit received by the designers/artists is $$30\% \times 100 \times 0.25 \times 100 \times 4^{0.3} = 1136.79$$, accounting for $$8.24\%$$ of the total revenue.
  * The total profit received by all successful bidders is $$50\% \times 100 \times 0.25 \times 100 \times 4^{0.3} = 1894.65$$, accounting for $$13.74\%$$ of the total revenue.
  * The profit received by each successful bidder is $$1894.65 \div 4 = 473.66$$, accounting for $$3.43\%$$ of the total revenue.
  * The profit received by the platform is $$20\% \times 100 \times 0.25 \times 100 \times 4^{0.3} = 757.86$$, accounting for $$5.50\%$$ of the total revenue.
* When $$n = 8$$, the total revenue is $$100\times(100+0.25\times100\times8^{0.3})=14665.16$$.
  * The total cost is $$10000$$, accounting for $$68.19\%$$ of the total revenue.
  * The total profit is $$100\times0.25\times100\times8^{0.3}=4665.16$$, accounting for $$31.81\%$$ of the total revenue.
  * The total profit received by the designers/artists is $$30\%\times100\times0.25\times100\times8^{0.3}=1399.55$$, accounting for $$9.54\%$$ of the total revenue.
  * The total profit received by all successful bidders is $$50\%\times100\times0.25\times100\times8^{0.3}=2332.58$$, accounting for $$15.91\%$$ of the total revenue.
  * The profit received by each successful bidder is $$2332.58\div8=291.57$$, accounting for $$1.99\%$$ of the total revenue.
  * The profit received by the platform is $$20\%\times100\times0.25\times100\times8^{0.3}=933.03$$, accounting for $$6.36\%$$ of the total revenue.
* When $$n = 16$$, the total revenue is $$100\times(100+0.25\times100\times16^{0.3})=15743.49$$.
  * The total cost is $$10000$$, accounting for $$63.52\%$$ of the total revenue.
  * The total profit is $$100\times0.25\times100\times16^{0.3}=5743.49$$, accounting for $$36.48\%$$ of the total revenue.
  * The total profit received by the designers/artists is $$30\%\times100\times0.25\times100\times16^{0.3}=1723.05$$, accounting for $$10.94\%$$ of the total revenue.
  * The total profit received by all successful bidders is $$50\%\times100\times0.25\times100\times16^{0.3}=2871.75$$, accounting for $$18.24\%$$ of the total revenue.
  * The profit received by each successful bidder is $$2871.75\div16=179.48$$, accounting for $$1.14\%$$ of the total revenue.
  * The profit received by the platform is $$20\%\times100\times0.25\times100\times16^{0.3}=1148.70$$, accounting for $$7.30\%$$ of the total revenue.
* When $$n = 32$$, the total revenue is $$100\times(100+0.25\times100\times32^{0.3})=17071.07$$.
  * The total cost is $$10000$$, accounting for $$58.58\%$$ of the total revenue.
  * The total profit is $$100\times0.25\times100\times32^{0.3}=7071.07$$, accounting for $$41.42\%$$ of the total revenue.
  * The total profit received by the designers/artists is $$30\%\times100\times0.25\times100\times32^{0.3}=2121.32$$, accounting for $$12.43\%$$ of the total revenue.
  * The total profit received by all successful bidders is $$50\%\times100\times0.25\times100\times32^{0.3}=3535.53$$, accounting for $$20.71\%$$ of the total revenue.
  * The profit received by each successful bidder is $$3535.53\div32=110.49$$, accounting for $$0.65\%$$ of the total revenue.
  * The profit received by the platform is $$20\%\times100\times0.25\times100\times32^{0.3}=1414.21$$, accounting for $$8.28\%$$ of the total revenue.

### Explanation

Designers/Artists face a strategic decision when auctioning limited edition works: auctioning more pieces may increase their total revenue, but an oversupply could dilute the value of each individual piece. Theoretically, adding an additional limited edition piece to the auction means higher potential total profits, as there would be more sources of funds. However, this strategy also encounters the issue of diminishing marginal effects, that is, as the number of works increases, the incremental profit that each piece can bring will gradually decrease.

Moreover, if the number of limited edition works is too high, it may reduce the uniqueness and appeal of each piece, thus lowering the transaction rate of the auction. If the transaction rate is insufficient, it may lead to the crowdfunding campaign not launching successfully.

Similarly, for high-priced crowdfunding projects, if the pricing is too high, it may increase the profit per transaction, but at the same time, it will limit the participation of the broader consumer base, which may pose a risk to the success of the crowdfunding campaign. Therefore, designers/artists need to carefully balance the number of works and pricing strategy to ensure that they can attract investment while reaching a broad consumer base, thereby driving the success of the crowdfunding campaign.

The situation for investors is even more delicate. Although they may prefer a smaller number of limited edition works to maintain high unit profits, they also need to consider the importance of market validation. A successful auction can serve as an indicator of market demand, showing consumer interest and recognition of the works. This positive market response is crucial for subsequent crowdfunding activities, as it can greatly enhance the appeal and success rate of crowdfunding. Therefore, maintaining a certain number of limited edition works may help attract more investors to participate, thereby supporting the success of the entire project.

In this complex environment, mutual understanding and cooperation between designers/artists and investors are crucial. Establishing a clear and transparent auction and revenue distribution mechanism can help all parties understand the project's goals and potential returns, thereby building a foundation of trust and cooperation. Open communication helps to maintain relationships between participants, ensuring that everyone feels they are treated fairly and can work together to achieve project success. Ultimately, a fair, efficient, and win-win business model is key to achieving the goals of all parties involved.

### **Token Dynamics**

* Designers/Artists are required to spend a certain amount of PIT to launch a crowdfunding campaign.
* Consumers obtain 80% of system-generated PIT rewards for successful participation.
* Designers/Artists receive 15% of system-generated PIT rewards upon successful crowdfunding.
* Pido secures 2% of PIT rewards for successful crowdfunding facilitation.
* A deflationary policy ensures 3% of PIT rewards are burned upon successful participation.
