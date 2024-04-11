# Crowdfunding Index

## **Variable Naming**

* $$p$$: Crowdfunding price for the non-limited NFT
* $$l$$: Total number of units purchased by the crowdfunders
* $$h$$: Target number of units for the crowdfunding campaign
* $$m$$: Number of buyers who purchased the display rights for the NFT
* $$o$$: Number of effective votes from PIC recommendation
* $$t$$: Duration of the crowdfunding campaign

## **Calculation of NFT Influence Index during Crowdfunding**

For each NFT project that is being crowdfunded, its influence index $$f_2(p, l, m,o, t)$$ is defined as:

$$
f_2(p, l, m, o, t) = K_2 p^{u_1} l^{u_2} h^{u_3} m^{u_4} o^{u_5} c_2^{t} = X_2
$$

Where:

* $$u_1, u_2, u_3, u_4,u_5, c_2, K_2$$ are fixed constants.
* $$X_2$$ is the value of the influence index calculated using the above formula.

## **Average Value of Influence Index and Calculation of Pido Index**

* Calculate the influence index $$X_2$$ for all NFTs currently being crowdfunded, and find their average value $$\bar X_2$$.
* The Pido Index $$I_C$$ of the NFT project is calculated as follows:

$$
I_C = \frac{100}{1 + e^{-\alpha_2 (X_2 - \bar X_2)}}
$$

Where:

* $$\alpha_2=0.09$$ is a fixed constant that affects the slope of the Pido Index curve.
* $$I_C$$ increases with increases in $$p$$ and $$l$$, and decreases with the increase in $$t$$.
* When $$X_2 = \bar X_2$$, that is, when the project's influence index equals the average influence index of all projects, $$I_C = 50$$.

## **Pido Index after Successful Crowdfunding**

* After the crowdfunding is successful, $$I_C$$ will be fixed and no longer changes.

## **Inheritance of Pido Index for a New Round of Crowdfunding**

* The Pido Index $$I_C'$$ for a new round of crowdfunding by the same designer/artist can partially inherit the Pido Index from the previous round.
* If the original NFT's influence index is $$X_2'$$, the Pido Index $$I_C'$$ for the new NFT is calculated as:

$$
I_C' = \frac{100}{1 + e^{-\alpha_2 (X_2 + \beta_2 X_2' - \bar X_2)}}
$$

Where:

* $$0 < \beta_2 < 1$$ is a constant determining the proportion of the old NFT's influence index that the new NFT will inherit.
