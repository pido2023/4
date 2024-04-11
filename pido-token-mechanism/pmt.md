# PMT

## PMT Concept

PMT (Pido Merit Token) is a digital asset issued by designers/artists, embodying membership rights and privileges associated with the issuing designer/artist.

The value of PMT can fluctuate based on the designer/artist's influence. Holders may be entitled to certain benefits, such as the ability to purchase exclusive limited edition NFTs or receive discounts on unlimited edition NFTs.

## PMT Issuance

* Issued by the designer/artist with no cap on the total amount.
* PMTs are settled with PIT and are non-fungible tokens (NFTs).
* Designers/Artists set the initial price, price increase coefficient, and unlocking criteria.
* Designers/Artists receive 10% of the PMT revenue, with the remainder used to provide liquidity.
* Designers/Artists are prohibited from purchasing their own PMTs.
* A user can purchase only one PMT of a single designer/artist at most.

## PMT Functionality

* Purchase specific limited edition NFTs.
* Buy unlimited edition NFTs at a discount.
* Receive PIT airdrops from the designer/artist.
* Gain priority display rights in secondary market trading.

## PMT Circulation

* The initial price set by the designer/artist is $$X_0$$ PIT per PMT, with $$X_0$$ being greater than zero.
* The price increase coefficient is set by the designer/artist as $$\mu$$, where $$\mu > 1$$.
* If a user purchases the $$n^{th}$$ PMT to be issued, meaning there are $$n-1$$ PMTs in circulation, the cost for the user is $$X_0\mu \ln(n+1)$$ PIT.
* Initially, all PMTs are non-transferable. Trading is enabled once the number of PMTs in circulation reaches $$n_0$$.
* If a user sells their PMT as the $$m^{th}$$ in circulation, where there are $$m-1$$ PMTs in circulation, the selling price is $$X_0\mu i\ln(m+1)$$ PIT, where $$i \in {1,2,3}$$ represents the PMT level.
* The profit for the user from that PMT is $$X_0\mu \ln\frac{(m+1)^i}{n+1}$$ PIT.
* 10% of the PIT paid by the user to purchase the PMT goes to the designer/artist as income.
* 90% of the PIT paid is locked to fund subsequent PMT sales.
* If a user sells their PMT, it is destroyed, reducing the circulation count by one, and PIT is released from the locked pool.
* The PIT in the designer/artist's PMT pool participates in liquidity mining for profit. If the PIT pool is depleted, PMTs can no longer be sold.
* Designers/Artists can replenish the PIT pool with new PIT.

## PMT Upgrade

* Users accumulate PMT points with each purchase of a designer/artist's product, whether limited or unlimited NFTs.
* As PMT points increase, the user's PMT can be upgraded.
* The initial PMT level is one, with three being the highest level.
* Different levels provide different privileges, such as varying discount rates.
* PMTs at different levels will be sold at different prices.

## PMT Significance

* The concept ties the value of PMTs to the designer/artist's influence, which can encourage the holding of the token as a form of investment. The utility of these tokens (e.g., buying limited edition NFTs or getting discounts on non-limited NFTs) adds tangible benefits to owning PMTs.
* Uncapped issuance could potentially lead to inflation, devaluing individual PMTs if the demand doesn't keep up with the supply. However, the non-fungibility and scarcity of certain PMTs can counteract this. The revenue-sharing aspect incentivizes designers/artists to issue PMTs, while the inability to purchase their own PMTs prevents market manipulation.
* The logarithmic pricing mechanism ensures that early adopters pay less, potentially rewarding them as the value increases. The lock-up period can stabilize the initial market. The burning of tokens upon sale can create deflationary pressure, potentially increasing the value of remaining PMTs.
* This gamified element encourages continuous engagement with the designer/artist's work, as users are motivated to reach higher PMT levels for better rewards. However, it also means that the value of a PMT is not static and depends on the user's engagement with the platform.
