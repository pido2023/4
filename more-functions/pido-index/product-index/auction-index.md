# Auction Index

## **Variable Naming**

* $$p$$: Starting auction price for the limited NFT
* $$q$$: Current bid price for the limited NFT
* $$n$$: Number of bids for the limited NFT
* $$m$$: Number of curators who purchased the display rights for the NFT
* $$o$$: Number of effective votes from PIC recommendation
* $$t$$: Duration of the auction

## **Calculation of NFT Influence Index during Auction**

The calculation formula for the influence index $$f_1(p, q, n, m,o, t)$$ is:

$$
f_1(p, q, n, m, o, t) = K_1 p^{s_1} q^{s_2} n^{s_3} m^{s_4} o^{s_5} c_1^t = X_1
$$

Where:

* $$s_1=0.6$$, $$s_2=0.2$$, $$s_3=0.45$$, $$s_4=0.4$$, $$s_5=0.5$$, $$c_1=0.997$$ are fixed constants.
* $$K_1=0.2$$ is a constant, which is the initial multiplier for the influence index.
* $$X_1$$ is the value of the influence index calculated using the above formula.

## **Average Value of Influence Index and Calculation of Pido Index**

* Calculate the influence index $$X_1$$ for all NFTs currently being auctioned, and find their average value $$\bar X_1$$.
* The PIDO Index $$I_A$$ of the NFT project is calculated as follows:

$$
I_A = \frac{100}{1 + e^{-\alpha_1 (X_1 - \bar X_1)}}
$$

Where:

* $$\alpha_1=0.09$$ is a fixed constant that determines the slope of the Pido Index curve.
* $$I_A$$ increases with increases in $$p$$ and $$n$$, and decreases with the increase in $$t$$.
* When $$X_1 = \bar X_1$$, that is, when the project's influence index equals the average influence index of all projects, $$I_A = 50$$.

## **Pido Index after Successful Auction**

* After a successful auction, $$I_A$$ will be fixed and no longer changes.

## **Inheritance of Pido Index for New Tier NFTs**

* The new tier NFT (e.g., from tier S to A) of the same designer/artist can partially inherit the Pido Index of the previous NFT.
* If the original NFT's influence index is $$X_1'$$, the PIDO Index $$I_A'$$ for the new NFT is calculated as:

$$
I_A' = \frac{100}{1 + e^{-\alpha_1 (X_1 + \beta_1 X_1' - \bar X_1)}}
$$

Where:

* $$0 < \beta_1 < 1$$ is a constant determining the proportion of the old NFT's influence index that the new NFT will inherit.
